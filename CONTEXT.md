# CoCraft

**Suivi** (the product built in the **CoCraft** project — *suivi* is French for "tracking / follow-up") is a household management app: one growing system for the money, obligations, possessions, and pets a household keeps track of. It is built one module at a time on a shared money/ownership model, whose trunk is the Expense.

## Language

**Household**:
The shared space that all data belongs to; has one or more Members.
_Avoid_: account, family, group

**Member**:
A person with access to a Household.
_Avoid_: user (reserve "user" for the auth/identity sense)

**Expense**:
A single record of money leaving the household — an amount, a date, a Category, and an optional note/payee. The atomic ledger entry and the trunk of the model.
_Avoid_: transaction, payment, spend, cost

**Category**:
A label that classifies an Expense (e.g. Groceries, Utilities) for grouping and summaries.
_Avoid_: tag, type, label

**Bill**:
A recurring or anticipated obligation with a due date and cadence (rent, electricity). A Bill is owed/scheduled; **paying a Bill produces an Expense**.
_Avoid_: invoice, subscription, expense (a Bill is not yet an Expense)

**Purchase**:
An Expense that results in an owned Item. A Purchase is an Expense *plus* the thing you now own.
_Avoid_: order, transaction, expense (a Purchase is a kind of Expense, but not every Expense is a Purchase)

**Item**:
A thing the household owns, created by a Purchase. May carry a Warranty.
_Avoid_: product, asset, thing

**Warranty**:
Coverage on an Item with an expiry date.
_Avoid_: guarantee, insurance

## Flagged ambiguities

- **Expense vs Bill vs Purchase** — used interchangeably early on. Resolved: **Expense is the trunk.** A Bill is a *future obligation* that *produces* an Expense when paid. A Purchase is an Expense that *also produces* an owned Item. Income / money-in is out of scope; "Expense" means money out only.

## Example dialogue

> **Dev:** When rent is due, that's an Expense?
> **Expert:** No — rent due is a **Bill**. It becomes an **Expense** the day I actually pay it.
> **Dev:** And if I buy a blender?
> **Expert:** That's a **Purchase**. It's an Expense, but it also gives me an **Item** — the blender — which has a **Warranty** that expires in two years.
> **Dev:** What about my salary landing in the bank?
> **Expert:** Not tracked. CoCraft only records money *leaving* the **Household** right now.

# Access Modifiers

## What are access modifiers?

Access modifiers are one of the core elements of OOP. It helps you control who can access the properties and methods inside classes.

## Why use access modifiers?

let say we have a class:

```typescript
class BackAccount {
  balance: number = 10000;
}

const newAccount = new BackAccount();
newAccount.balance = 10;
```

Here anyone can just **change** the bank balance. This is why we use **access modifiers** to control how we can manipulate the properties and modifiers.

## Types of access modifiers

_There are three access modifiers. Those are:_

1. Public: It can be accessed and modified inside and outside the class
2. Private: It can only be accessed inside the class and only can be modified there.
3. Protected: It can only also be accessed and modified inside its child classes.

> There is another modifier called **readonly modifier**. Which behaves like const once you assign a **value** to it you **can't change** the value but you can use that value however you want.

## Real World Use

Let's say we have a class named `BankAccount` and it has three properties:

- `accountNumber` which can you accessed **outside the class** but can't be changed.
- `balance`: Which can only be accessed **inside the class**.
- `accountHolder`: which can only be accessed **inside the class and children classes**.

> Here is how it will look like:

```typescript
class BankAccount {
  constructor(
    public readonly accountNumber: number,
    private balance: number,
    protected accountHolder: string,
  ) {}
}
```

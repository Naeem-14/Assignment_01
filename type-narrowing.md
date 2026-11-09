# Type Narrowing

## What is type narrowing?

Type narrowing is a method we use to narrow down the types. It is one of the most important concept of typescript.

## Why use type narrowing?

Let's say we have a function:

```typescript
function returnValue(value: string | number) {
  return value.toUpperCase();
}
```

This will return an `error` cause the value can be a string or a number. Now if it's a string it can return an string changed to **uppercase** but if it's a number there is no `toUpperCase()` method so this function will return an error. This is the reason we need **type narrowing** to **narrow down** our types.

## Different ways to narrow down types

_There are many ways to narrow down our types. Here are some of them:_

1. **typeof:** Checks the type of the value.
2. **truthiness**: Checks if the value is true
3. **in**: Checks if a property is in a object
4. **instanceOf**: Checks if x is in a class
5. **Array.isArray(x)**: Checks if x is an array or not

## Real World Use

Let's say we have a function that accepts a value which may be a `string, number, or boolean`, and returns a formatted result based on the value's type:

- If the input is a **string** → trim any **leading/trailing** spaces and return it in lowercase.
- If the input is a **number** → return the number **multiplied by 10.**
- If the input is a **boolean** → return **"Active"** if true, or **"Inactive"** if false.

> Here is how it will look like if we use **type narrowing**:

```typescript
function processInput(value: string | number | boolean): string | number {
  if (typeof value === "string") {
    return value.trim().toLowerCase();
  } else if (typeof value === "number") {
    return value * 10;
  } else {
    return value ? "Active" : "Inactive";
  }
}
```

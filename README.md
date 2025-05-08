# 📘 TypeScript Interview Questions

## ✅ 1.  How TypeScript Improves Code Quality and Maintainability
### 💡 Key Benefits:

| Feature               | `interface`                                                 |
|-----------------------|-------------------------------------------------------------|
|Type Safety:           |Detects type errors at compile time, before running the code.|
|Better IDE Support:    |Autocompletion, inline docs, refactoring help.               |
|Self-Documentation:    |Code becomes easier to understand due to explicit types.     |
|Refactor-Friendly:     |Safe renaming and refactoring across large codebases.        |
|Scalability:           | Perfect for large teams and long-term projects.             |

📝 TypeScript adds strong typing, better tooling, and scalable architecture to JavaScript. 
It helps developers catch bugs early, write self-explanatory code, and maintain large projects with confidence.

## ✅ 2. Differences Between `interface` and `type` in TypeScript

### ✔️ Common Features:
- Both `interface` and `type` can describe the shape of an object.
- Both can be extended and reused.

### ✔️ Key Differences:

| Feature                          | `interface`                               | `type`                                       |
|----------------------------------|-------------------------------------------|----------------------------------------------|
| Extending                        |  Can extend multiple interfaces         |  Can use intersections to combine types    |
| Use with primitives & unions     |  Only for object shapes                 |  Can represent any type (union, primitive) |
| Preferred for OOP                 |  Yes                                    |  Not ideal      |

###  Example:
```ts
interface User {
  name: string;
  age: number;
}

type Product = {
  title: string;
  price: number;
};
```

## ✅ 3. Union and Intersection Types in TypeScript
🔹 Union ( | ) : A variable can be one of multiple types.
```ts
function printId(id: string | number) {
  console.log("Your ID is: " + id);
}

printId(101);        
printId("abc-123");  
```

🔸 Intersection ( & ) : Combines multiple types into one.
```ts
type Person = {
  name: string;
};

type Employee = {
  employeeId: number;
};

type Staff = Person & Employee;

const staffMember: Staff = {
  name: "Alice",
  employeeId: 1234,
};
```
✔️ Note: Use union types when a value can be one of many types.

✔️ Use intersection when you want to merge multiple types into one.
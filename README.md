# 📘 TypeScript Interview Questions

##  1.  How TypeScript Improves `Code Quality` and `Maintainability`
###  Key Benefits:

|                |                                               |
|-----------------------|-------------------------------------------------------------|
|Type Safety:           |Detects type errors at compile time, before running the code.|
|Better IDE Support:    |Autocompletion, inline docs, refactoring help.               |
|Self-Documentation:    |Code becomes easier to understand due to explicit types.     |
|Refactor-Friendly:     |Safe renaming and refactoring across large codebases.        |
|Scalability:           | Perfect for large teams and long-term projects.             |
|||

### TypeScript adds strong typing, better tooling, and scalable architecture to JavaScript. 
It helps developers catch bugs early, write self-explanatory code, and maintain large projects with confidence.

![TypeScript Logo](https://assets-eu-01.kc-usercontent.com/5dddefee-e8bb-013a-3b4e-7907971cf825/36961122-2fd0-4bd1-8aad-40c4c5dfa139/benefits_of_typescript_without_typescript_blog_index.webp)

## 2. Differences Between `interface` and `type` in TypeScript

### Common Features:
- Both `interface` and `type` can describe the shape of an object.
- Both can be extended and reused.

### Key Differences:

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

## 3. Union and Intersection Types in TypeScript
![TypeScript Logo](https://habrastorage.org/getpro/habr/upload_files/02b/2e8/138/02b2e8138888d8def09d733235fb8f0f.jpg)
## Union ( | ) : A variable can be one of multiple types.
```ts
function printId(id: string | number) {
  console.log("Your ID is: " + id);
}

printId(101);        
printId("abc-123");  
```

## Intersection ( & ) : Combines multiple types into one.
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
### Note: 
Use union types when a value can be one of many types. Use intersection when you want to merge multiple types into one.
A **Java `record`** is a special kind of class introduced in **Java 14 (preview)** and officially added in **Java 16**. It simplifies the creation of immutable data-holding objects by automatically generating common boilerplate code like constructors, `equals()`, `hashCode()`, and `toString()`.

---

### **Key Features**

1. **Immutable**: Fields of a `record` are final by default.
2. **Concise Syntax**: Automatically generates:
    - Constructor
    - Getters (for all fields)
    - `equals()`, `hashCode()`, and `toString()`
3. **Compact Definition**: Define only the fields; Java handles the rest.

---

### **Syntax**

``` java
public record RecordName(Type field1, Type field2) { }
```

---

### **Example**

```java
public record Person(String name, int age) { }  

public class Main {     
	public static void main(String[] args) {         
		Person person = new Person("Alice", 30); // Access fields    
		System.out.println(person.name()); // Output: Alice
	    System.out.println(person.age());  // Output: 30          
	     
	     // Auto-generated toString()         
	     System.out.println(person); // Output: Person[name=Alice, age=30]     
	} 
}
```

---

### **Benefits**

1. Reduces boilerplate for data classes.
2. Ensures immutability by default.
3. Automatically provides meaningful `equals()` and `hashCode()` implementations.

---

### **When to Use**

- Ideal for **DTOs (Data Transfer Objects)** or simple immutable data carriers.

---

### **Limitations**

1. Cannot extend other classes (but can implement interfaces).
2. Fields are implicitly `final`, so they cannot be changed after object creation.
3. No setters or custom mutable behavior allowed.
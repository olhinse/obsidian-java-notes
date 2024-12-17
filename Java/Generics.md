A **type variable** in Java is a placeholder for a type that is specified when a generic class, interface, or method is instantiated or invoked. It enables **type parameterization**, allowing code to be more flexible and reusable while maintaining type safety.

---

### **Key Features**

1. **Placeholder for a Type**: Represented by a single uppercase letter (e.g., `T`, `E`, `K`, `V`).
2. **Defined in Generics**: Used in generic classes, interfaces, and methods.
3. **Ensures Type Safety**: Allows the compiler to catch type errors at compile time.

---

### **Syntax**

```java
class GenericClass<T> {     
	private T value; // T is the type variable      
	public GenericClass(T value) {         
		this.value = value;     
	}    
	  
	public T getValue() {         
		return value;     
	}
}
```

---

### **Example**

```java
GenericClass<String> stringInstance = new GenericClass<>("Hello"); System.out.println(stringInstance.getValue()); // Output: Hello

GenericClass<Integer> intInstance = new GenericClass<>(42); System.out.println(intInstance.getValue()); // Output: 42
```

---

### **Type Variables in Methods**

```java
public static <T> void printArray(T[] array) {     
	for (T element : array) {         
		System.out.println(element);     
	}
}
```

Usage:

``` java
printArray(new String[] {"A", "B", "C"});
printArray(new Integer[] {1, 2, 3});
```

---

### **Common Type Variable Names**

- **`T`**: Type
- **`E`**: Element (used in collections)
- **`K`**, **`V`**: Key, Value (used in maps)
- **`N`**: Number

---

### **Key Points**

- Type variables are part of Java Generics.
- They make code reusable and type-safe.
- Specified at compile time to ensure type compatibility.
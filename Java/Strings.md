Here’s a list of the **most useful `String` methods** in Java, organized by functionality:

---

### **1. Basic Information**

|**Method**|**Description**|**Example**|
|---|---|---|
|`length()`|Returns the length of the string.|`"hello".length()` → `5`|
|`isEmpty()`|Checks if the string is empty.|`"".isEmpty()` → `true`|
|`isBlank()` (Java 11+)|Checks if the string is empty or contains only whitespace.|`" ".isBlank()` → `true`|

---

### **2. Character Access**

|**Method**|**Description**|**Example**|
|---|---|---|
|`charAt(index)`|Returns the character at the specified index.|`"hello".charAt(1)` → `'e'`|
|`codePointAt(index)`|Returns the Unicode code point at the specified index.|`"abc".codePointAt(1)` → `98` (for `'b'`)|
|`toCharArray()`|Converts the string to a character array.|`"java".toCharArray()` → `['j', 'a', 'v', 'a']`|

---

### **3. Substring Operations**

|**Method**|**Description**|**Example**|
|---|---|---|
|`substring(beginIndex)`|Extracts substring from `beginIndex` to the end of the string.|`"hello".substring(2)` → `"llo"`|
|`substring(beginIndex, endIndex)`|Extracts substring between `beginIndex` (inclusive) and `endIndex` (exclusive).|`"hello".substring(1, 4)` → `"ell"`|

---

### **4. Case Conversion**

|**Method**|**Description**|**Example**|
|---|---|---|
|`toLowerCase()`|Converts the string to lowercase.|`"Hello".toLowerCase()` → `"hello"`|
|`toUpperCase()`|Converts the string to uppercase.|`"hello".toUpperCase()` → `"HELLO"`|

---

### **5. Trim and Whitespace**

|**Method**|**Description**|**Example**|
|---|---|---|
|`trim()`|Removes leading and trailing whitespace.|`" hello ".trim()` → `"hello"`|
|`strip()` (Java 11+)|Removes leading and trailing whitespace (handles Unicode).|`" hello ".strip()` → `"hello"`|
|`stripLeading()` (Java 11+)|Removes leading whitespace only.|`" hello ".stripLeading()` → `"hello "`|
|`stripTrailing()` (Java 11+)|Removes trailing whitespace only.|`" hello ".stripTrailing()` → `" hello"`|

---

### **6. Search**

|**Method**|**Description**|**Example**|
|---|---|---|
|`indexOf(char)`|Returns the index of the first occurrence of a character.|`"hello".indexOf('e')` → `1`|
|`indexOf(String)`|Returns the index of the first occurrence of a substring.|`"hello".indexOf("lo")` → `3`|
|`lastIndexOf(char)`|Returns the index of the last occurrence of a character.|`"hello".lastIndexOf('l')` → `3`|
|`contains(CharSequence)`|Checks if the string contains the specified sequence.|`"hello".contains("ell")` → `true`|
|`startsWith(String)`|Checks if the string starts with the specified prefix.|`"hello".startsWith("he")` → `true`|
|`endsWith(String)`|Checks if the string ends with the specified suffix.|`"hello".endsWith("lo")` → `true`|

---

### **7. Replace and Modify**

|**Method**|**Description**|**Example**|
|---|---|---|
|`replace(oldChar, newChar)`|Replaces all occurrences of a character.|`"java".replace('a', 'o')` → `"jovo"`|
|`replace(CharSequence, CharSequence)`|Replaces all occurrences of a substring.|`"hello".replace("ell", "ipp")` → `"hippo"`|
|`replaceAll(regex, replacement)`|Replaces all substrings matching a regex.|`"a1b2c3".replaceAll("\\d", "*")` → `"a*b*c*"`|
|`replaceFirst(regex, replacement)`|Replaces the first substring matching a regex.|`"a1b2c3".replaceFirst("\\d", "*")` → `"a*b2c3"`|

---

### **8. Split and Join**

|**Method**|**Description**|**Example**|
|---|---|---|
|`split(String regex)`|Splits the string into an array using a regex delimiter.|`"a,b,c".split(",")` → `["a", "b", "c"]`|
|`split(String regex, limit)`|Splits the string into an array, limiting the number of results.|`"a,b,c".split(",", 2)` → `["a", "b,c"]`|
|`join(CharSequence, CharSequence...)`|Joins strings with a delimiter.|`String.join("-", "a", "b", "c")` → `"a-b-c"`|

---

### **9. Comparison**

|**Method**|**Description**|**Example**|
|---|---|---|
|`equals(Object)`|Checks if two strings are equal.|`"hello".equals("hello")` → `true`|
|`equalsIgnoreCase(String)`|Compares strings ignoring case.|`"hello".equalsIgnoreCase("HELLO")` → `true`|
|`compareTo(String)`|Compares strings lexicographically.|`"abc".compareTo("bcd")` → `-1`|
|`compareToIgnoreCase(String)`|Compares strings lexicographically, ignoring case.|`"abc".compareToIgnoreCase("ABC")` → `0`|

---

### **10. Formatting**

|**Method**|**Description**|**Example**|
|---|---|---|
|`format(String format, Object...)`|Formats the string like `printf`.|`String.format("Hello %s", "World")` → `"Hello World"`|
|`valueOf(Object)`|Converts an object to a string.|`String.valueOf(123)` → `"123"`|

---

### **11. Encoding and Decoding**

|**Method**|**Description**|**Example**|
|---|---|---|
|`getBytes()`|Converts the string into a byte array using the platform's default charset.|`"hello".getBytes()`|
|`getBytes(Charset)`|Converts the string into a byte array using a specified charset.|`"hello".getBytes(StandardCharsets.UTF_8)`|

---

### **12. Miscellaneous**

|**Method**|**Description**|**Example**|
|---|---|---|
|`intern()`|Returns the canonical representation of the string.|`"hello".intern()`|
|`repeat(int)` (Java 11+)|Repeats the string multiple times.|`"hi".repeat(3)` → `"hihihi"`|

---

These methods cover the majority of operations you'll need when working with strings in Java!
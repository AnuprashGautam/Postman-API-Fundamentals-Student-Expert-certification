We use **path variables** in APIs to make parts of the URL dynamic, allowing the API to handle different inputs without creating multiple endpoints. They are commonly used to identify specific resources.

### **Example Scenario**  
Imagine an API that retrieves details of a user by their ID.

### **Without Path Variables**  
You'd have to use different endpoints like:  
- `/getUserById1`  
- `/getUserById2`

This is inefficient.

### **With Path Variables**  
Use a single endpoint with a path variable:  
```http
GET /users/{id}
```

### **How It Works**
- The `{id}` in the path is dynamic.  
- Example: `GET /users/123` retrieves details of the user with ID `123`.  
- The API extracts the value of `{id}` and processes it.

### **Code Example** (Java Spring Boot)
```java
@GetMapping("/users/{id}")
public ResponseEntity<User> getUserById(@PathVariable int id) {
    // Logic to fetch user by id
    return ResponseEntity.ok(userService.getUserById(id));
}
```

### **Benefits**  
1. **Cleaner URLs**: Focused and readable.
2. **Dynamic Data**: Handle variable inputs easily.
3. **RESTful Design**: Follows REST conventions. 

In short, path variables make APIs efficient and flexible. 🚀
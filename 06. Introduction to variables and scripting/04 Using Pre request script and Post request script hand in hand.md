# how to make the local variable that have scope limited to an endpoint in `get book by id` and I want to initialise that local variable by a collection scope variable by using pre request script?


1. **Use a Collection Variable**  
    Collection variables are predefined in your Postman collection and can be accessed using `pm.collectionVariables.get()`.
    
2. **Set a Local Variable in Pre-request Script**  
    Use `pm.variables.set()` to initialize a local variable using the value of the collection variable.
    
3. **Access the Local Variable in the Request**  
    You can refer to the local variable in your request by enclosing it in double curly braces, e.g., `{{localVariableName}}`.
### Why Use Query Parameters?

Query parameters are used in URLs to pass **data** to a server for filtering, searching, or customizing responses without altering the endpoint. They are part of the URL after the `?` symbol and typically appear as key-value pairs, separated by `&`.

### Example

#### URL with Query Parameters:
```plaintext
https://example.com/products?category=electronics&sort=price_asc
```

- `category=electronics`: Filters the products by category.
- `sort=price_asc`: Sorts the products by price in ascending order.

#### Explanation
1. **Flexibility:** The same endpoint (`/products`) can handle multiple requests with different data.
2. **Statelessness:** Parameters do not require maintaining server-side session data.
3. **Clarity:** They make it easy to see the data being passed to the API in the URL.

#### Code Example

**Frontend Call:**
```javascript
fetch('https://example.com/products?category=electronics&sort=price_asc')
  .then(response => response.json())
  .then(data => console.log(data));
```

**Backend Handling (Express.js):**
```javascript
app.get('/products', (req, res) => {
  const { category, sort } = req.query; // Get query params
  const products = getProducts(category, sort); // Function to filter and sort
  res.json(products);
});
```

Query parameters are essential for APIs that support customization and filtering in a clean, maintainable way.
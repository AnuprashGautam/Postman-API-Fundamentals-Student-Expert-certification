### __Task: Get Books from the Library API__

First things first: a librarian must know how to view all the books in the library catalog. According to the API documentation, you can get all the books in the library by making a request to `GET https://library-api.postmanlabs.com/books`. Here, `GET` is the request method, and the request URL indicates where the request is sent.

#### __Steps to Make Your First Request__

1. **Create a new request**:
   - Click "Add a request" inside your new Collection or hover on your Collection, then click the three dots icon and "Add request".
   - Name your request "get books".
   - Set the request method to `GET`, and the request URL to `GET https://library-api.postmanlabs.com/books`.
   - Save your work.

2. **Send your request**:
   - Click the "Send" button.

3. **View the response**:
   - If everything goes well, you will see a response from the server in the lower half of Postman. It should look like a JSON (JavaScript Object Notation) response body with an array of book objects. You might see different books because this public library is being modified in real-time by other Postman librarians worldwide!

#### __Request Methods__

When making an HTTP call to a server, specify a request method that indicates the type of operation to perform. These are also called HTTP verbs. Some common HTTP request methods correspond to the CRUD operations:

| Method Name | Operation |
|-------------|------------|
| GET         | Retrieve data (Read) |
| POST        | Send data (Create) |
| PUT/PATCH   | Update data (Update) |
| DELETE      | Delete data (Delete) |

Since we are "getting" books and not modifying any data, it makes sense that we are making a `GET` request. These are just conventions - it all depends on how the API is coded. Always read the documentation for the API you're working with!

#### __Request URL__

In addition to a request method, a request must include a request URL that indicates where to make the API call. A request URL has three parts: a protocol (such as `http://` or `https://`), host (location of the server), and path (route on the server). In REST APIs, the path often points to a reference entity, like "books".

| Protocol | Host | Path |
|----------|------|------|
| https:// | library-api.postmanlabs.com | /books |

Paths and complete URLs are also sometimes called API endpoints.

#### __Response Status Codes__

The Postman Library API v2 has returned a response status code of "200 OK". Status codes are indicators of whether a request failed or succeeded. Status codes have conventions. For example, any status code starting with a "2xx" (a "200-level response") represents a successful call.

| Code Range | Meaning | Example |
|------------|---------|---------|
| 2xx        | Success | 200 - OK, 201 - Created, 204 - No content (silent OK) |
| 3xx        | Redirection | 301 - Moved (path changed) |
| 4xx        | Client error | 400 - Bad request, 401 - Unauthorized, 403 - Not Permitted, 404 - Not Found |
| 5xx        | Server error | 500 - Internal server error, 502 - Bad gateway, 504 - Gateway timeout |

In Postman, you can hover over any response code to see what it means.
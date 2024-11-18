### __Query Parameters__

Query parameters are key-value pairs added to the end of a request URL to refine the request.

#### __Syntax__
- Query parameters start with a question mark `?` and follow the format: `<key>=<value>`.
- Multiple query parameters are separated by an ampersand `&`.

Example:
- To fetch all photos with landscape orientation: `GET https://some-api.com/photos?orientation=landscape`
- To specify orientation and size: `GET https://some-api.com/photos?orientation=landscape&size=500x400`

#### __Google Search Example__
- To search for "Postman" on Google: `https://www.google.com/search?q=postman`
- The query parameter `q=postman` adds the search term to the request.

#### __Usage__
- Query parameters can be optional or required, depending on the API documentation.
- They allow adding filters or extra data to responses.

#### __Postman Library API v2 Example__
- The API allows adding optional query parameters to requests to `GET /books` to filter the books returned in the response.
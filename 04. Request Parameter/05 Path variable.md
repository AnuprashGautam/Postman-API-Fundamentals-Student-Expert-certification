### __Path Variable__

Another way of passing request data to an API is via path variables (also known as "path parameters"). A path variable is a dynamic section of a path and is often used for IDs and entity names such as usernames.

#### __Path Variable Syntax__

- The path variable comes immediately after a slash in the path.
- Example: The GitHub API allows you to search for GitHub users by providing a username in the path in place of `{username}`:
  - `GET https://api.github.com/users/{username}`
  - Making this API call with a value for `{username}` will fetch data about that user:
    - `GET https://api.github.com/users/postmanlabs`

- Multiple path variables can be used in a single request:
  - Example: To get information about the newman code repository from postmanlabs:
    - `GET https://api.github.com/repos/postmanlabs/newman`

#### __Path vs. Query Parameters__

| Path Variable | Query Parameters |
|---------------|------------------|
| Example: `/books/abc123` | Example: `/books?search=borges&checkedOut=false` |
| Located directly after a slash in the path. It can be anywhere on the path. | Located only at the end of a path, right after a question mark `?`. |
| Accepts dynamic values. | Accepts defined query keys with potentially dynamic values. |
| Often used for IDs or entity names. | Often used for options and filters. |

These are just conventions! Some APIs might ask you to pass an ID or username in a query parameter like this: `/users?username=getpostman`.

#### __When to Use Path Variables?__

Always read the API documentation! If a path parameter is required, the documentation will mention this. Note that some API documentation uses colon syntax to represent a wildcard in the path like `/users/:username`, while some use curly braces like `/users/{username}`. They both mean the same thing: that part of the path is dynamic!

Next, we will use the path variable with the Postman Library API v2 to get a specific book.
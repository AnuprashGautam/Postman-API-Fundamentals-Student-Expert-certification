### __Setting Variables Programmatically__

Postman allows you to add automation and dynamic behaviors to your collections with scripting. Scripts can be executed at two points in the request flow:
- **Pre-request Script**: Runs immediately before a request is sent.
- **Post-response Script**: Runs immediately after a response is received.

#### __The `pm` Object__
Postman provides a helper object named `pm` that gives you access to data about your Postman environment, requests, responses, variables, and testing utilities.

- **Access JSON Response Body**: `pm.response.json()`
- **Get Collection Variables**: `pm.collectionVariables.get("baseUrl")`
- **Set Collection Variables**: `pm.collectionVariables.set("variableName", "variableValue")`

In the next task, you will use scripting and the `pm` object to set a new book's automatically generated id as a collection variable for use in other requests.
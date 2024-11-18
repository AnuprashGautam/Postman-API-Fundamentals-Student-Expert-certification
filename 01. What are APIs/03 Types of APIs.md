### __Types of APIs__

While this course will focus on Web APIs, it is important to know that "API" can apply to a broad range of interfaces.

#### __Hardware APIs__
Interface for software to talk to hardware.
- **Example**: How your phone's camera talks to the operating system.

#### __Software Library APIs__
Interface for directly consuming code from another code base.
- **Example**: Using methods from a library you import into your application.

#### __Web APIs__
Interface for communicating across code bases over a network.
- **Example**: Fetching current stock prices from a finance API over the internet.

Multiple API types may be used to achieve a task. For example, uploading a photo to Instagram makes use of various APIs:
- **Hardware API** for the app to talk to your camera.
- **Software library API** for the image to be processed with filters.
- **Web API** for sending your image to Instagram's servers so your friends can like it!

### __Architectures__

There is more than one way to build and consume APIs. Some architecture types you may come across are:
- **REST (Representational State Transfer)**
- **GraphQL**
- **WebSockets**
- **Webhooks**
- **SOAP (Simple Object Access Protocol)**
- **gRPC (Google Remote Procedure Call)**
- **MQTT (MQ Telemetry Transport)**

This course will focus on REST APIs since this is the most widely adopted API architecture.

#### __REST APIs__
Some traits of REST APIs include not storing session state between requests, the ability to cache, and the ability to send and receive various data types.

### __Access APIs__

APIs also vary in the scope of who can access them.

- **Public APIs (aka Open APIs)**: Consumed by anyone who discovers the API.
- **Private APIs**: Consumed only within an organization and not made public.
- **Partner APIs**: Consumed between one or more organizations that have an established relationship.

The API we will use in this course will be a Public, REST, Web API. You can read more about types of APIs on the Postman Blog.
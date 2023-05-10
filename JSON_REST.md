# JSON

1. **Syntax**:
   * JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy to read and write.
   * JSON objects are surrounded by curly braces {} and consist of key-value pairs separated by commas.
   * Keys must be strings and are enclosed in double quotes.
   * Values can be strings, numbers, booleans, objects, or arrays.
   * Arrays are enclosed in square brackets [] and can contain values of any type, separated by commas.

2. **Data Types**:
   * String: Enclosed in double quotes, e.g., `"Hello, World!"`
   * Number: Integer or floating-point, e.g., `42 or 3.14`
   * Boolean: `true or false`
   * Object: A collection of key-value pairs, e.g., `{"name": "John", "age": 30}`
   * Array: An ordered list of values, e.g., `["apple", "banana", "cherry"]`
   * Null: Represents an empty or non-existent value, e.g., `null`

3. **JSON.parse() and JSON.stringify()**:
   * `JSON.parse()`: Converts a JSON string into a JavaScript object.
   * `JSON.stringify()`: Converts a JavaScript object into a JSON string.

4. **JSON Schema**:
   * JSON Schema is a vocabulary that allows you to annotate and validate JSON documents.
   * It provides a way to describe the structure, constraints, and requirements of a JSON object.
   * Using JSON Schema can help ensure that the JSON data exchanged between services or components is well-formed and adheres to a predefined structure.

# REST

1. **RESTful Architecture**:
   * REST (Representational State Transfer) is an architectural style for designing networked applications.
   * It relies on a stateless, client-server protocol, usually HTTP.
   * RESTful APIs expose resources (e.g., users, products, orders) that can be manipulated using standard HTTP methods.
   * RESTful APIs are designed to be cacheable, scalable, and maintainable.
2. **HTTP Methods**:
   * `GET`: Retrieve a resource or collection of resources.
   * `POST`: Create a new resource.
   * `PUT`: Update an existing resource.
   * `PATCH`: Partially update an existing resource.
   * `DELETE`: Remove a resource.
3. **Status Codes**:
HTTP status codes are three-digit numbers that indicate the outcome of an HTTP request.
   * 1xx (Informational): The request was received, and the server is continuing to process it.
   * 2xx (Successful): The request was successfully received, understood, and accepted.
   * 3xx (Redirection): The request needs further action to be completed, usually by following a provided URL.
   * 4xx (Client Error): The request contains bad syntax or cannot be fulfilled by the server.
   * 5xx (Server Error): The server failed to fulfill a valid request.

4. **RESTful API Design Best Practices**:
   * Use consistent and descriptive resource naming conventions (e.g., nouns in plural form).
   * Use standard HTTP methods to perform actions on resources.
   * Return appropriate HTTP status codes to indicate the outcome of a request.
   * Provide clear and concise error messages when a request cannot be fulfilled.
   * Use query parameters for filtering, sorting, and pagination in resource collections.
   * Use versioning to manage changes to the API and maintain backward compatibility.
   * Leverage caching to improve performance and reduce server load.
   * Secure the API using authentication and authorization mechanisms, such as OAuth or JWT.
------------------


###### Here are some of the most common HTTP status codes and their meanings:

* `200 OK`: The request has succeeded, and the server has returned the requested data.
* `201 Created`: The request has been fulfilled, and a new resource has been created as a result.
* `204 No Content`: The request has succeeded, but there is no additional information to send back (usually used for DELETE requests).
* `400 Bad Request`: The server cannot process the request due to malformed syntax or invalid data.
* `401 Unauthorized`: The request requires authentication, and the client has failed to provide valid credentials.
* `403 Forbidden`: The client does not have permission to access the requested resource.
* `404 Not Found`: The requested resource could not be found on the server.
* `405 Method Not Allowed`: The HTTP method used in the request is not supported for the specified resource.
* `409 Conflict`: The request could not be completed due to a conflict with the current state of the resource (e.g., an attempt to create a resource with a duplicate identifier).
* `500 Internal Server Error`: The server encountered an error while processing the request.
* `502 Bad Gateway`: The server, while acting as a gateway or proxy, received an invalid response from an upstream server.
* `503 Service Unavailable`: The server is currently unable to handle the request due to temporary overload or maintenance.

These are just some examples of the many HTTP status codes that can be returned by a server. Each status code provides information about the outcome of a request, allowing clients to handle different scenarios appropriately.

------------------


# REST API

REST (Representational State Transfer) is an architectural style for designing networked applications. RESTful APIs use HTTP methods to interact with resources in a stateless, scalable, and cacheable manner. Here's a more in-depth look at RESTful API concepts, along with examples using FastAPI, a modern Python web framework for building APIs.

1. ### Resources:

Resources are the core building blocks of a RESTful API, representing entities such as users, products, or orders.
Resources are identified by unique URIs (Uniform Resource Identifiers), which are used to interact with them.
Example: In FastAPI, you can define a resource using route decorators and functions:

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/users/{user_id}")
async def get_user(user_id: int):
    # Retrieve and return the user with the specified user_id.

```

2. ### HTTP Methods:

* **RESTful APIs use standard HTTP methods to perform actions on resources**:
  * `GET`: Retrieve a resource or a collection of resources.
  * `POST`: Create a new resource.
  * `PUT`: Update an existing resource.
  * `PATCH`: Partially update an existing resource.
  * `DELETE`: Remove a resource.
* Example: FastAPI allows you to define handlers for different HTTP methods using route decorators:
    ```python
    @app.post("/users/")
    async def create_user(user: UserCreate):
        # Create and return a new user.

    @app.put("/users/{user_id}")
    async def update_user(user_id: int, user: UserUpdate):
        # Update and return the user with the specified user_id.

    @app.delete("/users/{user_id}")
    async def delete_user(user_id: int):
        # Delete the user with the specified user_id.
    ```

3. ### Status Codes:
As discussed earlier, HTTP status codes indicate the outcome of a request. In FastAPI, the status code can be set using the status_code parameter in the route decorator:
```python
@app.post("/users/", status_code=201)
async def create_user(user: UserCreate):
    # Create and return a new user.
```

4. ### Query Parameters, Path Parameters, and Request Bodies:

  * RESTful APIs can use query parameters, path parameters, and request bodies to pass data between the client and the server.
  * Example: FastAPI automatically handles query parameters, path parameters, and request bodies based on type annotations and Pydantic models:
    ```python
    from fastapi import FastAPI
    from pydantic import BaseModel

    app = FastAPI()

    class UserCreate(BaseModel):
        name: str
        age: int

    @app.get("/users/")
    async def get_users(skip: int = 0, limit: int = 10):
        # Retrieve users with pagination using the 'skip' and 'limit' query parameters.

    @app.post("/users/")
    async def create_user(user: UserCreate):
        # Create a new user using data from the request body (automatically parsed as a UserCreate object).
    ```

5. ### Error Handling:
  * RESTful APIs should provide clear and concise error messages when a request cannot be fulfilled.
  * Example: FastAPI automatically generates error responses based on the status codes and exceptions raised by your code:
    ```python
    from fastapi import FastAPI, HTTPException

    app = FastAPI()

    @app.get("/users/{user_id}")
    async def get_user(user_id: int):
        user = find_user(user_id)
        if user is None:
            raise HTTPException(status_code=404, detail="User not found")
        return user
    ```

    In this example, FastAPI raises an HTTPException with a 404 status code and a detail message when the user is not found. FastAPI will automatically convert the exception into a JSON error response.

6. ### Authentication and Authorization:
  * RESTful APIs should secure resources using authentication and authorization mechanisms, such as OAuth or JWT.
  * Example: FastAPI provides built-in support for OAuth2 and dependencies for handling authentication and authorization:
    ```python
    from fastapi import FastAPI, Depends, HTTPException
    from fastapi.security import OAuth2PasswordBearer

    app = FastAPI()

    oauth2_scheme = OAuth2PasswordBearer(tokenUrl="token")

    async def get_current_user(token: str = Depends(oauth2_scheme)):
        user = get_user_from_token(token)
        if user is None:
            raise HTTPException(status_code=401, detail="Invalid token")
        return user

    @app.get("/users/me")
    async def get_me(current_user: User = Depends(get_current_user)):
        return current_user
    ```

In this example, the `oauth2_scheme` is defined to handle OAuth2 tokens, and the `get_current_user` function is declared as a dependency to retrieve the current user based on the token. The `get_me` endpoint uses the `get_current_user` dependency to ensure that only authenticated users can access their own information.

By following RESTful principles and using frameworks like FastAPI, you can design and implement APIs that are easy to understand, maintain, and scale.

------------------

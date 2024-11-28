#### 1. Loading and Installation 
- In this, the compiled class file is loaded in the memory.
- An object is created of the _Main_ Servlet file.

#### 2. Initialization 
- Servlet methods will be initialized by the `init()` method.

#### 3. Request Handling
- This step calls the `service()` method, when the client send the request to the server.
- It also check the type of the request and calls the required method accordingly.
- each request created a new thread that handles the client request according to its type.

#### 4. Destroy 
- The method used here is `destroy()`. 
- This method is executed when the main servlet file’s object is being destroyed.
- This method is executed when the server is shutdown and memory is freed.


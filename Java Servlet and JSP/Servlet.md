**Servlet:** It is a server-side technology that i sused to handle client requests, process the requests and generate dynamic responses.

##### What happens at backend
- The client (browser) send a request to the server. The server accepts the request.
- The server are of two types –
  1. **Web server:** Apache Tomcat, Glassfish, Jetty
  2. **Application server:** JBoss IBM workspace, WebLogic
- The server has different containers taht handles and processes the request. Some container examples are JSP, Servlet container, Security container, WebSocket container, JNDI container, etc.
- These containers processes the request and creates a static or dynamic responses, and this dynamic responses are sent to the client.
- Some otehr server-side technologies are JSP, Spring/Springboot, Srouts/JFS, PHP, etc.

#### Servlet
- A servlet is a pre-defined interface.
- There’s another class called generic-servlet that inherits the servlet interface.
- HTTP servlet that inherits the GenericServlet
```
   Servlet
     ↓
GenericServlet
     ↓
 HTTPServlet
```
- The **Servlet** only has lifecycle methods.
- The **GenericServlet** used when we want to use protocol-independent servlet.
- **Protocol-independent** servlet is the one that can handle requests from different network protocols such as HTTP, HTTPS, FTP, etc.
- The class dows not have the request and response object.
 - **HTTPServlet** used when we require the request and response object, HTTP specific methods.
 - These HTTP specific methods includes – GET, POST, HEAD, PUT, DELETE

###### A basic Boiler-Plate code for usage:
```Java
public class Main extends HTTPServlet {
	@override
	public static void service(HTTPServletRequest request, HTTPServletRequest response) {
		// backend code
	}
}
```

> [!NOTE] Note
> We also have to create one more file, the **Deployment Descriptor** file named as “web.xml”.

- When extending the _HTTPServlet_ class, we need to throw the **IOException**, **ServletException**. 
**web.xml** is also known as  deployment descriptor file, because when a project is deployed, all its description is stored in this file.
- This file has the servlet mapping feature that directs the client to the desired java servlet file.
- It uses the XML syntax.

###### A basic syntax for this file is
```XML
<webapp>
	<servlet-mapping>
		<servlet-name>   </servlet-name>
		<url-pattern>   </url-pattern>
	</servlet-mapping>
	<servlet>
		<servlet-name>   </servlet-name>
		<servlet-class>   </servlet-class>
	</servlet>
</webapp>
```

- This file is created in the **WEB-INF** folder, in **webapp** folder.
- In the latest java edition, its not compulsory to create the web.xml file. 
- We use annotations instead – `@WebServlet`,  `@WebFilter`, etc.

##### Tasks of Deployment Descriptor file
- Servlet Configuration 
- JSP File Configuration 
- Filter Configuration 
- Listeners Configuration 
- Error Page Configuration 
- Welcome Page Configuration 

#### _HttpServletRequest_ and _HttpServletResponse_
- _HttpServletRequest_ and _HttpServletResponse_ are the two interfaces in java that are used to send and retrieve information from a webapp. 
- The _HttpServletRequest_ object is used to retrieve the data that the webapp is sending and stores it at backend using `getParameter()` method. 
- Similarly, the _HttpServletResponse_ object is used to send data to the webapp from backend. Eg. we use _PrintWriter_ class with response object to display something in the screen. 


#### Running the project without the Deployment Descriptor
- The latest Java servlets can be executed without the presence of the deployment descriptor.
- Instead of the web.xml file, the main Java contains an annotation in the beginning (before the Main class):
  `@WebServlet("/demo")`


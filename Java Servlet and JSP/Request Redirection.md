### External Request Redirection 
- We use `sendRequest()` method for external request redirection. 
- When a redirection from our application to another external application is called **External Request Redirection**. 
- Its a method of _HttpServletResponse_ class. 
- `sendRedirect()` method will change the URLs. 
- E.g. A button in my application that redirects the user to a google search page
- This method is used with _HttpServletResponse_ object. 

### Internal Request Redirection 
- The _RequestDispatcher_ Interface is used to request from another source from same application. 
- No URL is changed in this case. 
- When a redirection from our application page is done to another page of the our same application is called **Internal Request Redirection**. 
- The `forward()` method adds the given content to the pre-existing resource. The browser still interacts with the same page. 
- Another method named `include()` is also there, to include additional elements on the redirected page. 
 > [!Tip] Tip  
 > A method name `setContentType()` is used to add attributes to the included part of the webpage. 


| _**HttpServletResponse**_ **Class**                         | _**RequestDispatcher**_ **Interface**                               |
| ----------------------------------------------------------- | ------------------------------------------------------------------- |
| It is used for external request redirection.                | It is used for internal request redirection.                        |
| It redirects the request to a different application or URL. | It forwards or includes the request to the same application or URL. |
| It uses the `sendRedirect()` method.                        | It has 2 methods, `forward()` and `include()`.                      |
| It change the URL on the browser.                           | It does not change the URL on the browser.                          |





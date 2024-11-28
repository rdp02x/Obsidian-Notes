- GET and POST are the Http methods/Http verbs.
- There are many Http Methods other than GET and POST. 
- These Http methods defines the specific actions that can be performed on the resources like Java files, Images files, Document files, etc. that are present/stored on server. 
- **GET Method:** It sends the data through URL and hence is not secure (but faster).
- **POST Method:** It sends the data through HTTP message body and hence is more secured. 

###### Difference between GET and POST:

| **GET**                                                                                 | **POST**                                                                  |
| --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| Sends data through resource URLs                                                        | Send data through HTP message body.                                       |
| Not secure as URL is visible                                                            | Secure as no data is in URL                                               |
| Faster as values are send in header                                                     | Slower as values are send in request bodies                               |
| Very less data can be sent through GET as URL length is limited to 2048 characters only | Huge amount of data can be send through POST as there are no restrictions |
| Method used here is `doGet()`                                                           | Method used here is `doPost()`                                            |

### Fetching Data
- To fetch data from a search bar in a HTML page, we first we give an attribute called _name_ to the element.
- Then using the name element, we fetch the data through the servlet code.
- Here comes the use of the method `getParameter()`, and the parameter it is going to accept will be same as the value of _name_, attribute. (The parameter value should be a string, so add in double quotes).
- This method is used with the _HttpServletRequest_ object. 




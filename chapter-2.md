<strong>
<p align="justify">

# Getting started with Postman

![](imgs/api3.png)

## Creating a Workspace

> This REST API allows you to CRUD (Create, Read, Update, Delete) books in a public library database. You will use Postman to interact with this API and manage books.

- Workspaces dropdown > Create Workspace
<br>

<img width="50%" src="./imgs/api4.png"/>

<br>

- Name your workspace "Postman API Fundamentals Student Expert" and set the visibility to Public (or Personal if you cannot make a Public workspace on your team). Then click "Create Workspace"
<br><br>

<img width="50%" src="./imgs/api5.png"/>

<br><br>

## Create a Collection

- From the left pane, either click the plus ("+") icon or Create collection.
<br><br>
<img width="50%" src="./imgs/api6.png"/>
<br>

- Name your new Collection as "Postman Library API v2".
<br><br>
<img width="50%" src="./imgs/api7.png"/>
<br>

## Make your First Request

> Keep in mind all this is a tutorial from Postman Student Program, so you can refer the main documentation as well by enrolling there for free.

> According to the API documentation, you can get all the books in the library by making a request to GET https://library-api.postmanlabs.com/books. Here, GET is the request method and the url is the request URL.

- Create a new request by either clicking Add a request inside your new Collection, or hovering on your Collection, then clicking the three dots icon and "Add request"
<br><br>
<img width="50%" src="./imgs/api8.png"/>
<br>

- Name your request "get books". Set the request method to GET, and the request URL to GET https://library-api.postmanlabs.com/books. Be sure to hit Save!
- Send your request by clicking the Send button
- If everything goes well, you will see a response from the server in the lower half of Postman. 

- It should look something like this: a JSON (JavaScript Object Notation) response body that is an array of book objects. You can scroll down to see more books.

<br><br>
<img width="100%" src="./imgs/api9.png"/>
<br>


## Request Methods

- When we make an HTTP call to a server, we specify a request method that indicates the type of operation we are about to perform. These are also called HTTP verbs.

<table>
    <tr>
        <th>Method Name</th>
        <th>Operation</th>
    </tr>
    <tr>
        <td>GET</td>
        <td>Retrieve data (Read)</td>
    </tr>
    <tr>
        <td>POST</td>
        <td>Send data (Create)</td>
    </tr>
    <tr>
        <td>PUT/PATCH</td>
        <td>
            Update data (Update)
            * PUT usually replaces an entire resource, whereas PATCH usually is for partial updates
        </td>
    </tr>
    <tr>
        <td>DELETE</td>
        <td>Delete data (Delete)</td>
    </tr>
</table>

<br>

> Since we are "getting" books and not modifying any data, it makes sense that we are making a GET request. 

## Request URL

In addition to a request method, a request must include a request URL that indicates where to make the API call. A request URL has three parts: a protocol (such as http:// or https://), host (location of the server), and path (route on the server). In REST APIs, the path often points to a reference entity, like "books".

> Paths and full URLs are also sometimes called API endpoints.

## Response Status Codes

> The "Postman Library API v2" has sent back a response status code of "200 OK". Status codes are indicators of whether a request failed or succeeded. Status codes have conventions.

<br>

<table>
    <tr>
        <th>Code Range</th>
        <th>Meaning</th>
        <th>Example</th>
    </tr>
    <tr>
        <td>2xx</td>
        <td>Success</td>
        <td>
            200 - OK <br>
            201 - Created <br>
            204 - No content (silent OK)</td>
    </tr>
    <tr>
        <td>3xx<br><br><br><br>4xx</td>
        <td>Redirection<br><br><br><br>Client Error</td>
        <td>
            301 - Moved (path changed) <br><br>
            400 - Bad request <br>
            401 - Unauthorized <br>
            403 - Not Permitted <br>
            404 - Not Found</td>
    </tr>
    <tr>
        <td>5xx</td>
        <td>Server Error</td>
        <td>
            500 - Internal server error <br>
            502 - Bad gateway <br>
            504 - Gateway timeout</td>
    </tr>
</table>

<br>

## Request Response Pattern

- Now you can understand the request response pattern, which represents how computers communicate over a network. An API is the interface that lets us know what kind of response to expect when we make certain calls to a server.

You made an HTTP GET request to https://library-api.postmanlabs.com/books and received a response from the server.

<br><br>
<img width="50%" src="./imgs/api10.png"/>
<br>


The client is the agent making a request. A client could be a browser or an application you have coded, for example. In our case Postman is the client because that's how we sent the request. 

The request is sent over a network to some server. In our case, we made a request over the public internet to a server located at the address https://library-api.postmanlabs.com. 

The server interpreted the request (GET /books) and sent the appropriate response over the network back to the Postman client: a list of books.


</strong>
</p>

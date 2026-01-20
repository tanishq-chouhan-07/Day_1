# Frontend Vs Backend

## Frontend 

- is the GUI of a Full Stack Application used by the End user.

- It Mainly Focuses on the Sending the User interactions to the backend or the Sever side of the Application. 

- Frontend may different for the different types of the devices like they have the different interface but they will work with the same backend appliaction services

- Fundamentally WE use the html ,css and js for the interaction of the users and storing and for the work of Response and Request cycle in the client Sever Architecture

## Backend

- is the Kind of the Functional part of a functional part of the Full stack application.

- this part of the full stack application is the not interacting with the user.

- Their are lot of services and request are made to the backend of the application.

- A single Backend can handle large number of the request from different frontend services and other services in the same application to work

## Key Difference Between them includes

- Frontend focuses on the what the end user see and interact with. but for the functional part of the the application and the response generation of the user query is the generated or responsed by this part.

- Example : think of the Frontend as exterior of the car and the Backend of the car is the engine and other things which make the car functional and runnable

### Development Goals : 

- Frontend developers aim to develop a positive user experience, optimize the application for accessibility and performance, and create responsive designs.
 
 - Backend developers build and then maintain the server-side operations of an application. Their main development goals are to create reliable architecture that performs application functions accurately and efficiently. 

 - Concurreny : of in the full stack project is primary focuses on the backend of the system not in the frontend part of the system

 other are : Security , Development Goals , Caching

---

# Client Server Architecture 

in the client Server Architecture is a network model in which two entities - 

- Client  : Responsible for interacting with the user, it requests services and resources.
- Server: Processes the requests and manages the resources, sending appropriate responses back to clients.

communicates with each other to complete the specific tasks or share the data.

## Key Benifits of the CLient Server Architecture

- to understand how the data flow in the Request Response cycle 

- help to understand the requirement of resources and cost to provide the scalable and the reliable Applications

## Types of the Architectures

- Two-Tier Architecture: The simplest form where clients and servers communicate directly.

- Three-Tier Architecture: A middleware layer, often called the application layer, is added between the client and server.

- N-Tier Architecture: Involves multiple intermediary layers, such as security and business logic, to manage complex data processing and ensure security.

---

# How the web works: DNS → HTTP → Response

## Components of Web : 

- Client : who initialize the requests 
- Server : which Respond to the user query
- Ip address : used to identify the device over the internet to make the connection for the communication
- ISP : it is the middle man btw the client and server
- DNS : Domain Name System is the phonebook for the websites like they map the websites hosted ipaddress to their respective domain names .
- Domain name : Users use the domain name instead of the ip address to find websites over the internet. because the typing of the Ip address is not reliable and easy because the changing of one single character can redirect the user to some else website. 

- TCP/IP: Transmission Control Protocol / internet Protocol is the most widely used communication protocols used for the communicaton over the browser

- Port Number : A 16-bit integer that identifies a specific port on a server and is always associated with an IP address. It serves as a way to identify a specific process on a server that network requests could be forwarded to.

- Host : All servers are host but not all Hosts are servers. A computer connected to a network — it can be a client, server or any other type of device. Each host has a unique IP address

- HTTP: Hyper-text Transfer Protocol. The protocol that web browsers and web servers use to communicate with each other over the Internet.

- URL: Uniform Resource Locators. URLs identify a particular web resource.



---
## DNS : Domain Name System

The Domain Name System (DNS) is the phonebook of the Internet. Humans access information online through domain names, like nytimes.com or espn.com. Web browsers interact through Internet Protocol (IP) addresses. DNS translates domain names to IP addresses so browsers can load Internet resources.

### Working of DNS 

The process of DNS resolution involves converting a hostname (such as www.example.com) into a computer-friendly IP address (such as 192.168.1.1). An IP address is given to each device on the Internet, and that address is necessary to find the appropriate Internet device

### Their are 4 Servers are involved in the loading of a web page in the browser

- DNS Recursor : The DNS recursor is a server designed to receive queries from client machines through applications such as web browsers. Typically the recursor is then responsible for making additional requests in order to satisfy the client’s DNS query.

- Root Name Server : The root server is the first step in translating (resolving) human readable host names into IP addresses.

- TLD nameserver : This nameserver is the next step in the search for a specific IP address, and it hosts the last portion of a hostname 

- Authoritative nameserver :The authoritative nameserver is the last stop in the nameserver query. If the authoritative name server has access to the requested record, it will return the IP address for the requested hostname back to the DNS Recursor that made the initial request.

### Thier are 3 main type of DNS queries : 

- Recursive query - In a recursive query, a DNS client requires that a DNS server (typically a DNS recursive resolver) will respond to the client with either the requested resource record or an error message if the resolver can't find the record.
- Iterative query - in this situation the DNS client will allow a DNS server to return the best answer it can. If the queried DNS server does not have a match for the query name, it will return a referral to a DNS server authoritative for a lower level of the domain namespace. The DNS client will then make a query to the referral address. This process continues with additional DNS servers down the query chain until either an error or timeout occurs.
- Non-recursive query - typically this will occur when a DNS resolver client queries a DNS server for a record that it has access to either because it's authoritative for the record or the record exists inside of its cache. Typically, a DNS server will cache DNS records to prevent additional bandwidth consumption and load on upstream servers.



## Steps in the DNS http and Response Cycle 

### Step 1 : DNS Query

First the user make a query over the internet from the browsers or the applications from the system

### Step 2 :  Recursive DNS Query

The recursive DNS resolver handles the heavy lifting by querying multiple servers to find the correct IP address.

- Root name Server 

- TLC name Server 

- Authoritive name Server

### Step 3: Establishing a Connection

Once the browser has the correct IP address, it initiates a TCP (Transmission Control Protocol) connection with the server. If the site uses HTTPS (which most sites do today), an additional step occurs:

- TCP Handshake
- TLS Handshake (For HTTPS)

### Step 4: Sending the HTTP Request

With the connection established, the browser sends an HTTP request to the server. The request contains the following components:

- Method : GET , PUT , POST , PATCH , DELETE
- URL : 
- Headers : 
- Body : 


### Step 5: The Server’s Response :

- Status code 
- Headers 
 - Body 


### Step 6: Rendering the Webpage : 

- HTML Parsing: 
- CSS and JavaScript
- Images and Other Assets


## How HTTP Powers the Web

The Hypertext Transfer Protocol (HTTP) is the protocol that controls the interaction between a web browser and servers. It is a stateless protocol that means each request and response transaction is independent of the other. And whilst HTTP is unadorned and lightning fast, it omits any security, in fact it is plain text, open to snooping or interception attacks.

It has mainly 3 parts and process 

### Http Methods : 

- GET
 - PUT 
 - POST 
 - DELETE
 - PATCH

### HTTP Status Codes

EXAMPLE - 200 , 404 , 409 , 403 , 401 , 500 , 201 \, 304

### HTTP Headers 

- Request Headers: Contain information like browser type (User-Agent), accepted content types (Accept), and cookies.
- Response Headers: Indicate content type, length, caching policies, and more.

## Difference Between HTTP and HTTPS

HTTPS is just HTTP with encryption. The primary distinction between these two names is that HTTPS is more secure than HTTP since it uses TLS (SSL) encryption for all HTTP requests and responses, even the standard ones.

--- 

# REST API fundamentals

REST is an acronym for REpresentational State Transfer and an architectural style for distributed hypermedia systems. 

REST is not a protocol or a standard, it is an architectural style. During the development phase, API developers can implement REST in a variety of ways.

Like the other architectural styles, REST also has its guiding principles and constraints. These principles must be satisfied if a service interface is to be referred to as RESTful.

--- 

# API versioning basics

    REST API versioning helps to iterate faster when the required, breaking or non-breaking, changes are identified. Learn to devise a strategy for API versioning.


Change in an API is inevitable as our knowledge and experience of a system improve. Managing the impact of this change can be quite a challenge when it threatens to break existing client integration.


### 1. When to version?
APIs only need to be up-versioned when a breaking change is made.

Breaking changes include:

- a change in the format of the response data for one or more calls
- a change in the request or response type (i.e. changing an integer to a float)
- removing any part of the API.

Breaking changes should always result in a change to the major version number for an API or content response type.

    Non-breaking changes, such as adding new endpoints or new response parameters, do not require a change to the major version number.


### 2. How to version a REST API?
    REST doesn’t provide for any specific versioning guidelines, but the more commonly used approaches fall into three categories:

 - URI Versioning
 - Versioning using Custom Request Header
 - Versioning using “Accept” header


---

# HTTP response status codes
HTTP response status codes indicate whether a specific HTTP request has been successfully completed. Responses are grouped in five classes:

- Informational responses (100 – 199)

100 Continue

101 Switching Protocols

102 Processing Deprecated

103 Early Hints


- Successful responses (200 – 299)

200 OK

201 Created

202 Accepted

- Redirection messages (300 – 399)

300 Multiple Choices

301 Moved Permanently

302 Found

303 See Other

304 Not Modified

305 Use Proxy Deprecated

- Client error responses (400 – 499)

400 Bad Request

401 Unauthorized

402 Payment Required

403 Forbidden

404 Not Found

405 Method Not Allowed

429 Too Many Requests

- Server error responses (500 – 599)

500 Internal Server Error

501 Not Implemented

502 Bad Gateway

503 Service Unavailable

504 Gateway Timeout

505 HTTP Version Not Supported

--- 

# Why use Https ? 

HTTPS is HTTP with TLS encryption. HTTPS uses TLS (SSL) to encrypt normal HTTP requests and responses, making it safer and more secure. A website that uses HTTPS has https:// in the beginning of its URL instead of http://, like https://www.cloudflare.com.

### Reasons 

- Website using HTTPS are more trustworthy for users.

- Chrome and other browsers mark all HTTP websites as "not secure."

- HTTPS is more secure, for both users and website owners.

- HTTPS authenticates websites.

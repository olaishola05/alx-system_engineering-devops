# Simple Web Infrastructure,


## Infrastructure Components Explanation

### What is a Server
A server is a computer system that provides services, resources, or data to other computers (clients) over a network, typically running specialized software to handle requests and deliver responses.

### Role of the Domain Name
The domain name serves as a human-readable address that maps to the server's IP address, allowing users to access websites using memorable names like "foobar.com" instead of numerical IP addresses.
DNS Record Type for "www"
The "www" in "www.foobar.com" is a subdomain that typically uses a CNAME (Canonical Name) DNS record, which points to the main domain or an A record that resolves to the server's IP address.

### Role of the Web Server
The web server receives HTTP requests from clients, serves static content like HTML, CSS, and images directly, and forwards dynamic content requests to the application server for processing.

### Role of the Application Server
The application server executes the business logic of the website, processes dynamic requests, interacts with the database, and generates dynamic content that is sent back through the web server to the client.

### Role of the Database
The database stores, organizes, and manages the website's persistent data, allowing the application server to create, read, update, and delete information as needed for the website's functionality.

### Server-Client Communication Protocol
The server uses the HTTP/HTTPS protocol over TCP/IP to communicate with the user's computer, enabling the structured exchange of web requests and responses across the internet.

## Infrastructure Issues

### Single Point of Failure (SPOF)
The entire infrastructure represents one massive SPOF since all components (web server, application server, and database) reside on a single machine, meaning any hardware failure, software crash, or network issue will make the entire website unavailable.

### Maintenance Downtime Issue
Downtime is inevitable during maintenance activities such as deploying new code, applying security patches, or restarting services, as there are no backup servers to handle requests while the primary server is being updated.

### Scaling Limitations
The infrastructure cannot scale to handle increased traffic since all requests must be processed by the single server's limited CPU, memory, and network resources, creating a hard ceiling on the number of concurrent users the system can support.

-   `Apache2` is an HTTP server
    
    -   Usually, we give `Apache2` some static `HTML` & `CSS` files.
    -   It runs in the background, listening to the network on ports `80` and `443` for incoming HTTP requests .
    -   When the client (the browser) requests a certain URL, it sends the corresponding file (if any) to the network.
-   `Tomcat` is a **servlet container**
    
    -   Usually, we give `Tomcat` some `servlets`
    
    >  Think of a `Servlet` as some Java code that runs when a certain URL is reached. A servlet outputs data that will be sent to the client.
    
    -   It runs in background, listening to the network on ports `8080` for incoming HTTP requests.
    -   When the client (
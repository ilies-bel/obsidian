-   Spring registers its own servlet: the [`DispatcherServlet`](https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html#mvc-servlet).
    
> To summarize, the `DispatcherServlet` is a `Servlet` that listens on all urls.
    
-   A request comes in. For example: `GET /api-url?param=value`
    -   The `DispatcherServlet` looks at all the classes with the `@Controller` annotation.
    -   If a `@Controller` has a method bound to `GET /api-url`, call this method with `param=value` as argument.
    -   If the method outputs something, serialize the output (i.e.: to `JSON` or `XML`), and send it back to the client.
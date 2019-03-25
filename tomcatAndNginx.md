##Apache Tomcat

###Apache/Nginx应该是HTTP Server


```
  HTTP Server关心的是HTTP协议层面的传输和访问控制，
  所以在Apache/Nginx上可以看到代理、负载均衡等功能。
  客户端通过HTTP Server访问服务器上的存储的资源（HTML文件，图片文件等）。
  通过CGI技术，也可以将处理过的内容通过HTTP Server分发，
  但是一个HTTP Server始终只是把服务器上的文件如实的通过HTTP协议传输
  给客户端。
```


###Tomcat是Application Server

而应用服务器，则是一个应用执行的容器。它首先需要支持开发语言的Runtime（对于Tomcat来说，就是java），保证应用能够在应用服务器上正常运行。其次，需要支持应用相关的规范，例如类库、安全方面的特性。对于Tomcat来说，就是需要体统JSP、Servlet运行需要的标准类库、Interface等。为了方便，应用服务器往往也会集成HTTP Server的功能，但不如专业的HTTP Server强大，所以应用服务器往往是运行在HTTP Server的背后，执行应用，将动态的内容转化为静态的内容之后，通过HTTP Server分发到客户端。


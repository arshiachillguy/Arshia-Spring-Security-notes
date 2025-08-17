# **what is a server?**   
    (in the context of spring boot & security)


A server is a software or hardware system that proccesses requests and delivers responses to clients.(e.g , browsers , mobile appa).            
    in java/spring , it refers to the runtime environment that executs your web application and handles HTTP traffic.

**how many types of servers in java we have ?**

***web server*** :handle HTTP request(GET / POST) like : Tomcat ,Jetty , Nginx , Apache HTTP  server 


***servlet containers ***: run java servlet/jsp  application(like spring mvc ) like : Apache tomcat , eclipse jetty , undertow . 
    

***full application servers*** :  support java specs like : wildfly , payara , weblogic/websphere 
 
***Reactive server*** : handle non-blocking , asynchronous requests like : netty , undertow


the default server in spring boot server is tomcat becase of easy deployment . 


[for more information read this article of spring web site](https://docs.spring.io/spring-boot/how-to/webserver.html)

**key notes**
 spring security works with all these servers but uses diffrenct mechanisms . 


for start simple we use Tomcat(default).


need hight performance we try undertwo or netty.

enterprise features we weploy to wildfly.



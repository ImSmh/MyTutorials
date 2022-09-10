# request、response 乱码
## request
## response
### 字符流-PrintWriter
```java
response.setContentType("text/html;charset=UTF-8");
PrintWriter out = response.getWriter();
out.write("<h1>嘿嘿</h1>");
```
### 字节流-ServletOutputStream
```java
ServletOutputStream writer = response.getOutputStream();
response.setHeader("content-type", "text/html;charset=utf-8");
writer.write("<p>嘿嘿</p>".getBytes("utf-8"));
```
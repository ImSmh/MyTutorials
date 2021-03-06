# Cookie 乱码
## 保存 Cookie
```java
    String name = "姓名";
    String value = "张三";
    name = URLEncoder.encode(name);
    value = URLEncoder.encode(value);
    Cookie cookie = new Cookie(name, value);
    response.addCookie(cookie);
```
## 读取 Cookie
```java
    URLDecoder.decode(cookie.getName());
```
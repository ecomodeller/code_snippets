Connection string for web/app.config
```xml
<connectionStrings>
    <add connectionString="Server=server;Database=db;Uid=user;Pwd=pwd" name="my_db" providerName="MySql.Data.MySqlClient" />
  </connectionStrings>
```

Connect to database with connection string in web.config

```C#
var db = DB("my_db");
```



Read request data i.e. either from QueryString or HTTP Post

```C#
var waterdepth = Request["waterdepth"];
```
Write new row to database and get id of new row

```C#
var sql = "INSERT INTO simulations (water_depth,created_at,updated_at) VALUES(@0,@1,@2);SELECT LAST_INSERT_ID();";
var id = db.QuerySingle(sql,waterdepth,DateTime.UtcNow,DateTime.UtcNow)[0];
```

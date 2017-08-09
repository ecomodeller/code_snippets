Connect to MySql

```R
my_db <- src_mysql(dbname = "db", 
                   host = "host", 
                   user = "username",
                   port = 3306,
                   password = "pwd")
                   
```                  
Read data
```R

sources <- tbl(my_db,"sources")  
  %>%   filter(origin_id == 16)   
  %>% select(id,tag_name)
  %>% collect()

```

# PSQL

## List all schemas

```
=> \dn

     List of schemas
  Name  |      Owner
--------+-----------------
 model  | blue
 obs    | blue
 public | azure_superuser
(3 rows)
```

## List tables

```
=> \d

                    List of relations
 Schema |        Name        |   Type   |      Owner
--------+--------------------+----------+-----------------
 public | pg_buffercache     | view     | azure_superuser
 public | pg_stat_statements | view     | azure_superuser
 public | processes          | table    | blue
 public | processes_id_seq   | sequence | blue
 public | progress           | table    | blue
 public | progress_id_seq    | sequence | blue
 public | recent             | view     | blue
(7 rows)


```

## Select a specific schema

```
SET search_path TO model;
```

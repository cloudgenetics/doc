# Using IAM authentication with PostgreSQL

To use IAM authentication with PostgreSQL, connect to the DB instance, create database users, and then grant them the `rds_iam` role:

```pgqsl
CREATE USER dev; 
GRANT rds_iam TO dev;
```

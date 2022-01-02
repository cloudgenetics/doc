# Using IAM authentication with PostgreSQL

To use IAM authentication with PostgreSQL, connect to the DB instance, create database users, and then grant them the `rds_iam` role:

```pgqsl
CREATE USER dev; 
GRANT rds_iam TO dev;
```

## IAM Policy
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "rds-db:connect"
            ],
            "Resource": [
                "arn:aws:rds-db:<region>:<account>:dbuser:<resource id>/username"
            ]
        }
    ]
}
```


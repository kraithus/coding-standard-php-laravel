# 1. Database Naming Conventions
Lower case and underscores, e.g. a database for deceased infants.
```sql
CREATE DATABASE `deceased_infants`;
```

# 2. Database Engine and Collation
Database engine to be used always is InnoDB and the character set is utf8mb4 and the collation is utf8mb4_unicode_ci

```sql
CREATE DATABASE `deceased_infants`
  CHARACTER SET `utf8mb4`
  COLLATE `utf8mb4_unicode_ci`
  ENGINE `InnoDB`;
```
Of course we will be using docker so we will all have access to the same database I presume. This is whenever setting up the database is your responsibility.
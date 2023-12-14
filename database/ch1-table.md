# Table Structure
All tables must have a primary key, unless we are doing something crazy, which I cannot think an example of atm. A table containing a column named email, should always have this set to a unique key, same with other humanoid attributes such as a phone number.

## Timestamps
I love auditing. Good thing laravel has the `$table->timestamps()` method which adds the `created_at` and `updated_at` columns to your table. Always include this unless we are doing something crazy and that is irrelevant to our cause(ehem, table)

# Table Naming Convention
Underscores and plural. A table for animals that have died.
```sql
CREATE TABLE `dead_animals`
```
Not `DeadAnimals`, `dead_Animals` and finally nor `deadanimals`

# Character SET and Collation
Same as the database. Do not mix collations.
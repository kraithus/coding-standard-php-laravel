# 1. Column Naming Convention 
The article I am referencing I disagree with on this point because Laravel does not agree with it, you can go read his argument for educations sake. We are slaves to the framework.

## 1.1. I love ids
All table primary keys should be named `id`, unless we go big and decide to use `uuids`, but I think they co-exist.

# 2. Data types and lengths, constraints for common columns
```sql
CREATE TABLE `common_columns`(
    `id` BIGINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    `name` VARCHAR(255) NOT NULL,
    `email` VARCHAR(255) NOT NULL UNIQUE,
    `password` VARCHAR(255) NOT NULL,
    `phone_number` VARCHAR(20) NOT NULL UNIQUE,
    `created_at` TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    `updated_at` TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);
```
## 2.1. What this looks like in laravel

```php
<?php

use Illuminate\Database\Migrations\Migration;
use Illuminate\Database\Schema\Blueprint;
use Illuminate\Support\Facades\Schema;

return new class extends Migration
{
    /**
     * Run the migrations.
     */
    public function up(): void
    {
        Schema::create('common_columns', function (Blueprint $table) {
            $table->id();
            $table->string('name');
            $table->string('email')->unique();
            $table->string('password');
            $table->string('phone_number', 20);
            $table->timestamps();
        });
    }

    /**
     * Reverse the migrations.
     */
    public function down(): void
    {
        Schema::dropIfExists('common_columns');
    }
};
```
### 2.1.1. Laravel migrations string() method
`string()` sets the data type to `VARCHAR` and column length to `255`. From my pseudo-knowledge it can take up to 2 arguments, `string('column_name', INT_LENGTH)`. The column name and its length. 

### 2.1.2. Laravel migrations timestamps() method
`timestamps()` creates the lovely audits `created_at` and `updated_at`

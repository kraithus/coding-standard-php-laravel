# 1. Classes, constants, methods and variables
> Class names MUST be declared in `StudlyCaps`  
Class constants MUST be declared in all upper case with underscore separators.
Method names MUST be declared in `camelCase`

Yeah, that was copy/paste from the coding standard, this is [the exact section](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md)

Variable names, the guide leaves it up to the team whatever feels good I would day. I vote `camelCase`.

On this what it explicitly says is:

> This guide intentionally avoids any recommendation regarding the use of `$StudlyCaps`, `$camelCase`, or `$under_score` property names. 

> Whatever naming convention is used SHOULD be applied consistently within a reasonable scope. That scope may be vendor-level, package-level, class-level, or method-level.

## 1.1. Examples
Some quick code samples on how to go about it

### 1.1.1. Classes
> Namespaces and classes MUST follow an "autoloading" PSR: [[PSR-0], [PSR-4]]. 
This means each class is in a file by itself, and is in a namespace of at least one level: a top-level vendor name. Class names MUST be declared in `StudlyCaps`. Code written for PHP 5.3 and after MUST use formal namespaces.

For example:

```php
<?php
// PHP 5.3 and later:
namespace Vendor\Model;

class FooBar
{
}
```
### 1.1.2. Methods
```php
<?php
namespace Vendor\Model;

class Foo
{
    function fooBar()
}
```
### 1.1.3. Constants
```php
<?php
namespace Vendor\Model;

class Foo
{
    const VERSION = '6.9';
    const DATE_APPROVED = '2023-06-09';
}
```
# 2. Comments
There is an indepth section on PHP Files. Link to [the section](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md#2-files). Pay close attention on `2.3. Side Effects`

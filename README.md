# datatables-php
DataTables server side rendering library.


| SUPPORTED FRAMEWORKS |
|:--------------------:|
| CodeIgniter 4 |

Minimal:
```php
$dt = new DataTables("your_table");

$dt->select("id, name, another_column")
  ->generate();
```

or
```php
DataTables::table("your_table")
  ->select("id, name, another_column")
  ->generate();
```

Use mapping:
```php
$user = new DataTables("user");
$user->map("id", function($col) {
  // Mapping column id.
  return "<a href=\"/profile/{$col['id']}\">View</a>";
})->generate();
```
Using where clause:
```php
$user = new DataTables("user");
$user->where("name", "Ridintek")->generate();
```
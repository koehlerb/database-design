---
title: PHP Example
description: PHP Example
hide_table_of_contents: false
---

# PHP Example

This is an example of simple PHP application accessing a MySQL
database using the `mysqli` API.

```php
<!DOCTYPE html>
<html lang="en">
<?php

include 'dbconnection.php';
// dbconnection.php contains one line like:
//
// $mysqli = new mysqli(null, "username", "password", "bkoehler_menagerie");
//

if ( $_SERVER['REQUEST_METHOD'] == "POST" ) {
    $stmt = $mysqli->prepare("INSERT INTO pet VALUES (?, ?, ?, ?, ?, ?)");
    $stmt->bind_param( 
        "ssssss",
        $_POST['name'],
        $_POST['owner'],
        $_POST['species'],
        $_POST['sex'],
        $_POST['birth'],
        $_POST['death']
    );
    $stmt->execute();
}

$result = $mysqli->query("SELECT * FROM pet");


?>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdn.simplecss.org/simple.min.css">
    <title>PHP/MySQL Demo</title>
</head>
<body>
  <header>
    <h1>PHP/MySQL Demo</h1>
    <p>CPS 146</p>
  </header>

  <main>
    <form method="post">
    <table>
        <tr>
            <th>Name</th>
            <th>Owner</th>
            <th>Species</th>
            <th>Sex</th>
            <th>Birth</th>
            <th>Death</th>
            <th>Add</th>
        </tr>
        <tr>
            <td><input type="text" name="name" size="10"></td>
            <td><input type="text" name="owner" size="10"></td>
            <td><input type="text" name="species" size="10"></td>
            <td>
                <select name="sex">
                    <option selected="selected">m</option>
                    <option>f</option>
                </select>
            </td>
            <td><input type="text" name="birth" size="10"></td>
            <td><input type="text" name="death" size="10"></td>
            <td><input type="submit" value="Add Pet" /></td>
        </tr>
        <?php
        foreach ($result as $row) {
            echo( "<tr>");
            echo( "<td>{$row['name']}</td>" );
            echo( "<td>{$row['owner']}</td>" );
            echo( "<td>{$row['species']}</td>" );
            echo( "<td>{$row['sex']}</td>" );
            echo( "<td>{$row['birth']}</td>" );
            echo( "<td>{$row['death']}</td>" );
            echo( "<td></td></tr>");
        }

        ?>
        
    </table>
    </form>    
  </main>

  <footer>
    <p>&copy; 2024, Brian Koehler</p>
  </footer>
</body>
</html>
```
# Ejercicios variados de PHP 2

## Tablas HTML personalizadas con PHP
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tablas Personalizadas</title>
</head>
<body>

<form action="registros2.php" method="POST">

        <p><br>
            <label>Nombre</label>
            <input type="text" name="Nombre" style=position:absolute;top:30px;left:85px>
        </p>

        <p>
            <label>Apellido-1</label>
            <input type="text" name="Apellido1" style=position:absolute;top:65px;left:85px>
        </p>

        <p>
            <label>Apellido-2</label>
            <input type="text" name="Apellido2" style=position:absolute;top:100px;left:85px>
        </p><br>
        <button type="submit">Enviar</button>  

    </form>
    
</body>
</html>
```
```php
  <?php
   
   $Nombre = $_POST["Nombre"];
   $Apellido1 = $_POST["Apellido1"];
   $Apellido2 = $_POST["Apellido2"];

   echo "<table border=1>";
                echo"<tr>";
                        echo"<td><b>Nombre</b></td>";
                        echo"<td><b>Apellido 1</b></td>";
                        echo"<td><b>Apellido 2</b></td>";
                    echo"</tr>";

                    echo"<tr>";
                        echo"<td>$Nombre</td>";
                        echo"<td>$Apellido1</td>";
                        echo"<td>$Apellido2</td>";
                    echo"</tr>";

                echo"</table>";
    ?>
```

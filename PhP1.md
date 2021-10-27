# Ejercicios variados sobre PHP
- Cadenas
- Buscar en ficheros .log
- Bucle FOR en php
- Funciones básicas
- Tablas html y objetos array
---------------------------------------

## Analizar cadenas de caracteres con PHP
```php
<?php

$cadena = 'abc';
$encontrar = 'w';
$pos = strpos($cadena, $encontrar);

if ($pos === false) 
{
    echo "'$encontrar' no se encuentra en la cadena '$cadena'";
}else 
{
    echo "'$encontrar' fue econtrada en la posición '$pos' de la cadena '$cadena'";
}

?>
```
## Mostrar el contenido de un fichero error.log con PHP y seleccionar los [php:error]
```php
<?php

$errorlogs= fopen("C:\\xampp\\apache\\logs\\error.log" , "r");
$encontrar = '[php:error]';

while (!feof($errorlogs))
{
    $lineas = fgets($errorlogs);
    if (strpos($lineas,$encontrar) !== false)
    {
       echo $lineas;
       echo "<br>";
    }
}

fclose($errorlogs);

?>
```
## Obtener mediante un bucle FOR y un array una lista ordenada en HTML

```php
<?php
$lista=array("Uno","Dos","Tres","Cuatro");
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DocumentArray</title>
</head>
<body>
    <ol>
        <?php
            foreach ($lista as $dato)
            {
                echo "<li>".$dato."</li>";
            }
        ?>
    </ol>
</body>
</html>
```
## Función en php para saludar a usuarios
```php
<?php

    function saludar($Saludado)
    {
        echo "Buenos días $Saludado<br>";
    }

saludar('Rocío');
saludar('Carlos');

?>
```
## Crear una tabla HTML con nombres y apellidos de personas utilizando objetos ARRAY
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tablas</title>
</head>
<body> 
    <?php
    
        $Usuario1= array('José','Minaya','Robles');
        $Usuario2= array('Laura','Díaz','Castilla');    

                echo "<table border=1>";
                    echo"<tr>";
                        echo"<td><b>Nombre</b></td>";
                        echo"<td><b>Apellido 1</b></td>";
                        echo"<td><b>Apellido 2</b></td>";
                    echo"</tr>";

                    echo"<tr>";
                        echo"<td>$Usuario1[0]</td>";
                        echo"<td>$Usuario1[1]</td>";
                        echo"<td>$Usuario1[2]</td>";
                    echo"</tr>";

                    echo"<tr>";
                        echo"<td>$Usuario2[0]</td>";
                        echo"<td>$Usuario2[1]</td>";
                        echo"<td>$Usuario2[2]</td>";
                    echo"</tr>";

                echo"</table>";

    ?>          
</body>
</html>
```

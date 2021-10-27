# Ejercicios variados sobre PHP
- Cadenas
- Buscar en ficheros .log
- Bucle FOR en php
- Funciones básicas
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

```html
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

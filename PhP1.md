# Ejercicios variados sobre PHP
- Cadenas
- Logs
- Buscar en ficheros
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

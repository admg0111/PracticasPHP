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

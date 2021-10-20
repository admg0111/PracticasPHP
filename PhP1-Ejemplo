# Calculadores con PHP


## Formulario HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Documento php</title>
</head>
<body>
    
   <h1>FORMULARIO DE EJEMPLO</h1>
    <form action="registro.php" method="POST">
        <p>
            <label>Numero 1:</label>
            <input type="float" name="numero1">

                <br><br>

                    <select name="select">

                        <option value="Sumar" name="Suma">Sumar</option>
                        <option value="Restar" name="Resta">Restar</option>
                        <option value="Multiplicar" name="Multiplicacion">Multiplicar</option>
                        <option value="Dividir" name="Division">Dividir</option>

                    </select>

                <br><br>

            <label>Numero 2:</label>
            <input type="float" name="numero2">
            <br><br>
            
            <button type="submit">Calcular</button>
             
        </p>  
    </form>
</body>
</html>



## Instrucciones en PHP

<?php

$calculo = $_POST["select"];
$num1 = $_POST["numero1"];
$num2 = $_POST["numero2"];

if ($calculo == "Sumar"){
    $resultado = $num1 + $num2;
}else if($calculo == "Restar"){
    $resultado = $num1 - $num2;  
}else if($calculo =="Multiplicar"){
    $resultado = $num1 * $num2;  
}else if($calculo == "Dividir"){
    $resultado = $num1 / $num2;  
}

echo "El resultado de la operación es: ".$resultado;


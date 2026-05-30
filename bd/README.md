<?php

$conexion = mysqli_connect(
"localhost",
"usuario",
"password",
"basedatos"
);

$sql = "SELECT * FROM kits_arduino";

$resultado = mysqli_query($conexion,$sql);

while($fila=mysqli_fetch_assoc($resultado)){
    echo json_encode($fila);
    echo "<br>";
}

?>

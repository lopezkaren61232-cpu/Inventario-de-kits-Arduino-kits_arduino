<?php

$conexion = mysqli_connect(
"localhost",
"usuario",
"password",
"basedatos"
);

$nombre = $_POST['nombre'];
$categoria = $_POST['categoria'];
$cantidad = $_POST['cantidad'];
$observaciones = $_POST['observaciones'];

$sql = "INSERT INTO kits_arduino
(nombre,categoria,cantidad,observaciones,fecha_registro)
VALUES
('$nombre','$categoria','$cantidad','$observaciones',NOW())";

mysqli_query($conexion,$sql);

echo "Registro guardado";

?>

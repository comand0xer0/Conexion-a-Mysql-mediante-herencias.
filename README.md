
# Conexion-a-Mysql-mediante-herencias.
<?php 
/*
* Conexion a la base de datos con herencia...
*/
class Conexion extends mysqli
{
	public function __construct()
	{
		/* Llamando al constructor de mysqli */
		parent::__construct('localhost', 'root', '', 'proyecto_final');
		/* Para hacer las llamadas */
		$this->query("SET NAMES 'utf8';");
		$this->connect_errno ? die("Error con la conexion") : $correcto = "coectado";
		//echo $correcto;
		//unset($correcto);
		
		
	}
}

$conexion = new Conexion();
?>

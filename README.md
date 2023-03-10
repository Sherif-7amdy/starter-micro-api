<?php
ini_set('user_agent', 'Android Vinebre Software');
$arrContextOptions=array("ssl"=>array("verify_peer"=>false,"verify_peer_name"=>false,),); 
$tilfazarab = file_get_contents('https://config.e-droid.net/srv/config.php?v=142&vname=1.0&idapp=1185384&idusu=0&cod_g=&pw=1&gp=0&am=0&idl=en&pa_env1&pa=US&pn=com.tilfazarab2020&fus=191121122231&aid=07eaa387a0ff21bd'', false, stream_context_create($arrContextOptions));
$first_step = explode( '[s349579_url=' , $tilfazarab );
$second_step = explode("][" , $first_step[1] );
$user= $second_step[0];
$a=str_replace("/98",$_GET['s'], $user);
header('Location: '.$a);
?>

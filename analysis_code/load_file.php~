<?php
$con=mysql_connect('localhost','root','');
$db_conn=mysql_select_db('cern',$con);

$handle=@fopen("dimuon-output.csv","r");
if($handle) {
	while (($buffer = fgets ($handle, 4096)) !== false) {
		$q="insert into mass values ('',$buffer)";
		$q1=mysql_query($q);
}
	if(!feof($handle)) {
		echo "Error\n";
	}
	fclose($handle);
}
?>

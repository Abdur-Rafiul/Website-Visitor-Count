# Website-Visitor-Count


<!DOCTYPE html>
<html>
<head>
<title>Visitor Count</title>

</head>
<body>


<h3>YouTube Link : <a style="color:red" href="https://www.youtube.com/@rafiulislam7097">Rafiul Islam</a><h3>
<br><br><br>
  $ip_address = $_SERVER['REMOTE_ADDR'];<br>
  $visit_time = date("h:i:sa");<br>
  $visit_date = date("d-m-y");<br>

  $country = date_default_timezone_get();<br><br>

  $ipdat = @json_decode(file_get_contents(<br>
    "http://www.geoplugin.net/json.gp?ip=" . $ip_address));<br><br><br>
   

 $sql1 = "INSERT INTO question_2 (time1,ip,country,city)<br>
VALUES ('$visit_time', '$ip_address', '$ipdat->geoplugin_countryName',<br> '$ipdat->geoplugin_city')";<br><br>
 
$result = mysqli_query($conn,$sql1);<br><br><br><br>


</body>
</html>



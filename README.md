# Website-Visitor-Count


<h6 style="color:red">


include('db.php');
  $ip_address = $_SERVER['REMOTE_ADDR'];
  $visit_time = date("h:i:sa");
  $visit_date = date("d-m-y");

  $country = date_default_timezone_get();

  $ipdat = @json_decode(file_get_contents(
    "http://www.geoplugin.net/json.gp?ip=" . $ip_address));
   

 $sql1 = "INSERT INTO question_2 (time1,ip,country,city)
VALUES ('$visit_time', '$ip_address', '$ipdat->geoplugin_countryName', '$ipdat->geoplugin_city')";
 
$result = mysqli_query($conn,$sql1);



<h6>

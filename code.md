<html class="gr__localhost"><head><title>Demo|Lisenme</title>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">   
</head>
<body>
<div class="container">
  <form class="form-horizontal" action=" " method="post"  id="reg_form" >
    <fieldset> 
      <!-- Form Name -->
        <div class="form-group">
        <div class="col-md-3 selectContainer">
          <div class="input-group"> 
            <label> Select your destination <span id="field">*</span></label>
            <Select name="destination" id="colorselector"  required>
              <option value="">select the destination</option>
   <option value="asdasd-Bangalore">The asdasd, Bangalore</option>
   <option value="adasd-Namseling">The asdasd Namseling, Bhutan</option>
</Select>
          </div>
        </div>
        <div class="col-md-3  inputGroupContainer">
          <div class="input-group">
            <label> Check in date <span id="field">*</span></label>           
<input type="text" name="checkin" class="from_date" required="Enter Check-in  Date" />  
          </div>
        </div>
        <div class="col-md-3  inputGroupContainer">
          <div class="input-group"> 
            <label> Check out date <span id="field">*</span></label>
                <input type="text" name="checkout" class="to_date" required="Enter Check in  Date" />
          </div>
        </div>
         <div class="col-md-3  inputGroupContainer">
          <div class="input-group">
            <label> &nbsp;&nbsp;&nbsp;&nbsp;</label>
          <a onclick="myFunction()" id="Book-now-more">More options</a>
         </div>
         </div>
      </div>
     
      <!-- Text input-->

      <div id="mydiv" class="container hotel-form-click">
      
      <div class="form-group">

         <div class="col-md-3 selectContainer">
             <label> No of Guests<span id="field">*</span></label>
          <div class="input-group"> 
            <select name="people" class="form-control selectpicker" required="" >
              <option value="" >No of people</option>
              <option value="2">1 </option>
              <option value="3">2 </option>
              <option value="4">3</option>
               <option value="5">4 </option>
            </select>
          </div>
        </div>
         <div class="col-md-3 selectContainer">
             <label> No of children <span>*</span></label>
          <div class="input-group"> 
            <select name="childrens" class="form-control selectpicker" >
              <option value="" >No of children</option>
<option value="0">0 </option>
              <option value="1">1 </option>
              <option value="2">2 </option>
              <option value="3">3</option>
               <option value="4">4 </option>

            </select>
          </div>
        </div>
         <div class="col-md-3 selectContainer">
           <label> No of Rooms<span id="field">*</span></label>
          <div class="input-group"> 
            <select name="noforooms" class="form-control selectpicker" required="" >
             <option value="">Select the no of Room</option>
             <option value="1">1</option>
             <option value="2">2</option>
             <option value="3">3</option>
             <option value="4">4</option>
            </select>
          </div>
        </div>
         <div class="col-md-3 selectContainer">
           <label> Types of Rooms <span id="field">*</span></label>
          <div class="input-group"> 
            <div >  
              <select name="roomtypes" class="form-control selectpicker" required="" >
                <option value="" >Select the type of room</option>
              <optgroup  label="The asdasd, Bangalore" id="adasd-Bangalore" class="colors" style="display:none">                
             <option value="Superior">Superior</option>
             <option value="Deluxe">Deluxe</option>
             <option value="Club">Club</option>
             <option value="Suite">Suite</option>
 </optgroup>

 <optgroup label="The asdasd Namseling, Bhutan" id="asdasd-Namseling" class="colors" style="display:none">
 
    <option value="Sunny Room">Sunny Room</option>
             <option value="Balance &amp; Harmony Room">Balance &amp; Harmony Room</option>
             <option value="Luxury Room (Deluxe)">Luxury Room (Deluxe)</option>
             <option value="Peace &amp; Tranquility Room (Deluxe)">Peace &amp; Tranquility Room (Deluxe)</option>

            </optgroup>
            </select> </div>
<div> 
</div>
          </div>
        </div>
       
    </div>
      <!-- Text input--> 
      <div class="form-group">
        <div class="col-md-4  inputGroupContainer">
          <div class="input-group"> 
            <label> Name <span id="field">*</span></label>
            <input  name="full_name" placeholder="Enter your name" class="form-control"  type="text" required="">

          </div>
        </div>

        <div class="col-md-4 inputGroupContainer">
          <div class="input-group"> 
            <label> Phone No  <span id="field">*</span></label>
            <input name="phone" placeholder="Enter your mobile no" class="form-control" type="text" required="">
          </div>
        </div>
        <div class="col-md-4  inputGroupContainer">
          <div class="input-group"> 
            <label> Email <span id="field">*</span></label>
            <input name="email" placeholder="example@abc.com" class="form-control"  type="email" required="Enter valid email address">
          </div>
        </div>
      </div>
      <!-- Button -->
      <div class="form-group">
        <label class="col-md-4 control-label"></label>
        <div class="col-md-4">
          <input type="submit"  name="submit" class="btn btn-primary btn-lg btn-block hotelbutton" >
        </div>
      </div>
    </fieldset>
  </form>
</div></div></div></div>

<script>
function myFunction() {
    var x = document.getElementById("mydiv");
    if (x.style.display === "none") {
        x.style.display = "block";
    } else {
        x.style.display = "none";
    }
var x = document.getElementById("thankyou-message");
    if (x.style.display === "none") {
        x.style.display = "none";
    } else {
        x.style.display = "none";
    }
}
window.onload = function() {
  document.getElementById('mydiv').style.display = 'none';
};
</script>
    <script>
jQuery(document).ready(function($){

    $(function() {
        $('#colorselector').change(function(){
            $('.colors').hide();
            $('#' + $(this).val()).show();
        });
    });
});
    
</script>
    </div>  </div> </div></div></div>
</body>
<?php
extract($_POST);
/**
* Filter the mail content type.
*/
function wpdocs_set_html_mail_content_type() {
   return 'text/html';
}
add_filter( 'wp_mail_content_type', 'wpdocs_set_html_mail_content_type' );
if(isset($submit)){
$to      = 'reservations@adasdasd.com';
$subject = 'The asdasds Booking Form';
$headers = 'From: The asdasd <sales@asdasdas.com>' . "\r\n";
$body    = "Greetings, <br><br/> Thank you for choosing The asdasd. We have received your request and will get back to you at the earliest. Find the details below:<br/><br/>
<strong>Destination : </strong>" .$destination."<br/>
<strong>Check In Date : </strong>".$checkin."<br/>
 <strong>Check Out Date:</strong> ".$checkout."<br/>
 <strong>No of People: </strong>".$people."<br/>
  <strong> No of Children: </strong>".$childrens. "<br/>
   <strong>No of rooms: </strong>".$noforooms."<br/>
 <strong>Type of rooms: </strong>".$roomtypes."<br/>
 <strong>Name: </strong>".$full_name."<br/>
 <strong>Ph No: </strong>" .$phone."<br/>
 <strong>Email: </strong>: ".$email."<br/>
<br/><br/>
 Regards,<br>The asdas Team";

if(wp_mail($to, $subject, $body, $headers))
{
header("Refresh: 5; url=http://example.com");
   echo '<div id="thankyou-message">We have received your booking request. Our sales team will get in touch shortly to finalise your booking</div>';
}
else 
{
  echo "failed";
}}
add_filter( 'wp_mail_content_type', 'wpdocs_set_html_mail_content_type' );
if(isset($submit)){
$to = $email;
$subject = 'Acknowledgement of Your Booking Request ';
$headers = 'From: The asdasd <sales@abc.com>' . "\r\n";
$body = 
"Hello ".$full_name."<br/><br/>
Greetings,
<br/><br/>
Thank you for choosing The asas. We have received your booking request. Our sales team will get in touch shortly to finalise your booking.<br>
Regards,<br>
The asdasd Team";

wp_mail( $to, $subject, $body, $headers  );

} 
// Reset content-type to avoid conflicts -- https://core.trac.wordpress.org/ticket/23578
remove_filter( 'wp_mail_content_type', 'wpdocs_set_html_mail_content_type' );
?>
</html>

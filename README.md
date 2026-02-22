<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Velora | Where Emotions Meet Clarity</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}

body{
background:#f3f7ff;
color:#1a1a1a;
}

header{
background:#0a1f44;
color:#fff;
padding:70px 20px;
text-align:center;
}

header h1{
font-size:48px;
font-weight:700;
letter-spacing:1px;
}

header p{
margin-top:10px;
font-size:18px;
opacity:0.85;
}

.container{
max-width:1100px;
margin:auto;
padding:60px 20px;
}

.section-title{
text-align:center;
font-size:30px;
margin-bottom:40px;
color:#0a1f44;
font-weight:600;
}

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
gap:30px;
}

.card{
background:#ffffff;
padding:30px;
border-radius:16px;
box-shadow:0 10px 30px rgba(10,31,68,0.08);
border-top:5px solid #2d6bff;
transition:0.3s;
}

.card:hover{
transform:translateY(-6px);
}

.card h3{
color:#0a1f44;
margin-bottom:10px;
}

.price{
color:#2d6bff;
font-weight:600;
margin:10px 0;
font-size:18px;
}

form{
background:#ffffff;
padding:40px;
border-radius:16px;
box-shadow:0 10px 30px rgba(10,31,68,0.08);
max-width:700px;
margin:auto;
border-top:5px solid #2d6bff;
}

form input, form select{
width:100%;
padding:14px;
margin:14px 0;
border-radius:8px;
border:1px solid #ccd6ff;
font-size:14px;
}

button{
background:#2d6bff;
color:#fff;
padding:14px 22px;
border:none;
border-radius:8px;
cursor:pointer;
font-weight:600;
font-size:15px;
}

button:hover{
background:#1f4ed8;
}

.policy{
background:#ffffff;
padding:30px;
border-radius:16px;
box-shadow:0 10px 30px rgba(10,31,68,0.08);
margin-bottom:25px;
border-left:5px solid #2d6bff;
}

footer{
background:#0a1f44;
color:#fff;
text-align:center;
padding:40px;
margin-top:60px;
font-size:14px;
}
</style>
</head>

<body>

<header>
<h1>Velora</h1>
<p>Where Emotions Meet Clarity</p>
</header>

<div class="container">

<div class="section-title">Services</div>

<div class="grid">
<div class="card">
<h3>General Guidance</h3>
<p>Family • Career • Life • Crush</p>
<div class="price">₹149 • 40 Minutes</div>
</div>

<div class="card">
<h3>Partner Conflict</h3>
<p>Structured clarity session</p>
<div class="price">₹249 • 40 Minutes</div>
</div>

<div class="card">
<h3>Breakup Recovery</h3>
<p>Emotional reset & stability</p>
<div class="price">₹349 • 45 Minutes</div>
</div>

<div class="card">
<h3>Deep Reset Intensive</h3>
<p>Focused 1:1 clarity transformation</p>
<div class="price">₹399 • 60 Minutes</div>
</div>
</div>

</div>

<div class="container">

<div class="section-title">Book Appointment</div>

<form onsubmit="handleBooking(event)">
<input type="text" id="name" placeholder="Full Name" required>
<input type="email" id="email" placeholder="Email Address" required>
<input type="tel" id="phone" placeholder="Phone Number" required>

<select id="service" required>
<option value="">Select Service</option>
<option value="149">General Guidance - ₹149</option>
<option value="249">Partner Conflict - ₹249</option>
<option value="349">Breakup Recovery - ₹349</option>
<option value="399">Deep Reset - ₹399</option>
</select>

<input type="date" id="date" required>
<input type="time" id="time" required>

<button type="submit">Confirm & Pay</button>
</form>

</div>

<div class="container">

<div class="section-title">Policies</div>

<div class="policy">
<h3>Appointment Policy</h3>
<p>All sessions require advance booking. Rescheduling permitted up to 12 hours before the scheduled time. Missed sessions without notice are non-adjustable.</p>
</div>

<div class="policy">
<h3>Payment Policy</h3>
<p>Payment is accepted via UPI only. Booking is confirmed after successful payment. All confirmed bookings are non-refundable.</p>
</div>

<div class="policy">
<h3>Call Conduct Policy</h3>
<p>All sessions are confidential. Any abusive or inappropriate behavior results in immediate termination without refund. This platform provides emotional guidance, not medical or psychological treatment.</p>
</div>

</div>

<footer>
© 2026 Velora • Private Emotional Guidance
</footer>

<script>
function handleBooking(event){
event.preventDefault();

let amount=document.getElementById("service").value;
let name=document.getElementById("name").value;
let date=document.getElementById("date").value;
let time=document.getElementById("time").value;

if(!amount){
alert("Please select a service.");
return;
}

let upi="upi://pay?pa=velora.aditya@fam&pn=Velora&am="+amount+"&cu=INR";

let message="Hello Velora,%0AName: "+name+
"%0ADate: "+date+
"%0ATime: "+time+
"%0AAmount Paid: ₹"+amount+
"%0APlease confirm my appointment.";

let whatsapp="https://wa.me/?text="+message;

window.location.href=upi;

setTimeout(function(){
window.open(whatsapp,"_blank");
},3000);
}
</script>

</body>
</html>

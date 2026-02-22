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
background:#f5f7fa;
color:#1c1c1c;
}

header{
background:#0b1f3a;
color:#fff;
padding:60px 20px;
text-align:center;
}

header h1{
font-size:42px;
font-weight:700;
}

header p{
margin-top:10px;
font-size:18px;
opacity:0.8;
}

.container{
max-width:1100px;
margin:auto;
padding:50px 20px;
}

.section-title{
text-align:center;
font-size:28px;
margin-bottom:40px;
color:#0b1f3a;
}

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
gap:25px;
}

.card{
background:#fff;
padding:25px;
border-radius:12px;
box-shadow:0 6px 18px rgba(0,0,0,0.08);
}

.card h3{
margin-bottom:8px;
color:#0b1f3a;
}

.price{
font-weight:600;
margin:10px 0;
color:#0b1f3a;
}

button{
padding:10px 18px;
border:none;
background:#0b7a75;
color:#fff;
border-radius:8px;
cursor:pointer;
margin-top:10px;
}

button:hover{
background:#095e5a;
}

form{
background:#fff;
padding:30px;
border-radius:12px;
box-shadow:0 6px 18px rgba(0,0,0,0.08);
max-width:600px;
margin:auto;
}

form input, form select{
width:100%;
padding:10px;
margin:10px 0;
border-radius:6px;
border:1px solid #ccc;
}

.policy{
background:#fff;
padding:30px;
border-radius:12px;
box-shadow:0 6px 18px rgba(0,0,0,0.08);
margin-bottom:20px;
}

footer{
background:#0b1f3a;
color:#fff;
text-align:center;
padding:30px;
margin-top:40px;
}
</style>
</head>

<body>

<header>
<h1>Velora</h1>
<p>Where Emotions Meet Clarity</p>
</header>

<div class="container">

<div class="section-title">Our Services</div>

<div class="grid">

<div class="card">
<h3>Family / Career / Life / Crush</h3>
<p>Structured private guidance session</p>
<div class="price">₹149 • 40 Minutes</div>
</div>

<div class="card">
<h3>Partner Conflict</h3>
<p>Conflict resolution & emotional clarity</p>
<div class="price">₹249 • 40 Minutes</div>
</div>

<div class="card">
<h3>Breakup Recovery</h3>
<p>Emotional reset & stability session</p>
<div class="price">₹349 • 45 Minutes</div>
</div>

<div class="card">
<h3>Deep Reset Session</h3>
<p>Intensive emotional clarity session</p>
<div class="price">₹399 • 60 Minutes</div>
</div>

</div>

</div>

<div class="container">

<div class="section-title">Book Appointment</div>

<form onsubmit="redirectPayment(event)">
<input type="text" placeholder="Full Name" required>
<input type="email" placeholder="Email Address" required>
<input type="tel" placeholder="Phone Number" required>

<select required>
<option value="">Select Service</option>
<option value="149">General Session - ₹149</option>
<option value="249">Partner Conflict - ₹249</option>
<option value="349">Breakup Recovery - ₹349</option>
<option value="399">Deep Reset - ₹399</option>
</select>

<input type="date" required>
<input type="time" required>

<button type="submit">Confirm & Pay</button>
</form>

</div>

<div class="container">

<div class="section-title">Policies</div>

<div class="policy">
<h3>Appointment Policy</h3>
<p>All sessions must be booked in advance. Appointment confirmation is sent after successful payment. Rescheduling allowed 12 hours prior.</p>
</div>

<div class="policy">
<h3>Payment Policy</h3>
<p>All payments are accepted via UPI only. Sessions are non-refundable once booked. In case of emergency reschedule, credit will be adjusted.</p>
</div>

<div class="policy">
<h3>Call Conduct Policy</h3>
<p>Sessions are strictly confidential. No abusive language or inappropriate requests tolerated. This is emotional support guidance, not medical or psychological therapy.</p>
</div>

</div>

<footer>
© 2026 Velora • Private Emotional Guidance
</footer>

<script>
function redirectPayment(event){
event.preventDefault();
let amount=document.querySelector("select").value;
if(!amount){alert("Please select a service."); return;}
window.location.href="upi://pay?pa=velora.aditya@fam&pn=Velora&am="+amount+"&cu=INR";
}
</script>

</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Velora | Where Emotions Meet Clarity</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}

body{
background: radial-gradient(circle at top left,#0f2b5f,#081224 60%);
color:#ffffff;
overflow-x:hidden;
}

section{
padding:80px 20px;
max-width:1200px;
margin:auto;
}

h1,h2,h3{letter-spacing:0.5px;}

.hero{
text-align:center;
padding-top:120px;
padding-bottom:100px;
}

.hero h1{
font-size:56px;
font-weight:800;
background:linear-gradient(90deg,#5fa8ff,#00e0ff);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

.hero p{
margin-top:20px;
font-size:20px;
opacity:0.85;
}

.cta-btn{
margin-top:30px;
padding:14px 28px;
border:none;
border-radius:40px;
background:linear-gradient(90deg,#00e0ff,#5fa8ff);
color:#000;
font-weight:700;
cursor:pointer;
font-size:16px;
box-shadow:0 0 25px rgba(0,224,255,0.4);
transition:0.3s;
}

.cta-btn:hover{
transform:translateY(-3px);
}

.section-title{
text-align:center;
font-size:34px;
margin-bottom:50px;
font-weight:700;
}

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:30px;
}

.card{
background:rgba(255,255,255,0.06);
backdrop-filter:blur(12px);
border-radius:20px;
padding:30px;
border:1px solid rgba(255,255,255,0.1);
transition:0.3s;
}

.card:hover{
transform:translateY(-6px);
border:1px solid #00e0ff;
box-shadow:0 0 25px rgba(0,224,255,0.2);
}

.card h3{
margin-bottom:12px;
font-size:20px;
}

.price{
margin-top:12px;
font-weight:600;
color:#00e0ff;
}

form{
background:rgba(255,255,255,0.05);
padding:40px;
border-radius:20px;
border:1px solid rgba(255,255,255,0.1);
backdrop-filter:blur(12px);
max-width:700px;
margin:auto;
}

form input, form select{
width:100%;
padding:14px;
margin:14px 0;
border-radius:10px;
border:none;
background:rgba(255,255,255,0.08);
color:#fff;
}

form input::placeholder{color:#ccc;}

.submit-btn{
width:100%;
margin-top:15px;
padding:15px;
border:none;
border-radius:12px;
background:linear-gradient(90deg,#00e0ff,#5fa8ff);
color:#000;
font-weight:700;
cursor:pointer;
font-size:16px;
}

.policy{
background:rgba(255,255,255,0.05);
padding:30px;
border-radius:20px;
border:1px solid rgba(255,255,255,0.1);
margin-bottom:25px;
}

footer{
text-align:center;
padding:40px;
opacity:0.7;
font-size:14px;
}
</style>
</head>

<body>

<section class="hero">
<h1>Velora</h1>
<p>Where Emotions Meet Clarity</p>
<button class="cta-btn" onclick="document.getElementById('booking').scrollIntoView()">Book Private Session</button>
</section>

<section>
<h2 class="section-title">Private Sessions</h2>
<div class="grid">
<div class="card">
<h3>General Guidance</h3>
<p>Family • Career • Life • Crush</p>
<div class="price">₹149 • 40 Min</div>
</div>
<div class="card">
<h3>Partner Conflict</h3>
<p>Structured clarity session</p>
<div class="price">₹249 • 40 Min</div>
</div>
<div class="card">
<h3>Breakup Recovery</h3>
<p>Emotional reset & stability</p>
<div class="price">₹349 • 45 Min</div>
</div>
<div class="card">
<h3>Deep Reset Intensive</h3>
<p>Focused transformation session</p>
<div class="price">₹399 • 60 Min</div>
</div>
</div>
</section>

<section id="booking">
<h2 class="section-title">Book Appointment</h2>

<form onsubmit="pay(event)">
<input type="text" id="name" placeholder="Full Name" required>
<input type="email" placeholder="Email Address" required>
<input type="tel" placeholder="Phone Number" required>

<select id="service" required>
<option value="">Select Service</option>
<option value="149">General - ₹149</option>
<option value="249">Partner - ₹249</option>
<option value="349">Breakup - ₹349</option>
<option value="399">Deep Reset - ₹399</option>
</select>

<input type="date" required>
<input type="time" required>

<button class="submit-btn">Confirm & Pay</button>
</form>
</section>

<section>
<h2 class="section-title">Policies</h2>

<div class="policy">
<h3>Appointment Policy</h3>
<p>Advance booking required. Reschedule up to 12 hours prior. Missed sessions without notice are non-adjustable.</p>
</div>

<div class="policy">
<h3>Payment Policy</h3>
<p>UPI payment only. Booking confirmed after successful payment. All payments are non-refundable.</p>
</div>

<div class="policy">
<h3>Conduct Policy</h3>
<p>Strict confidentiality maintained. Inappropriate behavior results in termination without refund. This is guidance support, not medical therapy.</p>
</div>

</section>

<footer>
© 2026 Velora • Private Emotional Guidance
</footer>

<script>
function pay(e){
e.preventDefault();
let amount=document.getElementById("service").value;
if(!amount){alert("Select service");return;}
window.location.href="upi://pay?pa=velora.aditya@fam&pn=Velora&am="+amount+"&cu=INR";
}
</script>

</body>
</html>

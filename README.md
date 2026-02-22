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
background:linear-gradient(135deg,#020617,#0f172a,#1e293b);
color:#fff;
overflow-x:hidden;
}

header{
text-align:center;
padding:120px 20px 100px;
background:radial-gradient(circle at center,#1e3a8a,#020617);
}

header h1{
font-size:64px;
font-weight:800;
background:linear-gradient(90deg,#00d4ff,#ffd700);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

header p{
margin-top:15px;
font-size:20px;
opacity:0.9;
}

.cta{
margin-top:35px;
padding:16px 32px;
border:none;
border-radius:50px;
background:linear-gradient(90deg,#ffd700,#00d4ff);
color:#000;
font-weight:700;
cursor:pointer;
font-size:16px;
box-shadow:0 0 30px rgba(255,215,0,0.4);
transition:0.3s;
}

.cta:hover{transform:scale(1.05);}

section{
max-width:1200px;
margin:auto;
padding:80px 20px;
}

.section-title{
text-align:center;
font-size:38px;
font-weight:700;
margin-bottom:60px;
background:linear-gradient(90deg,#00d4ff,#ffd700);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:30px;
}

.card{
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.1);
backdrop-filter:blur(20px);
padding:35px;
border-radius:25px;
transition:0.4s;
}

.card:hover{
transform:translateY(-8px);
border:1px solid #ffd700;
box-shadow:0 0 40px rgba(255,215,0,0.3);
}

.card h3{
font-size:22px;
margin-bottom:15px;
}

.price{
margin-top:10px;
font-size:18px;
font-weight:600;
color:#00d4ff;
}

form{
background:rgba(255,255,255,0.05);
padding:45px;
border-radius:25px;
border:1px solid rgba(255,255,255,0.1);
backdrop-filter:blur(20px);
max-width:700px;
margin:auto;
}

form input, form select{
width:100%;
padding:16px;
margin:14px 0;
border-radius:12px;
border:none;
background:rgba(255,255,255,0.08);
color:#fff;
font-size:14px;
}

form input::placeholder{color:#ccc;}

.submit{
margin-top:15px;
width:100%;
padding:16px;
border:none;
border-radius:15px;
background:linear-gradient(90deg,#ffd700,#00d4ff);
color:#000;
font-weight:700;
font-size:16px;
cursor:pointer;
}

.policy{
background:rgba(255,255,255,0.05);
padding:35px;
border-radius:25px;
border:1px solid rgba(255,255,255,0.1);
margin-bottom:30px;
}

footer{
text-align:center;
padding:50px 20px;
opacity:0.7;
font-size:14px;
border-top:1px solid rgba(255,255,255,0.1);
}
</style>
</head>

<body>

<header>
<h1>Velora</h1>
<p>Where Emotions Meet Clarity</p>
<button class="cta" onclick="document.getElementById('booking').scrollIntoView()">Book Private Session</button>
</header>

<section>
<h2 class="section-title">Our Private Sessions</h2>

<div class="grid">
<div class="card">
<h3>General Guidance</h3>
<p>Family • Career • Life • Crush</p>
<div class="price">₹149 • 40 Minutes</div>
</div>

<div class="card">
<h3>Partner Conflict</h3>
<p>Structured clarity & resolution</p>
<div class="price">₹249 • 40 Minutes</div>
</div>

<div class="card">
<h3>Breakup Recovery</h3>
<p>Emotional reset & stabilization</p>
<div class="price">₹349 • 45 Minutes</div>
</div>

<div class="card">
<h3>Deep Reset Intensive</h3>
<p>Focused transformation session</p>
<div class="price">₹399 • 60 Minutes</div>
</div>
</div>
</section>

<section id="booking">
<h2 class="section-title">Book Appointment</h2>

<form onsubmit="pay(event)">
<input type="text" placeholder="Full Name" required>
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

<button class="submit">Confirm & Pay</button>
</form>
</section>

<section>
<h2 class="section-title">Policies</h2>

<div class="policy">
<h3>Appointment Policy</h3>
<p>Advance booking required. Rescheduling allowed 12 hours prior. Missed sessions without notice are non-adjustable.</p>
</div>

<div class="policy">
<h3>Payment Policy</h3>
<p>UPI payment only. Booking confirmed after successful transaction. Payments are non-refundable.</p>
</div>

<div class="policy">
<h3>Conduct Policy</h3>
<p>Strict confidentiality maintained. Inappropriate behavior leads to termination without refund. This platform offers guidance, not medical therapy.</p>
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

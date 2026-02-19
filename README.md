<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>PulseIQ – Hospital Dashboard</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="header">
    <h1>PulseIQ – Hospital Dashboard</h1>
    <p>Hospital: Meerut District Hospital</p>
</div>

<div class="container">

    <div class="login-card">
        <h2>Login</h2>
        <input type="text" id="username" placeholder="Username">
        <input type="password" id="password" placeholder="Password">
        <button onclick="login()">Login</button>
        <p id="login-msg"></p>
    </div>

    <div class="dashboard" style="display:none;">
        <h2>Welcome <span id="user-role"></span></h2>
        <div class="card-row">
            <div class="card">
                <h3>Total Patients</h3>
                <p>128</p>
            </div>
            <div class="card">
                <h3>Available Beds</h3>
                <p>22</p>
            </div>
            <div class="card">
                <h3>Staff on Duty</h3>
                <p>Doctors:12 | Nurses:18</p>
            </div>
        </div>
        <div class="alerts">
            <h3>Alerts</h3>
            <ul>
                <li>ICU 5 – High Heart Rate</li>
                <li>Ward 12 – Low Oxygen Level</li>
                <li>ER – Ventilator Disconnected</li>
            </ul>
        </div>
    </div>

</div>

<script src="script.js"></script>
</body>
</html>
body { font-family: Arial; background: #f2f4f8; margin:0; }
.header { background: #2f3e5c; color:white; padding:20px; text-align:center; }
.container { padding: 20px; max-width: 900px; margin:auto; }
.login-card { background:white; padding:20px; border-radius:10px; box-shadow:0 4px 10px rgba(0,0,0,0.1); margin-bottom:20px; text-align:center; }
.login-card input { padding:10px; margin:10px 0; width:80%; }
.login-card button { padding:10px 20px; background:#2d6cdf; color:white; border:none; cursor:pointer; }
.login-card p { color:red; }
.dashboard { background:white; padding:20px; border-radius:10px; box-shadow:0 4px 10px rgba(0,0,0,0.1); }
.card-row { display:flex; gap:20px; margin-bottom:20px; }
.card { flex:1; background:#f8f9fb; padding:15px; border-radius:8px; text-align:center; }
.alerts { background:#fff3cd; padding:10px; border-left:5px solid #ff9800; border-radius:5px; }
async function login() {
    const username = document.getElementById('username').value;
    const password = document.getElementById('password').value;
    const msg = document.getElementById('login-msg');

    if(!username || !password) {
        msg.innerText = "Enter both fields";
        return;
    }

    const res = await fetch('http://localhost:3000/login', {
        method: 'POST',
        headers: {'Content-Type':'application/json'},
        body: JSON.stringify({ username, password })
    });

    const data = await res.json();

    if(data.success) {
        document.querySelector('.login-card').style.display = 'none';
        document.querySelector('.dashboard').style.display = 'block';
        document.getElementById('user-role').innerText = data.role;
    } else {
        msg.innerText = data.message;
    }
}


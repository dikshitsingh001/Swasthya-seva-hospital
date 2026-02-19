<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>PulseIQ Login</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="container">

    <!-- LOGIN CARD -->
    <div class="login-card" id="login-card">
        <h2>Login</h2>
        <input type="text" id="username" placeholder="Username">
        <input type="password" id="password" placeholder="Password">
        <button onclick="login()">Login</button>
        <p id="login-msg"></p>
    </div>

    <!-- DASHBOARD -->
    <div class="dashboard" id="dashboard" style="display:none;">
        <h2>Welcome, <span id="user-role"></span></h2>
        <p>This is a simple dashboard demo.</p>
        <button onclick="logout()">Logout</button>
    </div>

</div>

<script src="script.js"></script>
</body>
</html>

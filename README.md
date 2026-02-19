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
body {
    font-family: Arial, sans-serif;
    background: linear-gradient(120deg, #3498db, #2ecc71);
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0;
}

.container {
    background: white;
    padding: 30px;
    border-radius: 15px;
    box-shadow: 0 5px 20px rgba(0,0,0,0.3);
    text-align: center;
    width: 300px;
}

input {
    width: 90%;
    padding: 10px;
    margin: 10px 0;
    border-radius: 5px;
    border: 1px solid #ccc;
}

button {
    padding: 10px 20px;
    background: #3498db;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
}

button:hover {
    background: #2c80b4;
}

#login-msg {
    color: red;
    margin-top: 10px;
}



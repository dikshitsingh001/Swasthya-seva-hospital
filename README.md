<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>PulseIQ – Hospital Dashboard</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>

<div class="header">
    <h1>PulseIQ – Hospital Dashboard</h1>
    <p>Hospital: Meerut District Hospital</p>
    <div id="user-role-display"></div>
</div>

<div class="container">

    <!-- LOGIN CARD -->
    <div class="login-card">
        <h2>Login</h2>
        <input type="text" id="username" placeholder="Username">
        <input type="password" id="password" placeholder="Password">
        <button onclick="login()">Login</button>
        <p id="login-msg"></p>
    </div>

    <!-- DASHBOARD -->
    <div class="dashboard" style="display:none;">

        <div class="card-row">
            <div class="card total-patients">
                <h3>Total Patients</h3>
                <p>128</p>
            </div>
            <div class="card available-beds">
                <h3>Available Beds</h3>
                <p>22</p>
            </div>
            <div class="card staff-duty">
                <h3>Staff on Duty</h3>
                <p>Doctors:12 | Nurses:18 | Ambulances:4</p>
            </div>
        </div>

        <div class="alerts">
            <h3>Alerts</h3>
            <ul>
                <li class="critical">ICU 5 – High Heart Rate</li>
                <li>Ward 12 – Low Oxygen Level</li>
                <li class="critical">ER – Ventilator Disconnected</li>
            </ul>
        </div>

        <div class="patient-table">
            <h3>Patient List</h3>
            <table>
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Age</th>
                        <th>Bed</th>
                        <th>Heart Rate</th>
                        <th>BP</th>
                        <th>SpO2</th>
                        <th>Assigned Doctor</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>John Doe</td>
                        <td>56</td>
                        <td>ICU5</td>
                        <td>120</td>
                        <td>140/90</td>
                        <td>92%</td>
                        <td>Dr. Sharma</td>
                    </tr>
                    <tr>
                        <td>Mary Jane</td>
                        <td>45</td>
                        <td>Ward12</td>
                        <td>80</td>
                        <td>120/80</td>
                        <td>98%</td>
                        <td>Dr. Singh</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <div class="graph">
            <h3>Real-Time Monitoring (Demo)</h3>
            <canvas id="vitalsChart" width="800" height="300"></canvas>
        </div>

    </div>

</div>

<footer>
    © 2026 PulseIQ Monitoring System
</footer>

<script src="script.js"></script>
</body>
</html>
body { margin:0; font-family: Arial, sans-serif; background:#eef2f6; }
.header { background:#2c3e50; color:white; padding:20px; text-align:center; position:relative; }
#user-role-display { position:absolute; right:20px; top:30px; color:#f1c40f; font-weight:bold; }

.container { padding:20px; max-width:1200px; margin:auto; }

.login-card { background:#ffffff; padding:30px; border-radius:15px; box-shadow:0 5px 15px rgba(0,0,0,0.2); text-align:center; }
.login-card input { padding:10px; margin:10px 0; width:80%; border-radius:5px; border:1px solid #ccc; }
.login-card button { padding:10px 25px; margin-top:10px; border:none; background:#27ae60; color:white; font-weight:bold; cursor:pointer; border-radius:5px; }
.login-card button:hover { background:#2ecc71; }
#login-msg { color:red; }

.dashboard { margin-top:20px; }

.card-row { display:flex; gap:20px; flex-wrap:wrap; margin-bottom:20px; }
.card { flex:1; min-width:200px; padding:20px; border-radius:15px; color:white; font-weight:bold; text-align:center; box-shadow:0 4px 10px rgba(0,0,0,0.15); }
.total-patients { background:#3498db; }
.available-beds { background:#2ecc71; }
.staff-duty { background:#e67e22; }

.alerts { background:#fef9e7; padding:15px; border-left:6px solid #f1c40f; border-radius:10px; margin-bottom:20px; }
.alerts .critical { border-left:6px solid red; background:#fdecea; }

.patient-table table { width:100%; border-collapse:collapse; background:white; border-radius:10px; overflow:hidden; }
.patient-table th, td { padding:12px; border-bottom:1px solid #ddd; text-align:center; }
.patient-table th { background:#34495e; color:white; }
.patient-table tr:nth-child(even) { background:#f2f2f2; }

.graph { background:white; padding:20px; border-radius:15px; box-shadow:0 4px 10px rgba(0,0,0,0.1); margin-bottom:20px; }

footer { background:#2c3e50; color:white; text-align:center; padding:15px; }

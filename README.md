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

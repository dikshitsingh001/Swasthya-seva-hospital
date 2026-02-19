# Swasthya-seva-hospital
<!DOCTYPE html>
<html>
<head>
<title>Swasthya Seva Hospital Dashboard</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<style>
body{
    margin:0;
    font-family: Arial, sans-serif;
    background:#f4f6f9;
}

header{
    background:#0a1f44;
    color:white;
    padding:15px 30px;
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.container{
    display:flex;
}

.sidebar{
    width:20%;
    background:white;
    padding:20px;
    box-shadow:2px 0 5px rgba(0,0,0,0.1);
}

.main{
    width:80%;
    padding:20px;
}

.cards{
    display:flex;
    gap:20px;
    margin-bottom:20px;
}

.card{
    flex:1;
    padding:20px;
    border-radius:8px;
    color:white;
    text-align:center;
    font-size:18px;
}

.blue{background:#4e73df;}
.green{background:#1cc88a;}
.orange{background:#f6c23e;}
.red{background:#e74a3b;}

.patient-card{
    background:white;
    padding:20px;
    border-radius:8px;
    box-shadow:0 4px 8px rgba(0,0,0,0.1);
}

.alert-box{
    background:#e74a3b;
    color:white;
    padding:15px;
    margin-top:15px;
    border-radius:8px;
    font-weight:bold;
}
</style>
</head>

<body>

<header>
<h2>Swasthya Seva Hospital Dashboard</h2>
<div>Dr. Sharma (Logout)</div>
</header>

<div class="container">

<div class="sidebar">
<h3>Patient List</h3>
<p>Rajesh Kumar - Stable</p>
<p>Anita Verma - Warning</p>
<p style="color:red;">Sunil Mehta - Critical</p>
<p>Pooja Singh - Stable</p>
</div>

<div class="main">

<div class="cards">
<div class="card blue">Total Patients<br><h2>28</h2></div>
<div class="card green">Stable<br><h2>16</h2></div>
<div class="card orange">Warning<br><h2>8</h2></div>
<div class="card red">Critical<br><h2>4</h2></div>
</div>

<div class="patient-card">
<h3>Patient Details: Sunil Mehta</h3>
<p><b>Age:</b> 58</p>
<p><b>Heart Rate:</b> 128 bpm</p>
<p><b>SpO₂:</b> 88%</p>
<p><b>Temperature:</b> 38.5°C</p>

<canvas id="myChart"></canvas>

<div class="alert-box">
CRITICAL ALERT: High Risk of Cardiac Arrest!
</div>

</div>

</div>

</div>

<script>
const ctx = document.getElementById('myChart');

new Chart(ctx, {
type: 'line',
data: {
labels: ['1','2','3','4','5','6','7'],
datasets: [{
label: 'Heart Rate',
data: [80,85,90,100,110,120,128],
borderColor: 'red',
fill:false
}]
},
});
</script>

</body>
</html>

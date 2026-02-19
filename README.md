<!DOCTYPE html>
<html>
<head>
<title>Swasthya Seva Hospital | Advanced Dashboard</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<style>
body{
    margin:0;
    font-family: 'Segoe UI', sans-serif;
    background:#eef2f7;
}

/* HEADER */
header{
    background:#0d1b2a;
    color:white;
    padding:15px 30px;
    display:flex;
    justify-content:space-between;
    align-items:center;
}

header h2{
    margin:0;
}

nav a{
    color:white;
    margin:0 15px;
    text-decoration:none;
}

/* LAYOUT */
.container{
    display:flex;
    height:calc(100vh - 60px);
}

/* SIDEBAR */
.sidebar{
    width:250px;
    background:white;
    padding:20px;
    box-shadow:2px 0 8px rgba(0,0,0,0.05);
}

.sidebar h3{
    margin-top:0;
}

.patient{
    padding:10px;
    border-radius:6px;
    margin-bottom:8px;
    cursor:pointer;
}

.patient.active{
    background:#dbeafe;
    font-weight:bold;
}

.patient.critical{
    color:red;
}

/* MAIN */
.main{
    flex:1;
    padding:25px;
    overflow:auto;
}

/* CARDS */
.cards{
    display:flex;
    gap:20px;
    margin-bottom:20px;
}

.card{
    flex:1;
    padding:20p

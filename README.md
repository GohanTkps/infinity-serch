<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Infinity Search</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Segoe UI,Arial,sans-serif;
}

body{

height:100vh;

display:flex;
justify-content:center;
align-items:center;

background:url("https://images.unsplash.com/photo-1462331940025-496dfbfc7564?auto=format&fit=crop&w=2000&q=80") center center/cover no-repeat fixed;

overflow:hidden;

}

body::before{

content:"";
position:absolute;
width:100%;
height:100%;
background:rgba(0,0,0,.45);

}

.container{

position:relative;
z-index:2;
text-align:center;
width:100%;

}

.logo{

font-size:72px;
font-weight:700;
color:white;
letter-spacing:2px;

text-shadow:
0 0 15px #00d9ff,
0 0 30px #00d9ff,
0 0 60px #7d3cff;

animation:glow 3s infinite alternate;

}

.logo span{

color:#00d9ff;

}

@keyframes glow{

from{

text-shadow:
0 0 10px #00d9ff,
0 0 20px #7d3cff;

}

to{

text-shadow:
0 0 25px #00d9ff,
0 0 45px #7d3cff,
0 0 80px #7d3cff;

}

}

.subtitle{

margin-top:10px;
margin-bottom:40px;

font-size:20px;
color:white;
opacity:.9;

}

.search-box{

width:650px;
max-width:90%;

margin:auto;

display:flex;

padding:14px 22px;

border-radius:40px;

background:rgba(255,255,255,.15);

backdrop-filter:blur(12px);

border:1px solid rgba(255,255,255,.3);

transition:.3s;

}

.search-box:hover{

box-shadow:0 0 30px rgba(0,217,255,.5);

}

.search-box input{

flex:1;
background:transparent;
border:none;
outline:none;
color:white;
font-size:19px;

}

.search-box input::placeholder{

color:#ddd;

}

.buttons{

margin-top:35px;

}

button{

padding:12px 25px;

margin:8px;

border:none;

border-radius:25px;

cursor:pointer;

font-size:16px;

color:white;

background:linear-gradient(45deg,#00b7ff,#7d3cff);

transition:.3s;

}

button:hover{

transform:scale(1.05);

box-shadow:0 0 25px #00d9ff;

}

.footer{

position:absolute;

bottom:25px;

width:100%;

text-align:center;

color:white;

opacity:.8;

font-size:14px;

z-index:2;

}

</style>

</head>

<body>

<div class="container">

<h1 class="logo">
<span>∞</span> Infinity Search
</h1>

<div class="subtitle">

Explore Beyond Limits

</div>

<div class="search-box">

<input
id="search"
type="text"
placeholder="Cerca sul Web...">

</div>

<div class="buttons">

<button onclick="searchWeb()">
🔍 Cerca
</button>

<button onclick="lucky()">
✨ Esplora
</button>

</div>

</div>

<div class="footer">

Infinity Search © 2026

</div>

<script>

function searchWeb(){

const text=document.getElementById("search").value.trim();

if(text==="") return;

window.location.href=
"https://www.google.com/search?q="+encodeURIComponent(text);

}

function lucky(){

const text=document.getElementById("search").value.trim();

if(text==="") return;

window.location.href=
"https://www.google.com/search?btnI=I&q="+encodeURIComponent(text);

}

document
.getElementById("search")
.addEventListener("keypress",function(e){

if(e.key==="Enter"){

searchWeb();

}

});

</script>

</body>
</html>

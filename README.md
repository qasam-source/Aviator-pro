<!DOCTYPE html>
<html>
<head>
<title>Mini Aviator</title>
<style>
body{
background:black;
color:white;
text-align:center;
font-family:Arial;
}
#plane{
font-size:50px;
margin-top:40px;
}
button{
padding:10px 20px;
font-size:18px;
}
</style>
</head>

<body>

<h1>Mini Aviator</h1>

<div id="plane">✈️</div>

<h2 id="multi">1.00x</h2>

<button onclick="startGame()">START</button>

<script>

let multi=1;
let running=false;

function startGame(){

multi=1;
running=true;

let interval=setInterval(()=>{

multi+=0.05;

document.getElementById("multi").innerText=multi.toFixed(2)+"x";

if(Math.random()<0.05){

running=false;

alert("IMEANGUKA "+multi.toFixed(2)+"x");

clearInterval(interval);

}

},100);

}

</script>

</body>
</html>

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>جرب حظك</title>

<style>

body{
text-align:center;
font-family:Arial;
margin-top:120px;
overflow:hidden;
background:#f2f2f2;
}

button{
position:absolute;
padding:15px 25px;
font-size:18px;
border:none;
background:#ff4444;
color:white;
border-radius:10px;
}

#prank{
display:none;
font-size:35px;
color:red;
margin-top:50px;
}

</style>
</head>

<body>

<h2>اضغط على الزر لتحصل على هدية 🎁</h2>

<button id="btn">اضغط هنا</button>

<div id="prank">😂 تم خداعك!</div>

<script>

let btn = document.getElementById("btn");
let prank = document.getElementById("prank");

let tries = 0;

btn.addEventListener("touchstart", move);
btn.addEventListener("mouseover", move);

function move(){

tries++;

if(tries > 6){

btn.style.display="none";
prank.style.display="block";

document.body.style.animation="shake 0.3s infinite";

return;

}

let x = Math.random()*(window.innerWidth-120);
let y = Math.random()*(window.innerHeight-120);

btn.style.left=x+"px";
btn.style.top=y+"px";

}

</script>

<style>

@keyframes shake{
0%{transform:translate(0)}
25%{transform:translate(5px)}
50%{transform:translate(-5px)}
75%{transform:translate(5px)}
100%{transform:translate(0)}
}

</style>

</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For My Babyyy ❤️</title>

<style>
body{
margin:0;
padding:0;
font-family: 'Georgia', serif;
background:linear-gradient(to bottom,#ffc0cb,#ff9eb5);
overflow-x:hidden;
text-align:center;
}

/* POPUP */
#popup{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.8);
display:flex;
justify-content:center;
align-items:center;
z-index:1000;
color:white;
font-size:22px;
padding:20px;
}

.popup-box{
background:#ff4d6d;
padding:30px;
border-radius:20px;
box-shadow:0 0 20px white;
}

button{
padding:12px 25px;
border:none;
border-radius:30px;
background:#c9184a;
color:white;
font-size:16px;
cursor:pointer;
margin-top:20px;
}

/* LETTER STYLE */
.letter{
background:#fdf0d5;
width:90%;
max-width:500px;
margin:40px auto;
padding:30px;
box-shadow:0 0 25px rgba(0,0,0,0.4);
border-radius:10px;
position:relative;
display:none;
overflow-y:auto;
max-height:70vh;
}

/* Burn effect */
.letter:before{
content:"";
position:absolute;
top:-10px;
left:-10px;
right:-10px;
bottom:-10px;
background:radial-gradient(circle at top left, rgba(0,0,0,0.6), transparent 70%),
radial-gradient(circle at bottom right, rgba(0,0,0,0.6), transparent 70%);
z-index:-1;
border-radius:15px;
}

.hidden{
display:none;
}

/* Hearts Fountain */
.heart{
position:fixed;
font-size:30px;
animation:float 3s linear forwards;
color:red;
}

@keyframes float{
0%{transform:translateY(0);opacity:1;}
100%{transform:translateY(-600px);opacity:0;}
}

img{
width:90%;
max-width:400px;
margin-top:20px;
border-radius:20px;
box-shadow:0 0 20px pink;
}
</style>
</head>

<body>

<!-- Background Song -->
<audio autoplay loop>
<source src="song.mp3" type="audio/mpeg">
</audio>

<!-- POPUP -->
<div id="popup">
<div class="popup-box">
Happy Valentine's Day Babyyy 🥹🫂❤️🫶💋<br>
<button onclick="openLetter()">Open My Heart 💌</button>
</div>
</div>

<!-- FIRST LETTER -->
<div class="letter" id="letter1">
<p>
Aaj zarur Valentine’s Day hai… but yeh ek din mujhe nahi bata sakta  
ki main aapko kitna pyaar karta hoon.  
Main roz aapko bahut bahut bahut zyada pyaar karta hoon meri jaan 🥹🫶  

Aaj hum nahi milenge… no problem.  
Dil toh hamesha se ek saath hi tha, hai, aur rahega.  

Yes… I love you sooooo muchhh ❤️  
Itna karta hoon ki shabdon mein kabhi bata nahi sakta.  
You know that right, bacha?  

Tum meri life ki sabse special insaan ho.  
My heart’s queen. My everything.  

</p>
<button onclick="nextLetter()">Next 💌</button>
</div>

<!-- SECOND LETTER CLOSED -->
<div class="letter hidden" id="letter2">
<p>Click to open the sealed love letter 💌</p>
<button onclick="openFinal()">Click Here ❤️</button>
</div>

<!-- FINAL SECTION -->
<div id="final" class="hidden">
<h2>I Love You Subhuu My Wifeyyy 🥹❤️🫂🧿💋🫶</h2>
</div>

<script>

function openLetter(){
document.getElementById("popup").style.display="none";
document.getElementById("letter1").style.display="block";
}

function nextLetter(){
document.getElementById("letter1").style.display="none";
document.getElementById("letter2").classList.remove("hidden");
}

function openFinal(){
document.getElementById("letter2").style.display="none";
startHearts();

setTimeout(function(){
document.getElementById("final").classList.remove("hidden");
},3000);
}

function startHearts(){
for(let i=0;i<40;i++){
let heart=document.createElement("div");
heart.className="heart";
heart.innerHTML="❤️";
heart.style.left=Math.random()*100+"vw";
heart.style.bottom="0";
document.body.appendChild(heart);

setTimeout(()=>heart.remove(),3000);
}
}

</script>

</body>
</html>

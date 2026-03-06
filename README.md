<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Hindu Youth Summit 2026</title>

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,#ff9933,#ffd699,#ffffff);
    font-family:Arial, sans-serif;
    overflow:hidden;
}

h1{
    font-size:3em;
    text-align:center;
    color:#c62828;
    text-shadow:2px 2px 12px rgba(0,0,0,0.3);
    z-index:2;
}

/* balloons */
.balloon{
    position:absolute;
    bottom:-150px;
    width:60px;
    height:80px;
    border-radius:50%;
    animation:float 10s linear infinite;
}

.balloon:after{
    content:'';
    position:absolute;
    width:2px;
    height:50px;
    background:#555;
    left:50%;
    top:80px;
}

@keyframes float{
    0%{transform:translateY(0);}
    100%{transform:translateY(-120vh);}
}

/* confetti */
.confetti{
    position:absolute;
    width:10px;
    height:10px;
    top:-10px;
    opacity:0.8;
    animation:fall linear forwards;
}

@keyframes fall{
    to{
        transform:translateY(110vh) rotate(720deg);
    }
}
</style>
</head>

<body>

<h1>🎉 HINDU YOUTH SUMMIT 2026 is here woooh!! 🎉</h1>

<script>

/* balloons */
function createBalloon(){
    const balloon=document.createElement("div");
    balloon.classList.add("balloon");

    const colors=["#ff4d4d","#4da6ff","#66ff66","#ffff66","#ff66ff","#ff9933"];
    balloon.style.background=colors[Math.floor(Math.random()*colors.length)];

    balloon.style.left=Math.random()*100+"vw";
    balloon.style.animationDuration=(6+Math.random()*6)+"s";

    document.body.appendChild(balloon);

    setTimeout(()=>{balloon.remove();},12000);
}

setInterval(createBalloon,600);


/* confetti */
function createConfetti(){
    const conf=document.createElement("div");
    conf.classList.add("confetti");

    const colors=["red","blue","yellow","green","orange","purple"];
    conf.style.background=colors[Math.floor(Math.random()*colors.length)];

    conf.style.left=Math.random()*100+"vw";
    conf.style.animationDuration=(3+Math.random()*3)+"s";

    document.body.appendChild(conf);

    setTimeout(()=>{conf.remove();},6000);
}

setInterval(createConfetti,120);

</script>

</body>
</html>

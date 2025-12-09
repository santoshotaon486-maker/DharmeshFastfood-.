lp# DharmeshFastfood-.
Dharmesh Fast food 
<!DOCTYPE html>
<html>
<head>
<title>Tap Tap Roll</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
    body{text-align:center;background:#fff3e0;}
    canvas{margin-top:20px;background:#ffe0b2;border-radius:10px;}
</style>
</head>

<body>
<h2>🌯 TAP TAP ROLL</h2>
<canvas id="cv" width="320" height="500"></canvas>

<script>
const cv=document.getElementById("cv");
const cx=cv.getContext("2d");

let roll={x:50,y:250,r:15,vy:0};
let gravity=0.4;

document.addEventListener("click",()=> roll.vy=-7 );

function loop(){
    cx.clearRect(0,0,320,500);

    roll.vy+=gravity;
    roll.y+=roll.vy;

    cx.fillStyle="brown";
    cx.beginPath();
    cx.arc(roll.x,roll.y,roll.r,0,Math.PI*2);
    cx.fill();

    if(roll.y>500 || roll.y<0){
        alert("Game Over!");
        location.reload();
    }

    requestAnimationFrame(loop);
}
loop();
</script>
</body>
</html>

<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>🎯ルーレット🎯</title>

<style>
body{
  margin:0;
  color:#fff;
  font-family:sans-serif;
  height:100vh;
  display:flex;
  flex-direction:column;
  align-items:center;
  justify-content:center;
  overflow:hidden;
}

/* タイトル */
h2{
  position:absolute;
  top:20px;
  padding:8px 20px;
  background:rgba(0,0,0,0.4);
  border-radius:12px;
  backdrop-filter:blur(6px);
  text-shadow:
    0 0 5px #fff,
    0 0 10px #fff,
    0 0 20px #fff;
}

/* UI */
#container, #result, button{
  position:relative;
  z-index:10;
}

#container{
  width:80vw;
  max-width:320px;
  aspect-ratio:1;
  position:relative;
}

/* ▼ピン（半分かぶせ） */
#pointer{
  position:absolute;
  left:50%;
  top:-14px; /* ←ここがポイント（半分重ねる） */
  transform:translate(-50%,0);
  font-size:28px;
  text-shadow:0 0 10px #fff;
  z-index:20;
}

/* ルーレット */
canvas{
  width:100%;
  height:100%;
  border-radius:50%;
  border:5px solid #000;
  display:block;
  transition:transform 3s ease-out;

  box-shadow:
    inset 0 0 35px rgba(0,0,0,0.95),
    0 0 25px rgba(0,0,0,0.9);
}

/* 結果 */
#result{
  margin-top:20px;
  font-size:22px;
  text-shadow:0 0 5px #000;
}

/* ボタン */
button{
  margin-top:12px;
  padding:12px 24px;
  font-size:16px;
  border:2px solid #000;
  border-radius:10px;
  background:linear-gradient(45deg,#fff,#ccc);
  color:#000;
  cursor:pointer;
  transition:0.2s;
}

button:hover{
  transform:scale(1.05);
  box-shadow:0 0 15px #fff;
}

button:active{
  transform:scale(0.95);
}

button:disabled{
  opacity:0.5;
}
</style>
</head>

<body>

<h2>🎯ルーレット🎯</h2>

<div id="container">
  <div id="pointer">▼</div>
  <canvas id="wheel"></canvas>
</div>

<h3 id="result">結果：</h3>
<button id="spinBtn">回してゲット！</button>

<script>
/* 背景（虹） */
let hue = 0;
function animateBackground(){
  hue += 1;
  document.body.style.background = `hsl(${hue}, 100%, 50%)`;
  requestAnimationFrame(animateBackground);
}
animateBackground();

/* ルーレット */
const canvas = document.getElementById("wheel");
const ctx = canvas.getContext("2d");
const btn = document.getElementById("spinBtn");
const result = document.getElementById("result");

function resizeCanvas(){
  const rect = canvas.getBoundingClientRect();
  canvas.width = rect.width;
  canvas.height = rect.height;
  draw();
}

const slots = [
"当たり","ハズレ",
"当たり","ハズレ",
"当たり","ハズレ",
"当たり","ハズレ"
];

const angle = 360 / slots.length;

function draw(){
  let size = canvas.width;
  let center = size/2;
  let rad = 2*Math.PI/slots.length;

  ctx.clearRect(0,0,size,size);

  for(let i=0;i<slots.length;i++){
    ctx.beginPath();
    ctx.moveTo(center,center);
    ctx.arc(center,center,center,i*rad,(i+1)*rad);
    ctx.closePath();

    ctx.fillStyle = slots[i] === "当たり" ? "gold" : "gray";
    ctx.fill();

    ctx.save();
    ctx.translate(center,center);
    ctx.rotate(i*rad + rad/2);

    ctx.fillStyle = "#000";
    ctx.textAlign = "center";
    ctx.textBaseline = "middle";

    if(slots[i] === "当たり"){
      ctx.font = `bold ${size*0.065}px sans-serif`;
    }else{
      ctx.font = `${size*0.055}px sans-serif`;
    }

    ctx.fillText(slots[i], center*0.35, 0);

    ctx.restore();
  }
}

resizeCanvas();
window.addEventListener("resize", resizeCanvas);

/* 回転 */
btn.onclick = function(){
  btn.disabled = true;
  result.textContent = "回転中...";

  canvas.style.transition = "none";
  canvas.style.transform = "rotate(0deg)";
  void canvas.offsetWidth;

  canvas.style.transition = "transform 3s ease-out";

  let atariIndex = [0,2,4,6];
  let i = atariIndex[Math.floor(Math.random()*atariIndex.length)];

  let stop = 360 - (i * angle) - angle/2;
  let total = 360 * 6 + stop;

  canvas.style.transform = "rotate(" + total + "deg)";

  setTimeout(()=>{
    result.textContent = "結果：当たり！";
    btn.disabled = false;
  },3000);
};
</script>

</body>
</html>

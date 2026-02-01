<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>My Pookie Elif 💖</title>

<style>
:root{
  --bg1:#120018;
  --bg2:#2b0036;
  --pink:#ff4da6;
  --hot:#ff1f8f;
  --soft:#ffd1e8;
  --card: rgba(255,255,255,0.08);
  --card2: rgba(255,255,255,0.12);
  --shadow: 0 20px 60px rgba(0,0,0,.45);
}

*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;
  font-family: ui-rounded, system-ui, -apple-system, Arial, sans-serif;
  background:
    radial-gradient(1200px 700px at 20% 10%, #3d004f 0%, transparent 60%),
    radial-gradient(900px 600px at 80% 20%, #5a0040 0%, transparent 55%),
    linear-gradient(160deg,var(--bg1),var(--bg2));
  color:var(--soft);
  overflow:hidden;
  position:relative;
}

/* Floating heart with text */
.float-heart{
  position:absolute;
  width:26px;height:26px;
  background:var(--pink);
  transform:rotate(45deg);
  opacity:.18;
  animation:floatUp linear infinite;
  pointer-events:none;
  filter: blur(.15px);
}
.float-heart:before,.float-heart:after{
  content:"";
  position:absolute;
  width:26px;height:26px;
  background:var(--pink);
  border-radius:50%;
}
.float-heart:before{left:-13px}
.float-heart:after{top:-13px}

.float-heart .name{
  position:absolute;
  left:50%;
  top:50%;
  transform: translate(-50%,-50%) rotate(-45deg);
  font-weight:900;
  font-size: 12px;
  letter-spacing:.4px;
  color: rgba(255,255,255,.92);
  text-shadow: 0 4px 16px rgba(0,0,0,.45);
  white-space:nowrap;
  opacity:.95;
}
.float-heart.tiny .name{ display:none; }

@keyframes floatUp{
  from{transform:translateY(120vh) rotate(45deg)}
  to{transform:translateY(-160vh) rotate(45deg)}
}

.wrap{
  height:100%;
  display:flex;
  justify-content:center;
  align-items:center;
  padding:24px;
  position:relative;
  z-index:2;
}

.card{
  width:min(560px,92vw);
  background:linear-gradient(180deg,var(--card),var(--card2));
  border: 1px solid rgba(255,255,255,0.14);
  border-radius:26px;
  padding:26px 22px 22px;
  text-align:center;
  backdrop-filter:blur(12px);
  box-shadow: var(--shadow);
  position:relative;
}

.title{
  font-size: clamp(28px, 4.8vw, 44px);
  margin: 10px 0 10px;
  line-height:1.05;
  text-shadow: 0 6px 22px rgba(255,0,140,.22);
}

.subtitle{opacity:.9; margin: 0 0 10px;}

/* cat eyes */
.eyes{display:flex;justify-content:center;gap:22px;margin: 10px 0 12px; user-select:none}
.eye{
  width:130px;height:90px;
  background: rgba(0,0,0,0.35);
  border: 1px solid rgba(255,255,255,0.12);
  border-radius:999px;
  position:relative;
  overflow:hidden;
  box-shadow: inset 0 0 22px rgba(255,77,166,.18);
}
.shine{
  position:absolute;
  inset:-30% -40%;
  background: radial-gradient(circle at 40% 40%, rgba(255,255,255,.18), transparent 55%);
  transform: rotate(12deg);
  pointer-events:none;
}
.pupil{
  position:absolute;
  width:34px;height:34px;
  left:50%;top:50%;
  transform:translate(-50%,-50%);
  transition: transform .08s linear;
  filter: drop-shadow(0 10px 12px rgba(255,31,143,.24));
}
.pupil:before{
  content:"";
  position:absolute;
  width:18px;height:18px;
  background:var(--hot);
  transform:rotate(45deg);
  left:8px;top:8px;
}
.pupil:after{
  content:"";
  position:absolute;
  width:18px;height:18px;
  background:var(--hot);
  border-radius:50%;
  box-shadow:-9px 0 0 var(--hot),0 -9px 0 var(--hot);
  transform:rotate(45deg);
}

/* buttons arena */
.buttons{
  margin-top:18px;
  position:relative;
  height:96px;
}

button{
  border:0;
  border-radius:18px;
  padding:14px 20px;
  font-size:18px;
  cursor:pointer;
  min-width: 132px;
  -webkit-tap-highlight-color: transparent;
  touch-action: manipulation;
  transition: transform .12s ease, filter .12s ease;
}
button:active{ transform: scale(0.98); }

#yes{
  background:linear-gradient(#ff6ab8,#ff1f8f);
  color:white;
  font-weight:900;
  letter-spacing:.3px;
  box-shadow: 0 14px 30px rgba(255,31,143,.22);
}
#yes:hover{ filter: brightness(1.05); }

#no{
  position:absolute;
  background: rgba(255,255,255,0.10);
  color: rgba(255,255,255,0.92);
  border: 1px solid rgba(255,255,255,0.16);
  left:55%;
  top:8px;
  box-shadow: 0 10px 20px rgba(0,0,0,.20);
}

.msg{ margin-top: 12px; min-height: 24px; opacity:.95; }

/* overlay */
.overlay{
  position:fixed;
  inset:0;
  display:none;
  justify-content:center;
  align-items:center;
  background: rgba(0,0,0,0.55);
  backdrop-filter: blur(10px);
  z-index:5;
  padding: 22px;
}
.box{
  width:min(560px, 92vw);
  background: linear-gradient(180deg, rgba(255,255,255,.10), rgba(255,255,255,.14));
  border: 1px solid rgba(255,255,255,.18);
  border-radius: 26px;
  padding: 26px 22px 22px;
  text-align:center;
  box-shadow: var(--shadow);
  position:relative;
  overflow:hidden;
}
.confetti{
  position:absolute;
  inset:-40%;
  background:
    radial-gradient(circle at 10% 20%, rgba(255,31,143,.28), transparent 35%),
    radial-gradient(circle at 70% 20%, rgba(255,255,255,.14), transparent 40%),
    radial-gradient(circle at 50% 80%, rgba(255,77,166,.20), transparent 42%);
  transform: rotate(12deg);
  pointer-events:none;
}
.box h2{ margin: 0 0 10px; font-size: clamp(26px, 4.6vw, 40px); }
.box p{ margin: 0; font-size: 16px; opacity:.92; }
.mini{ margin-top: 12px; font-size: 12px; opacity:.72; }

/* explosion hearts */
.pop-heart{
  position:fixed;
  width:14px; height:14px;
  background: var(--pink);
  transform: rotate(45deg);
  pointer-events:none;
  will-change: transform, opacity;
}
.pop-heart:before,.pop-heart:after{
  content:"";
  position:absolute;
  width:14px; height:14px;
  background: var(--pink);
  border-radius:50%;
}
.pop-heart:before{ left:-7px; top:0; }
.pop-heart:after{ left:0; top:-7px; }

/* Hidden YouTube player container */
#yt-wrap{
  position:fixed;
  width:1px; height:1px;
  left:-9999px; top:-9999px;
  overflow:hidden;
}
</style>
</head>

<body>

<!-- Hidden YouTube player -->
<div id="yt-wrap"><div id="yt-player"></div></div>

<div class="wrap">
  <div class="card">
    <div class="eyes" aria-hidden="true">
      <div class="eye" id="eyeL"><div class="shine"></div><div class="pupil" id="pupilL"></div></div>
      <div class="eye" id="eyeR"><div class="shine"></div><div class="pupil" id="pupilR"></div></div>
    </div>

    <h1 class="title">My pookie Elif… will you be my Valentine? 💖</h1>
    <p class="subtitle">Say YES my pookie… and I’ll make it the most unforgettable Valentine ever 😼💘</p>

    <div class="buttons" id="arena">
      <button id="yes">YES 😍</button>
      <button id="no">NO 🙅‍♀️</button>
    </div>

    <div class="msg" id="msg"></div>
    <div class="mini">Tap anywhere to start the music 🎶 (starts at 0:33)</div>
  </div>
</div>

<div class="overlay" id="overlay">
  <div class="box">
    <div class="confetti"></div>
    <h2>My pookie Elif said YES 😍💞</h2>
    <p>Valentine secured forever.</p>
    <div class="mini">Screenshot this and send it to Amir 😏💘</div>
  </div>
</div>

<script>
/* ========= FLOATING NAME HEARTS ========= */
const NAME_TEXT = "Elif";
const FLOAT_COUNT = 22;

function makeFloatHeart(){
  const h = document.createElement("div");
  h.className = "float-heart";
  const name = document.createElement("div");
  name.className = "name";
  name.textContent = NAME_TEXT;

  const size = 14 + Math.random()*26;
  h.style.width = size + "px";
  h.style.height = size + "px";
  h.style.left = (Math.random()*100) + "vw";
  h.style.opacity = (0.10 + Math.random()*0.22).toFixed(2);

  const scale = size / 26;
  h.style.transform = `rotate(45deg) scale(${scale})`;

  const dur = 7 + Math.random()*11;
  const delay = -Math.random()*dur;
  h.style.animationDuration = dur + "s";
  h.style.animationDelay = delay + "s";

  if (size < 20) h.classList.add("tiny");

  h.appendChild(name);
  document.body.appendChild(h);
}
for(let i=0;i<FLOAT_COUNT;i++) makeFloatHeart();

/* ========= CAT EYES FOLLOW ========= */
const pupilL = document.getElementById('pupilL');
const pupilR = document.getElementById('pupilR');

function movePupils(clientX, clientY){
  const rectL = document.getElementById('eyeL').getBoundingClientRect();
  const rectR = document.getElementById('eyeR').getBoundingClientRect();

  const dxL = clientX - (rectL.left + rectL.width/2);
  const dyL = clientY - (rectL.top + rectL.height/2);
  const dxR = clientX - (rectR.left + rectR.width/2);
  const dyR = clientY - (rectR.top + rectR.height/2);

  const clamp = (v, max)=> Math.max(-max, Math.min(max, v));
  const maxMove = 14;

  pupilL.style.transform =
    `translate(-50%,-50%) translate(${clamp(dxL/18,maxMove)}px, ${clamp(dyL/18,maxMove)}px)`;
  pupilR.style.transform =
    `translate(-50%,-50%) translate(${clamp(dxR/18,maxMove)}px, ${clamp(dyR/18,maxMove)}px)`;
}
window.addEventListener('mousemove', e => movePupils(e.clientX, e.clientY), {passive:true});
window.addEventListener('touchmove', e => {
  const t = e.touches[0];
  if (t) movePupils(t.clientX, t.clientY);
}, {passive:true});

/* ========= RUNAWAY NO ========= */
const arena = document.getElementById('arena');
const noBtn = document.getElementById('no');
const yesBtn = document.getElementById('yes');
const msg = document.getElementById('msg');
const overlay = document.getElementById('overlay');

function randomWithin(min, max){ return Math.random() * (max - min) + min; }

function placeNoButtonAway(fromX, fromY){
  const a = arena.getBoundingClientRect();
  const b = noBtn.getBoundingClientRect();
  const pad = 8;
  const maxX = a.width - b.width - pad;
  const maxY = a.height - b.height - pad;

  let best = {x: randomWithin(pad, maxX), y: randomWithin(pad, maxY), d:-1};
  for (let i=0;i<14;i++){
    const x = randomWithin(pad, maxX);
    const y = randomWithin(pad, maxY);
    const dx = (a.left + x + b.width/2) - fromX;
    const dy = (a.top + y + b.height/2) - fromY;
    const d = Math.hypot(dx, dy);
    if (d > best.d) best = {x,y,d};
  }
  noBtn.style.left = best.x + 'px';
  noBtn.style.top  = best.y + 'px';
}

const teasing = ["Nice try 😼","Nopeee 💅","You can’t catch me 😹","I’m shy 🙈","Say YES 😍","Come onnn 💘"];
function tease(){
  msg.textContent = teasing[Math.floor(Math.random()*teasing.length)];
  setTimeout(()=>{ msg.textContent=""; }, 900);
}

noBtn.addEventListener('mouseenter', (e)=>{ placeNoButtonAway(e.clientX, e.clientY); tease(); });
noBtn.addEventListener('touchstart', (e)=>{
  const t = e.touches[0];
  if (t) placeNoButtonAway(t.clientX, t.clientY);
  tease();
  e.preventDefault();
}, {passive:false});
noBtn.addEventListener('click', (e)=>{ placeNoButtonAway(e.clientX, e.clientY); tease(); });

window.addEventListener('load', ()=>{
  const a = arena.getBoundingClientRect();
  placeNoButtonAway(a.left + a.width/2, a.top + a.height/2);
});

/* ========= YES HEART EXPLOSION ========= */
function createPopHeart(x, y){
  const h = document.createElement("div");
  h.className = "pop-heart";
  document.body.appendChild(h);

  h.style.left = (x - 7) + "px";
  h.style.top  = (y - 7) + "px";

  const angle = Math.random() * Math.PI * 2;
  const dist  = 60 + Math.random()*120;
  const dx = Math.cos(angle) * dist;
  const dy = Math.sin(angle) * dist;

  const rot = 45 + (Math.random()*120 - 60);
  const scale = 0.8 + Math.random()*1.2;
  const duration = 700 + Math.random()*600;

  const start = performance.now();
  function tick(now){
    const t = Math.min(1, (now - start)/duration);
    const ease = 1 - Math.pow(1 - t, 3);

    const cx = x + dx*ease;
    const cy = y + dy*ease;

    h.style.transform = `translate(${cx - x}px, ${cy - y}px) rotate(${rot}deg) scale(${scale})`;
    h.style.opacity = (1 - t).toFixed(3);

    if (t < 1) requestAnimationFrame(tick);
    else h.remove();
  }
  requestAnimationFrame(tick);
}

function explodeHeartsFrom(el){
  const r = el.getBoundingClientRect();
  const x = r.left + r.width/2;
  const y = r.top + r.height/2;

  for(let i=0;i<28;i++) createPopHeart(x, y);
  for(let i=0;i<16;i++) setTimeout(()=>createPopHeart(x,y), 60 + i*20);
}

/* ========= YOUTUBE BACKGROUND MUSIC ========= */
const YT_VIDEO_ID = "39bTjy3q74g";
const START_AT_SECONDS = 33; // 0:33
let player = null;
let musicStarted = false;

// Load YouTube IFrame API
const tag = document.createElement('script');
tag.src = "https://www.youtube.com/iframe_api";
document.head.appendChild(tag);

window.onYouTubeIframeAPIReady = function() {
  player = new YT.Player('yt-player', {
    height: '1',
    width: '1',
    videoId: YT_VIDEO_ID,
    playerVars: {
      autoplay: 0,
      controls: 0,
      disablekb: 1,
      fs: 0,
      playsinline: 1,
      modestbranding: 1,
      rel: 0,
      start: START_AT_SECONDS
    },
    events: {
      onReady: () => {
        try { player.mute(); } catch(e){}
      }
    }
  });
};

function tryStartMusic(){
  if (musicStarted) return;
  if (!player) return;

  musicStarted = true;
  try{
    // seek first (in case player doesn't respect start param on some browsers)
    try { player.seekTo(START_AT_SECONDS, true); } catch(e){}
    player.playVideo();
    setTimeout(()=>{
      try{
        player.unMute();
        player.setVolume(65);
      }catch(e){}
    }, 250);
  }catch(e){
    musicStarted = false;
  }
}

// Start music on first interaction anywhere
window.addEventListener("pointerdown", tryStartMusic);
window.addEventListener("touchstart", tryStartMusic, {passive:true});

/* ========= YES ========= */
yesBtn.addEventListener("click", ()=>{
  explodeHeartsFrom(yesBtn);
  overlay.style.display="flex";
  if (navigator.vibrate) navigator.vibrate([60,40,60]);
  tryStartMusic();
});

overlay.addEventListener("click", ()=> overlay.style.display="none");
</script>

</body>
</html>

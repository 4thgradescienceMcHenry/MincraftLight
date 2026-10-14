<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Lumen Blocks</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Silkscreen:wght@400;700&family=Atkinson+Hyperlegible:wght@400;700&display=swap">
<style>
/* Layout: one game screen — block world canvas left, mission scroll right; stacks on phones. Single dusk-lighthouse look. */
:root{
  --night:#141a2e; --panel:#1d2540; --panel2:#26305a; --ink:#f3ecd8; --muted:#aab3d6;
  --sun:#ffc93d; --sun-deep:#e08a1e; --leaf:#4fae4a; --good:#7be08a; --warn:#ffb46b; --line:#3a4677;
  --display:"Silkscreen", "Courier New", monospace; --body:"Atkinson Hyperlegible", system-ui, sans-serif;
  color-scheme:dark;
}
html,body{background:var(--night);color:var(--ink);font-family:var(--body);font-size:16px}
body{padding-inline:16px;padding-block:14px}
*{box-sizing:border-box}
[hidden]{display:none!important}
.wrap{max-width:1180px;margin:0 auto;display:flex;flex-direction:column;gap:12px}
header{display:flex;flex-wrap:wrap;align-items:baseline;justify-content:space-between;gap:8px 16px}
h1{font-family:var(--display);font-weight:700;font-size:clamp(26px,4vw,40px);margin:0;letter-spacing:1px;color:var(--sun);text-shadow:3px 3px 0 #7a3d10}
.zone{font-family:var(--display);font-size:15px;color:var(--muted)}
.progress{display:flex;gap:6px}
.progress span{width:22px;height:22px;border:3px solid var(--line);background:var(--panel)}
.progress span.done{background:var(--sun);border-color:var(--sun-deep)}
.progress span.now{border-color:var(--sun)}
.game{display:grid;grid-template-columns:minmax(0,1fr) 330px;gap:14px;align-items:start}
@media (max-width:900px){.game{grid-template-columns:minmax(0,1fr)}}
.stage{position:relative;min-width:0;background:#0d1222;border:4px solid var(--line);padding:6px}
canvas{display:block;width:100%;height:auto;image-rendering:pixelated;touch-action:none}
.side{display:flex;flex-direction:column;gap:12px;min-width:0}
.card{background:var(--panel);border:3px solid var(--line);padding:12px 14px}
.card h2{font-family:var(--display);font-size:14px;letter-spacing:1px;margin:0 0 8px;color:var(--sun)}
.card p{margin:0 0 8px;line-height:1.45}
.goal{font-weight:700}
ul.check{list-style:none;margin:0;padding:0;display:flex;flex-direction:column;gap:6px}
ul.check li{display:flex;gap:8px;align-items:flex-start;line-height:1.35}
ul.check li i{flex:0 0 16px;height:16px;margin-top:2px;border:3px solid var(--line);background:var(--night)}
ul.check li.ok i{background:var(--good);border-color:#3c9b4b}
ul.check li.dim i{background:var(--warn);border-color:#b8742f}
.std{font-family:var(--display);font-size:11px;color:var(--muted)}
.held{display:flex;align-items:center;gap:10px}
.held canvas{width:40px;height:40px;border:3px solid var(--line);background:var(--night)}
.keys{font-size:14px;color:var(--muted);line-height:1.5}
kbd{font-family:var(--display);font-size:11px;background:var(--panel2);border:2px solid var(--line);padding:1px 5px;color:var(--ink)}
.pad{display:grid;grid-template-columns:repeat(3,52px);grid-template-rows:repeat(2,52px);gap:6px}
.controls{display:flex;flex-wrap:wrap;gap:14px;align-items:center;justify-content:space-between}
.acts{display:flex;gap:8px;flex-wrap:wrap}
button{font-family:var(--display);font-size:13px;background:var(--panel2);color:var(--ink);border:3px solid var(--line);padding:10px 12px;cursor:pointer;box-shadow:0 4px 0 #0a0f1e}
button:active{transform:translateY(3px);box-shadow:0 1px 0 #0a0f1e}
button:focus-visible{outline:3px solid var(--sun);outline-offset:2px}
button.primary{background:var(--sun);color:#3a1d05;border-color:var(--sun-deep)}
.pad button{padding:0;font-size:18px}
.toast{position:absolute;left:50%;top:10px;transform:translateX(-50%);background:var(--panel);border:3px solid var(--sun);padding:8px 14px;font-weight:700;pointer-events:none;max-width:90%;text-align:center}
.overlay{position:fixed;inset:0;z-index:20;background:rgba(9,12,24,.86);display:flex;align-items:center;justify-content:center;padding:16px}
.modal{background:var(--panel);border:4px solid var(--sun);max-width:560px;width:100%;padding:18px 20px;display:flex;flex-direction:column;gap:12px;max-height:100%;overflow:auto}
.modal h2{font-family:var(--display);color:var(--sun);margin:0;font-size:20px;text-wrap:balance}
.modal p{margin:0;line-height:1.5}
.choices{display:flex;flex-direction:column;gap:8px}
.choices button{font-family:var(--body);font-size:16px;text-align:left;text-transform:none;letter-spacing:0}
.choices button.wrong{border-color:#c0504d;background:#4a2430}
.choices button.right{border-color:#3c9b4b;background:#1f4a2c}
.code{font-family:var(--display);font-size:clamp(34px,8vw,56px);color:var(--sun);text-align:center;letter-spacing:4px;background:var(--night);border:4px dashed var(--sun-deep);padding:10px;user-select:all}
.shake{animation:shake .35s}
@keyframes shake{25%{transform:translateX(-6px)}50%{transform:translateX(6px)}75%{transform:translateX(-3px)}}
@media (prefers-reduced-motion:reduce){.shake{animation:none}}
</style>

</head>
<body>
<div class="wrap">
  <header>
    <div><h1>LUMEN BLOCKS</h1><div class="zone" id="zoneName">The Great Lighthouse has gone dark</div></div>
    <div class="progress" id="progress" aria-label="Zones completed"></div>
  </header>
  <div class="game">
    <div class="stage" id="stage">
      <canvas id="cv" width="768" height="528" aria-label="Block world game board"></canvas>
      <div class="toast" id="toast" hidden></div>
      <div class="overlay" id="overlay" hidden><div class="modal" id="modal"></div></div>
    </div>
    <aside class="side">
      <div class="card"><h2>MISSION</h2><p id="intro"></p><p class="goal" id="goal"></p><div class="std" id="std"></div></div>
      <div class="card"><h2>LIGHT CHECKS</h2><ul class="check" id="checks"></ul></div>
      <div class="card"><h2>IN YOUR HANDS</h2><div class="held"><canvas id="heldCv" width="16" height="16"></canvas><span id="heldName">Nothing yet</span></div></div>
    </aside>
  </div>
  <div class="controls">
    <div class="pad" aria-label="Move">
      <span></span><button id="bUp" aria-label="Move up">▲</button><span></span>
      <button id="bLeft" aria-label="Move left">◀</button><button id="bDown" aria-label="Move down">▼</button><button id="bRight" aria-label="Move right">▶</button>
    </div>
    <div class="acts">
      <button class="primary" id="bGrab">GRAB / PLACE</button>
      <button id="bRot">TURN MIRROR</button>
      <button id="bHint">HINT</button>
      <button id="bReset">RESTART ZONE</button>
      <button id="bSound" aria-pressed="true">SOUND ON</button>
    </div>
    <div class="keys">Press an arrow <kbd>←↑↓→</kbd> or <kbd>WASD</kbd> once to turn, again to walk · Grab/Place <kbd>E</kbd> or <kbd>Space</kbd> · Turn mirror <kbd>R</kbd><br>You act on the block your explorer is facing (yellow outline).</div>
  </div>
</div>
<script>
// ===== Lumen Blocks: core logic (shared by game + tests) =====
const W=16,H=11;
const LEVELS=[
 {name:"Zone 1 · Straight Shot", std:"4-PS4-2",
  intro:"The sun block is shining, but a stone is in the way. Light travels in a straight line, so it can't go around the stone.",
  goal:"Move the stone so the sunbeam reaches the flower pot.",
  map:[
  "TTTTTTTTTTTTTTTT",
  "T............T.T",
  "T............T.T",
  "T............T.T",
  "T............T.T",
  "TS....o.....XT.T",
  "T............T.T",
  "T............T.T",
  "T..@.........GET",
  "T............T.T",
  "TTTTTTTTTTTTTTTT"],
  emit:[{x:1,y:5,dx:1,dy:0}],
  q:{text:"How does light travel?",choices:["In a straight line until something changes its path","In a wiggly curve around objects","Only downward, like rain","It does not move at all"],a:0,
     why:"Light travels in straight lines. That is why the stone blocked the beam until you moved it."}},
 {name:"Zone 2 · Mirror Bend", std:"4-PS4-2",
  intro:"Trees block the straight path. A mirror reflects light, so the beam bounces off it in a new direction.",
  goal:"Turn both mirrors so the beam bends down and then over to the flower pot.",
  map:[
  "TTTTTTTTTTTTTTTT",
  "T.......T....T.T",
  "TS..../.T....T.T",
  "T.......T....T.T",
  "T.......T....GET",
  "T.......T....T.T",
  "T............T.T",
  "T...../.....XT.T",
  "T............T.T",
  "T..@.........T.T",
  "TTTTTTTTTTTTTTTT"],
  emit:[{x:1,y:2,dx:1,dy:0}],
  q:{text:"What happens when light hits a mirror?",choices:["The light disappears","The light reflects, bouncing off in a new direction","The light turns into sound","The light gets stuck inside the mirror"],a:1,
     why:"Mirrors reflect light. You changed the beam's direction twice by turning the mirrors."}},
 {name:"Zone 3 · See-Through Test", std:"4-PS4-2",
  intro:"The greenhouse window is broken and the owl wants to nap. Try glass, frosted glass and stone. Which lets ALL light through, SOME light, or NO light?",
  goal:"Fill the window so the plant gets full light, and make shade for the sleepy owl.",
  map:[
  "TTTTTTTTTTTTTTTT",
  "T.......T....T.T",
  "TS......w..X.T.T",
  "T.......T....T.T",
  "T.......T....T.T",
  "T.@g.f.o.....T.T",
  "T............GET",
  "T............T.T",
  "TS.........O.T.T",
  "T............T.T",
  "TTTTTTTTTTTTTTTT"],
  emit:[{x:1,y:2,dx:1,dy:0},{x:1,y:8,dx:1,dy:0}],
  needWindow:true,
  q:{text:"Frosted glass lets SOME light through. What kind of material is it?",choices:["Transparent","Opaque","Translucent","Reflective"],a:2,
     why:"Translucent materials let some light through. Transparent (clear glass) lets almost all light through. Opaque (stone) blocks light and makes a shadow."}},
 {name:"Zone 4 · Prism Rainbow", std:"4-PS4-2",
  intro:"White sunlight is really a mix of colors. A prism bends each color a different amount and splits the light apart.",
  goal:"Send each color of light to the gem that matches it: red, green and blue.",
  map:[
  "TTTTTTTTTTTTTTTT",
  "T............T.T",
  "T....\\....r..T.T",
  "T............T.T",
  "T............T.T",
  "TS...P..o..n.T.T",
  "T............T.T",
  "T............GET",
  "T..../....b..T.T",
  "T.@..........T.T",
  "TTTTTTTTTTTTTTTT"],
  emit:[{x:1,y:5,dx:1,dy:0}],
  q:{text:"When white light passes through a prism, what happens?",choices:["It turns into darkness","It splits into the colors of the rainbow","It gets hotter and melts the prism","It stops moving"],a:1,
     why:"White light is made of many colors. A prism bends each color by a different amount, so the colors spread apart into a rainbow."}},
 {name:"Zone 5 · How We See", std:"4-PS4-2",
  intro:"The villager lost her kitten! We see an object when light bounces off it and travels into our eyes. The lamp lights the kitten, but that light has to reach the villager's eyes.",
  goal:"Turn the two mirrors so light that bounces off the kitten travels into the villager's eyes.",
  map:[
  "TTTTTTTTTTTTTTTT",
  "T.S..........T.T",
  "T............T.T",
  "T............T.T",
  "T............T.T",
  "T............T.T",
  "T.K....T....VT.T",
  "T............T.T",
  "T...@........GET",
  "T./.........\\T.T",
  "TTTTTTTTTTTTTTTT"],
  emit:[{x:2,y:1,dx:0,dy:1}],
  q:{text:"How are we able to see the kitten?",choices:["Our eyes shoot out beams of light","Light reflects off the kitten and enters our eyes","The kitten makes its own light","We can see in total darkness"],a:1,
     why:"Light from a source (the lamp) hits the kitten and reflects off it. When that reflected light enters our eyes, we see the kitten."}},
 {name:"Zone 6 · Solar Lighthouse", std:"4-PS3-2",
  intro:"Light carries energy! A solar panel turns light energy into electrical energy. Get full sunlight to the panel to power the Great Lighthouse.",
  goal:"Aim the sunbeam at the solar panel at full strength.",
  map:[
  "TTTTTTTTTTTTTTTT",
  "TS......./...T.T",
  "T............THT",
  "T............T.T",
  "T........f...T.T",
  "T............T.T",
  "T...g........T.T",
  "T........L...T.T",
  "T.@..........GET",
  "T............T.T",
  "TTTTTTTTTTTTTTTT"],
  emit:[{x:1,y:1,dx:1,dy:0}],
  q:{text:"What does the solar panel show about light?",choices:["Light carries energy that can be changed into electricity","Light has no energy","Only batteries have energy","Light only makes things colder"],a:0,
     why:"Light energy traveled from the sun to the panel, and the panel changed it into electrical energy that powered the lighthouse."}}
];
const MOVABLE=new Set(['o','g','f','/','\\']);
const SOLID=new Set(['T','S','H','P','X','L','r','n','b','O','V','K','w','G','o','g','f','/','\\','W']);
function loadLevel(i){
  const L=LEVELS[i]; const grid=L.map.map(r=>r.split('')); let px=1,py=1;
  for(let y=0;y<H;y++)for(let x=0;x<W;x++){ if(grid[y][x]==='@'){px=x;py=y;grid[y][x]='.';} }
  return {i,grid,win:{}, px,py,fx:0,fy:1,held:null,open:false};
}
function trace(st){
  const L=LEVELS[st.i], g=st.grid; const segs=[]; const hits={};
  const hit=(x,y,info)=>{(hits[x+','+y]=hits[x+','+y]||[]).push(info);};
  const q=L.emit.map(e=>({x:e.x,y:e.y,dx:e.dx,dy:e.dy,c:'white',s:1,t:'direct'}));
  const seen=new Set(); let steps=0;
  while(q.length && steps<4000){
    const b=q.shift(); let {x,y,dx,dy,c,s,t}=b;
    while(steps++<4000){
      const nx=x+dx, ny=y+dy;
      const key=[nx,ny,dx,dy,c,t].join();
      if(seen.has(key)) break; seen.add(key);
      if(nx<0||ny<0||nx>=W||ny>=H){segs.push([x,y,x+dx*.5,y+dy*.5,c,s]);break;}
      const ch=g[ny][nx]; const win=st.win[nx+','+ny];
      const cell = ch==='w' ? (win?('w'+win):'w') : ch;
      const pass=()=>{segs.push([x,y,nx,ny,c,s]);x=nx;y=ny;};
      const stopAt=()=>{segs.push([x,y,nx-dx*.5,ny-dy*.5,c,s]);};
      const stopIn=()=>{segs.push([x,y,nx,ny,c,s]);};
      if(cell==='.'||cell==='E'||cell==='G'||cell==='W'||cell==='g'||cell==='w'||cell==='wg'){pass();continue;}
      if(cell==='f'||cell==='wf'){pass();s=s*0.5;continue;}
      if(cell==='/'||cell==='\\'){pass(); if(cell==='/'){const t2=dx;dx=-dy;dy=-t2;}else{const t2=dx;dx=dy;dy=t2;} continue;}
      if(cell==='P'){stopIn(); if(c==='white'){
          const lx=dy, ly=-dx, rx=-dy, ry=dx; // left & right turns
          q.push({x:nx,y:ny,dx:lx,dy:ly,c:'red',s,t},{x:nx,y:ny,dx,dy,c:'green',s,t},{x:nx,y:ny,dx:rx,dy:ry,c:'blue',s,t});
        } else q.push({x:nx,y:ny,dx,dy,c,s,t}); break;}
      if(cell==='K'){stopIn(); hit(nx,ny,{c,s,t}); for(const [ax,ay] of [[1,0],[-1,0],[0,1],[0,-1]]) if(!(ax===-dx&&ay===-dy)) q.push({x:nx,y:ny,dx:ax,dy:ay,c,s,t:'scattered'}); break;}
      if('XLrnbOV'.includes(cell)){stopIn(); hit(nx,ny,{c,s,t}); break;}
      stopAt(); break; // opaque: T S H o wo etc
    }
  }
  return {segs,hits};
}
function goals(st,tr){
  const g=st.grid, out=[]; const L=LEVELS[st.i];
  const H_=(x,y)=>tr.hits[x+','+y]||[];
  for(let y=0;y<H;y++)for(let x=0;x<W;x++){
    const ch=g[y][x], h=H_(x,y);
    if(ch==='X') out.push({k:'plant',ok:h.some(v=>v.s>=1&&v.c==='white'),dim:h.length>0, label:'Flower pot gets full sunlight'});
    if(ch==='L') out.push({k:'solar',ok:h.some(v=>v.s>=1),dim:h.length>0,label:'Solar panel gets full-strength light'});
    if('rnb'.includes(ch)){const col={r:'red',n:'green',b:'blue'}[ch]; out.push({k:'gem',ok:h.some(v=>v.c===col),dim:h.length>0,label:col[0].toUpperCase()+col.slice(1)+' gem gets '+col+' light'});}
    if(ch==='O') out.push({k:'owl',ok:h.length===0,label:'Sleepy owl is in the shade'});
    if(ch==='V') out.push({k:'eye',ok:h.some(v=>v.t==='scattered'),dim:h.length>0,label:'Light from the kitten reaches the villager\'s eyes'});
    if(ch==='w' && L.needWindow) out.push({k:'win',ok:!!st.win[x+','+y],label:'Greenhouse window is filled in'});
  }
  return out;
}
function act(st,kind){ // kind: 'grab' | 'rotate'
  const tx=st.px+st.fx, ty=st.py+st.fy; if(tx<0||ty<0||tx>=W||ty>=H) return 'none';
  const ch=st.grid[ty][tx], k=tx+','+ty;
  if(kind==='rotate'){
    if(ch==='/'){st.grid[ty][tx]='\\';return 'rot';} if(ch==='\\'){st.grid[ty][tx]='/';return 'rot';}
    return 'none';
  }
  if(!st.held){
    if(MOVABLE.has(ch)){st.held=ch; st.grid[ty][tx]='.'; return 'pick';}
    if(ch==='w'&&st.win[k]){st.held=st.win[k]; delete st.win[k]; return 'pick';}
    return 'none';
  } else {
    if(ch==='.'){st.grid[ty][tx]=st.held; st.held=null; return 'place';}
    if(ch==='w'&&!st.win[k]&&st.held!=='/'&&st.held!=='\\'){st.win[k]=st.held; st.held=null; return 'place';}
    return 'none';
  }
}
function move(st,dx,dy,force){
  if(!force && (st.fx!==dx || st.fy!==dy)){ st.fx=dx; st.fy=dy; return false; } // first press turns to face
  st.fx=dx; st.fy=dy; const nx=st.px+dx, ny=st.py+dy;
  if(nx<0||ny<0||nx>=W||ny>=H) return false;
  const ch=st.grid[ny][nx];
  if(ch==='G' && !st.open) return false;
  if(ch!=='G' && SOLID.has(ch)) return false;
  st.px=nx; st.py=ny; return true;
}


</script>
<script>
(function(){
const cv=document.getElementById('cv'), ctx=cv.getContext('2d');
const T=48; ctx.imageSmoothingEnabled=false;
// ---------- pixel sprites (16x16) ----------
function rng(seed){let s=seed>>>0;return()=>{s=(s*1664525+1013904223)>>>0;return s/4294967296;}}
function spr(fn,seed=1){const c=document.createElement('canvas');c.width=c.height=16;const x=c.getContext('2d');const r=rng(seed);fn(x,r);return c;}
const px=(x,c,X,Y,w=1,h=1)=>{x.fillStyle=c;x.fillRect(X,Y,w,h);};
function grassBase(x,r){px(x,'#5bab3f',0,0,16,16);for(let i=0;i<40;i++)px(x,r()<.5?'#4c9734':'#6cbd4c',(r()*16)|0,(r()*16)|0);}
const S={};
const GRASS=[1,2,3,4].map(s=>spr(grassBase,s*97));
S.T=spr((x,r)=>{px(x,'#2e7a2f',0,0,16,16);for(let i=0;i<70;i++)px(x,['#256a27','#3a9038','#1f5c22'][(r()*3)|0],(r()*16)|0,(r()*16)|0,2,2);px(x,'#1a4d1d',0,15,16,1);},7);
S.o=spr((x,r)=>{px(x,'#8b8d94',0,0,16,16);for(let i=0;i<30;i++)px(x,r()<.5?'#757780':'#a3a5ac',(r()*15)|0,(r()*15)|0,2,1);px(x,'#5f6168',3,5,5,1);px(x,'#5f6168',9,10,4,1);px(x,'#55575e',0,15,16,1);px(x,'#55575e',15,0,1,16);},11);
S.g=spr((x)=>{px(x,'rgba(190,235,255,.30)',0,0,16,16);px(x,'#e8fbff',0,0,16,1);px(x,'#e8fbff',0,15,16,1);px(x,'#e8fbff',0,0,1,16);px(x,'#e8fbff',15,0,1,16);px(x,'#ffffff',3,3,1,1);px(x,'#ffffff',4,4,1,1);px(x,'#ffffff',5,5,1,1);px(x,'#ffffff',10,3,1,1);px(x,'#ffffff',11,4,1,1);});
S.f=spr((x,r)=>{px(x,'rgba(232,240,246,.82)',0,0,16,16);for(let i=0;i<30;i++)px(x,'rgba(255,255,255,.9)',(r()*16)|0,(r()*16)|0);px(x,'#c9d6df',0,0,16,1);px(x,'#c9d6df',0,15,16,1);px(x,'#c9d6df',0,0,1,16);px(x,'#c9d6df',15,0,1,16);},5);
function mirror(x,dir){px(x,'#8a5a2b',1,1,14,14);px(x,'#6e4520',1,14,14,1);for(let i=0;i<14;i++){const a=dir==='/'?14-i:1+i;px(x,'#dfe7ee',1+i,a-1,1,3);px(x,'#ffffff',1+i,a,1,1);}}
S['/']=spr(x=>mirror(x,'/'));S['\\']=spr(x=>mirror(x,'\\'));
S.S=spr(x=>{px(x,'#e08a1e',0,0,16,16);px(x,'#ffc93d',1,1,14,14);px(x,'#fff1a8',4,4,8,8);px(x,'#ffffff',6,6,4,4);[[0,7],[15,7],[7,0],[7,15]].forEach(([a,b])=>px(x,'#ffe27a',a,b,1,2));});
S.P=spr(x=>{for(let i=0;i<12;i++){px(x,'rgba(220,240,255,.85)',8-i/2,2+i,i+1,1);}px(x,'#ffffff',8,2,1,1);px(x,'#ff5a5a',2,14,4,1);px(x,'#5ad16a',6,14,4,1);px(x,'#5a8cff',10,14,4,1);});
S.X0=spr(x=>{px(x,'#8a4b2a',4,9,8,6);px(x,'#a85d36',3,8,10,2);px(x,'#3d8b3a',7,4,2,5);px(x,'#3d8b3a',5,5,2,1);px(x,'#3d8b3a',9,6,2,1);});
S.X1=spr(x=>{px(x,'#8a4b2a',4,9,8,6);px(x,'#a85d36',3,8,10,2);px(x,'#3d8b3a',7,4,2,5);px(x,'#ff7ab0',5,1,6,4);px(x,'#ffd23f',7,2,2,2);px(x,'#3d8b3a',9,6,2,1);});
S.L=spr(x=>{px(x,'#c9ccd6',0,0,16,16);px(x,'#1f3a93',1,1,14,14);for(let i=1;i<15;i+=4)px(x,'#6f8fe8',i,1,1,14);for(let j=1;j<15;j+=4)px(x,'#6f8fe8',1,j,14,1);});
function gem(col,dark){return spr(x=>{px(x,'#8b8d94',2,11,12,4);px(x,'#6d6f76',2,14,12,1);px(x,dark,5,3,6,8);px(x,col,6,4,4,6);px(x,'#ffffff',6,4,1,2);});}
S.r=gem('#ff5a5a','#9c1f2a');S.n=gem('#5ad16a','#1f7a2e');S.b=gem('#5a8cff','#1f3a93');
S.O=spr(x=>{px(x,'#8a5a36',3,3,10,12);px(x,'#c49a6c',5,7,6,7);px(x,'#8a5a36',3,1,2,3);px(x,'#8a5a36',11,1,2,3);px(x,'#2b1a10',5,5,2,1);px(x,'#2b1a10',9,5,2,1);px(x,'#f0a830',7,7,2,2);});
S.V=spr(x=>{px(x,'#7a4a2a',3,1,10,4);px(x,'#c68642',3,4,10,8);px(x,'#ffffff',4,6,3,2);px(x,'#ffffff',9,6,3,2);px(x,'#4b2e1a',5,6,2,2);px(x,'#4b2e1a',10,6,2,2);px(x,'#9a5b2f',7,9,2,1);px(x,'#8e3b5c',2,12,12,4);});
S.K=spr(x=>{px(x,'#f2a14a',3,5,10,9);px(x,'#f2a14a',3,3,2,2);px(x,'#f2a14a',11,3,2,2);px(x,'#d9822f',5,11,6,1);px(x,'#3b2a10',5,8,2,2);px(x,'#3b2a10',9,8,2,2);px(x,'#e86d8c',7,10,2,1);});
S.G=spr(x=>{px(x,'#7b4f2a',1,2,2,13);px(x,'#7b4f2a',7,2,2,13);px(x,'#7b4f2a',13,2,2,13);px(x,'#9c6a3a',0,5,16,2);px(x,'#9c6a3a',0,10,16,2);});
S.Gopen=spr(x=>{px(x,'#7b4f2a',0,2,2,13);px(x,'#7b4f2a',14,2,2,13);});
S.E=spr((x,r)=>{px(x,'#2a1f4a',1,1,14,14);px(x,'#8f6bff',3,3,10,10);px(x,'#c9b6ff',5,5,6,6);px(x,'#ffffff',7,7,2,2);});
S.w=spr(x=>{px(x,'#8b8d94',0,0,16,16);px(x,'#2a3046',3,3,10,10);px(x,'#55575e',3,3,10,1);});
S.H=spr(x=>{px(x,'#e8e4da',5,2,6,14);px(x,'#c0392b',5,5,6,2);px(x,'#c0392b',5,10,6,2);px(x,'#3a3a46',4,0,8,3);px(x,'#ffd84a',6,0,4,2);});
S.W=spr((x,r)=>{px(x,'#2f6fd0',0,0,16,16);for(let i=0;i<14;i++)px(x,'#5b93e6',(r()*14)|0,(r()*16)|0,3,1);},3);
// explorer (brown eyes)
S.me=spr(x=>{px(x,'#3b2416',4,0,8,4);px(x,'#c68642',4,3,8,6);px(x,'#3b2416',4,3,1,2);px(x,'#ffffff',5,5,2,2);px(x,'#ffffff',9,5,2,2);px(x,'#4b2e1a',6,5,1,2);px(x,'#4b2e1a',9,5,1,2);px(x,'#9a5b2f',7,7,2,1);px(x,'#1e9e8c',3,9,10,4);px(x,'#c68642',2,9,1,3);px(x,'#c68642',13,9,1,3);px(x,'#3e4a89',4,13,3,3);px(x,'#3e4a89',9,13,3,3);});
const NAMES={o:'Stone (opaque)',g:'Clear glass (transparent)',f:'Frosted glass (translucent)','/':'Mirror','\\':'Mirror'};
const BEAM={white:'#fff6c8',red:'#ff5a5a',green:'#5ad16a',blue:'#6f9bff'};
// ---------- state ----------
let save={lvl:0}; try{const s=JSON.parse(localStorage.getItem('lumenBlocks')||'null'); if(s&&Number.isInteger(s.lvl)) save=s;}catch(e){}
let st=null, tr=null, solvedOnce=false, mode='title', sound=true, actx=null, tick=0;
function persist(){try{localStorage.setItem('lumenBlocks',JSON.stringify(save));}catch(e){}}
function beep(f,d=.12,type='square',v=.05){if(!sound)return;try{actx=actx||new (window.AudioContext||window.webkitAudioContext)();const o=actx.createOscillator(),g=actx.createGain();o.type=type;o.frequency.value=f;g.gain.value=v;o.connect(g);g.connect(actx.destination);const t=actx.currentTime;g.gain.exponentialRampToValueAtTime(.0001,t+d);o.start(t);o.stop(t+d);}catch(e){}}
function chord(){[523,659,784,1047].forEach((f,i)=>setTimeout(()=>beep(f,.25,'triangle',.06),i*90));}
function start(i){st=loadLevel(i);solvedOnce=false;recompute();renderSide();}
function recompute(){tr=trace(st);const gs=goals(st,tr);const all=gs.every(g=>g.ok);
  if(all&&!st.open){st.open=true;if(!solvedOnce){solvedOnce=true;chord();toast('The gate is open! Walk to the glowing beacon.');}}
  if(!all&&st.open){st.open=false; if(st.grid[st.py][st.px]==='G'){} }
  renderChecks(gs);}
let toastT=0;function toast(m){const t=document.getElementById('toast');t.textContent=m;t.hidden=false;clearTimeout(toastT);toastT=setTimeout(()=>t.hidden=true,2600);}
function renderSide(){const L=LEVELS[st.i];document.getElementById('zoneName').textContent=L.name;document.getElementById('intro').textContent=L.intro;document.getElementById('goal').textContent=L.goal;document.getElementById('std').textContent='Louisiana standard '+L.std;
  const p=document.getElementById('progress');p.innerHTML='';LEVELS.forEach((_,k)=>{const s=document.createElement('span');if(k<st.i||mode==='done')s.className='done';else if(k===st.i)s.className='now';s.title='Zone '+(k+1);p.appendChild(s);});renderHeld();}
function renderChecks(gs){const ul=document.getElementById('checks');ul.innerHTML='';gs.forEach(g=>{const li=document.createElement('li');li.className=g.ok?'ok':(g.dim?'dim':'');let extra='';if(!g.ok&&g.dim){extra=g.k==='plant'||g.k==='solar'?' (light is too dim)':g.k==='gem'?' (wrong color)':g.k==='eye'?' (needs light bounced off the kitten)':'';}li.innerHTML='<i></i><span></span>';li.querySelector('span').textContent=g.label+extra;ul.appendChild(li);});}
function renderHeld(){const c=document.getElementById('heldCv'),x=c.getContext('2d');x.clearRect(0,0,16,16);x.imageSmoothingEnabled=false;document.getElementById('heldName').textContent=st.held?NAMES[st.held]:'Nothing yet';if(st.held)x.drawImage(S[st.held],0,0);}
// ---------- drawing ----------
function draw(){tick++;ctx.imageSmoothingEnabled=false;
  for(let y=0;y<11;y++)for(let x=0;x<16;x++){ctx.drawImage(GRASS[(x*7+y*13)%4],x*T,y*T,T,T);}
  for(let y=0;y<11;y++)for(let x=0;x<16;x++){const ch=st.grid[y][x];let s=null;
    if(ch==='X'){const h=tr.hits[x+','+y]||[];s=h.some(v=>v.s>=1)?S.X1:S.X0;}
    else if(ch==='G') s=st.open?S.Gopen:S.G;
    else if(ch!=='.') s=S[ch];
    if(s)ctx.drawImage(s,x*T,y*T,T,T);
    if(ch==='w'){const it=st.win[x+','+y];if(it)ctx.drawImage(S[it],x*T+T*.19,y*T+T*.19,T*.62,T*.62);}
    if(ch==='O'&&(tr.hits[x+','+y]||[]).length){ctx.fillStyle='#fff';ctx.font='bold '+(T*.3)+'px sans-serif';ctx.fillText('!',x*T+T*.78,y*T+T*.3);}
    if(ch==='O'&&!(tr.hits[x+','+y]||[]).length){ctx.fillStyle='#dfe7ff';ctx.font=(T*.25)+'px Silkscreen, monospace';ctx.fillText('z',x*T+T*.75,y*T+T*.28-(tick/8%6));}
    if(ch==='L'&&st.open){ctx.fillStyle='rgba(255,230,120,'+(.25+.15*Math.sin(tick/6))+')';ctx.fillRect(x*T,y*T,T,T);}
    if(ch==='E'&&st.open){ctx.fillStyle='rgba(200,180,255,'+(.25+.2*Math.sin(tick/7))+')';ctx.fillRect(x*T-2,y*T-2,T+4,T+4);}
  }
  // beams
  ctx.lineCap='butt';
  for(const [x1,y1,x2,y2,c,s] of tr.segs){const a=(x1+.5)*T,b=(y1+.5)*T,cc=(x2+.5)*T,d=(y2+.5)*T;
    ctx.globalAlpha=(s>=1?.35:.18)*(0.85+0.15*Math.sin(tick/5));ctx.strokeStyle=BEAM[c];ctx.lineWidth=T*(s>=1?.42:.26);ctx.beginPath();ctx.moveTo(a,b);ctx.lineTo(cc,d);ctx.stroke();
    ctx.globalAlpha=s>=1?.95:.55;ctx.lineWidth=T*(s>=1?.12:.07);ctx.beginPath();ctx.moveTo(a,b);ctx.lineTo(cc,d);ctx.stroke();ctx.globalAlpha=1;}
  // draw characters and sensors on top of the beams so they stay visible
  for(let y=0;y<11;y++)for(let x=0;x<16;x++){const ch=st.grid[y][x];if('KVOrnbL'.includes(ch))ctx.drawImage(S[ch],x*T,y*T,T,T);if(ch==='X'){const h=tr.hits[x+','+y]||[];ctx.drawImage(h.some(v=>v.s>=1)?S.X1:S.X0,x*T,y*T,T,T);}}
  // lighthouse glow zone 6
  if(st.i===5&&st.open){ctx.save();ctx.globalAlpha=.35+.15*Math.sin(tick/8);ctx.fillStyle='#fff3a0';ctx.beginPath();ctx.moveTo(14.5*T,2.1*T);ctx.lineTo(16*T,1*T);ctx.lineTo(16*T,3.4*T);ctx.closePath();ctx.fill();ctx.restore();}
  // explorer + facing outline
  const fx=st.px+st.fx, fy=st.py+st.fy;
  ctx.strokeStyle='#ffd23f';ctx.lineWidth=3;ctx.strokeRect(fx*T+2,fy*T+2,T-4,T-4);
  ctx.drawImage(S.me,st.px*T,st.py*T,T,T);
  if(st.held){ctx.drawImage(S[st.held],st.px*T+T*.55,st.py*T-T*.15,T*.45,T*.45);}
  if(mode==='play')requestAnimationFrame(draw);
}
// ---------- modals ----------
const ov=document.getElementById('overlay'), md=document.getElementById('modal');
function modal(html){md.innerHTML=html;ov.hidden=false;const b=md.querySelector('button');if(b)b.focus();}
function close(){ov.hidden=true;}
function titleScreen(){mode='title';modal(`<h2>The Great Lighthouse has gone dark</h2>
 <p>The block world needs a light scientist. Explore 6 zones. In each one, aim, bend, block and split beams of light to solve the puzzle. Then answer a science question at the glowing beacon.</p>
 <p>Finish every zone to light the lighthouse and earn your secret code.</p>
 <p class="keys">Press an arrow key (or WASD) once to turn and face a block, and again to walk. Press <kbd>E</kbd> to grab or place a block and <kbd>R</kbd> to turn a mirror. On a tablet, use the buttons under the map.</p>
 <button class="primary" id="go">${save.lvl>0?'CONTINUE · ZONE '+(save.lvl+1):'START EXPLORING'}</button>${save.lvl>0?'<button id="fresh">START OVER FROM ZONE 1</button>':''}`);
 document.getElementById('go').onclick=()=>{close();mode='play';start(save.lvl);requestAnimationFrame(draw);beep(660);};
 const f=document.getElementById('fresh'); if(f) f.onclick=()=>{save.lvl=0;persist();close();mode='play';start(0);requestAnimationFrame(draw);};
}
function quiz(){mode='quiz';const L=LEVELS[st.i],q=L.q;
 modal(`<h2>Beacon question · ${L.name.split('·')[0].trim()}</h2><p>${q.text}</p><div class="choices">${q.choices.map((c,k)=>`<button data-k="${k}">${c}</button>`).join('')}</div><p id="fb" aria-live="polite"></p>`);
 md.querySelectorAll('.choices button').forEach(b=>b.onclick=()=>{const k=+b.dataset.k;const fb=document.getElementById('fb');
   if(k===q.a){b.classList.add('right');beep(880,.15,'triangle');fb.innerHTML='<b>Correct!</b> '+q.why;md.querySelectorAll('.choices button').forEach(x=>x.disabled=true);
     const n=document.createElement('button');n.className='primary';n.textContent=st.i<LEVELS.length-1?'NEXT ZONE':'LIGHT THE LIGHTHOUSE';n.onclick=next;md.appendChild(n);n.focus();}
   else{b.classList.add('wrong');b.disabled=true;md.classList.remove('shake');void md.offsetWidth;md.classList.add('shake');beep(180,.2,'sawtooth',.04);fb.textContent='Not quite. Think about what you saw the light do in this zone, then try again.';}});
}
function next(){close();if(st.i<LEVELS.length-1){save.lvl=st.i+1;persist();mode='play';start(save.lvl);requestAnimationFrame(draw);}else finish();}
function finish(){mode='done';save.lvl=LEVELS.length-1;persist();renderSide();draw();
 const code=String.fromCharCode(76,105,103,104,116,50,54);
 modal(`<h2>The Great Lighthouse shines again!</h2><p>You bent light with mirrors, tested transparent, translucent and opaque blocks, split white light with a prism, showed how we see, and turned light energy into electricity.</p><p>Your completion code:</p><div class="code" id="code">${code}</div><button class="primary" id="cp">COPY CODE</button><p id="cpm" aria-live="polite"></p><button id="again">PLAY AGAIN</button>`);
 chord();
 document.getElementById('cp').onclick=()=>{const m=document.getElementById('cpm');navigator.clipboard.writeText(code).then(()=>m.textContent='Copied! Type it where your teacher asked.').catch(()=>{const r=document.createRange();r.selectNodeContents(document.getElementById('code'));const s=getSelection();s.removeAllRanges();s.addRange(r);m.textContent='Code selected. Copy it or write it down.';});};
 document.getElementById('again').onclick=()=>{save.lvl=0;persist();close();mode='play';start(0);requestAnimationFrame(draw);};
}
// ---------- input ----------
function doMove(dx,dy,force){if(mode!=='play')return;const turned=!force&&(st.fx!==dx||st.fy!==dy);const moved=move(st,dx,dy,force);if(turned){recompute();return;}if(moved){beep(220,.04,'square',.02);}else{const c=(st.grid[st.py+dy]||[])[st.px+dx];if(c==='G')toast('The gate stays locked until every light check is green.');}
  if(st.grid[st.py][st.px]==='E'&&st.open){quiz();}
  recompute();}
function doAct(k){if(mode!=='play')return;const r=act(st,k);
  if(r==='none'){toast(k==='rotate'?'Face a mirror to turn it.':st.held?'You can place blocks on grass or in an empty window frame.':'Face a stone, glass, frosted glass or mirror to pick it up.');beep(120,.08,'square',.03);}
  else beep(r==='rot'?520:r==='pick'?440:330,.08);
  renderHeld();recompute();}
addEventListener('keydown',e=>{if(mode!=='play')return;const k=e.key.toLowerCase();
  const m={arrowup:[0,-1],w:[0,-1],arrowdown:[0,1],s:[0,1],arrowleft:[-1,0],a:[-1,0],arrowright:[1,0],d:[1,0]}[k];
  if(m){e.preventDefault();doMove(...m);}else if(k==='e'||k===' '){e.preventDefault();doAct('grab');}else if(k==='r'){e.preventDefault();doAct('rotate');}});
const hold=(id,fn)=>{const b=document.getElementById(id);let t=null;b.addEventListener('pointerdown',e=>{e.preventDefault();fn();t=setInterval(fn,220);});['pointerup','pointerleave','pointercancel'].forEach(ev=>b.addEventListener(ev,()=>clearInterval(t)));};
hold('bUp',()=>doMove(0,-1));hold('bDown',()=>doMove(0,1));hold('bLeft',()=>doMove(-1,0));hold('bRight',()=>doMove(1,0));
document.getElementById('bGrab').onclick=()=>doAct('grab');document.getElementById('bRot').onclick=()=>doAct('rotate');
const HINTS=[
 "Walk next to the gray stone and face it (yellow outline). Press E to pick it up. Turn to face an empty grass block outside the beam and press E to set it down.",
 "Face the top mirror and press R once so it slants like \\ . The beam bends down. Then face the bottom mirror and press R once so it also slants like \\ . The beam bends right to the flower pot.",
 "Pick up the clear glass and place it in the empty window frame so the plant gets full light. Then pick up the stone, stand just above or below the bottom beam, press the arrow once to face the beam, and press E to set the stone down in it. Frosted glass would still let some light reach the owl, so it has to be the stone.",
 "Turn the top mirror so the red beam goes right to the red gem. Move the stone out of the green beam. Turn the bottom mirror so the blue beam goes right to the blue gem.",
 "Light bounces off the kitten in every direction, including down. Turn the mirror below the kitten so the light goes right along the bottom row. Then turn the mirror in the bottom-right corner, under the villager, so the light goes up into her eyes.",
 "Turn the top mirror so the sunbeam goes down. Take the frosted glass out of the beam so the solar panel gets full-strength light."];
document.getElementById('bHint').onclick=()=>{if(mode!=='play')return;mode='hint';modal('<h2>Hint · '+LEVELS[st.i].name.split('·')[0].trim()+'</h2><p>'+HINTS[st.i]+'</p><button class="primary" id="hk">BACK TO THE GAME</button>');document.getElementById('hk').onclick=()=>{close();mode='play';requestAnimationFrame(draw);};};
document.getElementById('bReset').onclick=()=>{if(mode==='play'){start(st.i);toast('Zone restarted.');}};
document.getElementById('bSound').onclick=e=>{sound=!sound;e.target.textContent=sound?'SOUND ON':'SOUND OFF';e.target.setAttribute('aria-pressed',sound);};
// tap on board: move toward tapped tile one step
cv.addEventListener('pointerdown',e=>{if(mode!=='play')return;e.preventDefault();const r=cv.getBoundingClientRect();const x=Math.floor((e.clientX-r.left)/r.width*16),y=Math.floor((e.clientY-r.top)/r.height*11);const dx=x-st.px,dy=y-st.py;
  if(!dx&&!dy)return;
  if(Math.abs(dx)+Math.abs(dy)===1){const c=st.grid[y][x];
    if(dx!==st.fx||dy!==st.fy){st.fx=dx;st.fy=dy;return;}
    const walkable=c==='.'||c==='E'||(c==='G'&&st.open);
    if(c==='.'&&st.held){doAct('grab');return;}
    if(walkable){doMove(dx,dy,true);return;}
    doAct(!st.held&&(c==='/'||c==='\\')?'rotate':'grab');
    return;}
  if(Math.abs(dx)>=Math.abs(dy))doMove(Math.sign(dx),0,true);else doMove(0,Math.sign(dy),true);});
// boot
start(Math.min(save.lvl,LEVELS.length-1));draw();titleScreen();
})();
</script>

</body>
</html>

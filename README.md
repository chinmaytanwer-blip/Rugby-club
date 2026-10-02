<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Mewar Warriors RFC</title>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@600;700;800&family=Barlow:wght@400;500;600&display=swap" rel="stylesheet">
<style>
:root{--bg:#05070d;--navy:#0a1226;--card:#0d1630;--line:#1c2850;--gold:#f5b800;--gold2:#ffd54a;--text:#fff;--mute:#a9b2c9;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
html{scroll-behavior:smooth;scroll-padding-top:80px}
*,*:before,*:after{box-sizing:inherit;margin:0}
body{background:var(--bg);color:var(--text);font:400 16px/1.6 Barlow,system-ui,sans-serif;overflow-x:hidden}
h1,h2,h3,.cond{font-family:'Barlow Condensed','Arial Narrow',Impact,sans-serif;text-transform:uppercase;letter-spacing:.02em;line-height:1}
a{color:inherit;text-decoration:none}
.gold{color:var(--gold)}
.wrap{max-width:1280px;margin:0 auto;padding:0 24px}
section{padding:96px 0}
a:focus-visible,button:focus-visible{outline:2px solid var(--gold);outline-offset:3px}
/* nav */
header{position:sticky;top:env(safe-area-inset-top,0px);z-index:50;background:rgba(5,7,13,.88);backdrop-filter:blur(12px);border-bottom:1px solid var(--line)}
.nav{display:flex;align-items:center;justify-content:space-between;height:72px;gap:16px}
.logo{display:flex;align-items:center;gap:12px;font:800 20px 'Barlow Condensed',sans-serif;letter-spacing:.08em;white-space:nowrap}
.diamond{width:26px;height:26px;background:var(--gold);transform:rotate(45deg);display:grid;place-items:center;border-radius:3px}
.diamond:after{content:"";width:10px;height:10px;background:var(--bg);border-radius:1px}
nav ul{display:flex;gap:28px;list-style:none;padding:0}
nav a{font:700 15px 'Barlow Condensed',sans-serif;letter-spacing:.12em;color:#dfe5f5;transition:color .25s}
nav a:hover{color:var(--gold)}
.btn{display:inline-block;padding:14px 28px;font:800 16px 'Barlow Condensed',sans-serif;letter-spacing:.12em;text-transform:uppercase;border:2px solid var(--gold);background:var(--gold);color:#0a0a0a;cursor:pointer;transition:all .3s ease}
.btn:hover{background:transparent;color:var(--gold);box-shadow:0 0 28px rgba(245,184,0,.35)}
.btn.out{background:transparent;color:#fff;border-color:rgba(255,255,255,.4)}
.btn.out:hover{border-color:var(--gold);color:var(--gold);background:rgba(245,184,0,.08)}
.btn.sm{padding:10px 20px;font-size:14px}
.burger{display:none;background:none;border:1px solid var(--line);color:#fff;padding:8px 12px;font:700 14px 'Barlow Condensed';letter-spacing:.1em;cursor:pointer}
/* hero */
.hero{position:relative;min-height:calc(100vh - 72px);display:flex;flex-direction:column;justify-content:space-between;text-align:center;padding:90px 0 40px;overflow:hidden;background:radial-gradient(ellipse at 50% 30%,#14234d 0%,#070b17 55%,#03040a 100%)}
.hero svg.bg{position:absolute;inset:0;width:100%;height:100%;opacity:.55}
.hero:after{content:"";position:absolute;inset:0;background:linear-gradient(180deg,rgba(5,7,13,.2),rgba(5,7,13,.85))}
.hero>*{position:relative;z-index:2}
.est{font:700 15px 'Barlow Condensed';letter-spacing:.35em;color:var(--gold);margin-bottom:20px;text-transform:uppercase}
.hero h1{font-size:clamp(52px,10vw,140px);font-weight:800;line-height:.92}
.hero h1 span{display:block}
.tag{font:700 clamp(18px,2.4vw,26px) 'Barlow Condensed';letter-spacing:.4em;margin:26px 0 34px;text-transform:uppercase}
.cta{display:flex;gap:14px;justify-content:center;flex-wrap:wrap}
.next{margin:64px auto 0;width:min(760px,100%);padding:22px 28px;background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.18);backdrop-filter:blur(16px);border-radius:6px;display:flex;align-items:center;justify-content:space-between;gap:24px;flex-wrap:wrap}
.next .lbl{font:700 13px 'Barlow Condensed';letter-spacing:.25em;color:var(--gold);text-align:left}
.next .vs{font:800 26px 'Barlow Condensed';text-transform:uppercase;text-align:left}
.cd{display:flex;gap:14px}
.cd div{text-align:center;min-width:58px}
.cd b{display:block;font:800 40px 'Barlow Condensed';color:#fff}
.cd small{font:600 11px 'Barlow Condensed';letter-spacing:.2em;color:var(--mute)}
/* headers */
.sh{margin-bottom:48px}
.sh h2{font-size:clamp(34px,5vw,60px);font-weight:800}
.sh p{color:var(--mute);margin-top:12px;max-width:560px}
.sh.c{text-align:center}.sh.c p{margin-inline:auto}
/* news */
.news{display:grid;grid-template-columns:repeat(4,1fr);gap:20px}
.nc{background:var(--card);border:1px solid var(--line);display:flex;flex-direction:column;transition:transform .3s,border-color .3s}
.nc:hover{transform:translateY(-6px);border-color:var(--gold)}
.nc .img{aspect-ratio:4/3;position:relative}
.nc .cat{position:absolute;left:12px;top:12px;padding:4px 10px;font:800 12px 'Barlow Condensed';letter-spacing:.14em;text-transform:uppercase;color:#05070d}
.nc .b{padding:18px;display:flex;flex-direction:column;gap:10px;flex:1}
.nc time{font-size:13px;color:var(--mute)}
.nc h3{font-size:24px;font-weight:700;line-height:1.05}
.nc p{font-size:14.5px;color:var(--mute);flex:1}
.more{font:800 14px 'Barlow Condensed';letter-spacing:.14em;color:var(--gold);transition:letter-spacing .3s,color .3s}
.more:hover{letter-spacing:.24em;color:var(--gold2)}
/* teams */
.teams{background:var(--navy)}
.tabs{display:flex;justify-content:center;gap:10px;flex-wrap:wrap;margin-bottom:48px}
.tab{padding:12px 24px;background:transparent;border:1px solid var(--line);color:#dfe5f5;font:800 16px 'Barlow Condensed';letter-spacing:.14em;cursor:pointer;transition:all .3s}
.tab:hover{border-color:var(--gold);color:var(--gold)}
.tab.on{background:var(--gold);border-color:var(--gold);color:#05070d}
.roster{display:grid;grid-template-columns:repeat(4,1fr);gap:20px;align-items:start}
.pc{position:relative;height:440px;overflow:hidden;border:1px solid var(--line);transition:border-color .3s,transform .3s}
.pc:nth-child(even){margin-top:36px}
.pc:hover{border-color:var(--gold);transform:translateY(-4px)}
.pc svg{position:absolute;inset:0;width:100%;height:100%}
.pc .no{position:absolute;right:16px;top:8px;font:800 64px 'Barlow Condensed';color:var(--gold);opacity:.95}
.pc .info{position:absolute;left:0;right:0;bottom:0;padding:60px 18px 18px;background:linear-gradient(0deg,#03040a 20%,transparent)}
.pc .pos{font:700 13px 'Barlow Condensed';letter-spacing:.2em;color:var(--gold)}
.pc h3{font-size:30px;font-weight:800;margin:4px 0 10px}
.pc .st{display:flex;gap:18px;font:700 14px 'Barlow Condensed';letter-spacing:.1em;color:#dfe5f5}
/* about */
.mv{display:grid;grid-template-columns:1fr 1fr;gap:20px;position:relative}
.mv .box{background:var(--card);border:1px solid var(--line);padding:44px 36px}
.mv h3{font-size:34px;color:var(--gold);margin-bottom:14px}
.mv p{color:var(--mute)}
.badge{position:absolute;left:50%;bottom:-54px;transform:translateX(-50%);background:var(--gold);color:#05070d;padding:14px 26px;text-align:center;z-index:3;box-shadow:0 14px 40px rgba(0,0,0,.6)}
.badge b{font:800 48px/1 'Barlow Condensed';display:block}
.badge span{font:800 13px 'Barlow Condensed';letter-spacing:.16em;text-transform:uppercase}
.aimg{margin-top:20px;height:260px;border:1px solid var(--line);position:relative;overflow:hidden}
.aimg svg{width:100%;height:100%}
.vals{display:grid;grid-template-columns:repeat(4,1fr);gap:20px;margin-top:96px}
.vc{padding:34px 26px;background:var(--card);border:1px solid var(--line);transition:border-color .3s,transform .3s}
.vc:hover{border-color:var(--gold);transform:translateY(-4px)}
.vc svg{width:44px;height:44px;stroke:var(--gold);fill:none;stroke-width:1.6;stroke-linecap:round;stroke-linejoin:round;margin-bottom:18px}
.vc h3{font-size:28px;font-weight:800;margin-bottom:8px}
.vc p{color:var(--mute);font-size:15px}
.staff{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;margin-top:20px}
.sc{display:flex;gap:18px;align-items:center;padding:20px;background:var(--card);border:1px solid var(--line)}
.sc i{width:64px;height:64px;flex:none;background:linear-gradient(135deg,var(--gold),#7a5a00);clip-path:polygon(50% 0,100% 50%,50% 100%,0 50%)}
.sc h3{font-size:24px;font-weight:700}.sc span{color:var(--mute);font-size:14px}
/* fixture + gallery */
.fx{display:flex;align-items:center;justify-content:space-between;gap:24px;flex-wrap:wrap;padding:34px 40px;background:linear-gradient(90deg,#0d1a3d,#05070d);border:1px solid var(--line);border-left:6px solid var(--gold)}
.fx .when{font:700 14px 'Barlow Condensed';letter-spacing:.22em;color:var(--gold)}
.fx h3{font-size:clamp(28px,4vw,46px);font-weight:800;margin-top:6px}
.fx p{color:var(--mute)}
.grid{display:grid;grid-template-columns:repeat(4,1fr);grid-auto-rows:170px;gap:10px;grid-auto-flow:dense}
.g{position:relative;overflow:hidden;border:1px solid var(--line);transition:border-color .3s}
.g:hover{border-color:var(--gold)}
.g svg{width:100%;height:100%;transition:transform .6s}
.g:hover svg{transform:scale(1.08)}
.g span{position:absolute;left:12px;bottom:10px;font:700 13px 'Barlow Condensed';letter-spacing:.16em;text-transform:uppercase}
.w2{grid-column:span 2}.h2{grid-row:span 2}
footer{border-top:1px solid var(--line);padding:40px 0;color:var(--mute);font-size:14px}
footer .wrap{display:flex;justify-content:space-between;gap:16px;flex-wrap:wrap;align-items:center}
@media(max-width:1100px){nav ul{gap:16px}.news,.roster,.vals{grid-template-columns:repeat(2,1fr)}.nav .btn{display:none}}
@media(max-width:860px){
 .burger{display:block}
 nav{position:absolute;left:0;right:0;top:72px;background:var(--bg);border-bottom:1px solid var(--line);display:none}
 nav.open{display:block}
 nav ul{flex-direction:column;padding:12px 24px 24px;gap:14px}
 .mv,.staff{grid-template-columns:1fr}
 .grid{grid-template-columns:repeat(2,1fr)}
 .badge{position:static;transform:none;margin-top:20px;display:inline-block}
 .vals{margin-top:48px}
 section{padding:64px 0}
}
@media(max-width:560px){.news,.roster,.vals{grid-template-columns:1fr}.pc:nth-child(even){margin-top:0}.cd b{font-size:32px}.cd div{min-width:46px}}
@media(prefers-reduced-motion:reduce){*{transition:none!important}html{scroll-behavior:auto}}
</style>
</head>
<body>
<header><div class="wrap nav">
 <a href="#home" class="logo"><span class="diamond"></span>MEWAR WARRIORS RFC</a>
 <nav id="nav"><ul>
  <li><a href="#home">HOME</a></li><li><a href="#about">ABOUT</a></li><li><a href="#teams">TEAMS</a></li><li><a href="#fixtures">FIXTURES</a></li><li><a href="#gallery">GALLERY</a></li><li><a href="#join">JOIN US</a></li><li><a href="#shop">SHOP</a></li><li><a href="#contact">CONTACT</a></li>
 </ul></nav>
 <a href="#join" class="btn sm">JOIN NOW</a>
 <button class="burger" id="burger" aria-label="Menu">MENU</button>
</div></header>
 
<main>
<section class="hero" id="home" style="padding-top:90px">
 <svg class="bg" viewBox="0 0 1200 700" preserveAspectRatio="xMidYMax slice" aria-hidden="true">
  <defs><linearGradient id="fl" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#fff" stop-opacity=".25"/><stop offset="1" stop-color="#fff" stop-opacity="0"/></linearGradient></defs>
  <polygon points="300,0 380,0 520,700 140,700" fill="url(#fl)"/><polygon points="820,0 900,0 1060,700 680,700" fill="url(#fl)"/>
  <g fill="#02030a">
   <circle cx="260" cy="470" r="22"/><path d="M215 700 L225 520 Q260 490 300 520 L315 700Z"/>
   <circle cx="470" cy="440" r="24"/><path d="M420 700 L432 500 Q470 465 512 500 L528 700Z"/>
   <circle cx="720" cy="450" r="24"/><path d="M670 700 L682 510 Q720 475 762 510 L778 700Z"/>
   <circle cx="940" cy="480" r="22"/><path d="M895 700 L905 530 Q940 500 980 530 L995 700Z"/>
   <ellipse cx="600" cy="560" rx="22" ry="13" transform="rotate(-20 600 560)" fill="#14234d"/>
  </g>
 </svg>
 <div>
  <p class="est">EST. 2011 • UDAIPUR, RAJASTHAN</p>
  <h1><span>MEWAR</span><span class="gold">WARRIORS</span><span style="font-size:.38em;letter-spacing:.12em;margin-top:14px">RUGBY FOOTBALL CLUB</span></h1>
  <p class="tag">STRENGTH. HONOR. VICTORY.</p>
  <div class="cta"><a class="btn" href="#join">JOIN THE CLUB</a><a class="btn out" href="#join">REGISTER →</a><a class="btn out" href="#fixtures">VIEW FIXTURES</a></div>
 </div>
 <div class="wrap" style="width:100%">
  <div class="next">
   <div><div class="lbl">NEXT MATCH</div><div class="vs">Mewar Warriors <span class="gold">vs</span> Jaipur Royals RFC</div></div>
   <div class="cd" id="cd" aria-live="off"><div><b id="d">00</b><small>DAYS</small></div><div><b id="h">00</b><small>HOURS</small></div><div><b id="m">00</b><small>MINS</small></div><div><b id="s">00</b><small>SECS</small></div></div>
  </div>
 </div>
</section>
 
<section id="news"><div class="wrap">
 <div class="sh"><h2>THE PRIDE — <span class="gold">LATEST NEWS</span></h2><p>Roars from the Warrior camp — match reports, signings, and stories from the pride.</p></div>
 <div class="news" id="newsGrid"></div>
</div></section>
 
<section class="teams" id="teams"><div class="wrap">
 <div class="sh c"><h2>THE <span class="gold">SQUAD</span></h2></div>
 <div class="tabs" id="tabs" role="tablist"></div>
 <div class="roster" id="roster"></div>
</div></section>
 
<section id="about"><div class="wrap">
 <div class="mv">
  <div class="box"><h3>MISSION</h3><p>To forge disciplined, resilient athletes and good people in the heart of Mewar — giving every child, woman and man in Rajasthan a place to play hard and play fair.</p></div>
  <div class="box"><h3>VISION</h3><p>To be India's most respected rugby club: a champion on the field, a pathway for young talent, and a source of pride for Udaipur.</p></div>
  <div class="badge"><b>14</b><span>Years of building warriors</span></div>
 </div>
 <div class="aimg"><svg viewBox="0 0 1200 260" preserveAspectRatio="xMidYMid slice"><defs><linearGradient id="ab" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#14234d"/><stop offset="1" stop-color="#05070d"/></linearGradient></defs><rect width="1200" height="260" fill="url(#ab)"/><g fill="#03040a"><circle cx="300" cy="120" r="20"/><path d="M265 260 L275 150 Q300 130 328 150 L340 260Z"/><circle cx="520" cy="110" r="22"/><path d="M482 260 L492 140 Q520 120 550 140 L562 260Z"/><circle cx="760" cy="120" r="20"/><path d="M725 260 L735 150 Q760 130 788 150 L800 260Z"/><circle cx="950" cy="130" r="18"/><path d="M918 260 L926 160 Q950 142 975 160 L985 260Z"/></g><path d="M0 230 H1200" stroke="#f5b800" stroke-opacity=".5"/></svg></div>
 
 <div class="sh" style="margin-top:96px"><h2>THE WARRIOR CODE — <span class="gold">CORE VALUES</span></h2></div>
 <div class="vals" style="margin-top:0">
  <div class="vc"><svg viewBox="0 0 48 48"><path d="M8 20h6v8H8zM34 20h6v8h-6zM14 24h20M17 16v16M31 16v16"/></svg><h3>STRENGTH</h3><p>Built in the off-season, proven in the final minute. We train for the game and for the grind.</p></div>
  <div class="vc"><svg viewBox="0 0 48 48"><path d="M24 5l16 6v12c0 10-7 17-16 20C15 40 8 33 8 23V11z"/><path d="M17 24l5 5 9-10"/></svg><h3>HONOR</h3><p>We respect the referee, the opponent and the jersey. How we play matters as much as the score.</p></div>
  <div class="vc"><svg viewBox="0 0 48 48"><path d="M15 6h18v10a9 9 0 01-18 0zM15 9H8v3a7 7 0 007 7M33 9h7v3a7 7 0 01-7 7M24 25v8M16 42h16M19 33h10"/></svg><h3>VICTORY</h3><p>We play to win — and to get better every week, whatever the scoreboard says.</p></div>
  <div class="vc"><svg viewBox="0 0 48 48"><circle cx="16" cy="16" r="6"/><circle cx="32" cy="16" r="6"/><path d="M4 40c0-7 5-12 12-12s12 5 12 12M20 40c0-7 5-12 12-12s12 5 12 12"/></svg><h3>BROTHERHOOD</h3><p>On the pitch we carry each other. Off it, the club is family — all genders, all ages.</p></div>
 </div>
 
 <div class="sh" style="margin:96px 0 0"><h2>GENERALS OF THE PRIDE — <span class="gold">COACHING STAFF</span></h2></div>
 <div class="staff">
  <div class="sc"><i></i><div><h3>Vikram Rathore</h3><span>Head Coach</span></div></div>
  <div class="sc"><i></i><div><h3>Anita Sisodia</h3><span>Women's Team Coach</span></div></div>
  <div class="sc"><i></i><div><h3>Dev Chauhan</h3><span>Strength &amp; Conditioning</span></div></div>
 </div>
</div></section>
 
<section id="fixtures" style="padding-top:0"><div class="wrap">
 <div class="fx">
  <div><div class="when">SAT 07 NOV 2026 • 4:00 PM IST • HOME</div><h3>Mewar Warriors <span class="gold">vs</span> Mumbai Marines</h3><p>Udaipur Sports Ground, Gate 2 opens at 2:30 PM</p></div>
  <a class="btn" href="#contact">GET TICKETS</a>
 </div>
</div></section>
 
<section id="gallery" style="padding-top:40px"><div class="wrap">
 <div class="sh"><h2>MOMENTS — <span class="gold">GALLERY</span></h2><p>Frozen frames of glory, grit, and Warrior spirit.</p></div>
 <div class="grid" id="gal"></div>
</div></section>
</main>
 
<footer id="contact"><div class="wrap"><div class="logo"><span class="diamond"></span>MEWAR WARRIORS RFC</div><div id="join">Udaipur, Rajasthan • info@mewarwarriors.example</div><div id="shop">© 2026 Mewar Warriors RFC</div></div></footer>
 
<script>
// countdown
const target=new Date('2026-10-24T16:00:00+05:30').getTime();
const pad=n=>String(n).padStart(2,'0');
function tick(){let t=Math.max(0,target-Date.now())/1000;
 d.textContent=pad(Math.floor(t/86400));h.textContent=pad(Math.floor(t/3600)%24);m.textContent=pad(Math.floor(t/60)%60);s.textContent=pad(Math.floor(t%60));}
tick();setInterval(tick,1000);
burger.onclick=()=>nav.classList.toggle('open');
nav.onclick=e=>{if(e.target.tagName==='A')nav.classList.remove('open')};
 
// scene art (inline SVG, no remote images)
const hues=[['#14234d','#05070d'],['#3a2a05','#05070d'],['#0f2a3d','#05070d'],['#2a1030','#05070d']];
function scene(i,kind){const[a,b]=hues[i%4];
 return `<svg viewBox="0 0 300 400" preserveAspectRatio="xMidYMid slice"><defs><linearGradient id="s${kind}${i}" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="${a}"/><stop offset="1" stop-color="${b}"/></linearGradient></defs><rect width="300" height="400" fill="url(#s${kind}${i})"/><circle cx="${90+i*40%120}" cy="90" r="60" fill="#f5b800" opacity=".08"/><g fill="#02030a"><circle cx="150" cy="${150+i%3*10}" r="26"/><path d="M95 400 L105 215 Q150 185 195 215 L208 400Z"/></g><ellipse cx="${210-i*12%60}" cy="${300+i%2*20}" rx="20" ry="12" transform="rotate(-25 210 300)" fill="#f5b800" opacity=".55"/></svg>`}
 
// news
const news=[
 ['Match Report','#f5b800','28 Sep 2026','Warriors Edge Thriller in Final Minute','A last-gasp try seals a 24–21 win over Delhi Dragons at home.'],
 ['Club News','#4fc3f7','24 Sep 2026','New Clubhouse Floodlights Switched On','Night training begins this week for all senior squads.'],
 ['Academy','#7bd88f','19 Sep 2026','Junior Academy Opens Autumn Intake','Boys and girls aged 8–14 can now register for weekend sessions.'],
 ['Signing','#ff7a59','12 Sep 2026','Captain Signs Three-Year Extension','Prop Arjun Singh commits his future to the pride until 2029.']];
newsGrid.innerHTML=news.map((n,i)=>`<article class="nc"><div class="img">${scene(i,'n')}<span class="cat" style="background:${n[1]}">${n[0]}</span></div><div class="b"><time>${n[2]}</time><h3>${n[3]}</h3><p>${n[4]}</p><a class="more" href="#news">READ MORE &gt;</a></div></article>`).join('');
 
// roster
const R={
 "MEN'S TEAM":[['LOOSEHEAD PROP','Arjun Singh',1,'6 TRIES','28 APPS'],['HOOKER','Rohan Rathore',2,'9 TRIES','26 APPS'],['FLY-HALF','Karan Mehta',10,'142 PTS','24 APPS'],['WINGER','Dev Chauhan',14,'14 TRIES','28 APPS']],
 "WOMEN'S TEAM":[['CAPTAIN · CENTRE','Meera Sisodia',12,'11 TRIES','22 APPS'],['SCRUM-HALF','Anika Joshi',9,'7 TRIES','20 APPS'],['FLANKER','Priya Rawat',7,'8 TRIES','21 APPS'],['FULLBACK','Tara Bhati',15,'12 TRIES','22 APPS']],
 "UNDER-18":[['NUMBER 8','Aarav Jain',8,'10 TRIES','18 APPS'],['WINGER','Ishaan Kumawat',11,'13 TRIES','17 APPS'],['LOCK','Veer Solanki',5,'3 TRIES','16 APPS'],['FLY-HALF','Yash Gehlot',10,'88 PTS','18 APPS']],
 "JUNIOR ACADEMY":[['ACADEMY · BACKS','Rudra Meena',9,'5 TRIES','12 APPS'],['ACADEMY · FORWARDS','Kabir Paliwal',6,'4 TRIES','12 APPS'],['ACADEMY · BACKS','Diya Purohit',13,'6 TRIES','10 APPS'],['ACADEMY · FORWARDS','Neel Vyas',4,'2 TRIES','11 APPS']]};
tabs.innerHTML=Object.keys(R).map((k,i)=>`<button class="tab${i?'':' on'}" role="tab">${k}</button>`).join('');
function draw(k){roster.innerHTML=R[k].map((p,i)=>`<article class="pc">${scene(i+k.length,'p')}<div class="no">${p[2]}</div><div class="info"><div class="pos">${p[0]}</div><h3>${p[1]}</h3><div class="st"><span>${p[3]}</span><span>${p[4]}</span></div></div></article>`).join('')}
draw("MEN'S TEAM");
tabs.onclick=e=>{const b=e.target.closest('.tab');if(!b)return;tabs.querySelectorAll('.tab').forEach(t=>t.classList.remove('on'));b.classList.add('on');draw(b.textContent)};
 
// gallery
const gl=[['Scrum down','w2 h2'],['Fans in gold',''],['Line-out',''],['Post-match huddle','h2'],['Try celebration',''],['Under the lights','w2'],['Academy day',''],['Trophy night','h2'],['Tackle','']];
gal.innerHTML=gl.map((g,i)=>`<div class="g ${g[1]}">${scene(i,'g')}<span>${g[0]}</span></div>`).join('');
</script>
</body>
</html

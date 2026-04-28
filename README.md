<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Didi ⚡</title>
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600&family=Lora:ital,wght@0,400;1,400;1,600&display=swap" rel="stylesheet">
<style>
:root{
  --cream:#FDF6EE;--blush:#F5D5D5;--lavender:#E8DEFF;--mint:#D4F0E8;
  --sky:#D6EEFF;--peach:#FFE8D6;--gold:#C9A96E;--gold-deep:#9B7A42;
  --mauve:#B897C2;--sage:#8BAF9A;--dusty:#C98B8B;
  --text:#3D2B1F;--soft:#7A6055;--border:rgba(180,140,100,0.22);
}
*{margin:0;padding:0;box-sizing:border-box;}
body{background:var(--cream);font-family:'Lora',serif;color:var(--text);min-height:100vh;overflow-x:hidden;}
<!-- Harry Potter Theme Music -->
<div style="display:none;">
    <iframe width="1" height="1" src="https://youtube.com" frameborder="0" allow="autoplay"></iframe>
</div>

#petals{position:fixed;inset:0;pointer-events:none;z-index:0;overflow:hidden;}
.petal{position:absolute;border-radius:50% 10% 50% 10%;opacity:0;animation:petalFall linear infinite;}
@keyframes petalFall{0%{transform:translateY(-20px) rotate(0);opacity:0}10%{opacity:.55}90%{opacity:.35}100%{transform:translateY(105vh) rotate(360deg);opacity:0}}

.slide{display:none;position:relative;z-index:10;min-height:100vh;flex-direction:column;align-items:center;justify-content:center;padding:28px 18px;}
.slide.active{display:flex;}
.slide-nav{display:flex;gap:10px;margin-top:22px;}
.s-dot{width:8px;height:8px;border-radius:50%;background:rgba(180,140,100,.22);border:1px solid var(--gold);cursor:pointer;transition:all .3s;}
.s-dot.active{background:var(--gold);transform:scale(1.3);}

#overlay{position:fixed;inset:0;background:var(--cream);z-index:999;display:flex;align-items:center;justify-content:center;opacity:0;pointer-events:none;transition:opacity .35s;}
#overlay.show{opacity:1;pointer-events:all;}
.ov-icon{font-size:52px;animation:ovPop .5s ease;}
@keyframes ovPop{0%{transform:scale(0) rotate(-20deg)}70%{transform:scale(1.15)}100%{transform:scale(1)}}

.top-btns{position:fixed;top:14px;right:14px;z-index:200;display:flex;gap:8px;flex-direction:column;align-items:flex-end;}
.pill-btn{background:rgba(255,255,255,.78);border:1px solid rgba(184,151,194,.4);border-radius:20px;padding:6px 13px;font-family:'Cinzel',serif;font-size:10px;color:var(--mauve);letter-spacing:1.5px;cursor:pointer;transition:all .2s;white-space:nowrap;backdrop-filter:blur(6px);}
.pill-btn:hover{background:var(--lavender);}

.cbit{position:fixed;top:-12px;pointer-events:none;z-index:500;border-radius:2px;animation:cFall linear forwards;}
@keyframes cFall{0%{transform:translateY(0) rotate(0);opacity:1}100%{transform:translateY(110vh) rotate(540deg);opacity:0}}

#wandShower{position:fixed;inset:0;pointer-events:none;z-index:450;overflow:hidden;}
@keyframes wandFall{
  0%{transform:translateY(-60px) translateX(0) rotate(-20deg);opacity:1;}
  60%{opacity:1;}
  100%{transform:translateY(110vh) translateX(var(--wx,0px)) rotate(30deg);opacity:0;}
}

/* ── SLIDE 1 ── */
#slide1{background:linear-gradient(160deg,#FEF0F5 0%,#F0EAFF 50%,#E8F5F0 100%);}
.badge{font-family:'Cinzel',serif;font-size:10px;letter-spacing:4px;color:var(--gold);text-align:center;margin-bottom:4px;}
.divider{display:flex;align-items:center;gap:10px;margin-bottom:18px;}
.divider::before,.divider::after{content:'';flex:1;height:.5px;background:var(--gold);opacity:.4;}
.divider span{font-size:13px;color:var(--gold);}
.cake-card{background:rgba(255,255,255,.62);border:1px solid var(--border);border-radius:22px;padding:24px 20px 18px;backdrop-filter:blur(6px);box-shadow:0 4px 28px rgba(180,140,100,.07);}
.cake-float{animation:cFloat 5s ease-in-out infinite;}
@keyframes cFloat{0%,100%{transform:translateY(0)}50%{transform:translateY(-8px)}}
@keyframes flameGlow{0%,100%{opacity:1}50%{opacity:.82}}
.flame-grp{animation:flameGlow 1.3s ease-in-out infinite;}
@keyframes tw{0%,100%{opacity:.8}50%{opacity:.1}}
.tw{animation:tw ease-in-out infinite;}
.blow-btn{font-family:'Cinzel',serif;font-size:12px;letter-spacing:3px;text-transform:uppercase;color:var(--cream);background:linear-gradient(135deg,var(--mauve),var(--dusty));border:none;border-radius:30px;padding:13px 36px;cursor:pointer;margin-top:18px;position:relative;overflow:hidden;transition:transform .15s,box-shadow .2s;box-shadow:0 4px 16px rgba(184,151,194,.38);}
.blow-btn::before{content:'';position:absolute;top:-50%;left:-70%;width:40%;height:200%;background:rgba(255,255,255,.28);transform:skewX(-20deg);animation:shim 2.5s ease-in-out infinite;}
@keyframes shim{0%{left:-70%}100%{left:160%}}
.blow-btn:hover{transform:scale(1.04);}
.blow-btn:active{transform:scale(.97);}
.blow-btn:disabled{opacity:.5;cursor:not-allowed;}
.spell-cap{font-style:italic;font-size:13px;color:var(--soft);margin-top:10px;text-align:center;}

/* ── SLIDE 2 ── */
#slide2{background:linear-gradient(170deg,#F0EAFF,#FEF0F5 60%,#E8F5F0);}
.scroll-card{background:rgba(255,255,255,.65);border:1px solid var(--border);border-radius:20px;padding:24px 22px;max-width:450px;width:100%;backdrop-filter:blur(8px);box-shadow:0 4px 26px rgba(180,140,100,.07);}
.s-title{font-family:'Cinzel',serif;font-size:14px;letter-spacing:3px;color:var(--gold-deep);text-align:center;margin-bottom:4px;text-transform:uppercase;}
.s-sub{font-style:italic;font-size:12px;color:var(--soft);text-align:center;margin-bottom:16px;}
.prog-track{width:100%;height:3px;background:rgba(180,140,100,.15);border-radius:2px;margin-bottom:4px;position:relative;}
.prog-fill{height:100%;background:linear-gradient(90deg,var(--mauve),var(--dusty));border-radius:2px;width:0%;transition:width .15s ease;position:relative;}
.prog-fill::after{content:'✦';position:absolute;right:-8px;top:-7px;color:var(--dusty);font-size:12px;animation:spinG 1.5s linear infinite;}
@keyframes spinG{0%{transform:rotate(0)}100%{transform:rotate(360deg)}}
.time-lbl{font-family:'Cinzel',serif;font-size:10px;color:var(--soft);text-align:right;margin-bottom:12px;letter-spacing:1px;}
.lyric-box{min-height:260px;}
.lyric-line{font-size:14px;line-height:1.95;opacity:0;transform:translateY(8px);transition:opacity .5s ease,transform .5s ease;color:var(--soft);padding:1px 0;}
.lyric-line.shown{opacity:1;transform:translateY(0);}
.lyric-line.active{color:var(--text);font-weight:600;font-size:15.5px;}
.lyric-line.done{opacity:.45;}
.lyric-line.chorus{font-style:italic;color:var(--mauve);}
.lyric-line.finale{font-family:'Cinzel',serif;font-size:13px;letter-spacing:2px;color:var(--gold-deep);text-align:center;margin-top:8px;}
.lyric-line.spacer{height:8px;opacity:1;transform:none;}
.wand-area{position:relative;height:55px;display:flex;align-items:center;justify-content:center;margin-bottom:8px;}
.wand-svg{animation:wRock 3s ease-in-out infinite;}
@keyframes wRock{0%,100%{transform:rotate(-8deg)}50%{transform:rotate(8deg)}}
.mnote{position:absolute;font-size:18px;color:var(--mauve);opacity:0;animation:nDrift 2.4s ease-out infinite;pointer-events:none;}
@keyframes nDrift{0%{opacity:0;transform:translateY(0) scale(.8)}25%{opacity:1}100%{opacity:0;transform:translateY(-52px) rotate(20deg) scale(1.1)}}

/* ── SLIDE 3 ── */
#slide3{background:linear-gradient(155deg,#E8F5F0,#F0EAFF 50%,#FEF0F5);}
.fc-hdr{text-align:center;margin-bottom:18px;}
.fc-ttl{font-family:'Cinzel',serif;font-size:18px;letter-spacing:3px;color:var(--gold-deep);margin-bottom:4px;}
.fc-stl{font-style:italic;font-size:12px;color:var(--soft);}
.fc-stage{perspective:1000px;width:272px;height:360px;position:relative;margin:0 auto 14px;}
.flashcard{width:100%;height:100%;position:relative;transform-style:preserve-3d;transition:transform .65s cubic-bezier(.23,1,.32,1);cursor:pointer;border-radius:20px;}
.flashcard.flipped{transform:rotateY(180deg);}
.card-face{position:absolute;inset:0;border-radius:20px;backface-visibility:hidden;-webkit-backface-visibility:hidden;overflow:hidden;display:flex;flex-direction:column;align-items:center;justify-content:center;}
.card-front{border:1px solid rgba(184,151,194,.28);box-shadow:0 8px 30px rgba(180,140,100,.1);padding:20px;}
.card-front::before{content:'';position:absolute;inset:10px;border:.5px solid rgba(184,151,194,.22);border-radius:13px;pointer-events:none;}
.front-num{font-family:'Cinzel',serif;font-size:10px;color:rgba(180,140,100,.55);letter-spacing:3px;margin-bottom:14px;}
.front-icon{font-size:48px;margin-bottom:12px;line-height:1;}
.front-label{font-style:italic;font-size:14px;color:var(--text);text-align:center;line-height:1.6;padding:0 6px;}
.front-hint{font-family:'Cinzel',serif;font-size:9px;letter-spacing:2px;color:rgba(180,140,100,.45);margin-top:14px;text-transform:uppercase;}
.gem{position:absolute;width:8px;height:8px;border-radius:50%;}
.gem-tl{top:15px;left:15px;background:var(--blush);box-shadow:0 0 5px var(--blush);}
.gem-tr{top:15px;right:15px;background:var(--lavender);box-shadow:0 0 5px var(--lavender);}
.gem-bl{bottom:15px;left:15px;background:var(--mint);box-shadow:0 0 5px var(--mint);}
.gem-br{bottom:15px;right:15px;background:var(--peach);box-shadow:0 0 5px var(--peach);}
.card-back{transform:rotateY(180deg);background:var(--cream);border:1px solid rgba(184,151,194,.22);box-shadow:0 8px 30px rgba(180,140,100,.1);}
.back-inner{width:100%;height:100%;display:flex;flex-direction:column;position:relative;}
.photo-area{flex:1;overflow:hidden;border-radius:20px 20px 0 0;position:relative;background:linear-gradient(145deg,#f0eaff,#fff0f5);}
.photo-area img{width:100%;height:100%;object-fit:cover;}
.add-zone{width:100%;height:100%;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:10px;padding:18px;border:2px dashed rgba(184,151,194,.32);border-radius:19px 19px 0 0;cursor:pointer;transition:background .2s;}
.add-zone:hover{background:rgba(232,222,255,.28);}
.add-zone .plus{font-size:36px;color:rgba(184,151,194,.48);line-height:1;}
.add-zone .add-txt{font-family:'Cinzel',serif;font-size:10px;letter-spacing:2px;color:rgba(184,151,194,.58);text-transform:uppercase;}
.add-zone input{display:none;}
.tag-strip{background:rgba(255,255,255,.9);border-top:1px solid var(--border);border-radius:0 0 20px 20px;padding:8px 12px;display:flex;align-items:center;gap:6px;min-height:44px;}
.tag-icon{font-size:14px;flex-shrink:0;}
.tag-input{flex:1;font-family:'Lora',serif;font-style:italic;font-size:12px;color:var(--text);border:none;background:transparent;outline:none;text-align:center;}
.tag-input::placeholder{color:rgba(120,90,80,.4);}
.change-btn{font-family:'Cinzel',serif;font-size:9px;letter-spacing:1px;color:var(--gold-deep);background:rgba(201,169,110,.1);border:1px solid rgba(201,169,110,.3);border-radius:8px;padding:3px 8px;cursor:pointer;flex-shrink:0;}
.fc-controls{display:flex;align-items:center;gap:14px;margin-bottom:8px;}
.fc-btn{width:38px;height:38px;border-radius:50%;border:1px solid rgba(184,151,194,.38);background:rgba(255,255,255,.7);color:var(--mauve);font-size:20px;display:flex;align-items:center;justify-content:center;cursor:pointer;transition:all .2s;font-family:serif;}
.fc-btn:hover{background:var(--lavender);transform:scale(1.08);}
.fc-count{font-family:'Cinzel',serif;font-size:11px;letter-spacing:2px;color:var(--soft);min-width:48px;text-align:center;}
.fc-dots{display:flex;gap:8px;justify-content:center;margin-bottom:8px;}
.fc-dot{width:7px;height:7px;border-radius:50%;background:rgba(180,140,100,.2);border:1px solid rgba(180,140,100,.3);cursor:pointer;transition:all .3s;}
.fc-dot.active{background:var(--gold);transform:scale(1.4);}
.flip-tip{font-style:italic;font-size:11px;color:var(--soft);text-align:center;margin-bottom:10px;}
.hp-quote{border-left:2px solid var(--mauve);padding:9px 14px;max-width:280px;margin:6px auto;background:rgba(255,255,255,.5);border-radius:0 8px 8px 0;}
.hp-quote p{font-style:italic;font-size:12px;color:var(--text);line-height:1.7;}
.hp-quote span{display:block;font-family:'Cinzel',serif;font-size:10px;color:var(--soft);letter-spacing:1px;margin-top:4px;}

/* ══════════════════════════════════════
   SLIDE 4 — ENVELOPE + HARRY
══════════════════════════════════════ */
#slide4{background:linear-gradient(160deg,#F0EAFF 0%,#FEF0F5 55%,#E8F5F0 100%);padding:32px 18px;}

/* ── ENVELOPE ── */
.envelope-scene{
  display:flex;flex-direction:column;align-items:center;
  width:100%;max-width:440px;
}
.env-label{
  font-family:'Cinzel',serif;font-size:10px;letter-spacing:3px;
  color:var(--gold-deep);margin-bottom:14px;text-transform:uppercase;text-align:center;
}
.env-wrap{
  position:relative;width:280px;height:180px;
  cursor:pointer;margin-bottom:8px;
  filter:drop-shadow(0 8px 24px rgba(140,90,30,.18));
}

/* Envelope body */
.env-body{
  position:absolute;inset:0;
  background:linear-gradient(160deg,#FFF8E8,#F5E8C0);
  border-radius:6px;
  border:1.5px solid rgba(201,169,110,.5);
  overflow:hidden;
}
/* Back flap (V-shape, bottom) */
.env-body::after{
  content:'';position:absolute;bottom:0;left:0;right:0;height:90px;
  background:linear-gradient(175deg,#F0DC98,#E8C870);
  clip-path:polygon(0 100%,50% 0%,100% 100%);
}
/* Left triangle */
.env-body::before{
  content:'';position:absolute;top:0;left:0;bottom:0;width:50%;
  background:linear-gradient(135deg,#F8ECC0,#EEDDA0);
  clip-path:polygon(0 0,100% 50%,0 100%);
}

/* Right triangle (separate el) */
.env-right{
  position:absolute;top:0;right:0;bottom:0;width:50%;
  background:linear-gradient(225deg,#F8ECC0,#EEDDA0);
  clip-path:polygon(0 50%,100% 0,100% 100%);
}

/* Top flap — opens upward */
.env-flap{
  position:absolute;top:0;left:0;right:0;height:100px;
  background:linear-gradient(160deg,#F5E098,#E8CE70);
  clip-path:polygon(0 0,100% 0,50% 100%);
  transform-origin:top center;
  transform:rotateX(0deg);
  transition:transform 1s cubic-bezier(.23,1,.32,1);
  transform-style:preserve-3d;
  border-radius:6px 6px 0 0;
  z-index:3;
}
.env-wrap.open .env-flap{transform:rotateX(-160deg);}

/* Wax seal on flap */
.env-seal{
  position:absolute;top:55px;left:50%;transform:translateX(-50%);
  width:36px;height:36px;
  background:radial-gradient(circle at 38% 38%,#C84040,#8B1010);
  border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  font-size:16px;
  box-shadow:0 2px 8px rgba(139,16,16,.4);
  z-index:4;
  transition:opacity .3s;
  border:1.5px solid rgba(255,180,180,.3);
}
.env-wrap.open .env-seal{opacity:0;pointer-events:none;}

/* Hogwarts crest text on envelope */
.env-address{
  position:absolute;bottom:24px;left:50%;transform:translateX(-50%);
  text-align:center;white-space:nowrap;z-index:2;
}
.env-address .to{font-family:'Cinzel',serif;font-size:9px;color:rgba(80,40,10,.6);letter-spacing:2px;}
.env-address .name{font-family:'Cinzel',serif;font-size:12px;color:rgba(60,20,5,.8);font-weight:600;letter-spacing:1px;margin-top:2px;}

/* Letter rising from envelope */
.env-letter{
  position:absolute;top:10px;left:10px;right:10px;
  background:linear-gradient(160deg,#FFF8EE,#FDF0D8);
  border-radius:4px;
  border:1px solid rgba(201,169,110,.35);
  padding:10px 14px 8px;
  transform:translateY(40px);
  transition:transform 1.2s cubic-bezier(.23,1,.32,1) .4s;
  z-index:2;
  box-shadow:0 2px 12px rgba(140,90,30,.1);
  text-align:center;
}
.env-letter .letter-top{
  font-family:'Cinzel',serif;font-size:8px;color:var(--gold-deep);
  letter-spacing:2px;border-bottom:0.5px solid rgba(201,169,110,.3);
  padding-bottom:4px;margin-bottom:4px;
}
.env-letter .letter-preview{
  font-style:italic;font-size:8px;color:var(--soft);
  line-height:1.5;
}
.env-wrap.open .env-letter{transform:translateY(-100px);}

.open-hint{
  font-family:'Cinzel',serif;font-size:10px;letter-spacing:2px;
  color:var(--gold-deep);margin-top:10px;text-align:center;
  animation:hintPulse 2s ease-in-out infinite;
}
@keyframes hintPulse{0%,100%{opacity:.5}50%{opacity:1}}

/* ── HARRY SECTION (hidden until envelope opened) ── */
.harry-reveal{
  width:100%;max-width:440px;
  opacity:0;transform:translateY(30px);
  transition:opacity .8s ease,transform .8s ease;
  pointer-events:none;
}
.harry-reveal.show{opacity:1;transform:translateY(0);pointer-events:all;}

.harry-row{display:flex;align-items:flex-start;gap:14px;margin-bottom:16px;}
.hp-avatar-ring{
  flex-shrink:0;
  width:80px;height:80px;border-radius:50%;
  border:2px solid rgba(201,169,110,.35);
  background:rgba(255,255,255,.4);
  animation:ringPulse 3s ease-in-out infinite;
  position:relative;overflow:hidden;
}
@keyframes ringPulse{0%,100%{box-shadow:0 0 0 0 rgba(201,169,110,.25)}50%{box-shadow:0 0 0 8px rgba(201,169,110,.08)}}
.hp-bolt-float{position:absolute;bottom:-2px;right:-2px;font-size:14px;animation:boltFloat 2.5s ease-in-out infinite;z-index:2;}
@keyframes boltFloat{0%,100%{transform:translateY(0) rotate(-10deg)}50%{transform:translateY(-4px) rotate(10deg)}}

.speech-bubble{
  flex:1;
  background:rgba(255,255,255,.72);
  border:1px solid var(--border);
  border-radius:0 18px 18px 18px;
  padding:16px 18px;
  backdrop-filter:blur(6px);
  box-shadow:0 4px 20px rgba(180,140,100,.08);
  position:relative;
  min-height:80px;
}
.speech-bubble::before{
  content:'';position:absolute;top:12px;left:-10px;
  width:0;height:0;
  border-top:8px solid transparent;
  border-bottom:8px solid transparent;
  border-right:10px solid rgba(255,255,255,.72);
}
.hp-name-tag{font-family:'Cinzel',serif;font-size:9px;letter-spacing:2px;color:var(--gold-deep);margin-bottom:8px;text-transform:uppercase;}
.hp-speech-text{font-size:13.5px;line-height:1.9;color:var(--text);font-style:italic;}
.hp-speech-text .w{display:inline;opacity:0;transition:opacity .25s ease;}
.hp-speech-text .w.show{opacity:1;}

.hp-footer{display:flex;align-items:center;justify-content:space-between;margin-top:14px;padding-top:12px;border-top:1px solid var(--border);opacity:0;transition:opacity .8s ease;}
.hp-footer.show{opacity:1;}
.hp-sig-txt{font-family:'Cinzel',serif;font-size:10px;letter-spacing:1px;color:var(--soft);}
.hp-hearts{text-align:center;font-size:20px;margin-top:12px;opacity:0;transition:opacity .8s ease;letter-spacing:6px;animation:heartBeat 1.8s ease-in-out infinite;}
.hp-hearts.show{opacity:1;}
@keyframes heartBeat{0%,100%{transform:scale(1)}50%{transform:scale(1.08)}}

/* SHARED BTNS */
.btn-ghost{font-family:'Cinzel',serif;font-size:10px;letter-spacing:2px;color:var(--mauve);background:rgba(255,255,255,.6);border:1px solid rgba(184,151,194,.38);border-radius:20px;padding:10px 20px;cursor:pointer;transition:all .2s;}
.btn-ghost:hover{background:var(--lavender);}
.btn-cta{font-family:'Cinzel',serif;font-size:10px;letter-spacing:2px;color:white;background:linear-gradient(135deg,var(--mauve),var(--dusty));border:none;border-radius:20px;padding:10px 20px;cursor:pointer;box-shadow:0 3px 12px rgba(184,151,194,.32);transition:all .2s;}
.btn-cta:hover{transform:scale(1.04);}
.nav-row{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;margin-top:14px;}
</style>
</head>
<body>

<div id="petals"></div>
<div id="overlay"><div class="ov-icon" id="ovIcon">✦</div></div>
<div id="wandShower"></div>

<div class="top-btns">
  <button class="pill-btn" id="bgmBtn" onclick="toggleBGM()">♫ MUSIC ON</button>
  <button class="pill-btn" id="sndBtn" onclick="toggleSFX()">♪ SFX ON</button>
</div>

<!-- ══════ SLIDE 1 — CAKE ══════ -->
<div id="slide1" class="slide active">
  <div class="badge">Hogwarts School of Witchcraft &amp; Wizardry</div>
  <div class="divider"><span>⚡</span></div>
  <div class="cake-card">
    <div class="cake-float">
      <svg width="300" height="360" viewBox="0 0 300 360" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <linearGradient id="g-bottom" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%"   stop-color="#F8D060"/>
            <stop offset="48%"  stop-color="#E09010"/>
            <stop offset="100%" stop-color="#8B1A1A"/>
          </linearGradient>
          <linearGradient id="g-top" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%"   stop-color="#FFF8DC"/>
            <stop offset="100%" stop-color="#F2C030"/>
          </linearGradient>
          <linearGradient id="g-wing" x1="0" y1="0" x2="1" y2="0">
            <stop offset="0%"   stop-color="#FFF5D0" stop-opacity=".95"/>
            <stop offset="100%" stop-color="#FFF5D0" stop-opacity="0"/>
          </linearGradient>
        </defs>
        <ellipse cx="150" cy="348" rx="124" ry="10" fill="rgba(120,60,10,.12)"/>
        <!-- Bottom tier -->
        <rect x="18" y="215" width="264" height="125" rx="18" fill="url(#g-bottom)"/>
        <clipPath id="clip-s"><rect x="18" y="315" width="264" height="25"/></clipPath>
        <g clip-path="url(#clip-s)">
          <rect x="18"  y="315" width="22" height="25" fill="#8B1A1A"/>
          <rect x="40"  y="315" width="22" height="25" fill="#F5C020"/>
          <rect x="62"  y="315" width="22" height="25" fill="#8B1A1A"/>
          <rect x="84"  y="315" width="22" height="25" fill="#F5C020"/>
          <rect x="106" y="315" width="22" height="25" fill="#8B1A1A"/>
          <rect x="128" y="315" width="22" height="25" fill="#F5C020"/>
          <rect x="150" y="315" width="22" height="25" fill="#8B1A1A"/>
          <rect x="172" y="315" width="22" height="25" fill="#F5C020"/>
          <rect x="194" y="315" width="22" height="25" fill="#8B1A1A"/>
          <rect x="216" y="315" width="22" height="25" fill="#F5C020"/>
          <rect x="238" y="315" width="22" height="25" fill="#8B1A1A"/>
          <rect x="260" y="315" width="22" height="25" fill="#F5C020"/>
        </g>
        <line x1="18" y1="315" x2="282" y2="315" stroke="rgba(255,220,80,.35)" stroke-width="1"/>
        <path d="M18,232 Q31,252 44,232 Q57,252 70,232 Q83,252 96,232 Q109,252 122,232 Q135,252 148,232 Q161,252 174,232 Q187,252 200,232 Q213,252 226,232 Q239,252 252,232 Q265,252 278,232" fill="rgba(255,248,180,.55)"/>
        <text x="145" y="300" font-family="Georgia,serif" font-size="56" font-weight="bold" fill="rgba(60,15,0,.75)" letter-spacing="8">HP</text>
        <circle cx="84"  cy="250" r="13" fill="none" stroke="#D4A020" stroke-width="2.5"/>
        <circle cx="114" cy="250" r="13" fill="none" stroke="#D4A020" stroke-width="2.5"/>
        <line x1="97"  y1="250" x2="101" y2="250" stroke="#D4A020" stroke-width="2.2"/>
        <line x1="71"  y1="246" x2="62"  y2="240" stroke="#D4A020" stroke-width="2"/>
        <line x1="127" y1="246" x2="136" y2="240" stroke="#D4A020" stroke-width="2"/>
        <circle cx="214" cy="252" r="12" fill="#F5C020" stroke="#C8900A" stroke-width="1.8"/>
        <circle cx="214" cy="252" r="5"  fill="#C8900A" opacity=".35"/>
        <ellipse cx="196" cy="247" rx="17" ry="7" fill="url(#g-wing)" transform="rotate(-22,196,247)"/>
        <ellipse cx="232" cy="247" rx="17" ry="7" fill="#FFF5D0" opacity=".72" transform="rotate(22,232,247)"/>
        <path d="M250,224 L238,248 L249,244 L237,270" stroke="#FFF3A0" stroke-width="3.2" fill="none" stroke-linecap="round" stroke-linejoin="round"/>
        <rect x="38" y="231" width="40" height="26" rx="4" fill="#8B1A1A" stroke="#D4A020" stroke-width="1.2"/>
        <text x="58" y="248" text-anchor="middle" font-family="Georgia,serif" font-size="11" fill="#FFD700" font-weight="bold">9¾</text>
        <ellipse cx="62" cy="280" rx="14" ry="9" fill="none" stroke="#D4A020" stroke-width="1.5"/>
        <ellipse cx="62" cy="280" rx="8"  ry="5"  fill="#C8900A" opacity=".5"/>
        <ellipse cx="62" cy="280" rx="4"  ry="2.5" fill="#5C2000" opacity=".7"/>
        <circle cx="46"  cy="272" r="7" fill="#F5C020" stroke="#C8900A" stroke-width="1.2"/>
        <circle cx="252" cy="278" r="6" fill="#F5C020" stroke="#C8900A" stroke-width="1.2"/>
        <circle cx="64"  cy="308" r="5" fill="#F5C020" stroke="#C8900A" stroke-width="1"/>
        <circle cx="234" cy="309" r="5" fill="#F5C020" stroke="#C8900A" stroke-width="1"/>
        <!-- Top tier -->
        <rect x="66" y="118" width="168" height="100" rx="15" fill="url(#g-top)"/>
        <path d="M66,134 Q78,152 90,134 Q102,152 114,134 Q126,152 138,134 Q150,152 162,134 Q174,152 186,134 Q198,152 210,134 Q222,152 232,134" fill="rgba(255,255,255,.6)"/>
        <rect x="82" y="174" width="72" height="5"  rx="2.5" fill="#7B4A18"/>
        <rect x="64" y="169" width="20" height="14" rx="2"   fill="#B87020" opacity=".9"/>
        <line x1="64" y1="170" x2="54" y2="163" stroke="#5C3010" stroke-width="1.4"/>
        <line x1="64" y1="172" x2="53" y2="167" stroke="#5C3010" stroke-width="1.4"/>
        <line x1="64" y1="174" x2="53" y2="171" stroke="#5C3010" stroke-width="1.4"/>
        <line x1="64" y1="176" x2="53" y2="175" stroke="#5C3010" stroke-width="1.4"/>
        <line x1="64" y1="178" x2="55" y2="180" stroke="#5C3010" stroke-width="1.4"/>
        <text x="104" y="162" font-size="13" fill="#C8900A" opacity=".85">★</text>
        <text x="192" y="158" font-size="11" fill="#C8900A" opacity=".8">★</text>
        <text x="170" y="170" font-size="9"  fill="#C8900A" opacity=".7">✦</text>
        <text x="88"  y="168" font-size="9"  fill="#C8900A" opacity=".7">✦</text>
        <!-- Hedwig -->
        <ellipse cx="188" cy="130" rx="19" ry="24" fill="#F8F8F0"/>
        <ellipse cx="168" cy="136" rx="13" ry="17" fill="#E4E4D8" transform="rotate(-14,168,136)"/>
        <ellipse cx="208" cy="136" rx="13" ry="17" fill="#E4E4D8" transform="rotate(14,208,136)"/>
        <ellipse cx="183" cy="122" rx="7" ry="8" fill="#EDEDEA"/>
        <ellipse cx="193" cy="122" rx="7" ry="8" fill="#EDEDEA"/>
        <circle cx="183" cy="122" r="5.5" fill="#1A1400"/>
        <circle cx="193" cy="122" r="5.5" fill="#1A1400"/>
        <circle cx="184.5" cy="120.5" r="1.8" fill="white"/>
        <circle cx="194.5" cy="120.5" r="1.8" fill="white"/>
        <path d="M185,128 L188,134 L191,128" fill="#D4900A"/>
        <path d="M180,112 L177,104 L183,111" fill="#DDDDC8"/>
        <path d="M196,112 L199,104 L193,111" fill="#DDDDC8"/>
        <line x1="164" y1="132" x2="158" y2="146" stroke="#BCBCAA" stroke-width=".9" opacity=".6"/>
        <line x1="167" y1="130" x2="161" y2="144" stroke="#BCBCAA" stroke-width=".9" opacity=".6"/>
        <line x1="212" y1="132" x2="218" y2="146" stroke="#BCBCAA" stroke-width=".9" opacity=".6"/>
        <!-- Scroll -->
        <rect x="86" y="122" width="58" height="36" rx="4" fill="#FFF8E8" stroke="#C8A040" stroke-width="1.2"/>
        <path d="M86,124 Q86,116 93,116 L86,116 Z" fill="#FFF0B8"/>
        <path d="M144,124 Q144,116 137,116 L144,116 Z" fill="#FFF0B8"/>
        <line x1="93" y1="129" x2="137" y2="129" stroke="#C8A040" stroke-width=".9" opacity=".4"/>
        <line x1="93" y1="134" x2="137" y2="134" stroke="#C8A040" stroke-width=".9" opacity=".4"/>
        <line x1="93" y1="139" x2="137" y2="139" stroke="#C8A040" stroke-width=".9" opacity=".4"/>
        <line x1="93" y1="144" x2="137" y2="144" stroke="#C8A040" stroke-width=".9" opacity=".4"/>
        <!-- Candles -->
        <rect x="101" y="77" width="10" height="44" rx="4" fill="#C8303A"/>
        <ellipse cx="106" cy="77" rx="5" ry="3.2" fill="#D84050"/>
        <g class="flame-grp" id="fl1"><ellipse cx="106" cy="73" rx="4.5" ry="7" fill="#FFA030"/><ellipse cx="106" cy="69" rx="2.8" ry="5" fill="#FFE060"/><ellipse cx="106" cy="66" rx="1.3" ry="2.3" fill="white" opacity=".9"/></g>
        <rect x="119" y="71" width="10" height="50" rx="4" fill="#3060C0"/>
        <ellipse cx="124" cy="71" rx="5" ry="3.2" fill="#4070D0"/>
        <g class="flame-grp" id="fl2"><ellipse cx="124" cy="67" rx="4.5" ry="7" fill="#FFA030"/><ellipse cx="124" cy="63" rx="2.8" ry="5" fill="#FFE060"/><ellipse cx="124" cy="60" rx="1.3" ry="2.3" fill="white" opacity=".9"/></g>
        <rect x="137" y="63" width="11" height="58" rx="4" fill="#40A860"/>
        <ellipse cx="142.5" cy="63" rx="5.5" ry="3.5" fill="#50B870"/>
        <g class="flame-grp" id="fl3"><ellipse cx="142.5" cy="58" rx="5" ry="8.5" fill="#FFB020"/><ellipse cx="142.5" cy="54" rx="3" ry="6" fill="#FFF050"/><ellipse cx="142.5" cy="50" rx="1.5" ry="2.5" fill="white" opacity=".9"/></g>
        <rect x="157" y="71" width="10" height="50" rx="4" fill="#C09020"/>
        <ellipse cx="162" cy="71" rx="5" ry="3.2" fill="#D0A030"/>
        <g class="flame-grp" id="fl4"><ellipse cx="162" cy="67" rx="4.5" ry="7" fill="#FFA030"/><ellipse cx="162" cy="63" rx="2.8" ry="5" fill="#FFE060"/><ellipse cx="162" cy="60" rx="1.3" ry="2.3" fill="white" opacity=".9"/></g>
        <circle cx="88"  cy="60" r="2" fill="#D4A020" opacity=".7"><animate attributeName="opacity" values=".7;.1;.7" dur="1.4s" repeatCount="indefinite"/></circle>
        <circle cx="180" cy="57" r="2" fill="#B897C2" opacity=".6"><animate attributeName="opacity" values=".6;.1;.6" dur="1.7s" repeatCount="indefinite" begin=".3s"/></circle>
        <circle cx="142" cy="38" r="2.5" fill="#D4A020" opacity=".8"><animate attributeName="opacity" values=".8;.1;.8" dur="1.2s" repeatCount="indefinite" begin=".6s"/></circle>
      </svg>
    </div>
    <div style="text-align:center;">
      <p class="spell-cap" id="cakeCaption">Incendio ✦ make a wish, Didi...</p>
      <button class="blow-btn" id="blowBtn" onclick="blowCandles()">✦ Blow the Candles ✦</button>
    </div>
  </div>
  <div class="slide-nav">
    <div class="s-dot active" onclick="goTo(1)"></div>
    <div class="s-dot" onclick="goTo(2)"></div>
    <div class="s-dot" onclick="goTo(3)"></div>
    <div class="s-dot" onclick="goTo(4)"></div>
  </div>
</div>

<!-- ══════ SLIDE 2 — SONG ══════ -->
<div id="slide2" class="slide">
  <div class="wand-area">
    <svg class="wand-svg" width="44" height="54" viewBox="0 0 44 54">
      <rect x="18" y="14" width="8" height="36" rx="3" fill="#C9A96E" opacity=".7"/>
      <ellipse cx="22" cy="14" rx="9" ry="10" fill="#F5D5A0"/>
      <ellipse cx="22" cy="6" rx="5" ry="6" fill="#FFF3A0"/>
      <circle cx="22" cy="3" r="3" fill="#C9A96E"><animate attributeName="r" values="3;5;3" dur="1.2s" repeatCount="indefinite"/></circle>
    </svg>
    <span class="mnote" style="left:22%;animation-delay:0s;">♪</span>
    <span class="mnote" style="left:52%;animation-delay:.8s;color:var(--sage);">♫</span>
    <span class="mnote" style="left:72%;animation-delay:1.5s;color:var(--dusty);">♩</span>
    <span class="mnote" style="left:8%;animation-delay:1.1s;color:var(--gold);">♬</span>
  </div>
  <div class="scroll-card">
    <div class="s-title">The Birthday Spell Song</div>
    <div class="s-sub">for Didi, from Hogwarts with love</div>
    <div class="prog-track"><div class="prog-fill" id="progFill"></div></div>
    <div class="time-lbl" id="timeLbl">0:00</div>
    <div class="lyric-box" id="lyricBox"></div>
  </div>
  <div class="nav-row" style="margin-top:14px;">
    <button class="btn-ghost" onclick="goTo(1)">← Cake</button>
    <button class="btn-cta"   onclick="goTo(3)">Our Photos →</button>
  </div>
  <div class="slide-nav">
    <div class="s-dot" onclick="goTo(1)"></div>
    <div class="s-dot active"></div>
    <div class="s-dot" onclick="goTo(3)"></div>
    <div class="s-dot" onclick="goTo(4)"></div>
  </div>
</div>

<!-- ══════ SLIDE 3 — FLASHCARDS ══════ -->
<div id="slide3" class="slide">
  <div class="fc-hdr">
    <div class="fc-ttl">Didi &amp; Me</div>
    <div class="fc-stl">Our magical memories ✦ tap to reveal</div>
  </div>
  <div class="fc-stage" id="fcStage"></div>
  <p class="flip-tip" id="flipTip">Tap to flip · swipe or arrows to browse</p>
  <div class="fc-controls">
    <button class="fc-btn" onclick="prevCard()">‹</button>
    <span class="fc-count" id="fcCount">1 / 4</span>
    <button class="fc-btn" onclick="nextCard()">›</button>
  </div>
  <div class="fc-dots" id="fcDots"></div>
  <div class="hp-quote">
    <p>"After all this time?" — "Always."</p>
    <span>Happy Birthday Didi. Forever your little one. 🪄</span>
  </div>
  <div class="nav-row">
    <button class="btn-ghost" onclick="goTo(2)">← Song</button>
    <button class="btn-cta"   onclick="goTo(4)">Harry's Letter →</button>
  </div>
  <div class="slide-nav">
    <div class="s-dot" onclick="goTo(1)"></div>
    <div class="s-dot" onclick="goTo(2)"></div>
    <div class="s-dot active"></div>
    <div class="s-dot" onclick="goTo(4)"></div>
  </div>
</div>

<!-- ══════ SLIDE 4 — ENVELOPE + HARRY ══════ -->
<div id="slide4" class="slide">

  <!-- ENVELOPE SCENE -->
  <div class="envelope-scene" id="envScene">
    <div class="env-label">✦ You've received a letter from Hogwarts ✦</div>

    <div class="env-wrap" id="envWrap" onclick="openEnvelope()">
      <div class="env-body"></div>
      <div class="env-right"></div>

      <!-- Letter peeking out -->
      <div class="env-letter">
        <div class="letter-top">HOGWARTS SCHOOL OF WITCHCRAFT &amp; WIZARDRY</div>
        <div class="letter-preview">Dear Didi,<br>Wishing you a most magical birthday...</div>
      </div>

      <!-- Flap -->
      <div class="env-flap">
        <div class="env-seal">⚡</div>
      </div>

      <!-- Address -->
      <div class="env-address">
        <div class="to">TO</div>
        <div class="name">Didi</div>
      </div>
    </div>

    <div class="open-hint" id="openHint">✦ Tap to open ✦</div>
  </div>

  <!-- HARRY REVEAL -->
  <div class="harry-reveal" id="harryReveal">
    <div class="harry-row">
      <div style="position:relative;">
        <div class="hp-avatar-ring">
          <svg width="80" height="80" viewBox="0 0 80 80">
            <circle cx="40" cy="40" r="40" fill="url(#hpBg2)"/>
            <defs><radialGradient id="hpBg2" cx="50%" cy="40%"><stop offset="0%" stop-color="#e8deff"/><stop offset="100%" stop-color="#f5d5e8"/></radialGradient></defs>
            <path d="M10,80 Q15,58 40,56 Q65,58 70,80 Z" fill="#1a1a2e"/>
            <path d="M31,60 L40,80 L49,60 Q44,58 40,58 Q36,58 31,60 Z" fill="#f5f5f5"/>
            <path d="M37,60 L40,72 L43,60 Z" fill="#8b0000"/>
            <rect x="35" y="53" width="10" height="8" rx="4" fill="#f5c5a0"/>
            <ellipse cx="40" cy="38" rx="18" ry="20" fill="#f5c5a0"/>
            <ellipse cx="22" cy="39" rx="4" ry="5" fill="#f5c5a0"/>
            <ellipse cx="58" cy="39" rx="4" ry="5" fill="#f5c5a0"/>
            <path d="M23,30 Q26,18 40,17 Q54,18 57,30 Q55,20 40,19 Q25,20 23,30 Z" fill="#2c1810"/>
            <path d="M28,24 Q30,17 37,18 Q31,19 30,25 Z" fill="#2c1810"/>
            <path d="M43,17 Q48,14 53,17 Q49,16 46,23 Z" fill="#2c1810"/>
            <path d="M22,35 Q19,29 21,24 Q22,30 25,33 Z" fill="#2c1810"/>
            <path d="M58,35 Q61,29 59,24 Q58,30 55,33 Z" fill="#2c1810"/>
            <path d="M30,35 Q33,33 36,34" stroke="#2c1810" stroke-width="1.2" fill="none" stroke-linecap="round"/>
            <path d="M44,34 Q47,33 50,35" stroke="#2c1810" stroke-width="1.2" fill="none" stroke-linecap="round"/>
            <ellipse cx="34" cy="39" rx="5" ry="4.5" fill="white"/>
            <ellipse cx="46" cy="39" rx="5" ry="4.5" fill="white"/>
            <ellipse cx="34" cy="39" rx="3.5" ry="3.5" fill="#3a7d44"/>
            <ellipse cx="46" cy="39" rx="3.5" ry="3.5" fill="#3a7d44"/>
            <ellipse cx="34" cy="39" rx="2" ry="2" fill="#1a3d20"/>
            <ellipse cx="46" cy="39" rx="2" ry="2" fill="#1a3d20"/>
            <circle cx="35" cy="37.5" r="1" fill="white"/>
            <circle cx="47" cy="37.5" r="1" fill="white"/>
            <circle cx="34" cy="39" r="6" fill="none" stroke="#5c3a1e" stroke-width="1.3"/>
            <circle cx="46" cy="39" r="6" fill="none" stroke="#5c3a1e" stroke-width="1.3"/>
            <path d="M40,39 Q40.5,38 41,39" stroke="#5c3a1e" stroke-width="1.3" fill="none"/>
            <path d="M28,37 Q25,35 23,37" stroke="#5c3a1e" stroke-width="1" fill="none"/>
            <path d="M52,37 Q55,35 57,37" stroke="#5c3a1e" stroke-width="1" fill="none"/>
            <path d="M38,43 Q40,46 42,43" stroke="#edb090" stroke-width="1" fill="none" stroke-linecap="round"/>
            <path d="M35,49 Q40,53 45,49" stroke="#c98b8b" stroke-width="1.3" fill="none" stroke-linecap="round"/>
            <path d="M38,27 L36,31 L39,30 L37,34" stroke="#c9a96e" stroke-width="1.5" fill="none" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <div class="hp-bolt-float">⚡</div>
      </div>
      <div class="speech-bubble">
        <div class="hp-name-tag">✦ Harry Potter — Gryffindor ✦</div>
        <div class="hp-speech-text" id="hpText"></div>
      </div>
    </div>

    <div class="hp-footer" id="hpFooter">
      <div class="hp-sig-txt">— Harry James Potter<br><span style="font-size:9px;opacity:.7;letter-spacing:1px;">The Boy Who Lived 🦁</span></div>
      <div style="font-size:20px;animation:sealSpin 6s linear infinite;">⚡</div>
    </div>
    @keyframes sealSpin{0%,100%{transform:rotate(0)}50%{transform:rotate(8deg)}}

    <div class="hp-hearts" id="hpHearts">🌸 🪄 🌸</div>

    <div class="nav-row" style="margin-top:14px;">
      <button class="btn-ghost" onclick="goTo(3)">← Photos</button>
      <button class="btn-ghost" onclick="goTo(1)">Start Over ✦</button>
    </div>
  </div>

  <div class="slide-nav" style="margin-top:18px;">
    <div class="s-dot" onclick="goTo(1)"></div>
    <div class="s-dot" onclick="goTo(2)"></div>
    <div class="s-dot" onclick="goTo(3)"></div>
    <div class="s-dot active"></div>
  </div>
</div>

<script>
/* ── PETALS ── */
const pC=['#F5D5D5','#E8DEFF','#D4F0E8','#FFE8D6','#D6EEFF','#FFF0F5'];
for(let i=0;i<20;i++){
  const p=document.createElement('div');p.className='petal';
  const sz=Math.random()*8+5;
  p.style.cssText=`width:${sz}px;height:${sz*1.4}px;background:${pC[~~(Math.random()*pC.length)]};left:${Math.random()*100}%;animation-duration:${Math.random()*10+8}s;animation-delay:${Math.random()*10}s;`;
  document.getElementById('petals').appendChild(p);
}

/* ════════════════════════════════════════
   AUDIO ENGINE
════════════════════════════════════════ */
let sfxOn=true,bgmOn=true,audioCtx=null,bgmRunning=false,bgmTimer=null;
let songAudioNodes=[];   // nodes created during song — we stop them when leaving

function getCtx(){
  if(!audioCtx) audioCtx=new(window.AudioContext||window.webkitAudioContext)();
  if(audioCtx.state==='suspended') audioCtx.resume();
  return audioCtx;
}
function toggleSFX(){sfxOn=!sfxOn;document.getElementById('sndBtn').textContent=sfxOn?'♪ SFX ON':'♪ SFX OFF';}
function toggleBGM(){
  bgmOn=!bgmOn;
  document.getElementById('bgmBtn').textContent=bgmOn?'♫ MUSIC ON':'♫ MUSIC OFF';
  if(bgmOn){try{startBGM();}catch(e){}}else{bgmRunning=false;clearTimeout(bgmTimer);}
}

/* ─── Hedwig's Theme for the BGM loop ─── */
const HEDWIG=[
  [0,.35],[494,.35],[0,.035],[740,.175],[0,.025],[659,.175],[0,.025],
  [740,.35],[0,.035],[494,.35],[622,.35],[0,.035],[587,.35],[0,.035],[554,.35],[0,.035],
  [740,.7],[0,.1],
  [494,.35],[0,.035],[880,.35],[0,.035],[784,.175],[0,.025],[740,.175],[0,.025],
  [784,.35],[0,.035],[494,.35],[622,.35],[0,.035],[587,.35],[0,.035],[554,.35],[0,.035],
  [988,.7],[0,.1],
  [494,.35],[0,.035],[1047,.35],[0,.035],[988,.35],[0,.035],[831,.175],[0,.025],[880,.175],[0,.025],
  [784,.35],[0,.035],[494,.35],[659,.35],[0,.035],[784,.35],[0,.035],
  [740,.175],[0,.025],[698,.175],[0,.025],[740,.35],[0,.035],
  [554,.175],[0,.025],[494,.175],[0,.025],[440,.175],[0,.025],[466,.7],[0,.9],
];

function startBGM(){if(bgmRunning)return;bgmRunning=true;loopHedwig();}
function loopHedwig(){
  if(!bgmOn){bgmRunning=false;return;}
  try{
    const ctx=getCtx();let t=ctx.currentTime+.08,total=0;
    HEDWIG.forEach(([f,d])=>{
      if(f>0){
        const o=ctx.createOscillator(),g=ctx.createGain();
        o.connect(g);g.connect(ctx.destination);o.type='triangle';o.frequency.value=f;
        g.gain.setValueAtTime(0,t);g.gain.linearRampToValueAtTime(.06,t+.02);
        g.gain.exponentialRampToValueAtTime(.001,t+d);
        o.start(t);o.stop(t+d+.02);
        const o2=ctx.createOscillator(),g2=ctx.createGain();
        o2.connect(g2);g2.connect(ctx.destination);o2.type='sine';o2.frequency.value=f/2;
        g2.gain.setValueAtTime(0,t);g2.gain.linearRampToValueAtTime(.02,t+.02);
        g2.gain.exponentialRampToValueAtTime(.001,t+d);
        o2.start(t);o2.stop(t+d+.02);
      }
      t+=d;total+=d;
    });
    bgmTimer=setTimeout(()=>{if(bgmOn)loopHedwig();else bgmRunning=false;},(total+.8)*1000);
  }catch(e){bgmRunning=false;}
}

/* tone helper */
function tone(ctx,f,st,dur,type,vol){
  const o=ctx.createOscillator(),g=ctx.createGain();
  o.connect(g);g.connect(ctx.destination);
  o.type=type||'sine';o.frequency.value=f;
  g.gain.setValueAtTime(0,st);g.gain.linearRampToValueAtTime(vol||.12,st+.025);
  g.gain.setValueAtTime(vol||.12,st+dur-.04);g.gain.linearRampToValueAtTime(0,st+dur);
  o.start(st);o.stop(st+dur+.01);
}
function playChime(ctx){
  [523,659,784,1047].forEach((f,i)=>{
    const o=ctx.createOscillator(),g=ctx.createGain();
    o.connect(g);g.connect(ctx.destination);o.type='triangle';o.frequency.value=f;
    const t=ctx.currentTime+i*.13;
    g.gain.setValueAtTime(.09,t);g.gain.exponentialRampToValueAtTime(.001,t+.9);
    o.start(t);o.stop(t+1);
  });
}
function playWhoosh(ctx){
  const b=ctx.createBuffer(1,ctx.sampleRate*.55,ctx.sampleRate);
  const d=b.getChannelData(0);for(let i=0;i<d.length;i++)d[i]=(Math.random()*2-1)*(1-i/d.length)*.18;
  const s=ctx.createBufferSource();s.buffer=b;
  const f=ctx.createBiquadFilter();f.type='bandpass';f.frequency.value=700;f.Q.value=.4;
  s.connect(f);f.connect(ctx.destination);s.start();
}
function playFlip(ctx){tone(ctx,900,ctx.currentTime,.06,'square',.04);tone(ctx,700,ctx.currentTime+.04,.06,'square',.03);}
function playSwipe(ctx){tone(ctx,440,ctx.currentTime,.07,'sine',.06);tone(ctx,350,ctx.currentTime+.04,.07,'sine',.05);}
function playPaperRustle(ctx){
  const b=ctx.createBuffer(1,ctx.sampleRate*.35,ctx.sampleRate);
  const d=b.getChannelData(0);
  for(let i=0;i<d.length;i++)d[i]=(Math.random()*2-1)*Math.sin(i/d.length*Math.PI)*.15;
  const s=ctx.createBufferSource();s.buffer=b;
  const f=ctx.createBiquadFilter();f.type='highpass';f.frequency.value=2000;
  s.connect(f);f.connect(ctx.destination);s.start();
}

/* ════════════════════════════════════════
   SONG — BGM SYNCED TO LYRICS
   Strategy: The Happy Birthday melody plays note-by-note timed
   so each musical phrase aligns to when that lyric line appears.
   Verse lines get a gentle harp-like arpeggio.
   Chorus lines get the actual Happy Birthday notes.
   Volume stays at 20% so lyrics dominate.
════════════════════════════════════════ */

/*
  Lyrics and their start times (seconds):
  0.3  — Wingardium Leviosa,
  1.9  — let the birthday rise —
  3.6  — Didi's another year older,
  5.2  — and twice as wise.
  6.6  — Expecto Patronum,
  8.1  — chase the dark away —
  9.6  — nothing but joy and magic
  11.1 — on your special day.
  12.5 — Happy Birthday to you,          ← HB melody line 1
  14.4 — by the Hogwarts decree —        ← HB melody line 2
  16.2 — the sorting hat agrees,         ← HB melody line 3
  17.9 — you're extraordinary.           ← HB melody line 3 cont
  19.6 — Accio happiness,                ← HB melody line 4 start
  21.1 — let it fill this room —
  22.7 — Happy Birthday, dear Didi,      ← HB melody line 4 "dear Didi"
  24.3 — let your magic bloom!
  25.8 — ✦ Mischief Managed ✦
  27.2 — Make a wish, Didi!
*/

const LYRICS=[
  {t:.3,  text:"Wingardium Leviosa,",                type:'verse'},
  {t:1.9, text:"let the birthday rise —",            type:'verse'},
  {t:3.6, text:"Didi's another year older,",         type:'verse'},
  {t:5.2, text:"and twice as wise.",                 type:'verse'},
  {t:6.4, text:"",                                   type:'spacer'},
  {t:6.6, text:"Expecto Patronum,",                  type:'verse'},
  {t:8.1, text:"chase the dark away —",              type:'verse'},
  {t:9.6, text:"nothing but joy and magic",          type:'verse'},
  {t:11.1,text:"on your special day.",               type:'verse'},
  {t:12.3,text:"",                                   type:'spacer'},
  {t:12.5,text:"Happy Birthday to you,",             type:'chorus'},
  {t:14.4,text:"by the Hogwarts decree —",           type:'chorus'},
  {t:16.2,text:"the sorting hat agrees,",            type:'chorus'},
  {t:17.9,text:"you're extraordinary.",              type:'chorus'},
  {t:19.4,text:"",                                   type:'spacer'},
  {t:19.6,text:"Accio happiness,",                   type:'chorus'},
  {t:21.1,text:"let it fill this room —",            type:'chorus'},
  {t:22.7,text:"Happy Birthday, dear Didi,",         type:'chorus'},
  {t:24.3,text:"let your magic bloom! ✨",           type:'chorus'},
  {t:25.6,text:"",                                   type:'spacer'},
  {t:25.8,text:"✦ Mischief Managed ✦",              type:'finale'},
  {t:27.2,text:"Make a wish, Didi!",                 type:'finale'},
];
const SONG_DUR=29;

/* Verse arpeggio notes — one gentle note per lyric line */
const VERSE_NOTES=[261.63,293.66,329.63,349.23,392,440,493.88,523.25];

/*
  Happy Birthday melody — 4 lines, each mapped to a chorus lyric pair:
  Line 1: "Hap-py Birth-day to you"        → t=12.5
  Line 2: "Hap-py Birth-day to you"        → t=14.4
  Line 3: "Hap-py Birth-day dear Di-di"    → t=16.2 + 17.9
  Line 4: "Hap-py Birth-day to you"        → t=19.6 + 21.1
  Final resolution                          → t=22.7 + 24.3
*/
const HB_LINES=[
  // Line 1: t=12.5 — "Happy Birthday to you"
  // [freq, duration_s, offset_from_line_start]
  {t:12.5, notes:[
    [261.63,.28,0],[261.63,.14,.3],[293.66,.38,.46],[261.63,.38,.86],
    [349.23,.38,1.26],[329.63,.76,1.66],
  ]},
  // Line 2: t=14.4 — "Happy Birthday to you"
  {t:14.4, notes:[
    [261.63,.28,0],[261.63,.14,.3],[293.66,.38,.46],[261.63,.38,.86],
    [392.00,.38,1.26],[349.23,.76,1.66],
  ]},
  // Line 3: t=16.2 — "Happy Birthday dear Didi"
  {t:16.2, notes:[
    [261.63,.28,0],[261.63,.14,.3],[523.25,.38,.46],[440.00,.38,.86],
    [349.23,.38,1.26],[329.63,.38,1.66],[293.66,.76,2.06],
  ]},
  // Line 4: t=19.6 — "Happy Birthday to you" (final)
  {t:19.6, notes:[
    [466.16,.28,0],[466.16,.14,.3],[440.00,.38,.46],[349.23,.38,.86],
    [392.00,.38,1.26],[349.23,.90,1.66],
  ]},
];

let songTimers=[],songInterval=null,songStarted=false;

function startSong(){
  const box=document.getElementById('lyricBox');
  box.innerHTML='';songTimers.forEach(clearTimeout);clearInterval(songInterval);

  if(!sfxOn) { renderLyricsOnly(); return; }

  try{
    const ctx=getCtx();

    // ── Verse arpeggio: one soft note per verse lyric ──
    let verseIdx=0;
    LYRICS.filter(l=>l.type==='verse').forEach((l,i)=>{
      const freq=VERSE_NOTES[i%VERSE_NOTES.length];
      const st=ctx.currentTime+l.t;
      // Soft pluck: triangle + quick decay
      const o=ctx.createOscillator(),g=ctx.createGain();
      o.connect(g);g.connect(ctx.destination);
      o.type='triangle';o.frequency.value=freq;
      g.gain.setValueAtTime(0,st);
      g.gain.linearRampToValueAtTime(.13,st+.03);
      g.gain.exponentialRampToValueAtTime(.001,st+1.2);
      o.start(st);o.stop(st+1.3);
      // Low octave warmth
      const o2=ctx.createOscillator(),g2=ctx.createGain();
      o2.connect(g2);g2.connect(ctx.destination);
      o2.type='sine';o2.frequency.value=freq/2;
      g2.gain.setValueAtTime(0,st);
      g2.gain.linearRampToValueAtTime(.04,st+.04);
      g2.gain.exponentialRampToValueAtTime(.001,st+.8);
      o2.start(st);o2.stop(st+1);
    });

    // ── Happy Birthday melody for each chorus line ──
    HB_LINES.forEach(line=>{
      line.notes.forEach(([freq,dur,offset])=>{
        const st=ctx.currentTime+line.t+offset;
        const o=ctx.createOscillator(),g=ctx.createGain();
        o.connect(g);g.connect(ctx.destination);
        o.type='triangle';o.frequency.value=freq;
        g.gain.setValueAtTime(0,st);
        g.gain.linearRampToValueAtTime(.16,st+.025);
        g.gain.setValueAtTime(.16,st+dur-.04);
        g.gain.linearRampToValueAtTime(0,st+dur);
        o.start(st);o.stop(st+dur+.02);
        // Harmony a third below
        const o3=ctx.createOscillator(),g3=ctx.createGain();
        o3.connect(g3);g3.connect(ctx.destination);
        o3.type='sine';o3.frequency.value=freq*0.79;
        g3.gain.setValueAtTime(0,st);g3.gain.linearRampToValueAtTime(.05,st+.03);
        g3.gain.setValueAtTime(.05,st+dur-.04);g3.gain.linearRampToValueAtTime(0,st+dur);
        o3.start(st);o3.stop(st+dur+.02);
      });
    });

    // ── Finale sparkle chord ──
    const finT=ctx.currentTime+25.8;
    [523,659,784,1047].forEach((f,i)=>{
      const o=ctx.createOscillator(),g=ctx.createGain();
      o.connect(g);g.connect(ctx.destination);o.type='triangle';o.frequency.value=f;
      g.gain.setValueAtTime(0,finT+i*.08);g.gain.linearRampToValueAtTime(.1,finT+i*.08+.04);
      g.gain.exponentialRampToValueAtTime(.001,finT+i*.08+1.2);
      o.start(finT+i*.08);o.stop(finT+i*.08+1.3);
    });

  }catch(e){console.log(e);}

  renderLyricsOnly();
}

function renderLyricsOnly(){
  const box=document.getElementById('lyricBox');
  box.innerHTML='';
  LYRICS.forEach(l=>{
    const div=document.createElement('div');
    if(l.type==='spacer'){div.className='lyric-line spacer';div.innerHTML='&nbsp;';}
    else{div.className='lyric-line '+l.type;div.textContent=l.text;}
    box.appendChild(div);
  });
  const lines=[...box.querySelectorAll('.lyric-line:not(.spacer)')];
  LYRICS.filter(l=>l.type!=='spacer').forEach((l,i)=>{
    const t=setTimeout(()=>{
      box.querySelectorAll('.lyric-line.active').forEach(e=>{e.classList.remove('active');e.classList.add('done');});
      lines[i].classList.add('shown','active');
    },l.t*1000);
    songTimers.push(t);
  });
  const sw=performance.now();
  songInterval=setInterval(()=>{
    const el=(performance.now()-sw)/1000;
    document.getElementById('progFill').style.width=Math.min(100,(el/SONG_DUR)*100)+'%';
    document.getElementById('timeLbl').textContent=`${Math.floor(el/60)}:${Math.floor(el%60).toString().padStart(2,'0')}`;
    if(el>=SONG_DUR)clearInterval(songInterval);
  },100);
}

/* ── WAND SHOWER ── */
function launchWandShower(){
  const c=document.getElementById('wandShower');c.innerHTML='';
  const pool=['🪄','🪄','🪄','⚡','✨','🌟','🪄','🪄','⚡','🪄'];
  let count=0;
  const iv=setInterval(()=>{
    if(count>=55){clearInterval(iv);setTimeout(()=>{c.innerHTML='';},3500);return;}
    const el=document.createElement('div');
    el.textContent=pool[~~(Math.random()*pool.length)];
    const x=Math.random()*100;const sz=Math.random()*24+18;
    const dur=(Math.random()*1.8+1.5).toFixed(2);
    const delay=(Math.random()*.25).toFixed(2);
    const wx=(Math.random()*80-40).toFixed(0);
    el.style.cssText=`position:absolute;top:-50px;left:${x}%;font-size:${sz}px;--wx:${wx}px;animation:wandFall ${dur}s ease-in ${delay}s forwards;pointer-events:none;`;
    c.appendChild(el);
    setTimeout(()=>el.remove(),(+dur+ +delay+.5)*1000);
    count++;
  },55);
}

/* ── BLOW CANDLES ── */
function blowCandles(){
  const btn=document.getElementById('blowBtn');
  btn.disabled=true;btn.textContent='✦ Wish Granted! ✦';
  document.getElementById('cakeCaption').textContent='Nox ✦ the flames fade into something magical...';
  if(sfxOn){try{const ctx=getCtx();playWhoosh(ctx);setTimeout(()=>playChime(ctx),520);}catch(e){}}
  ['fl1','fl2','fl3','fl4'].forEach(id=>{const el=document.getElementById(id);if(el)el.style.display='none';});
  launchWandShower();confetti();
  if(bgmOn&&!bgmRunning){try{startBGM();}catch(e){}}
  setTimeout(()=>goTo(2),2600);
}

/* confetti */
function confetti(){
  const cols=['#F5D5D5','#E8DEFF','#D4F0E8','#FFE8D6','#C9A96E','#B897C2'];
  for(let i=0;i<50;i++){
    const el=document.createElement('div');el.className='cbit';const sz=Math.random()*7+3;
    el.style.cssText=`left:${Math.random()*100}%;width:${sz}px;height:${sz}px;background:${cols[~~(Math.random()*cols.length)]};border-radius:${Math.random()>.5?'50%':'3px'};animation-duration:${Math.random()*2+2}s;animation-delay:${Math.random()*.4}s;`;
    document.body.appendChild(el);setTimeout(()=>el.remove(),(Math.random()*2+3)*1000);
  }
}

/* ── TRANSITIONS ── */
let currentSlide=1;
const ovIcons=['⚡','🪄','✦','🌟','🦉','✨'];
function goTo(n){
  if(n===currentSlide)return;
  const ov=document.getElementById('overlay');
  document.getElementById('ovIcon').textContent=ovIcons[~~(Math.random()*ovIcons.length)];
  ov.classList.add('show');
  setTimeout(()=>{
    document.querySelectorAll('.slide').forEach(s=>s.classList.remove('active'));
    document.getElementById('slide'+n).classList.add('active');
    currentSlide=n;
    document.querySelectorAll('.s-dot').forEach((d,i)=>d.classList.toggle('active',i===currentSlide-1));
    if(n===2&&!songStarted){songStarted=true;startSong();}
    if(n===3)initFC();
    if(n===4)initEnvelope();
    setTimeout(()=>ov.classList.remove('show'),300);
  },300);
}

/* ── ENVELOPE ── */
let envOpened=false;
function initEnvelope(){
  // reset in case revisited
  if(!envOpened){
    document.getElementById('envWrap').classList.remove('open');
    document.getElementById('openHint').style.display='block';
    document.getElementById('harryReveal').classList.remove('show');
    document.getElementById('envScene').style.display='flex';
  }
}

function openEnvelope(){
  if(envOpened)return;
  envOpened=true;
  const wrap=document.getElementById('envWrap');
  const hint=document.getElementById('openHint');
  wrap.classList.add('open');
  hint.textContent='✦ Opening... ✦';
  if(sfxOn){try{playPaperRustle(getCtx());}catch(e){}}
  setTimeout(()=>{
    hint.style.display='none';
    document.getElementById('envScene').style.display='none';
    document.getElementById('harryReveal').classList.add('show');
    startHPSpeech();
  },1400);
}

/* ── HARRY SPEECH ── */
const HP_WORDS=`Hey, Didi. I know this might be a bit unexpected — me, showing up like this. But honestly, Hermione told me about your birthday, and she gave me that look. You know the one. So here I am. I just wanted to say... Happy Birthday. Not in a spell-casting, wand-waving kind of way. Just genuinely, from the heart. Because the people who love us — the ones who stay with us through every chapter — those people deserve to be celebrated properly. And from everything I can see, you are one of those people. So have a brilliant day, Didi. Eat too much cake. Laugh until it hurts. And know that somewhere out there, the wizarding world is quietly raising a butterbeer to you. You deserve every bit of magic that comes your way. 🎂✨`.split(' ');

let hpDone=false;
function startHPSpeech(){
  if(hpDone)return;hpDone=true;
  const container=document.getElementById('hpText');container.innerHTML='';
  HP_WORDS.forEach((word,i)=>{
    const sp=document.createElement('span');sp.className='w';
    sp.textContent=word+(i<HP_WORDS.length-1?' ':'');
    container.appendChild(sp);
    setTimeout(()=>{
      sp.classList.add('show');
      if(sfxOn&&i%12===0&&i>0){try{const ctx=getCtx();tone(ctx,392,ctx.currentTime,.2,'sine',.022);}catch(e){}}
    },i*115);
  });
  const total=HP_WORDS.length*115;
  setTimeout(()=>{
    document.getElementById('hpFooter').classList.add('show');
    setTimeout(()=>document.getElementById('hpHearts').classList.add('show'),500);
    if(sfxOn){try{playChime(getCtx());}catch(e){}}
    confetti();
  },total+400);
}

/* ── FLASHCARDS ── */
const CARDS=[
  {icon:'⚡',label:'Our first adventure together',bg:'linear-gradient(145deg,#F7F0FF,#FFF0F5)',tag:'Our first adventure 🪄'},
  {icon:'🪄',label:'My favourite witch & best didi',bg:'linear-gradient(145deg,#FFF0F5,#FFF8E8)',tag:'My favourite witch 💜'},
  {icon:'🦉',label:'Always by each other\'s side',bg:'linear-gradient(145deg,#F0FFF8,#F0EAFF)',tag:'Always together 🌟'},
  {icon:'⭐',label:'You are my Hogwarts, Didi',bg:'linear-gradient(145deg,#FFFBF0,#FFF0F5)',tag:'You\'re my Hogwarts ⭐'},
];
let curCard=0,isFlipped=false,photos=new Array(4).fill(null),tags=CARDS.map(c=>c.tag),fcReady=false;

function initFC(){
  if(fcReady)return;fcReady=true;
  const w=document.getElementById('fcDots');w.innerHTML='';
  CARDS.forEach((_,i)=>{const d=document.createElement('div');d.className='fc-dot'+(i===0?' active':'');d.onclick=()=>jumpCard(i);w.appendChild(d);});
  renderCard(0);
}
function renderCard(idx){
  isFlipped=false;
  const stage=document.getElementById('fcStage');stage.innerHTML='';
  const data=CARDS[idx];
  const card=document.createElement('div');card.className='flashcard';card.id='aC';
  const front=document.createElement('div');front.className='card-face card-front';front.style.background=data.bg;
  front.innerHTML=`<div class="gem gem-tl"></div><div class="gem gem-tr"></div><div class="gem gem-bl"></div><div class="gem gem-br"></div><div class="front-num">MEMORY ${idx+1} OF ${CARDS.length}</div><div class="front-icon">${data.icon}</div><div class="front-label">${data.label}</div><div class="front-hint">✦ tap to reveal ✦</div>`;
  const back=document.createElement('div');back.className='card-face card-back';
  const inner=document.createElement('div');inner.className='back-inner';
  const pa=document.createElement('div');pa.className='photo-area';
  const inp=document.createElement('input');inp.type='file';inp.accept='image/*';
  inp.onchange=()=>{const f=inp.files[0];if(!f)return;const r=new FileReader();r.onload=e=>{photos[idx]=e.target.result;isFlipped=true;renderCard(idx);};r.readAsDataURL(f);};
  if(photos[idx]){
    const img=document.createElement('img');img.src=photos[idx];pa.appendChild(img);
    const cb=document.createElement('button');cb.className='change-btn';cb.textContent='Change';cb.onclick=e=>{e.stopPropagation();inp.click();};pa.appendChild(cb);
  }else{
    const z=document.createElement('div');z.className='add-zone';z.innerHTML='<div class="plus">+</div><div class="add-txt">Add your photo</div>';z.onclick=e=>{e.stopPropagation();inp.click();};pa.appendChild(z);
  }
  pa.appendChild(inp);inner.appendChild(pa);
  const strip=document.createElement('div');strip.className='tag-strip';strip.innerHTML=`<span class="tag-icon">${data.icon}</span>`;
  const ti=document.createElement('input');ti.type='text';ti.className='tag-input';ti.placeholder='Write a memory caption...';ti.value=tags[idx];
  ti.onclick=e=>e.stopPropagation();ti.oninput=()=>{tags[idx]=ti.value;};
  strip.appendChild(ti);inner.appendChild(strip);
  back.appendChild(inner);card.appendChild(front);card.appendChild(back);
  card.onclick=()=>{isFlipped=!isFlipped;card.classList.toggle('flipped',isFlipped);if(sfxOn){try{playFlip(getCtx());}catch(e){}}document.getElementById('flipTip').textContent=isFlipped?'Tap to flip back · edit caption below':'Tap to flip · swipe or arrows to browse';};
  let sx=0;
  card.addEventListener('touchstart',e=>{sx=e.touches[0].clientX;},{passive:true});
  card.addEventListener('touchend',e=>{const dx=e.changedTouches[0].clientX-sx;if(Math.abs(dx)>45){dx<0?nextCard():prevCard();}},{passive:true});
  stage.appendChild(card);
  if(isFlipped)requestAnimationFrame(()=>requestAnimationFrame(()=>card.classList.add('flipped')));
  document.getElementById('fcCount').textContent=`${idx+1} / ${CARDS.length}`;
  document.querySelectorAll('.fc-dot').forEach((d,i)=>d.classList.toggle('active',i===idx));
}
function nextCard(){if(curCard>=CARDS.length-1)return;if(sfxOn){try{playSwipe(getCtx());}catch(e){}}curCard++;renderCard(curCard);}
function prevCard(){if(curCard<=0)return;if(sfxOn){try{playSwipe(getCtx());}catch(e){}}curCard--;renderCard(curCard);}
function jumpCard(idx){if(idx===curCard)return;curCard=idx;renderCard(idx);}

/* start BGM on first tap */
document.addEventListener('click',()=>{if(bgmOn&&!bgmRunning){try{startBGM();}catch(e){}}},{once:true});
</script>
</body>
</html>

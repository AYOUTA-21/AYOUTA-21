<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aya Brahimi — README</title>
<style>
  @keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-10px)}}
  @keyframes fadeIn{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:translateY(0)}}
  @keyframes shimmer{0%,100%{opacity:1}50%{opacity:0.5}}
  @keyframes bounce{0%,100%{transform:translateY(0)}50%{transform:translateY(-6px)}}
  @keyframes blink{0%,100%{opacity:1}50%{opacity:0}}
  @keyframes slide-l{from{opacity:0;transform:translateX(-20px)}to{opacity:1;transform:translateX(0)}}
  @keyframes slide-r{from{opacity:0;transform:translateX(20px)}to{opacity:1;transform:translateX(0)}}
  @keyframes pop{0%{transform:scale(0.7);opacity:0}80%{transform:scale(1.05)}100%{transform:scale(1);opacity:1}}
  @keyframes orbit{from{transform:rotate(0deg) translateX(50px) rotate(0deg)}to{transform:rotate(360deg) translateX(50px) rotate(-360deg)}}
  @keyframes typing{from{width:0}to{width:100%}}
  @keyframes bar-grow{from{width:0}to{width:var(--w)}}
  @keyframes wiggle{0%,100%{transform:rotate(-8deg)}50%{transform:rotate(8deg)}}

  *{box-sizing:border-box;margin:0;padding:0}

  body {
    font-family: system-ui, sans-serif;
    background: #f9f9fb;
    display: flex;
    justify-content: center;
    padding: 2rem 1rem;
    min-height: 100vh;
  }

  .wrap{max-width:680px;width:100%;padding:1rem}

  .hero{
    position:relative;
    background:#fce7f3;
    border-radius:20px;
    padding:2rem 1.5rem 1.5rem;
    text-align:center;
    overflow:hidden;
    animation:fadeIn .5s ease both;
    border:1px solid #f4c0d1;
    margin-bottom:1rem;
  }

  .hero-avatar{
    width:72px;height:72px;border-radius:50%;
    background:linear-gradient(135deg,#a78bfa,#f472b6);
    display:flex;align-items:center;justify-content:center;
    font-size:28px;font-weight:600;color:white;
    margin:0 auto 1rem;
    animation:float 3s ease-in-out infinite;
    position:relative;z-index:1;
  }

  .orbiter{
    position:absolute;top:50%;left:50%;
    width:16px;height:16px;margin:-8px;
    font-size:14px;
    animation:orbit var(--spd) linear infinite;
    animation-delay:var(--del);
  }

  .hero h1{font-size:22px;font-weight:600;color:#7c3aed;margin-bottom:.3rem;animation:fadeIn .5s .1s ease both}
  .hero-sub{font-size:14px;color:#be185d;animation:fadeIn .5s .2s ease both}

  .cursor{
    display:inline-block;width:2px;height:1em;
    background:#be185d;
    animation:blink 1s step-end infinite;
    vertical-align:middle;margin-left:1px;
  }

  .badge-row{display:flex;flex-wrap:wrap;gap:6px;justify-content:center;margin-top:.9rem;animation:fadeIn .5s .3s ease both}
  .badge{font-size:11px;font-weight:600;padding:3px 10px;border-radius:99px;animation:pop .4s ease both;animation-delay:var(--del,0s)}
  .b-pink{background:#fce7f3;color:#9d174d}
  .b-purple{background:#ede9fe;color:#5b21b6}
  .b-blue{background:#dbeafe;color:#1e40af}
  .b-green{background:#dcfce7;color:#166534}

  .card{
    background:#fff;
    border:1px solid #e5e5e5;
    border-radius:14px;
    padding:1.1rem 1.3rem;
    margin-bottom:.9rem;
    animation:fadeIn .5s ease both;
    animation-delay:var(--del,0s);
  }

  .card-title{font-size:14px;font-weight:600;color:#111;margin-bottom:.8rem;display:flex;align-items:center;gap:7px}
  .card-icon{animation:wiggle 2s ease-in-out infinite}

  .grid2{display:grid;grid-template-columns:1fr 1fr;gap:8px}

  .mini-card{
    background:#f9f9f9;border-radius:10px;
    padding:.8rem;border:1px solid #e5e5e5;
    animation:pop .4s ease both;animation-delay:var(--del,0s);
  }
  .mini-icon{font-size:20px;margin-bottom:5px;display:block}
  .mini-title{font-size:13px;font-weight:600;color:#111}
  .mini-desc{font-size:12px;color:#555;line-height:1.5;margin-top:2px}

  .step{display:flex;gap:10px;align-items:flex-start;margin-bottom:.75rem;animation:slide-l .4s ease both;animation-delay:var(--del,0s)}
  .step-dot{
    width:26px;height:26px;border-radius:50%;
    display:flex;align-items:center;justify-content:center;
    font-size:12px;font-weight:600;flex-shrink:0;color:white;
    animation:bounce 2s ease-in-out infinite;animation-delay:var(--del,0s);
  }
  .step-text{font-size:13px;color:#555;line-height:1.6;padding-top:3px}
  .step-text strong{color:#111;font-weight:600}

  .bar-row{margin-bottom:.7rem;animation:slide-r .4s ease both;animation-delay:var(--del,0s)}
  .bar-label{display:flex;justify-content:space-between;font-size:12px;color:#666;margin-bottom:4px}
  .bar-track{height:8px;background:#f3f3f3;border-radius:99px;overflow:hidden}
  .bar-fill{height:100%;border-radius:99px;animation:bar-grow 1.2s ease both;animation-delay:var(--del,0s)}

  .fact-box{
    background:#fce7f3;border-radius:12px;
    padding:.9rem 1rem;font-size:13px;color:#9d174d;
    line-height:1.6;border:1px solid #f4c0d1;
    animation:fadeIn .5s ease both;animation-delay:.9s;
    margin-bottom:1rem;
  }

  .dots{display:flex;justify-content:center;gap:5px;margin:.75rem 0}
  .dot{width:8px;height:8px;border-radius:50%;animation:bounce 1.2s ease-in-out infinite;animation-delay:var(--del)}

  .typing-line{
    font-size:13px;color:#555;
    font-family:monospace;
    overflow:hidden;white-space:nowrap;
    animation:typing 2s steps(30,end) .5s both;
    border-right:2px solid #a78bfa;
    margin-bottom:.8rem;
  }
</style>
</head>
<body>
<div class="wrap">

  <!-- HERO -->
  <div class="hero">
    <div style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);width:120px;height:120px;pointer-events:none;opacity:.35">
      <div class="orbiter" style="--spd:4s;--del:0s">🌸</div>
      <div class="orbiter" style="--spd:6s;--del:-2s">⭐</div>
      <div class="orbiter" style="--spd:5s;--del:-1s">💜</div>
      <div class="orbiter" style="--spd:7s;--del:-3s">✨</div>
    </div>
    <div class="hero-avatar">AB</div>
    <h1>Hi there, I'm Aya Brahimi 👋</h1>
    <div class="hero-sub">20 y/o · learner · building one tag at a time<span class="cursor"></span></div>
    <div class="badge-row">
      <span class="badge b-pink" style="--del:.3s">🌸 Algeria</span>
      <span class="badge b-purple" style="--del:.4s">💜 20 years old</span>
      <span class="badge b-blue" style="--del:.5s">🎓 student</span>
      <span class="badge b-green" style="--del:.6s">🌱 learning every day</span>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="card" style="--del:.1s">
    <div class="card-title"><span class="card-icon">🧠</span> About me</div>
    <div class="typing-line">const aya = { age: 20, passion: "web dev", status: "learning..." };</div>
    <div style="font-size:13px;color:#555;line-height:1.7">
      I'm a 20-year-old beginner developer from Algeria, currently on a journey to learn
      <strong style="color:#111">HTML</strong>,
      <strong style="color:#111">CSS</strong>, and
      <strong style="color:#111">JavaScript</strong>.
      Every day I write a little more code and understand a little more — and that feeling is incredible 🌟
    </div>
  </div>

  <!-- LEARNING -->
  <div class="card" style="--del:.2s">
    <div class="card-title"><span class="card-icon">🛠️</span> What I'm learning</div>
    <div class="grid2">
      <div class="mini-card" style="--del:.3s">
        <span class="mini-icon">🌐</span>
        <div class="mini-title">HTML</div>
        <div class="mini-desc">Building the structure of web pages</div>
      </div>
      <div class="mini-card" style="--del:.4s">
        <span class="mini-icon">🎨</span>
        <div class="mini-title">CSS</div>
        <div class="mini-desc">Making everything look beautiful</div>
      </div>
      <div class="mini-card" style="--del:.5s">
        <span class="mini-icon">⚡</span>
        <div class="mini-title">JavaScript</div>
        <div class="mini-desc">Adding life and interactivity</div>
      </div>
      <div class="mini-card" style="--del:.6s">
        <span class="mini-icon">🔮</span>
        <div class="mini-title">Coming soon...</div>
        <div class="mini-desc">React? Python? The journey continues</div>
      </div>
    </div>
  </div>

  <!-- PROGRESS -->
  <div class="card" style="--del:.35s">
    <div class="card-title"><span class="card-icon">📈</span> My progress so far</div>
    <div class="bar-row" style="--del:.4s">
      <div class="bar-label"><span>HTML</span><span>getting there! 🌱</span></div>
      <div class="bar-track"><div class="bar-fill" style="--w:65%;width:65%;background:#f472b6"></div></div>
    </div>
    <div class="bar-row" style="--del:.55s">
      <div class="bar-label"><span>CSS</span><span>loving the colors! 🎨</span></div>
      <div class="bar-track"><div class="bar-fill" style="--w:55%;width:55%;background:#a78bfa"></div></div>
    </div>
    <div class="bar-row" style="--del:.7s">
      <div class="bar-label"><span>JavaScript</span><span>just started ✨</span></div>
      <div class="bar-track"><div class="bar-fill" style="--w:30%;width:30%;background:#60a5fa"></div></div>
    </div>
  </div>

  <!-- GOALS -->
  <div class="card" style="--del:.5s">
    <div class="card-title"><span class="card-icon">🚀</span> My learning goals</div>
    <div class="step" style="--del:.55s">
      <div class="step-dot" style="background:#f472b6;--del:.1s">1</div>
      <div class="step-text"><strong>Master HTML & CSS</strong> — build beautiful, responsive layouts</div>
    </div>
    <div class="step" style="--del:.65s">
      <div class="step-dot" style="background:#a78bfa;--del:.2s">2</div>
      <div class="step-text"><strong>Learn JavaScript</strong> — make my pages interactive and fun</div>
    </div>
    <div class="step" style="--del:.75s">
      <div class="step-dot" style="background:#60a5fa;--del:.3s">3</div>
      <div class="step-text"><strong>Build my first real project</strong> — a full website I'm proud of</div>
    </div>
    <div class="step" style="--del:.85s">
      <div class="step-dot" style="background:#34d399;--del:.4s">4</div>
      <div class="step-text"><strong>Keep going, never give up</strong> — every expert was once a beginner 💪</div>
    </div>
  </div>

  <!-- FUN FACT -->
  <div class="fact-box">
    🌸 <strong>Fun fact:</strong> I'm a girl who codes — and that makes the tech world a better and more beautiful place. Welcome to my corner of the internet!
  </div>

  <!-- DOTS -->
  <div class="dots">
    <div class="dot" style="background:#f472b6;--del:0s"></div>
    <div class="dot" style="background:#a78bfa;--del:.1s"></div>
    <div class="dot" style="background:#60a5fa;--del:.2s"></div>
    <div class="dot" style="background:#34d399;--del:.3s"></div>
    <div class="dot" style="background:#fbbf24;--del:.4s"></div>
  </div>

</div>
</body>
</html>

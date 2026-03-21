
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Syne:wght@400;700;800&display=swap');
  *{box-sizing:border-box;margin:0;padding:0}
  .wrap{background:#0a0e17;color:#e2e8f0;font-family:'JetBrains Mono',monospace;padding:0 0 40px 0;min-height:100vh}
  .hero{background:#0a0e17;padding:48px 32px 32px;border-bottom:1px solid #1e2d40;position:relative;overflow:hidden}
  .hero-grid{position:absolute;inset:0;opacity:0.07;background-image:linear-gradient(#00d4aa 1px,transparent 1px),linear-gradient(90deg,#00d4aa 1px,transparent 1px);background-size:40px 40px}
  .hero-accent{position:absolute;top:0;right:0;width:320px;height:320px;background:radial-gradient(circle at 80% 20%,rgba(0,212,170,0.15),transparent 60%);pointer-events:none}
  .tag-line{font-size:11px;color:#00d4aa;letter-spacing:3px;text-transform:uppercase;margin-bottom:16px;font-family:'JetBrains Mono',monospace}
  .hero-name{font-family:'Syne',sans-serif;font-size:42px;font-weight:800;color:#fff;line-height:1.1;margin-bottom:6px}
  .hero-name span{color:#00d4aa}
  .hero-sub{font-size:13px;color:#64748b;margin-bottom:24px;letter-spacing:1px}
  .code-intro{background:#0f1923;border:1px solid #1e2d40;border-left:3px solid #00d4aa;border-radius:8px;padding:20px 24px;font-size:12px;line-height:1.9;max-width:560px;position:relative;z-index:1}
  .code-intro .kw{color:#7c9cbf}.code-intro .cl{color:#e2985c}.code-intro .st{color:#a3e8d0}.code-intro .cm{color:#3d5266}.code-intro .val{color:#d4a0ff}.code-intro .num{color:#f9c74f}
  .dot-row{display:flex;gap:6px;margin-bottom:14px}
  .dot{width:10px;height:10px;border-radius:50%}
  .dot-r{background:#ff5f57}.dot-y{background:#febc2e}.dot-g{background:#28c840}
  .links{display:flex;gap:10px;flex-wrap:wrap;margin-top:24px;position:relative;z-index:1}
  .lbtn{display:inline-flex;align-items:center;gap:6px;padding:8px 16px;border-radius:6px;font-size:11px;font-family:'JetBrains Mono',monospace;letter-spacing:1px;text-decoration:none;border:1px solid #1e3a52;color:#94a3b8;background:#0f1923;transition:all .2s}
  .lbtn:hover{border-color:#00d4aa;color:#00d4aa}
  .lbtn.primary{background:#00d4aa;color:#0a0e17;border-color:#00d4aa;font-weight:700}
  .lbtn.primary:hover{background:#00b899}

  .section{padding:28px 32px}
  .section-label{font-size:10px;letter-spacing:3px;color:#00d4aa;text-transform:uppercase;margin-bottom:20px;display:flex;align-items:center;gap:10px}
  .section-label::after{content:'';flex:1;height:1px;background:#1e2d40}

  .skill-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(130px,1fr));gap:10px}
  .skill-chip{background:#0f1923;border:1px solid #1e2d40;border-radius:6px;padding:10px 12px;font-size:11px;color:#94a3b8;display:flex;align-items:center;gap:8px;transition:all .2s}
  .skill-chip:hover{border-color:#00d4aa;color:#00d4aa}
  .skill-chip .dot-s{width:6px;height:6px;border-radius:50%;background:#00d4aa;flex-shrink:0}
  .skill-chip.hot .dot-s{background:#f9c74f}
  .skill-chip.ai .dot-s{background:#d4a0ff}

  .stat-row{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-top:4px}
  .stat-card{background:#0f1923;border:1px solid #1e2d40;border-radius:8px;padding:16px;text-align:center}
  .stat-num{font-size:28px;font-weight:700;color:#fff;font-family:'Syne',sans-serif}
  .stat-num span{color:#00d4aa}
  .stat-lbl{font-size:10px;color:#3d5266;letter-spacing:2px;margin-top:4px;text-transform:uppercase}

  .exp-card{background:#0f1923;border:1px solid #1e2d40;border-radius:8px;padding:20px;display:flex;gap:16px;align-items:flex-start;margin-bottom:10px}
  .exp-icon{width:40px;height:40px;background:#0a1a2e;border:1px solid #00d4aa;border-radius:6px;display:flex;align-items:center;justify-content:center;font-size:16px;flex-shrink:0}
  .exp-title{font-size:13px;font-weight:700;color:#e2e8f0;font-family:'Syne',sans-serif}
  .exp-co{font-size:11px;color:#00d4aa;margin-top:2px}
  .exp-date{font-size:10px;color:#3d5266;margin-top:4px}
  .exp-badge{display:inline-block;background:#0a1a2e;border:1px solid #1e3a52;border-radius:4px;padding:2px 8px;font-size:10px;color:#94a3b8;margin-top:8px}

  .cert-row{display:grid;grid-template-columns:1fr 1fr;gap:8px}
  .cert-item{background:#0f1923;border:1px solid #1e2d40;border-radius:6px;padding:12px;font-size:11px;color:#64748b;display:flex;gap:8px;align-items:flex-start}
  .cert-item .ci{color:#00d4aa;flex-shrink:0}

  .footer-bar{background:#0f1923;border-top:1px solid #1e2d40;padding:20px 32px;display:flex;justify-content:space-between;align-items:center;font-size:11px;color:#3d5266}
  .footer-bar .pulse{display:inline-flex;align-items:center;gap:6px;color:#00d4aa}
  .pulse-dot{width:6px;height:6px;border-radius:50%;background:#00d4aa;animation:pulse 2s infinite}
  @keyframes pulse{0%,100%{opacity:1}50%{opacity:0.3}}

  .social-row{display:flex;gap:8px;flex-wrap:wrap;margin-top:4px}
  .sbtn{padding:7px 14px;border-radius:5px;font-size:10px;letter-spacing:1px;border:1px solid #1e2d40;color:#64748b;background:#0f1923;font-family:'JetBrains Mono',monospace}

  .divider{height:1px;background:#1e2d40;margin:0 32px}
</style>

<div class="wrap">
  <div class="hero">
    <div class="hero-grid"></div>
    <div class="hero-accent"></div>
    <div class="tag-line">// backend engineer & python api specialist</div>
    <div class="hero-name">Rajesh<br><span>Balasubramaniam</span></div>
    <div class="hero-sub">$ uptime --career: 2.3+ yrs · DEIENAMI · Palakkad, Kerala</div>

    <div class="code-intro">
      <div class="dot-row"><div class="dot dot-r"></div><div class="dot dot-y"></div><div class="dot dot-g"></div></div>
      <span class="kw">class</span> <span class="cl">Engineer</span><span style="color:#e2e8f0">:</span><br>
      &nbsp;&nbsp;<span class="st">role</span> &nbsp;&nbsp;&nbsp;&nbsp;= <span class="val">"Software Engineer @ DEIENAMI"</span><br>
      &nbsp;&nbsp;<span class="st">exp</span> &nbsp;&nbsp;&nbsp;&nbsp;= <span class="num">2.3</span><span style="color:#e2e8f0"> years</span><br>
      &nbsp;&nbsp;<span class="st">core</span> &nbsp;&nbsp;&nbsp;= [<span class="val">"Python"</span>, <span class="val">"FastAPI"</span>, <span class="val">"Django"</span>]<br>
      &nbsp;&nbsp;<span class="st">cloud</span> &nbsp;&nbsp;= [<span class="val">"AWS"</span>, <span class="val">"Docker"</span>, <span class="val">"Nginx"</span>]<br>
      &nbsp;&nbsp;<span class="st">passion</span> = [<span class="val">"AI/ML"</span>, <span class="val">"API Architecture"</span>]<br>
      &nbsp;&nbsp;<span class="st">status</span> &nbsp;= <span class="val">"open to opportunities"</span> <span class="cm">🟢</span>
    </div>

    <div class="links">
      <a class="lbtn primary" href="#">⟶ Portfolio</a>
      <a class="lbtn" href="#">Resume</a>
      <a class="lbtn" href="#">LinkedIn</a>
      <a class="lbtn" href="#">rajesh@gmail.com</a>
    </div>
  </div>

  <div class="section">
    <div class="section-label">stat.overview()</div>
    <div class="stat-row">
      <div class="stat-card"><div class="stat-num">2<span>.3+</span></div><div class="stat-lbl">Years Experience</div></div>
      <div class="stat-card"><div class="stat-num" style="color:#d4a0ff">10<span>+</span></div><div class="stat-lbl">Certifications</div></div>
      <div class="stat-card"><div class="stat-num" style="color:#f9c74f">∞</div><div class="stat-lbl">Coffee Consumed</div></div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section">
    <div class="section-label">tech.stack.load()</div>
    <div style="margin-bottom:14px;font-size:10px;color:#3d5266;letter-spacing:2px">PYTHON · BACKEND · APIs</div>
    <div class="skill-grid">
      <div class="skill-chip hot">Python</div>
      <div class="skill-chip hot">FastAPI</div>
      <div class="skill-chip hot">Django REST</div>
      <div class="skill-chip">Go / Gin</div>
      <div class="skill-chip">Node.js</div>
      <div class="skill-chip">Express.js</div>
      <div class="skill-chip">PostgreSQL</div>
      <div class="skill-chip">MongoDB</div>
      <div class="skill-chip">DynamoDB</div>
      <div class="skill-chip">Docker</div>
      <div class="skill-chip">AWS</div>
      <div class="skill-chip">Nginx</div>
    </div>
    <div style="margin:14px 0 10px;font-size:10px;color:#3d5266;letter-spacing:2px">AI · ML · INTELLIGENCE</div>
    <div class="skill-grid">
      <div class="skill-chip ai">TensorFlow</div>
      <div class="skill-chip ai">PyTorch</div>
      <div class="skill-chip ai">HuggingFace</div>
      <div class="skill-chip ai">Ollama</div>
      <div class="skill-chip ai">Stable Diff.</div>
      <div class="skill-chip ai">NumPy/Pandas</div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section">
    <div class="section-label">experience.log()</div>
    <div class="exp-card">
      <div class="exp-icon">⚙</div>
      <div>
        <div class="exp-title">Software Engineer</div>
        <div class="exp-co">DEIENAMI</div>
        <div class="exp-date">Jan 2024 → Present · Full-time</div>
        <div class="exp-badge">● ACTIVE PROCESS</div>
      </div>
    </div>
    <div class="exp-card">
      <div class="exp-icon">🐍</div>
      <div>
        <div class="exp-title">Python Full Stack Developer</div>
        <div class="exp-co">Luminar Technolab</div>
        <div class="exp-date">Internship · Completed</div>
        <div class="exp-badge">✓ EXITED</div>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section">
    <div class="section-label">certs.list()</div>
    <div class="cert-row">
      <div class="cert-item"><span class="ci">▸</span>Infosys Power Programmer</div>
      <div class="cert-item"><span class="ci">▸</span>IBM Data Science Tools</div>
      <div class="cert-item"><span class="ci">▸</span>Agile · SCRUM · KANBAN</div>
      <div class="cert-item"><span class="ci">▸</span>React.JS Complete Course</div>
      <div class="cert-item"><span class="ci">▸</span>Python & Django Framework</div>
      <div class="cert-item"><span class="ci">▸</span>Web Development Cert.</div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section">
    <div class="section-label">social.connect()</div>
    <div class="social-row">
      <div class="sbtn">LinkedIn</div>
      <div class="sbtn">Instagram</div>
      <div class="sbtn">Facebook</div>
      <div class="sbtn">Gmail</div>
    </div>
  </div>

  <div class="footer-bar">
    <span class="pulse"><span class="pulse-dot"></span>Available for work</span>
    <span>"First solve the problem. Then write the code."</span>
  </div>
</div>

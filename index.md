<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>aniliitmbsc1974 — GitHub Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }


  :root {
    --bg: #fafaf8;
    --bg-card: #ffffff;
    --bg-surface: #f4f3ef;
    --text-primary: #1a1a18;
    --text-secondary: #5a5a55;
    --text-muted: #9a9a93;
    --border: #e8e7e2;
    --border-hover: #c8c7c0;
    --accent: #2563eb;
    --accent-light: #eff6ff;
    --accent-text: #1d4ed8;
    --green: #16a34a;
    --green-light: #f0fdf4;
    --radius-sm: 6px;
    --radius-md: 10px;
    --radius-lg: 16px;
    --radius-xl: 24px;
  }


  html { scroll-behavior: smooth; }


  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--bg);
    color: var(--text-primary);
    line-height: 1.6;
    min-height: 100vh;
  }


  /* NAV */
  nav {
    position: sticky; top: 0; z-index: 100;
    background: rgba(250,250,248,0.9);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    padding: 0 2rem;
    display: flex; align-items: center; justify-content: space-between;
    height: 56px;
  }
  .nav-brand {
    font-family: 'DM Mono', monospace;
    font-size: 14px; font-weight: 500;
    color: var(--text-primary); text-decoration: none;
    display: flex; align-items: center; gap: 8px;
  }
  .nav-brand .dot {
    width: 8px; height: 8px; border-radius: 50%;
    background: var(--green); display: inline-block;
  }
  .nav-links { display: flex; gap: 1.5rem; }
  .nav-links a {
    font-size: 13px; color: var(--text-secondary);
    text-decoration: none; transition: color 0.15s;
  }
  .nav-links a:hover { color: var(--text-primary); }


  /* HERO */
  .hero {
    max-width: 900px; margin: 0 auto;
    padding: 4rem 2rem 3rem;
    display: grid; grid-template-columns: auto 1fr; gap: 2.5rem;
    align-items: start;
    animation: fadeUp 0.5s ease both;
  }


  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }


  .avatar-col { display: flex; flex-direction: column; align-items: center; gap: 1rem; }


  .avatar-frame {
    width: 120px; height: 120px;
    border-radius: 50%;
    border: 3px solid var(--border);
    overflow: hidden;
    background: var(--bg-surface);
    display: flex; align-items: center; justify-content: center;
    font-family: 'DM Serif Display', serif;
    font-size: 40px; color: var(--text-muted);
  }
  .avatar-frame img { width: 100%; height: 100%; object-fit: cover; }


  .contact-links { display: flex; flex-direction: column; gap: 6px; width: 100%; }
  .contact-link {
    display: flex; align-items: center; gap: 7px;
    font-size: 12px; color: var(--text-secondary);
    text-decoration: none; padding: 6px 12px;
    border: 1px solid var(--border);
    border-radius: var(--radius-sm);
    transition: all 0.15s; background: var(--bg-card);
    justify-content: center;
  }
  .contact-link:hover { border-color: var(--accent); color: var(--accent); background: var(--accent-light); }
  .contact-link svg { width: 14px; height: 14px; flex-shrink: 0; }


  .hero-info { padding-top: 6px; }
  .hero-name {
    font-family: 'DM Serif Display', serif;
    font-size: 36px; line-height: 1.15;
    color: var(--text-primary); margin-bottom: 4px;
  }
  .hero-handle {
    font-family: 'DM Mono', monospace;
    font-size: 14px; color: var(--text-muted); margin-bottom: 12px;
  }
  .hero-bio {
    font-size: 15px; color: var(--text-secondary);
    max-width: 520px; line-height: 1.7; margin-bottom: 1.25rem;
  }


  .hero-meta { display: flex; gap: 1rem; flex-wrap: wrap; margin-bottom: 1.5rem; }
  .meta-item {
    display: flex; align-items: center; gap: 5px;
    font-size: 13px; color: var(--text-secondary);
  }
  .meta-item svg { width: 14px; height: 14px; color: var(--text-muted); }


  .stats-chips { display: flex; gap: 10px; flex-wrap: wrap; }
  .chip {
    display: flex; align-items: center; gap: 8px;
    background: var(--bg-surface); border: 1px solid var(--border);
    border-radius: var(--radius-sm); padding: 6px 14px;
    font-size: 13px; color: var(--text-secondary);
  }
  .chip strong { color: var(--text-primary); font-weight: 500; }


  /* METRICS */
  .metrics-section {
    max-width: 900px; margin: 0 auto; padding: 0 2rem 2rem;
    animation: fadeUp 0.5s 0.1s ease both;
  }
  .metrics-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 10px; }
  .metric-card {
    background: var(--bg-card); border: 1px solid var(--border);
    border-radius: var(--radius-md); padding: 16px 18px;
    transition: border-color 0.15s;
  }
  .metric-card:hover { border-color: var(--border-hover); }
  .metric-label { font-size: 11px; color: var(--text-muted); text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 6px; }
  .metric-value { font-family: 'DM Serif Display', serif; font-size: 28px; color: var(--text-primary); }


  /* DIVIDER */
  .section-divider {
    max-width: 900px; margin: 0 auto; padding: 0 2rem 1.5rem;
  }
  .section-label {
    font-family: 'DM Mono', monospace;
    font-size: 11px; color: var(--text-muted);
    text-transform: uppercase; letter-spacing: 0.12em;
    padding-bottom: 10px; border-bottom: 1px solid var(--border);
    display: flex; align-items: center; justify-content: space-between;
  }


  /* CONTROLS */
  .controls-section {
    max-width: 900px; margin: 0 auto; padding: 0 2rem 1rem;
    display: flex; gap: 10px; flex-wrap: wrap; align-items: center;
  }
  .search-wrap { position: relative; flex: 1; min-width: 200px; }
  .search-wrap svg { position: absolute; left: 11px; top: 50%; transform: translateY(-50%); width: 15px; height: 15px; color: var(--text-muted); pointer-events: none; }
  .search-input {
    width: 100%; padding: 9px 12px 9px 34px;
    border: 1px solid var(--border); border-radius: var(--radius-md);
    font-family: 'DM Sans', sans-serif; font-size: 13px;
    color: var(--text-primary); background: var(--bg-card);
    outline: none; transition: border-color 0.15s;
  }
  .search-input:focus { border-color: var(--accent); }
  .search-input::placeholder { color: var(--text-muted); }


  .sort-select {
    padding: 9px 12px; border: 1px solid var(--border);
    border-radius: var(--radius-md); font-family: 'DM Sans', sans-serif;
    font-size: 13px; color: var(--text-primary); background: var(--bg-card);
    outline: none; cursor: pointer;
  }
  .count-label { font-size: 12px; color: var(--text-muted); white-space: nowrap; }


  /* LANG FILTER */
  .lang-filter {
    max-width: 900px; margin: 0 auto; padding: 0 2rem 1.25rem;
    display: flex; gap: 6px; flex-wrap: wrap;
  }
  .lang-pill {
    display: inline-flex; align-items: center; gap: 5px;
    font-size: 12px; padding: 4px 12px;
    border: 1px solid var(--border); border-radius: 20px;
    cursor: pointer; color: var(--text-secondary);
    background: var(--bg-card); transition: all 0.12s;
    font-family: 'DM Sans', sans-serif;
  }
  .lang-pill:hover, .lang-pill.active {
    border-color: var(--accent); color: var(--accent-text);
    background: var(--accent-light);
  }
  .lang-dot { width: 8px; height: 8px; border-radius: 50%; }


  /* REPOS GRID */
  .repos-section { max-width: 900px; margin: 0 auto; padding: 0 2rem 4rem; }
  .repos-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(270px, 1fr)); gap: 12px; }


  .repo-card {
    background: var(--bg-card); border: 1px solid var(--border);
    border-radius: var(--radius-md); padding: 1.125rem 1.25rem;
    display: flex; flex-direction: column; gap: 8px;
    text-decoration: none; color: inherit;
    transition: border-color 0.12s, transform 0.12s;
  }
  .repo-card:hover { border-color: var(--accent); transform: translateY(-2px); }


  .repo-name {
    font-size: 14px; font-weight: 500; color: var(--accent-text);
    display: flex; align-items: center; gap: 6px;
  }
  .repo-icon { width: 14px; height: 14px; color: var(--text-muted); flex-shrink: 0; }
  .repo-desc { font-size: 12px; color: var(--text-secondary); line-height: 1.55; flex: 1; }
  .repo-topics { display: flex; gap: 5px; flex-wrap: wrap; }
  .repo-topic {
    font-size: 11px; padding: 2px 8px; border-radius: 20px;
    background: var(--accent-light); color: var(--accent-text);
  }
  .repo-footer { display: flex; gap: 12px; align-items: center; flex-wrap: wrap; margin-top: 2px; }
  .repo-lang { display: flex; align-items: center; gap: 5px; font-size: 11px; color: var(--text-secondary); }
  .repo-stat { display: flex; align-items: center; gap: 3px; font-size: 11px; color: var(--text-secondary); }
  .repo-stat svg, .repo-lang-dot { width: 11px; height: 11px; }
  .repo-lang-dot { border-radius: 50%; display: inline-block; }
  .repo-updated { font-size: 11px; color: var(--text-muted); margin-left: auto; }


  .empty-state { text-align: center; padding: 4rem 2rem; color: var(--text-muted); font-size: 14px; }


  /* FOOTER */
  footer {
    border-top: 1px solid var(--border); padding: 1.5rem 2rem;
    text-align: center; font-size: 12px; color: var(--text-muted);
    font-family: 'DM Mono', monospace;
  }
  footer a { color: var(--accent-text); text-decoration: none; }


  /* RESPONSIVE */
  @media (max-width: 640px) {
    .hero { grid-template-columns: 1fr; gap: 1.5rem; padding: 2rem 1.25rem 1.5rem; }
    .avatar-col { flex-direction: row; align-items: flex-start; gap: 1rem; }
    .avatar-frame { width: 72px; height: 72px; font-size: 26px; }
    .contact-links { flex-direction: row; width: auto; }
    .hero-name { font-size: 26px; }
    .metrics-grid { grid-template-columns: repeat(2, 1fr); }
    .metrics-section, .controls-section, .lang-filter, .repos-section, .section-divider { padding-left: 1.25rem; padding-right: 1.25rem; }
  }
</style>
</head>
<body>


<nav>
  <a class="nav-brand" href="#">
    <span class="dot"></span>
    aniliitmbsc1974
  </a>
  <div class="nav-links">
    <a href="#repos">repositories</a>
    <a href="https://github.com/aniliitmbsc1974" target="_blank">github ↗</a>
  </div>
</nav>


<!-- HERO -->
<section class="hero" id="top">
  <div class="avatar-col">
    <div class="avatar-frame" id="avatarEl">AN</div>
    <div class="contact-links" id="contactLinks">
      <a class="contact-link" href="https://github.com/aniliitmbsc1974" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.166 6.839 9.489.5.092.682-.217.682-.483 0-.237-.009-.868-.013-1.703-2.782.604-3.369-1.34-3.369-1.34-.454-1.156-1.11-1.463-1.11-1.463-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0112 6.836c.85.004 1.705.114 2.504.336 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.202 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.743 0 .267.18.579.688.481C19.138 20.163 22 16.418 22 12c0-5.523-4.477-10-10-10z"/></svg>
        github
      </a>
    </div>
  </div>
  <div class="hero-info">
    <div class="hero-name" id="nameEl">Loading…</div>
    <div class="hero-handle" id="handleEl">@aniliitmbsc1974</div>
    <div class="hero-bio" id="bioEl">Fetching profile…</div>
    <div class="hero-meta" id="metaEl"></div>
    <div class="stats-chips" id="statsEl"></div>
  </div>
</section>


<!-- METRICS -->
<section class="metrics-section">
  <div class="metrics-grid">
    <div class="metric-card"><div class="metric-label">repositories</div><div class="metric-value" id="mRepos">–</div></div>
    <div class="metric-card"><div class="metric-label">total stars</div><div class="metric-value" id="mStars">–</div></div>
    <div class="metric-card"><div class="metric-label">total forks</div><div class="metric-value" id="mForks">–</div></div>
    <div class="metric-card"><div class="metric-label">followers</div><div class="metric-value" id="mFollowers">–</div></div>
  </div>
</section>


<!-- REPOS -->
<div class="section-divider" id="repos">
  <div class="section-label">
    <span>repositories</span>
    <span id="countLabel" style="font-size:11px;"></span>
  </div>
</div>


<div class="controls-section">
  <div class="search-wrap">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
    <input class="search-input" id="searchInput" type="text" placeholder="search by name or description…" oninput="renderRepos()" />
  </div>
  <select class="sort-select" id="sortSel" onchange="renderRepos()">
    <option value="updated">recently updated</option>
    <option value="stars">most stars</option>
    <option value="name">name a–z</option>
    <option value="forks">most forks</option>
  </select>
</div>


<div class="lang-filter" id="langFilter"></div>


<section class="repos-section">
  <div id="reposContainer"><div class="empty-state">loading repositories…</div></div>
</section>


<footer>
  built with the <a href="https://docs.github.com/en/rest" target="_blank">github api</a> &nbsp;·&nbsp;
  <a href="https://github.com/aniliitmbsc1974" target="_blank">aniliitmbsc1974</a>
</footer>


<script>
const LANG_COLORS={JavaScript:'#f1e05a',TypeScript:'#3178c6',Python:'#3572A5',Java:'#b07219','C++':'#f34b7d',C:'#555555','C#':'#178600',Go:'#00ADD8',Rust:'#dea584',Ruby:'#701516',PHP:'#4F5D95',Swift:'#F05138',Kotlin:'#A97BFF',HTML:'#e34c26',CSS:'#563d7c',Shell:'#89e051',Dart:'#00B4AB',Vue:'#41b883',R:'#198CE7',Jupyter:'#DA5B0B',Scala:'#c22d40'};
let allRepos=[],activeLang='all';


function timeAgo(d){const days=Math.floor((Date.now()-new Date(d))/86400000);if(days===0)return'today';if(days===1)return'yesterday';if(days<30)return days+'d ago';const m=Math.floor(days/30);if(m<12)return m+'mo ago';return Math.floor(m/12)+'y ago';}


function icon(path){return`<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" style="width:13px;height:13px;display:inline-block;vertical-align:-2px;">${path}</svg>`;}


async function init(){
  try{
    const[uRes,rRes]=await Promise.all([fetch('https://api.github.com/users/aniliitmbsc1974'),fetch('https://api.github.com/users/aniliitmbsc1974/repos?per_page=100&sort=updated')]);
    if(!uRes.ok)throw new Error(uRes.status===404?'User not found':'GitHub API error');
    const u=await uRes.json();
    const repos=await rRes.json();
    allRepos=repos.filter(r=>!r.fork);


    if(u.avatar_url)document.getElementById('avatarEl').innerHTML=`<img src="${u.avatar_url}" alt="avatar">`;
    document.getElementById('nameEl').textContent=u.name||u.login;
    document.getElementById('handleEl').textContent='@'+u.login;
    document.getElementById('bioEl').textContent=u.bio||'Open source developer on GitHub.';


    const meta=[];
    if(u.location)meta.push(`${icon('<path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7z"/><circle cx="12" cy="9" r="2.5"/>')} ${u.location}`);
    if(u.company)meta.push(`${icon('<rect x="2" y="7" width="20" height="14" rx="2"/><path d="M16 7V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v2"/>')} ${u.company}`);
    if(u.blog)meta.push(`<a href="${u.blog}" target="_blank" style="display:inline-flex;align-items:center;gap:4px;color:var(--accent-text);text-decoration:none;">${icon('<circle cx="12" cy="12" r="10"/><path d="M12 2a14.5 14.5 0 0 1 0 20 14.5 14.5 0 0 1 0-20"/><path d="M2 12h20"/>')} ${u.blog.replace(/^https?:\/\//,'')}</a>`);
    document.getElementById('metaEl').innerHTML=meta.map(m=>`<span class="meta-item">${m}</span>`).join('');


    document.getElementById('statsEl').innerHTML=`
      <span class="chip"><strong>${u.followers}</strong> followers</span>
      <span class="chip"><strong>${u.following}</strong> following</span>
      <span class="chip"><strong>${u.public_repos}</strong> repos</span>`;


    const ts=allRepos.reduce((s,r)=>s+r.stargazers_count,0);
    const tf=allRepos.reduce((s,r)=>s+r.forks_count,0);
    document.getElementById('mRepos').textContent=u.public_repos;
    document.getElementById('mStars').textContent=ts;
    document.getElementById('mForks').textContent=tf;
    document.getElementById('mFollowers').textContent=u.followers;


    buildLangFilter();
    renderRepos();
  }catch(e){
    document.getElementById('nameEl').textContent='aniliitmbsc1974';
    document.getElementById('bioEl').textContent='';
    document.getElementById('reposContainer').innerHTML=`<div class="empty-state">${e.message==='User not found'?'GitHub user not found.':'Could not load profile. The GitHub API may be rate-limited — try refreshing in a moment.'}</div>`;
  }
}


function buildLangFilter(){
  const langs=[...new Set(allRepos.map(r=>r.language).filter(Boolean))].sort();
  const bar=document.getElementById('langFilter');
  bar.innerHTML=`<button class="lang-pill active" onclick="setLang('all',this)">all languages</button>`;
  langs.forEach(l=>{
    const col=LANG_COLORS[l]||'#888';
    const b=document.createElement('button');
    b.className='lang-pill';
    b.onclick=function(){setLang(l,this);};
    b.innerHTML=`<span class="lang-dot" style="background:${col}"></span>${l}`;
    bar.appendChild(b);
  });
}


function setLang(lang,el){
  activeLang=lang;
  document.querySelectorAll('.lang-pill').forEach(p=>p.classList.remove('active'));
  el.classList.add('active');
  renderRepos();
}


function renderRepos(){
  const q=document.getElementById('searchInput').value.toLowerCase();
  const sort=document.getElementById('sortSel').value;
  let repos=allRepos.filter(r=>{
    const ml=activeLang==='all'||r.language===activeLang;
    const ms=!q||r.name.toLowerCase().includes(q)||(r.description||'').toLowerCase().includes(q);
    return ml&&ms;
  });
  repos.sort((a,b)=>{
    if(sort==='stars')return b.stargazers_count-a.stargazers_count;
    if(sort==='forks')return b.forks_count-a.forks_count;
    if(sort==='name')return a.name.localeCompare(b.name);
    return new Date(b.updated_at)-new Date(a.updated_at);
  });
  document.getElementById('countLabel').textContent=repos.length+' repos';
  if(!repos.length){document.getElementById('reposContainer').innerHTML='<div class="empty-state">no repositories match your search or filter</div>';return;}
  const grid=document.createElement('div');
  grid.className='repos-grid';
  repos.forEach(r=>{
    const col=LANG_COLORS[r.language]||'#9a9a93';
    const topics=(r.topics||[]).slice(0,3).map(t=>`<span class="repo-topic">${t}</span>`).join('');
    const a=document.createElement('a');
    a.className='repo-card';
    a.href=r.html_url;
    a.target='_blank';
    a.rel='noopener noreferrer';
    a.innerHTML=`
      <div class="repo-name">
        <svg class="repo-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/><path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/></svg>
        ${r.name}
      </div>
      <div class="repo-desc">${r.description||'<span style="color:var(--text-muted);font-style:italic">no description provided</span>'}</div>
      ${topics?`<div class="repo-topics">${topics}</div>`:''}
      <div class="repo-footer">
        ${r.language?`<span class="repo-lang"><span class="repo-lang-dot" style="background:${col};display:inline-block;"></span>${r.language}</span>`:''}
        ${r.stargazers_count?`<span class="repo-stat"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>${r.stargazers_count}</span>`:''}
        ${r.forks_count?`<span class="repo-stat"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><circle cx="12" cy="18" r="3"/><circle cx="6" cy="6" r="3"/><circle cx="18" cy="6" r="3"/><path d="M18 9v1a2 2 0 0 1-2 2H8a2 2 0 0 1-2-2V9"/><line x1="12" y1="12" x2="12" y2="15"/></svg>${r.forks_count}</span>`:''}
        <span class="repo-updated">${timeAgo(r.updated_at)}</span>
      </div>`;
    grid.appendChild(a);
  });
  document.getElementById('reposContainer').innerHTML='';
  document.getElementById('reposContainer').appendChild(grid);
}


init();
</script>
</body>
</html>





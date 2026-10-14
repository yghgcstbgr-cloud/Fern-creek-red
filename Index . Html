<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>JCPS Soccer League Central</title>
<style>
:root{--bg:#0b1220;--panel:#121e30;--panel2:#1b2a41;--line:#2b3c52;--text:#f4f7fb;--muted:#b5c4d8;--lime:#b6f36a}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--text);font:15px/1.45 system-ui,-apple-system,Segoe UI,Roboto,sans-serif}
button,input,select{font:inherit}
button{cursor:pointer;border:0;border-radius:10px;padding:10px 13px;background:var(--lime);color:#15200d;font-weight:750}
button.secondary{background:#26374d;color:var(--text);border:1px solid var(--line)}
button.danger{background:#572b35;color:#fff;border:1px solid #8a4651}
button.small{padding:6px 9px;font-size:13px}
header{padding:20px max(16px,calc((100% - 1100px)/2));background:#101c31;border-bottom:1px solid var(--line)}
.brand{display:flex;align-items:center;gap:13px}
.crest{display:grid;place-items:center;background:var(--lime);color:#13200a;width:48px;height:48px;border-radius:13px;font-size:25px}
.brand h1{font-size:21px;margin:0}
.brand p{margin:2px 0 0;color:var(--lime);font-size:11px;font-weight:800;letter-spacing:1.2px}
.wrap{max-width:1100px;margin:auto;padding:18px 16px 40px}
.hero{background:linear-gradient(130deg,#1b2a41,#122034);padding:20px;border:1px solid var(--line);border-radius:18px;margin-bottom:16px}
.hero small,.muted{color:var(--muted)}
.hero h2{margin:5px 0 8px;font-size:clamp(23px,4vw,34px)}
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-top:17px}
.stat{background:#0f1a2b;padding:13px;border-radius:12px}
.stat strong{display:block;font-size:24px}
.stat span{color:var(--muted);font-size:12px}
nav{display:flex;gap:7px;flex-wrap:wrap;margin:16px 0}
nav button{background:#172338;color:var(--muted);border:1px solid var(--line)}
nav button.active{background:var(--lime);color:#15200d;border-color:var(--lime)}
.panel{background:var(--panel);border:1px solid var(--line);border-radius:16px;padding:17px;margin:12px 0}
.panel h3{margin:0 0 12px}
.grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:12px}
.grid3{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:10px}
label{display:block;color:var(--muted);font-size:13px;margin:0 0 5px}
input,select{width:100%;padding:10px;background:#0c1727;color:var(--text);border:1px solid #34465d;border-radius:9px;min-width:0}
.field{margin-bottom:12px}
.actions{display:flex;gap:8px;flex-wrap:wrap;align-items:center}
.tablewrap{overflow:auto}
table{border-collapse:collapse;width:100%;min-width:540px}
th,td{text-align:left;padding:10px 8px;border-bottom:1px solid var(--line);font-size:13px}
th{color:var(--muted);font-weight:650}
td.num,th.num{text-align:right}
.pill{display:inline-block;padding:3px 8px;border-radius:99px;background:#26374d;color:#dce8f8;font-size:11px}
.match{background:#0f1a2b;border:1px solid var(--line);padding:12px;border-radius:12px;margin:9px 0}
.matchteams{display:grid;grid-template-columns:1fr auto 1fr;gap:10px;align-items:center}
.away{text-align:right}
.score{font-size:18px;font-weight:850;color:var(--lime);white-space:nowrap}
.empty{padding:22px;text-align:center;color:var(--muted);border:1px dashed var(--line);border-radius:12px}
.notice{background:#203a2b;color:#d6ffb5;border:1px solid #42643b;border-radius:10px;padding:10px;margin:10px 0}
.warning{background:#3a2e1b;color:#ffe1a2;border:1px solid #72572b;border-radius:10px;padding:10px;margin:10px 0}
.team-list{max-height:430px;overflow:auto}
.teamrow{display:flex;justify-content:space-between;gap:12px;padding:9px 0;border-bottom:1px solid var(--line)}
footer{text-align:center;color:var(--muted);font-size:12px;padding:18px}
@media(max-width:650px){
.grid,.grid3{grid-template-columns:1fr}
.panel{padding:13px}
.hero{padding:16px}
header{padding:17px 16px}
.matchteams{font-size:13px}
}
</style>
</head>
<body>
<header>
  <div class="brand">
    <div class="crest">⚽</div>
    <div>
      <h1>JCPS SOCCER</h1>
      <p>SCHOOL LEAGUE MANAGEMENT</p>
    </div>
  </div>
</header>

<main class="wrap">
<section class="hero">
  <small>LEAGUE CENTRAL · 2026–27</small>
  <h2 id="heroLeague">JCPS DIV 1 JV</h2>
  <div class="muted">Fixtures · Rankings · Tournaments · Results</div>
  <div class="stats">
    <div class="stat"><strong id="schoolCount">33</strong><span>Registered schools</span></div>
    <div class="stat"><strong id="fixtureCount">0</strong><span>Fixtures</span></div>
    <div class="stat"><strong id="leagueCount">1</strong><span>Leagues</span></div>
  </div>
</section>
<nav id="nav"></nav>
<div id="notice" aria-live="polite"></div>
<section id="content"></section>
<footer>JCPS Soccer League Central · Browser prototype</footer>
</main>

<script>
"use strict";

const SCHOOLS=[
"Jctms","Shawnee Academy","Carrithers","Crosby","Eco Trail",
"Farnsley","Highland","Hudson","Tomas Jefferson Academy",
"TJ Knight Middle","Kammer","Lassiter","Meyzeek","Moore Middle",
"Newburgh","Noee Middle","Olmsted Academy S","Olmsted Academy N",
"Ramsey","Stuart","Westport","Barret Traditional","Brown Middle",
"Web Dubois Academy","James Academy","Johnson Traditional",
"Western Middle School","B Bernheim Middle School",
"B Mt. Washington Middle School","B Hebron Middle School",
"B Eastside Middle School","B Zoneton Middle School",
"B Bullitt Lick Middle School"
];

const MAIN="JCPS DIV 1 JV";
const KEY="jcpsSoccerLeague_v1";
const TABS=["Home","Leagues","Fixtures","Rankings","Teams","Tournaments","Admin"];

let activeTab="Home";
let selectedLeagueId="main";
let state=loadState();
let noticeTimer;

function uid(){
  return Math.random().toString(36).slice(2,9)+Date.now().toString(36).slice(-4);
}

function defaultState(){
  return {
    schools:SCHOOLS.slice(),
    leagues:[{
      id:"main",
      name:MAIN,
      isMain:true,
      levels:["A"],
      fixtures:[],
      tournaments:[]
    }]
  };
}

function loadState(){
  try{
    const x=JSON.parse(localStorage.getItem(KEY));
    if(x&&Array.isArray(x.leagues)&&Array.isArray(x.schools))return x;
  }catch(e){}
  return defaultState();
}

function save(){
  try{
    localStorage.setItem(KEY,JSON.stringify(state));
    render();
  }catch(e){
    notify("Could not save in this browser. Export a backup from Admin.",true);
  }
}

function league(){
  return state.leagues.find(l=>l.id===selectedLeagueId)||state.leagues[0];
}

function esc(s){
  return String(s??"").replace(/[&<>"']/g,c=>({
    "&":"&amp;",
    "<":"&lt;",
    ">":"&gt;",
    '"':"&quot;",
    "'":"&#39;"
  }[c]));
}

function teams(l,all=false){
  return state.schools.flatMap(name=>
    (all?["A","B","C"]:(l.levels||["A"])).map(level=>({
      id:name+"::"+level,
      label:name+" "+level,
      name,
      level
    }))
  );
}

function teamOptions(l,selected="",all=false){
  return `<option value="">Select team</option>`+
    teams(l,all).map(t=>
      `<option value="${esc(t.id)}" ${t.id===selected?"selected":""}>${esc(t.label)}</option>`
    ).join("");
}

function notify(msg,warn=false){
  const el=document.getElementById("notice");
  el.innerHTML=`<div class="${warn?"warning":"notice"}">${esc(msg)}</div>`;
  clearTimeout(noticeTimer);
  noticeTimer=setTimeout(()=>el.innerHTML="",5000);
}

/* Navigation and Create League shortcut */
function nav(){
  document.getElementById("nav").innerHTML=
    TABS.map(t=>
      `<button data-tab="${t}" class="${activeTab===t?"active":""}">${t}</button>`
    ).join("")+
    `<button data-create-league="true">＋ Create League</button>`;

  document.querySelectorAll("[data-tab]").forEach(b=>{
    b.onclick=()=>{
      const tab=b.dataset.tab;

      if(tab==="Admin"){
        const entered=prompt("Enter admin password:");
        if(entered!=="1291"){
          if(entered!==null)notify("Incorrect admin password.",true);
          return;
        }
      }

      activeTab=tab;
      render();
    };
  });

  const create=document.querySelector("[data-create-league]");
  if(create){
    create.onclick=()=>{
      activeTab="Leagues";
      render();

      const form=document.getElementById("leagueForm");
      if(form){
        form.scrollIntoView({behavior:"smooth",block:"start"});
        form.querySelector('input[name="name"]').focus();
      }
    };
  }
}

function standings(l){
  const map=new Map(
    teams(l).map(t=>[t.id,{
      ...t,p:0,w:0,d:0,l:0,gf:0,ga:0,pts:0
    }])
  );

  for(const m of l.fixtures){
    if(m.status!=="Final"||m.homeScore==null||m.awayScore==null)continue;

    const h=map.get(m.home);
    const a=map.get(m.away);
    if(!h||!a)continue;

    h.p++;
    a.p++;
    h.gf+=+m.homeScore;
    h.ga+=+m.awayScore;
    a.gf+=+m.awayScore;
    a.ga+=+m.homeScore;

    if(+m.homeScore>+m.awayScore){
      h.w++;
      a.l++;
      h.pts+=3;
    }else if(+m.homeScore<+m.awayScore){
      a.w++;
      h.l++;
      a.pts+=3;
    }else{
      h.d++;
      a.d++;
      h.pts++;
      a.pts++;
    }
  }

  return [...map.values()].sort((a,b)=>
    b.pts-a.pts||
    (b.gf-b.ga)-(a.gf-a.ga)||
    b.gf-a.gf||
    a.label.localeCompare(b.label)
  );
}

function dateText(s){
  if(!s)return "Date not set";
  try{
    return new Date(s+"T12:00:00").toLocaleDateString(undefined,{
      month:"short",day:"numeric",year:"numeric"
    });
  }catch(e){
    return s;
  }
}

function fixtureCard(m,l){
  const h=teams(l).find(t=>t.id===m.home);
  const a=teams(l).find(t=>t.id===m.away);

  return `<div class="match">
    <div class="row">
      <span class="muted">${esc(dateText(m.date))} · ${esc(m.competition||l.name)}</span>
      <span class="pill">${esc(m.status)}</span>
    </div>
    <div class="matchteams" style="margin:12px 0">
      <strong>${esc(h?.label||"Unknown team")}</strong>
      <span class="score">${m.status==="Final"?`${m.homeScore} – ${m.awayScore}`:"VS"}</span>
      <strong class="away">${esc(a?.label||"Unknown team")}</strong>
    </div>
    <div class="actions">
      <button class="small secondary" data-edit-match="${m.id}">Edit match</button>
      <button class="small danger" data-delete-match="${m.id}">Delete</button>
    </div>
  </div>`;
}

function homeView(l){
  const upcoming=l.fixtures.slice()
    .sort((a,b)=>(a.date||"").localeCompare(b.date||""))
    .slice(0,4);

  return `<div class="panel">
    <h3>Welcome to ${esc(l.name)}</h3>
    <p class="muted">Manage your school soccer league, match schedule, rankings and tournaments. The initial schedule starts empty so you can enter the official fixtures.</p>
    <div class="actions">
      <button data-go="Fixtures">Manage fixtures</button>
      <button class="secondary" data-go="Rankings">View rankings</button>
      <button class="secondary" data-go="Tournaments">Tournaments</button>
    </div>
  </div>
  <div class="panel">
    <h3>Upcoming fixtures</h3>
    ${upcoming.length
      ?upcoming.map(m=>fixtureCard(m,l)).join("")
      :'<div class="empty">No fixtures yet. Open Fixtures to create the schedule.</div>'}
  </div>
  <div class="panel">
    <h3>League rules</h3>
    <ul class="muted">
      <li>Each team plays every other team twice when you generate the double round-robin schedule.</li>
      <li>Rankings calculate automatically from saved final scores: win = 3 points, draw = 1, loss = 0.</li>
      <li>The school list is fixed. A, B and C are selectable team levels.</li>
    </ul>
  </div>`;
}

function fixturesView(l){
  return `<div class="panel">
    <h3>Create a fixture</h3>
    <p class="muted">Choose both teams from the registered list. The same team cannot play itself.</p>
    <form id="fixtureForm">
      <div class="grid">
        <div class="field">
          <label>Home team</label>
          <select name="home" required>${teamOptions(l)}</select>
        </div>
        <div class="field">
          <label>Away team</label>
          <select name="away" required>${teamOptions(l)}</select>
        </div>
        <div class="field">
          <label>Date</label>
          <input type="date" name="date">
        </div>
        <div class="field">
          <label>Competition / round label</label>
          <input name="competition" placeholder="${esc(l.name)}">
        </div>
      </div>
      <button type="submit">Add fixture</button>
      <button type="button" class="secondary" id="generateSchedule">Generate double round-robin</button>
    </form>
  </div>
  <div class="panel">
    <div class="row">
      <h3>Fixtures & results</h3>
      <span class="pill">${l.fixtures.length} matches</span>
    </div>
    ${l.fixtures.length
      ?l.fixtures.slice().sort((a,b)=>(a.date||"").localeCompare(b.date||"")).map(m=>fixtureCard(m,l)).join("")
      :'<div class="empty">No fixtures have been added yet.</div>'}
  </div>`;
}

function rankingsView(l){
  const rows=standings(l);

  return `<div class="panel">
    <h3>${esc(l.name)} rankings</h3>
    <p class="muted">Updated automatically from fixtures marked Final. Teams with equal points are sorted by goal difference, then goals scored.</p>
    <div class="tablewrap">
      <table>
        <thead>
          <tr>
            <th>#</th><th>Team</th>
            <th class="num">P</th><th class="num">W</th>
            <th class="num">D</th><th class="num">L</th>
            <th class="num">GF</th><th class="num">GA</th>
            <th class="num">GD</th><th class="num">Pts</th>
          </tr>
        </thead>
        <tbody>
          ${rows.map((t,i)=>`<tr>
            <td>${i+1}</td>
            <td>${esc(t.label)}</td>
            <td class="num">${t.p}</td>
            <td class="num">${t.w}</td>
            <td class="num">${t.d}</td>
            <td class="num">${t.l}</td>
            <td class="num">${t.gf}</td>
            <td class="num">${t.ga}</td>
            <td class="num">${t.gf-t.ga}</td>
            <td class="num"><strong>${t.pts}</strong></td>
          </tr>`).join("")}
        </tbody>
      </table>
    </div>
  </div>`;
}

function teamsView(l){
  return `<div class="panel">
    <h3>Registered schools and team levels</h3>
    <p class="muted">All 33 school names are locked. Each school can have A, B and C entries. Enable levels for this league below; it won't add new schools.</p>
    <form id="levelsForm">
      <div class="actions">
        ${["A","B","C"].map(x=>`<label style="display:flex;align-items:center;gap:6px;background:#0c1727;padding:10px;border-radius:9px">
          <input type="checkbox" name="level" value="${x}" ${(l.levels||["A"]).includes(x)?"checked":""}> ${x} teams
        </label>`).join("")}
      </div>
      <p><button type="submit">Save league team levels</button></p>
    </form>
    <input id="schoolSearch" placeholder="Search schools…">
    <div class="team-list" id="schoolList">
      ${state.schools.map((s,i)=>`<div class="teamrow" data-school="${esc(s.toLowerCase())}">
        <span>${i+1}. ${esc(s)}</span>
        <span class="muted">${(l.levels||["A"]).map(x=>esc(x)).join(" / ")}</span>
      </div>`).join("")}
    </div>
  </div>`;
}

function tournamentsView(l){
  return `<div class="panel">
    <h3>Create tournament</h3>
    <form id="tournamentForm">
      <div class="grid">
        <div class="field">
          <label>Tournament name</label>
          <input name="name" required placeholder="e.g. JCPS Cup">
        </div>
        <div class="field">
          <label>Format</label>
          <select name="format">
            <option value="groups">Group stage + knockout</option>
            <option value="knockout">Knockout only</option>
            <option value="league">League format</option>
          </select>
        </div>
        <div class="field">
          <label>Teams per group (group stage only)</label>
          <select name="groupSize">
            <option>3</option><option selected>4</option><option>5</option>
          </select>
        </div>
        <div class="field">
          <label>Teams advancing per group</label>
          <select name="advance">
            <option value="1">Top 1</option>
            <option value="2" selected>Top 2</option>
          </select>
        </div>
      </div>
      <p class="muted">This creates the tournament setup. Assign its registered teams and generate the bracket in a later step; no teams are invented.</p>
      <button type="submit">Create tournament</button>
    </form>
  </div>
  <div class="panel">
    <h3>Tournaments in ${esc(l.name)}</h3>
    ${l.tournaments.length
      ?l.tournaments.map(t=>`<div class="match">
        <div class="row">
          <strong>${esc(t.name)}</strong>
          <span class="pill">${esc(t.formatLabel)}</span>
        </div>
        <p class="muted">Group size: ${t.format==="groups"?t.groupSize:"Not applicable"} · Advance: ${t.format==="groups"?t.advance:"Not applicable"}</p>
        <button class="small danger" data-delete-tournament="${t.id}">Delete tournament</button>
      </div>`).join("")
      :'<div class="empty">No tournaments created yet.</div>'}
  </div>`;
}

function leaguesView(){
  return `<div class="panel" id="leagueFormPanel">
    <h3>Create another league</h3>
    <p class="muted">Create a separate league while keeping JCPS DIV 1 JV and its data intact.</p>
    <form id="leagueForm">
      <div class="grid">
        <div class="field">
          <label>League name</label>
          <input name="name" required placeholder="e.g. JCPS DIV 2 JV">
        </div>
        <div class="field">
          <label>Starting team levels</label>
          <select name="level">
            <option value="A">A teams</option>
            <option value="B">B teams</option>
            <option value="C">C teams</option>
            <option value="ABC">A, B and C teams</option>
          </select>
        </div>
      </div>
      <button type="submit">+ Create league</button>
    </form>
  </div>
  <div class="panel">
    <h3>Your leagues</h3>
    ${state.leagues.map(l=>`<div class="match">
      <div class="row">
        <div>
          <strong>${esc(l.name)}</strong>
          <div class="muted">${l.fixtures.length} fixtures · ${l.tournaments.length} tournaments</div>
        </div>
        <span class="pill">${l.isMain?"Main league":"League"}</span>
      </div>
      <div class="actions" style="margin-top:10px">
        <button class="small" data-select-league="${l.id}">Open league</button>
        ${!l.isMain?`<button class="small danger" data-delete-league="${l.id}">Delete league</button>`:""}
      </div>
    </div>`).join("")}
  </div>`;
}

function adminView(){
  return `<div class="panel">
    <h3>Admin controls</h3>
    <p class="muted">Admin password is enabled for this prototype. Important: because this is a static GitHub Pages website, the password can be found in the page source and is not secure protection for a public site. Real protection requires server-side authentication. Browser storage is not shared between devices.</p>
    <div class="warning">Reset and delete actions permanently change the data stored in this browser. Export a backup first.</div>

    <h3>Create another league</h3>
    <form id="leagueForm">
      <div class="grid">
        <div class="field">
          <label>League name</label>
          <input name="name" required placeholder="e.g. JCPS DIV 2 JV">
        </div>
        <div class="field">
          <label>Starting team levels</label>
          <select name="level">
            <option value="A">A teams</option>
            <option value="B">B teams</option>
            <option value="C">C teams</option>
            <option value="ABC">A, B and C teams</option>
          </select>
        </div>
      </div>
      <button type="submit">Create league</button>
    </form>

    <h3 style="margin-top:22px">Manage leagues</h3>
    ${state.leagues.map(l=>`<div class="match">
      <div class="row">
        <div>
          <strong>${esc(l.name)}</strong>
          <div class="muted">${l.fixtures.length} fixtures · ${l.tournaments.length} tournaments</div>
        </div>
        <span class="pill">${l.isMain?"Main league":"League"}</span>
      </div>
      <div class="actions" style="margin-top:10px">
        <button class="small secondary" data-select-league="${l.id}">Open league</button>
        ${!l.isMain?`<button class="small danger" data-delete-league="${l.id}">Delete league</button>`:""}
      </div>
    </div>`).join("")}

    <div class="actions" style="margin-top:18px">
      <button class="secondary" id="exportData">Export backup JSON</button>
      <label class="secondary" style="padding:10px 13px;border-radius:10px;cursor:pointer">
        <input id="importData" type="file" accept="application/json" style="display:none">
        Import backup JSON
      </label>
      <button class="danger" id="resetLeague">Reset current league data</button>
      <button class="danger" id="resetAll">Reset whole website</button>
    </div>
  </div>`;
}

function render(){
  if(!state.leagues.length)state=defaultState();

  if(!state.leagues.some(l=>l.id===selectedLeagueId)){
    selectedLeagueId=state.leagues[0].id;
  }

  const l=league();

  document.getElementById("heroLeague").textContent=l.name;
  document.getElementById("schoolCount").textContent=state.schools.length;
  document.getElementById("fixtureCount").textContent=
    state.leagues.reduce((n,x)=>n+x.fixtures.length,0);
  document.getElementById("leagueCount").textContent=state.leagues.length;

  nav();

  const views={
    Home:homeView,
    Leagues:leaguesView,
    Fixtures:fixturesView,
    Rankings:rankingsView,
    Teams:teamsView,
    Tournaments:tournamentsView,
    Admin:adminView
  };

  document.getElementById("content").innerHTML=views[activeTab](l);
  bind(l);
}

function bind(l){
  document.querySelectorAll("[data-go]").forEach(b=>{
    b.onclick=()=>{
      activeTab=b.dataset.go;
      render();
    };
  });

  const ff=document.getElementById("fixtureForm");

  if(ff)ff.onsubmit=e=>{
    e.preventDefault();

    const f=new FormData(ff);
    const home=f.get("home");
    const away=f.get("away");

    if(!home||!away)return notify("Choose both teams.",true);
    if(home===away)return notify("A team cannot play itself.",true);

    l.fixtures.push({
      id:uid(),
      home,
      away,
      date:f.get("date"),
      competition:(f.get("competition")||l.name).trim(),
      status:"Scheduled",
      homeScore:null,
      awayScore:null
    });

    save();
    notify("Fixture added.");
  };

  const gen=document.getElementById("generateSchedule");

  if(gen)gen.onclick=()=>{
    const ts=teams(l);
    const expected=ts.length*(ts.length-1);

    if(!confirm(`Generate a double round-robin schedule for ${ts.length} teams? This adds ${expected} fixtures. Existing fixtures will be kept.`))return;

    const exists=new Set(l.fixtures.map(m=>[m.home,m.away].join("|")));
    let count=0;

    for(let i=0;i<ts.length;i++){
      for(let j=i+1;j<ts.length;j++){
        for(const [h,a] of [[ts[i].id,ts[j].id],[ts[j].id,ts[i].id]]){
          const key=h+"|"+a;

          if(!exists.has(key)){
            l.fixtures.push({
              id:uid(),
              home:h,
              away:a,
              date:"",
              competition:l.name,
              status:"Scheduled",
              homeScore:null,
              awayScore:null
            });

            exists.add(key);
            count++;
          }
        }
      }
    }

    save();
    notify(`Added ${count} fixtures. Set dates and scores by editing each match.`);
  };

  document.querySelectorAll("[data-edit-match]").forEach(b=>{
    b.onclick=()=>{
      const m=l.fixtures.find(x=>x.id===b.dataset.editMatch);
      if(!m)return;

      const h=teams(l).find(t=>t.id===m.home)?.label||"Home";
      const a=teams(l).find(t=>t.id===m.away)?.label||"Away";

      const date=prompt("Match date (YYYY-MM-DD)",m.date||"");
      if(date===null)return;

      const status=prompt(
        "Status: Scheduled, Live, Half-time, Postponed, or Final",
        m.status
      );

      if(status===null)return;

      let hs=m.homeScore,as=m.awayScore;

      if(["final","live","half-time"].includes(status.toLowerCase())){
        hs=prompt(`${h} score`,hs??"0");
        if(hs===null)return;

        as=prompt(`${a} score`,as??"0");
        if(as===null)return;

        if(!/^\d+$/.test(hs)||!/^\d+$/.test(as)){
          return notify("Scores must be whole numbers zero or greater.",true);
        }

        hs=Number(hs);
        as=Number(as);
      }

      m.date=date;
      m.status=status.trim().replace(/\b\w/g,c=>c.toUpperCase());
      m.homeScore=hs===""?null:hs;
      m.awayScore=as===""?null:as;

      save();
      notify("Match updated; rankings recalculated.");
    };
  });

  document.querySelectorAll("[data-delete-match]").forEach(b=>{
    b.onclick=()=>{
      if(confirm("Delete this fixture and its result?")){
        l.fixtures=l.fixtures.filter(m=>m.id!==b.dataset.deleteMatch);
        save();
        notify("Fixture deleted.");
      }
    };
  });

  const lf=document.getElementById("levelsForm");

  if(lf)lf.onsubmit=e=>{
    e.preventDefault();

    const vals=[...lf.querySelectorAll('input[name="level"]:checked')]
      .map(x=>x.value);

    if(!vals.length)return notify("Select at least one team level.",true);

    l.levels=vals;
    save();
    notify("Team levels saved. Fixtures using a removed level remain in the schedule but won't appear in rankings.");
  };

  const search=document.getElementById("schoolSearch");

  if(search)search.oninput=()=>{
    document.querySelectorAll("[data-school]").forEach(el=>{
      el.style.display=el.dataset.school.includes(search.value.toLowerCase())?"flex":"none";
    });
  };

  const tf=document.getElementById("tournamentForm");

  if(tf)tf.onsubmit=e=>{
    e.preventDefault();

    const f=new FormData(tf);
    const format=f.get("format");

    l.tournaments.push({
      id:uid(),
      name:f.get("name").trim(),
      format,
      formatLabel:format==="groups"
        ?"Group stage + knockout"
        :format==="knockout"
          ?"Knockout only"
          :"League format",
      groupSize:Number(f.get("groupSize")),
      advance:Number(f.get("advance"))
    });

    save();
    notify("Tournament created. Add team assignments and fixtures as your next step.");
  };

  document.querySelectorAll("[data-delete-tournament]").forEach(b=>{
    b.onclick=()=>{
      if(confirm("Delete this tournament? League fixtures will not be deleted.")){
        l.tournaments=l.tournaments.filter(t=>t.id!==b.dataset.deleteTournament);
        save();
        notify("Tournament deleted.");
      }
    };
  });

  const lform=document.getElementById("leagueForm");

  if(lform)lform.onsubmit=e=>{
    e.preventDefault();

    const f=new FormData(lform);
    const name=f.get("name").trim();

    if(state.leagues.some(x=>x.name.toLowerCase()===name.toLowerCase())){
      return notify("A league with that name already exists.",true);
    }

    const level=f.get("level");
    const levels=level==="ABC"?["A","B","C"]:[level];

    const n={
      id:uid(),
      name,
      isMain:false,
      levels,
      fixtures:[],
      tournaments:[]
    };

    state.leagues.push(n);
    selectedLeagueId=n.id;
    activeTab="Home";
    save();
    notify("League created.");
  };

  document.querySelectorAll("[data-select-league]").forEach(b=>{
    b.onclick=()=>{
      selectedLeagueId=b.dataset.selectLeague;
      activeTab="Home";
      render();
    };
  });

  document.querySelectorAll("[data-delete-league]").forEach(b=>{
    b.onclick=()=>{
      const x=state.leagues.find(x=>x.id===b.dataset.deleteLeague);

      if(x&&!x.isMain&&confirm(
        `Delete "${x.name}" and all its fixtures, results and tournaments? This cannot be undone unless you have a backup.`
      )){
        state.leagues=state.leagues.filter(y=>y.id!==x.id);

        if(selectedLeagueId===x.id)selectedLeagueId="main";

        save();
        notify("League deleted.");
      }
    };
  });

  const ex=document.getElementById("exportData");

  if(ex)ex.onclick=()=>{
    const blob=new Blob([JSON.stringify(state,null,2)],{type:"application/json"});
    const url=URL.createObjectURL(blob);
    const a=document.createElement("a");

    a.href=url;
    a.download="jcps-soccer-backup.json";
    a.click();

    URL.revokeObjectURL(url);
  };

  const im=document.getElementById("importData");

  if(im)im.onchange=async()=>{
    const file=im.files[0];
    if(!file)return;

    try{
      const parsed=JSON.parse(await file.text());

      if(!Array.isArray(parsed.schools)||!Array.isArray(parsed.leagues)){
        throw Error();
      }

      if(!confirm("Replace current browser data with this backup?"))return;

      state=parsed;
      selectedLeagueId=state.leagues[0]?.id||"main";

      save();
      notify("Backup imported.");
    }catch(e){
      notify("That backup file is invalid.",true);
    }
  };

  const rl=document.getElementById("resetLeague");

  if(rl)rl.onclick=()=>{
    if(confirm(`Reset "${l.name}"? This clears its fixtures, results, and tournaments but keeps the league and registered schools.`)&&
       confirm("Are you absolutely sure? Export a backup first if you may need this data.")){
      l.fixtures=[];
      l.tournaments=[];
      save();
      notify("Current league reset.");
    }
  };

  const ra=document.getElementById("resetAll");

  if(ra)ra.onclick=()=>{
    if(confirm("Reset the entire website? This deletes all extra leagues, fixtures, results and tournaments from this browser. The main league and school list will be restored.")&&
       confirm("Final confirmation: erase all website data in this browser?")){
      state=defaultState();
      selectedLeagueId="main";
      activeTab="Home";
      save();
      notify("Website data reset.");
    }
  };
}

render();
</script>
</body>
</html>

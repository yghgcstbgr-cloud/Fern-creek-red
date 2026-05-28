<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Fern Creek Red</title>

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body{
  font-family:Arial, sans-serif;
  background:#000;
  color:black;
}

/* HEADER */
header{
  position:relative;
  height:320px;
  overflow:hidden;
  border-bottom:4px solid red;
}

header img{
  width:100%;
  height:100%;
  object-fit:cover;
  filter:brightness(45%);
}

.header-text{
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%);
  text-align:center;
}

.header-text h1{
  font-size:55px;
  color:red;
}

.header-text p{
  margin-top:10px;
  font-size:18px;
}

/* NAVBAR */
nav{
  background:#111;
  padding:15px;
  border-bottom:3px solid red;
  text-align:center;
}

nav a{
  color:white;
  text-decoration:none;
  margin:0 15px;
  font-weight:bold;
  transition:.3s;
}

nav a:hover{
  color:red;
}

/* SECTIONS */
section{
  padding:50px 20px;
}

.section-title{
  font-size:32px;
  color:red;
  margin-bottom:25px;
  border-left:5px solid red;
  padding-left:12px;
}

/* CARDS */
.cards{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
  gap:20px;
}

.card{
  background:#111;
  padding:20px;
  border:2px solid red;
  border-radius:12px;
  transition:.3s;
}

.card:hover{
  transform:translateY(-5px);
}

.card h3{
  color:red;
  margin-bottom:12px;
}

.card p{
  line-height:1.6;
}

/* PLAYER CARDS */
.player-card{
  background:#111;
  border:2px solid red;
  border-radius:15px;
  overflow:hidden;
  cursor:pointer;
  transition:.3s;
}

.player-card:hover{
  transform:translateY(-5px);
}

.player-card img{
  width:100%;
  height:250px;
  object-fit:contain;
  background:#000;
  padding:20px;
}

.player-box{
  background:red;
  padding:15px;
  text-align:center;
}

.player-box h3{
  color:white;
  margin-bottom:5px;
}

.player-box p{
  color:#ddd;
}

.player-stats{
  display:none;
  padding:20px;
  line-height:1.8;
}

/* FOOTER */
footer{
  text-align:center;
  padding:25px;
  background:#111;
  border-top:3px solid red;
  margin-top:40px;
}
</style>
</head>

<body>

<!-- HEADER -->
<header>
  <img src="https://images.unsplash.com/photo-1574629810360-7efbbe195018?q=80&w=1600&auto=format&fit=crop" alt="Soccer">

  <div class="header-text">
    <h1>Fern Creek Red</h1>
    <p>Official Team Website</p>
  </div>
</header>

<!-- NAVIGATION -->
<nav>
  <a href="#news">News</a>
  <a href="#players">Players</a>
  <a href="#scores">Scores</a>
  <a href="#games">Games</a>
  <a href="#stats">Stats</a>
</nav>

<!-- TEAM NEWS -->
<section id="news">
  <h2 class="section-title">Team News</h2>

  <div class="cards">
    <div class="card">
      <h3>📰 Elijah Lucena Set To Return</h3>

      <p>
        Fern Creek Red fans received exciting news as goalkeeper
        Elijah Lucena is expected to return next season.
      </p>

      <p style="margin-top:10px;">
        Star winger Willber Lopez is also planning to stay with
        Fern Creek Red alongside Lucena.
      </p>
    </div>
  </div>
</section>

<!-- PLAYER PROFILES -->
<section id="players">
  <h2 class="section-title">Player Profiles</h2>

  <div class="cards">

    <!-- ELIJAH -->
    <div class="player-card" onclick="toggleProfile('elijah')">

      <img 
      src="https://cdn-icons-png.flaticon.com/512/149/149071.png"
      alt="Elijah Lucena">

      <div class="player-box">
        <h3>Elijah Lucena</h3>
        <p>Mexico</p>
      </div>

      <div class="player-stats" id="elijah">
        <p><strong>Position:</strong> Goalkeeper</p>
        <p><strong>Preferred Foot:</strong> Right</p>
        <p><strong>Saves:</strong> 61</p>
        <p><strong>Recent Game:</strong> vs Spencer County</p>
      </div>

    </div>

    <!-- WILLBER -->
    <div class="player-card" onclick="toggleProfile('willber')">

      <img 
      src="https://cdn-icons-png.flaticon.com/512/149/149071.png"
      alt="Willber Lopez">

      <div class="player-box">
        <h3>Willber Lopez</h3>
        <p>Mexico</p>
      </div>

      <div class="player-stats" id="willber">
        <p><strong>Position:</strong> Winger</p>
        <p><strong>Preferred Foot:</strong> Both</p>
        <p><strong>Goals:</strong> 15</p>
        <p><strong>Recent Match:</strong> vs JYSA Sparks</p>
      </div>

    </div>

  </div>
</section>

<!-- FINAL SCORES -->
<section id="scores">
  <h2 class="section-title">Final Scores</h2>

  <div class="cards">

    <div class="card">
      <h3>Fern Creek Red 2 - 8 JYSA Inferno</h3>
    </div>

    <div class="card">
      <h3>Fern Creek Red 4 - 6 Nelson County</h3>
    </div>

    <div class="card">
      <h3>Fern Creek Red 8 - 2 JYSA Sparks</h3>
    </div>

    <div class="card">
      <h3>Fern Creek Red 3 - 2 Spencer County</h3>
    </div>

    <div class="card">
      <h3>Fern Creek Red 5 - 0 Sawyer</h3>
    </div>

    <div class="card">
      <h3>Fern Creek Red 2 - 2 JYSA</h3>
    </div>

  </div>
</section>

<!-- UPCOMING GAMES -->
<section id="games">
  <h2 class="section-title">Upcoming Games</h2>

  <div class="cards">

    <div class="card">
      <h3>Fern Creek Red vs Spencer</h3>
    </div>

    <div class="card">
      <h3>Fern Creek Red vs JYSA Sparks</h3>
    </div>

    <div class="card">
      <h3>Fern Creek Red vs JYSA Inferno</h3>
    </div>

  </div>
</section>

<!-- TEAM STATS -->
<section id="stats">
  <h2 class="section-title">Team Stats</h2>

  <div class="cards">

    <div class="card">
      <h3>⚽ Top Goal Scorer</h3>
      <p>Willber Lopez - 15 Goals</p>
    </div>

    <div class="card">
      <h3>🛡️ Top Defensive Player</h3>
      <p>Dorian</p>
    </div>

    <div class="card">
      <h3>🧤 Top Goalkeeper</h3>
      <p>Elijah Lucena - 61 Saves</p>
    </div>

    <div class="card">
      <h3>🎯 Top Assister</h3>
      <p>Angel</p>
    </div>

  </div>
</section>

<footer>
  <h3>Fern Creek Red © 2026</h3>
</footer>

<script>
function toggleProfile(id){
  const stats = document.getElementById(id);

  if(stats.style.display === "block"){
    stats.style.display = "none";
  } else {
    stats.style.display = "block";
  }
}
</script>

</body>
</html>

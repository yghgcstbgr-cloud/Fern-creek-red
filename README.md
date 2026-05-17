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
  font-family:Arial, Helvetica, sans-serif;
  background:#0d1117;
  color:white;
}

header{
  background:linear-gradient(90deg,#b30000,#ff1a1a);
  padding:20px;
  text-align:center;
  box-shadow:0 2px 10px rgba(0,0,0,0.4);
}

header h1{
  font-size:40px;
}

nav{
  display:flex;
  justify-content:center;
  gap:20px;
  background:#161b22;
  padding:15px;
  position:sticky;
  top:0;
  z-index:1000;
}

nav a{
  color:white;
  text-decoration:none;
  font-weight:bold;
  transition:0.3s;
}

nav a:hover{
  color:#ff4d4d;
}

.hero{
  height:300px;
  background:url('https://images.unsplash.com/photo-1574629810360-7efbbe195018?q=80&w=1600&auto=format&fit=crop') center/cover;
  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;
}

.hero h2{
  background:rgba(0,0,0,0.6);
  padding:20px;
  border-radius:10px;
  font-size:40px;
}

.container{
  width:90%;
  margin:auto;
  padding:40px 0;
}

.section-title{
  font-size:32px;
  margin-bottom:20px;
  border-left:5px solid red;
  padding-left:10px;
}

.cards{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
  gap:20px;
}

.card{
  background:#161b22;
  padding:20px;
  border-radius:12px;
  transition:0.3s;
  border:1px solid #2a2f37;
}

.card:hover{
  transform:translateY(-5px);
  border-color:red;
}

.card h3{
  margin-bottom:10px;
  color:#ff4d4d;
}

.match{
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-top:10px;
  padding:15px;
  background:#1f2630;
  border-radius:10px;
}

.score{
  font-size:28px;
  font-weight:bold;
  color:#ff4d4d;
}

footer{
  text-align:center;
  padding:20px;
  background:#161b22;
  margin-top:40px;
}

.badge{
  display:inline-block;
  background:red;
  padding:5px 12px;
  border-radius:20px;
  font-size:14px;
  margin-top:10px;
}
</style>
</head>

<body>

<header>
  <h1>FERN CREEK RED</h1>
  <p>Official Soccer Team Website</p>
</header>

<nav>
  <a href="#scores">Final Scores</a>
  <a href="#games">Upcoming Games</a>
  <a href="#news">Team News</a>
  <a href="#players">Team Info</a>
</nav>

<section class="hero">
  <h2>Welcome to Fern Creek Red ⚽</h2>
</section>

<div class="container">

  <!-- FINAL SCORES -->
  <section id="scores">
    <h2 class="section-title">Final Scores</h2>

    <div class="cards">

      <div class="card">
        <h3>Fern Creek Red vs JYSA Inferno</h3>

        <div class="match">
          <span>Fern Creek Red</span>
          <span class="score">2 - 8</span>
          <span>JYSA Inferno</span>
        </div>

        <div class="badge">LOSS</div>
      </div>

      <div class="card">
        <h3>Fern Creek Red vs Nelson County</h3>

        <div class="match">
          <span>Fern Creek Red</span>
          <span class="score">4 - 6</span>
          <span>Nelson County</span>
        </div>

        <div class="badge">LOSS</div>
      </div>

      <div class="card">
        <h3>Fern Creek Red vs JYSA Sparks</h3>

        <div class="match">
          <span>Fern Creek Red</span>
          <span class="score">8 - 2</span>
          <span>JYSA Sparks</span>
        </div>

        <div class="badge">WIN</div>
      </div>

      <div class="card">
        <h3>Fern Creek Red vs Spencer County</h3>

        <div class="match">
          <span>Fern Creek Red</span>
          <span class="score">3 - 2</span>
          <span>Spencer County</span>
        </div>

        <div class="badge">WIN</div>
      </div>

      <div class="card">
        <h3>Fern Creek Red vs Sawyer</h3>

        <div class="match">
          <span>Fern Creek Red</span>
          <span class="score">5 - 0</span>
          <span>Sawyer</span>
        </div>

        <div class="badge">WIN</div>
      </div>

    </div>
  </section>

  <!-- UPCOMING GAMES -->
  <section id="games" style="margin-top:60px;">
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

  <!-- TEAM NEWS -->
  <section id="news" style="margin-top:60px;">
    <h2 class="section-title">Team News</h2>

    <div class="cards">

      <div class="card">
        <h3>📰 Fern Creek Saying Goodbye To Stars Lucena & Lopez</h3>

        <p>
          Fern Creek Red is preparing to say goodbye to two of the team's
          biggest stars, Elijah Lucena and Willber Lopez.
        </p>

        <p style="margin-top:10px;">
          Lucena has already officially left the club after leading the team
          with 48 saves this season.
        </p>

        <p style="margin-top:10px;">
          Lopez also looks set to depart after scoring 15 goals this year,
          making this a difficult loss for Fern Creek Red.
        </p>

      </div>

    </div>
  </section>

  <!-- TEAM INFO -->
  <section id="players" style="margin-top:60px;">
    <h2 class="section-title">Team Information</h2>

    <div class="cards">

      <div class="card">
        <h3>⚽ Top Goal Scorer</h3>
        <p><strong>Willber Lopez</strong></p>
        <p>15 Goals This Season</p>
      </div>

      <div class="card">
        <h3>🛡️ Top Defensive Player</h3>
        <p><strong>Dorian</strong></p>
        <p>Most Tackles & Clearances</p>
      </div>

      <div class="card">
        <h3>🧤 Top Goalkeeper</h3>
        <p><strong>Elijah Lucena</strong></p>
        <p>48 Saves</p>
      </div>

      <div class="card">
        <h3>🎯 Top Assister</h3>
        <p><strong>Angel</strong></p>
        <p>11 Assists</p>
      </div>

    </div>
  </section>

</div>

<footer>
  <p>© 2026 Fern Creek Red | Official Team Website</p>
</footer>

</body>
</html>

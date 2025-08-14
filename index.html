<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Desafío 60</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body { 
      font-family: 'Segoe UI', Arial, sans-serif; 
      background: linear-gradient(135deg, #007BFF 25%, #71c7ec 100%);
      margin: 0; 
      min-height: 100vh;
      display: flex; 
      align-items: center; 
      justify-content: center; 
    }
    .card {
      background: white;
      padding: 2rem 1.5rem;
      margin: 1rem auto;
      width: 100%;
      max-width: 440px;
      border-radius: 16px;
      box-shadow: 0 8px 32px rgba(0,0,0,.10);
      text-align: center;
      position: relative;
      animation: fadeIn .7s;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: scale(.95);}
      to { opacity: 1; transform: scale(1);}
    }
    h1 {
      color: #007BFF;
      margin-bottom: .5rem;
      font-size: 2rem;
    }
    .score {
      display: flex; 
      justify-content: space-between;
      margin-bottom: 1rem;
      font-size: 1.1rem;
    }
    .joker-bar {
      margin: .5rem 0 1.5rem 0;
      font-size: 1.1rem;
      display: flex;
      gap: 1.5rem;
      justify-content: center;
      align-items: center;
    }
    .joker {
      display: flex; align-items: center; gap: .25rem;
      background: #f4f4f4;
      border-radius: 5px;
      padding: .25rem .5rem;
      font-size: 1rem;
      box-shadow: 0 2px 6px rgba(0,0,0,0.04);
    }
    .joker i {
      font-size: 1.2em;
    }
    #question h3 {
      margin-bottom: .8rem;
      font-size: 1.15rem;
    }
    #answers button {
      margin: .5rem .2rem;
      padding: .7rem 1.2rem;
      cursor: pointer;
      border: none;
      border-radius: 7px;
      background: #007BFF;
      color: white;
      font-size: 1rem;
      transition: background .2s;
      box-shadow: 0 2px 8px rgba(0,123,255,.08);
    }
    #answers button:hover, #answers button:focus {
      background: #0056b3;
      outline: 2px solid #0056b3;
    }
    .joker-btn {
      margin: .5rem .3rem;
      padding: .6rem 1.1rem;
      background: #f7c948;
      color: #222;
      border-radius: 7px;
      border: none;
      font-size: .98rem;
      cursor: pointer;
      transition: background .2s;
      box-shadow: 0 2px 8px rgba(247,201,72,0.09);
    }
    .joker-btn:hover, .joker-btn:focus {
      background: #f4b400;
      outline: 2px solid #f4b400;
    }
    .win-message {
      position: absolute;
      inset: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      background: rgba(255,255,255,0.96);
      border-radius: 16px;
      font-size: 2rem;
      color: #007BFF;
      animation: bounceWin 1s;
      z-index: 10;
    }
    @keyframes bounceWin {
      0% {transform: scale(.8); opacity: 0;}
      50% {transform: scale(1.1); opacity: 1;}
      100% {transform: scale(1); opacity: 1;}
    }
    @media (max-width: 600px) {
      .card { max-width: 97vw; padding: 1.2rem .4rem;}
      h1 { font-size: 1.3rem;}
    }
  </style>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
</head>
<body>
  <div class="card">
    <h1>Desafío 60</h1>
    <div class="score">
      <span id="level">Nivel: 1</span>
      <span id="points">Puntos: 15</span>
    </div>
    <div class="joker-bar">
      <div class="joker"><i class="fas fa-sync-alt"></i> <span id="joker-cambio">2</span></div>
      <div class="joker"><i class="fas fa-forward"></i> <span id="joker-salto">1</span></div>
    </div>
    <div id="question"></div>
    <div id="answers"></div>
    <div>
      <button class="joker-btn" onclick="useJoker('cambio')"><i class="fas fa-sync-alt"></i> Cambio de Pregunta</button>
      <button class="joker-btn" onclick="useJoker('salto')"><i class="fas fa-forward"></i> Saltar Turno</button>
    </div>
    <div id="win" style="display:none"></div>
  </div>
<script>
let level = 1;
let points = 15;
let jokers = { cambio: 2, salto: 1 };

const updateJokerUI = () => {
  document.getElementById("joker-cambio").innerText = jokers.cambio;
  document.getElementById("joker-salto").innerText = jokers.salto;
};

const questions = {
  1: [
    { q: "¿Cuál es la capital de Francia?", options: ["Madrid", "París", "Roma", "Berlín"], correct: 1, score: 1 },
    { q: "¿2 + 2 = ?", options: ["3", "4", "5", "6"], correct: 1, score: 1 }
  ],
  2: [
    { q: "¿Cuál es el planeta más grande?", options: ["Júpiter", "Saturno", "Marte", "Neptuno"], correct: 0, score: 2 },
    { q: "¿Quién pintó la Mona Lisa?", options: ["Picasso", "Leonardo Da Vinci", "Van Gogh", "Rembrandt"], correct: 1, score: 2 }
  ],
  3: [
    { q: "¿En qué continente está Egipto?", options: ["Asia", "África", "Europa", "Oceanía"], correct: 1, score: 3 },
    { q: "¿Cuántos lados tiene un hexágono?", options: ["5", "6", "7", "8"], correct: 1, score: 3 }
  ]
};

function loadQuestion() {
  const set = questions[level];
  const q = set[Math.floor(Math.random() * set.length)];
  document.getElementById("question").innerHTML = `<h3>${q.q}</h3>`;
  const ansDiv = document.getElementById("answers");
  ansDiv.innerHTML = '';
  q.options.forEach((opt, idx) => {
    let btn = document.createElement("button");
    btn.textContent = opt;
    btn.onclick = () => checkAnswer(idx, q);
    ansDiv.appendChild(btn);
  });
}

function checkAnswer(selected, q) {
  if (selected === q.correct) {
    points += q.score;
  } else {
    points -= q.score;
  }
  if (points >= 60) {
    showWin();
    return;
  }
  if (points < 0) points = 0;
  if (points > (level * 10) + 15 && questions[level + 1]) level++;
  document.getElementById("points").innerText = `Puntos: ${points}`;
  document.getElementById("level").innerText = `Nivel: ${level}`;
  loadQuestion();
}

function useJoker(type) {
  if (jokers[type] > 0) {
    jokers[type]--;
    updateJokerUI();
    loadQuestion();
  } else {
    alert("No te quedan comodines de este tipo");
  }
}

function showWin() {
  document.getElementById("win").style.display = "flex";
  document.getElementById("win").className = "win-message";
  document.getElementById("win").innerHTML = `
    <i class="fas fa-trophy"></i>
    <div>¡Ganaste el Desafío 60!</div>
    <button class="joker-btn" onclick="location.reload()">Volver a jugar</button>
  `;
  document.getElementById("question").innerHTML = "";
  document.getElementById("answers").innerHTML = "";
}

document.getElementById("points").innerText = `Puntos: ${points}`;
document.getElementById("level").innerText = `Nivel: ${level}`;
updateJokerUI();
loadQuestion();
</script>
</body>
</html>

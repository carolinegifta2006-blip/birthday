
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#080812">
<title>For Swetha | Birthday Surprise ✨</title>

<style>
:root {
  --gold: #f7cf83;
  --pink: #f5a8bd;
  --cream: #fff4df;
  --bg: #080812;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html { scroll-behavior: smooth; }

body {
  min-height: 100vh;
  background: var(--bg);
  color: var(--cream);
  font-family: Georgia, "Times New Roman", serif;
  overflow-x: hidden;
}

body::before {
  content: "";
  position: fixed;
  inset: 0;
  z-index: -1;
  background:
    radial-gradient(ellipse at 50% 0%, #392344, transparent 55%),
    radial-gradient(ellipse at 100% 80%, #15203a, transparent 40%),
    var(--bg);
}

#stars {
  position: fixed;
  inset: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
  pointer-events: none;
}

main {
  position: relative;
  z-index: 1;
}

nav {
  display: flex;
  justify-content: space-between;
  gap: 12px;
  padding: 24px 6%;
  color: var(--gold);
  font: 10px Arial, sans-serif;
  letter-spacing: 2px;
}

.hero {
  min-height: 90vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  text-align: center;
  padding: 35px 20px;
}

.hero-content {
  max-width: 800px;
  animation: appear 1.3s ease both;
}

.kicker {
  color: var(--gold);
  font: 11px Arial, sans-serif;
  letter-spacing: 4px;
  text-transform: uppercase;
}

h1 {
  font-size: clamp(55px, 12vw, 125px);
  font-weight: normal;
  line-height: 1;
  letter-spacing: -4px;
  margin: 28px 0;
}

h1 span {
  display: block;
  color: var(--gold);
  font-style: italic;
  text-shadow: 0 0 40px #f7cf8330;
}

.hero p {
  max-width: 550px;
  margin: auto;
  color: #d7cfdb;
  font-size: 17px;
  line-height: 1.9;
}

button {
  border: 1px solid var(--gold);
  background: linear-gradient(120deg, #f8dfac, #d5a968);
  color: #17101b;
  padding: 15px 22px;
  cursor: pointer;
  font: 11px Arial, sans-serif;
  letter-spacing: 1.5px;
  transition: .3s;
}

button:hover {
  transform: translateY(-3px);
  box-shadow: 0 0 25px #f7cf8350;
}

button:focus-visible,
input:focus-visible {
  outline: 2px solid var(--gold);
  outline-offset: 4px;
}

.primary {
  margin-top: 30px;
}

.secondary {
  background: transparent;
  color: var(--cream);
  border-color: #ffffff50;
  box-shadow: none;
}

section {
  width: min(950px, 92%);
  margin: auto;
  padding: 85px 0;
  scroll-margin-top: 25px;
}

.heading {
  text-align: center;
  margin-bottom: 35px;
}

.heading small {
  color: var(--gold);
  font: 11px Arial, sans-serif;
  letter-spacing: 3px;
  text-transform: uppercase;
}

h2 {
  font-size: clamp(35px, 7vw, 65px);
  font-weight: normal;
  margin: 18px 0;
}

.heading > p {
  max-width: 580px;
  margin: auto;
  color: #c4bdcc;
  line-height: 1.8;
}

.card {
  padding: clamp(22px, 5vw, 50px);
  border: 1px solid #ffffff24;
  background: linear-gradient(145deg, #ffffff10, #ffffff03);
  box-shadow: 0 20px 70px #0003;
}

.letter {
  max-width: 720px;
  margin: auto;
  text-align: center;
}

.letter h3 {
  color: var(--gold);
  font-size: 26px;
  font-weight: normal;
  font-style: italic;
  margin-bottom: 22px;
}

.letter p {
  color: #e4dce8;
  font-size: 17px;
  line-height: 2;
  margin: 17px 0;
}

.signature {
  color: var(--pink) !important;
  font-style: italic;
}

/* PHOTO GALLERY */

.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}

.photo {
  position: relative;
  height: 330px;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(145deg, #39263f, #13182b);
  border: 1px solid #ffffff30;
  transition: transform .4s;
}

.photo:nth-child(2) {
  transform: translateY(20px);
}

.photo:hover {
  transform: translateY(-5px);
}

.photo img {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  display: none;
  object-fit: cover;
  transition: transform .5s;
}

.photo.has-image img {
  display: block;
}

.photo:hover img {
  transform: scale(1.05);
}

.photo::after {
  content: "";
  position: absolute;
  inset: 40% 0 0;
  background: linear-gradient(transparent, #080812df);
  pointer-events: none;
}

.photo-text {
  position: absolute;
  z-index: 1;
  bottom: 22px;
  padding: 10px;
  text-align: center;
  color: #f9e8c5;
}

.photo-text h3 {
  font-size: 22px;
  font-weight: normal;
  font-style: italic;
}

.photo-text p {
  margin-top: 9px;
  font: 10px Arial, sans-serif;
  letter-spacing: 2px;
}

.upload-area {
  margin-top: 30px;
  text-align: center;
  color: #e4dce8;
}

.upload-area input {
  display: block;
  max-width: 100%;
  margin: 18px auto;
}

.note {
  max-width: 550px;
  margin: auto;
  color: #a99bb7;
  font: 12px/1.8 Arial, sans-serif;
}

/* CAKE */

.cake-area {
  text-align: center;
  padding: 35px 15px;
}

.cake-stage {
  position: relative;
  display: inline-block;
  margin: 20px 0;
}

.cake {
  display: block;
  font-size: clamp(100px, 23vw, 170px);
  animation: floatCake 2.5s ease-in-out infinite;
  filter: drop-shadow(0 0 30px #f5a8bd30);
}

.flame {
  position: absolute;
  top: -4px;
  left: 50%;
  transform: translateX(-50%);
  color: var(--gold);
  font-size: 28px;
  animation: flicker .6s ease-in-out infinite alternate;
}

@keyframes flicker {
  from { opacity: .6; transform: translateX(-50%) scale(.85); }
  to { opacity: 1; transform: translateX(-50%) scale(1.1); }
}

.cake-area > p {
  max-width: 500px;
  margin: 20px auto;
  color: #d7cbdc;
  line-height: 1.8;
}

.cake-buttons {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 12px;
  margin-top: 20px;
}

/* ANIMATIONS */

@keyframes appear {
  from {
    opacity: 0;
    transform: translateY(25px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes floatCake {
  0%, 100% { transform: translateY(0) rotate(-1deg); }
  50% { transform: translateY(-12px) rotate(1deg); }
}

footer {
  text-align: center;
  padding: 45px 18px;
  color: #94869d;
  font: 10px Arial, sans-serif;
  letter-spacing: 2px;
  line-height: 2;
}

@media (max-width: 650px) {
  nav {
    font-size: 8px;
    letter-spacing: 1px;
  }

  .hero {
    min-height: 85vh;
  }

  .gallery {
    grid-template-columns: 1fr;
  }

  .photo,
  .photo:nth-child(2) {
    height: 280px;
    transform: none;
  }

  section {
    padding: 60px 0;
  }

  .letter p {
    font-size: 16px;
  }
}

@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: .01ms !important;
    animation-iteration-count: 1 !important;
    scroll-behavior: auto !important;
    transition-duration: .01ms !important;
  }
}
</style>
</head>

<body>

<canvas id="stars" aria-hidden="true"></canvas>

<main>

<nav>
  <span>A LITTLE BIRTHDAY FILM</span>
  <span>FOR SWETHA ✦</span>
</nav>

<!-- SCENE 1: OPENING -->

<header class="hero" id="top">
  <div class="hero-content">
    <div class="kicker">A celebration of you</div>

    <h1>For you,<span>Swetha.</span></h1>

    <p>
      Some people make ordinary days feel like favourite
      memories. Today, this little universe is celebrating
      one of them.
    </p>

    <button class="primary" id="beginButton">
      BEGIN YOUR BIRTHDAY FILM ↗
    </button>
  </div>
</header>

<!-- SCENE 2: LETTER -->

<section id="message">
  <div class="heading">
    <small>Scene I · A note from the heart</small>
    <h2>To my favourite human.</h2>
    <p>A little message for someone who deserves a big celebration.</p>
  </div>

  <div class="card letter">
    <h3>Dear Swetha, 💌</h3>

    <p>Happy Birthday to a truly wonderful best friend! 💛</p>

    <p>
      Thank you for the laughs that arrive out of nowhere,
      the conversations that make time disappear, and the
      memories that become little treasures. Having you as
      a friend makes life brighter in ways that are hard
      to put into words.
    </p>

    <p>
      I hope this new chapter brings you courage for every
      dream, peace on difficult days, people who appreciate
      your heart, and countless reasons to smile.
    </p>

    <p>
      Never forget how special you are, not just today,
      but on all the ordinary days too. Keep shining in
      your own beautiful way.
    </p>

    <p class="signature">
      All the love, always. ✨
    </p>
  </div>
</section>

<!-- SCENE 3: PHOTO MEMORIES -->

<section id="memories">
  <div class="heading">
    <small>Scene II · Our memories</small>
    <h2>Little moments, forever.</h2>
    <p>
      Every friendship has moments worth keeping.
      Add your favourite photos to make this gallery yours.
    </p>
  </div>

  <div class="gallery">

    <div class="photo">
      <img alt="Friendship memory one">
      <div class="photo-text">
        <h3>Our kind of chaos</h3>
        <p>MEMORY NO. 01</p>
      </div>
    </div>

    <div class="photo">
      <img alt="Friendship memory two">
      <div class="photo-text">
        <h3>The laughing days</h3>
        <p>MEMORY NO. 02</p>
      </div>
    </div>

    <div class="photo">
      <img alt="Friendship memory three">
      <div class="photo-text">
        <h3>Always a favourite</h3>
        <p>MEMORY NO. 03</p>
      </div>
    </div>

  </div>

  <div class="upload-area">
    <label for="photos">Choose your friendship photos:</label>
    <input id="photos" type="file" accept="image/*" multiple>

    <p class="note">
      Select up to three photos. They appear in this browser
      only and are not uploaded to a server.
    </p>
  </div>
</section>

<!-- SCENE 4: BIRTHDAY CAKE -->

<section id="birthday">
  <div class="heading">
    <small>Scene III · Make a wish</small>
    <h2>One more thing…</h2>
    <p>A birthday deserves a little sparkle and a wish just for you.</p>
  </div>

  <div class="card cake-area">
    <div class="cake-stage">
      <span class="flame" id="flame">✦</span>
      <span class="cake" id="cake">🎂</span>
    </div>

    <p id="cakeMessage">
      Close your eyes for a second, Swetha.
      Think of a wish that makes your heart happy. ✨
    </p>

    <div class="cake-buttons">
      <button id="wishButton">MAKE A WISH ✨</button>
      <button class="secondary" id="celebrateButton">
        CELEBRATE AGAIN 🎉
      </button>
    </div>
  </div>
</section>

<footer>
  END CREDITS · FRIENDSHIP, LAUGHTER & A THOUSAND MORE MEMORIES
  <br>
  Made with love for Swetha 💛
</footer>

</main>

<script>
"use strict";

// Smoothly start the birthday experience.
document.getElementById("beginButton").addEventListener("click", () => {
  document.getElementById("message").scrollIntoView({
    behavior: "smooth"
  });

  celebrate(40);
});

// Photo gallery: display up to three local photos.
const photoInput = document.getElementById("photos");
const photoCards = document.querySelectorAll(".photo");
let photoURLs = [];

photoInput.addEventListener("change", function () {
  photoURLs.forEach(url => URL.revokeObjectURL(url));
  photoURLs = [];

  const files = Array.from(this.files || [])
    .filter(file => file.type.startsWith("image/"))
    .slice(0, 3);

  photoCards.forEach((card, index) => {
    const img = card.querySelector("img");

    if (files[index]) {
      const url = URL.createObjectURL(files[index]);
      photoURLs.push(url);

      img.src = url;
      card.classList.add("has-image");
    } else {
      img.removeAttribute("src");
      card.classList.remove("has-image");
    }
  });

  if (this.files.length > 3) {
    alert("Only the first three photos will be displayed.");
  }
});

// Birthday wish button.
let wishMade = false;

document.getElementById("wishButton").addEventListener("click", () => {
  const message = document.getElementById("cakeMessage");
  const button = document.getElementById("wishButton");

  if (!wishMade) {
    wishMade = true;

    message.textContent =
      "Your wish has been sent to the universe! ✨ " +
      "May beautiful things find their way to you, Swetha. " +
      "Happy Birthday! 💛";

    button.textContent = "WISH MADE ✓";
    document.getElementById("flame").textContent = "🔥";

    celebrate(180);
    sparkleBurst();
  } else {
    message.textContent =
      "Keep that wish close, Swetha. Here's to a year " +
      "full of lovely surprises! ✨";

    celebrate(70);
  }
});

document.getElementById("celebrateButton")
  .addEventListener("click", () => {
    celebrate(210);
    sparkleBurst();
  });

// Confetti animation.
function celebrate(count = 160) {
  const colors = [
    "#f7cf83",
    "#f5a8bd",
    "#fff4df",
    "#bba9f4",
    "#a8e6d7",
    "#e9a9ff"
  ];

  for (let i = 0; i < count; i++) {
    const piece = document.createElement("div");

    piece.style.position = "fixed";
    piece.style.zIndex = "9999";
    piece.style.top = "-15px";
    piece.style.left = Math.random() * 100 + "vw";
    piece.style.width = 5 + Math.random() * 8 + "px";
    piece.style.height = 8 + Math.random() * 12 + "px";
    piece.style.background =
      colors[Math.floor(Math.random() * colors.length)];
    piece.style.borderRadius = Math.random() > 0.5 ? "50%" : "1px";
    piece.style.pointerEvents = "none";

    document.body.appendChild(piece);

    const drift = (Math.random() - 0.5) * 260;
    const duration = 2000 + Math.random() * 2000;
    const rotation = Math.random() * 800;

    const animation = piece.animate([
      {
        transform: "translate(0, 0) rotate(0deg)",
        opacity: 1
      },
      {
        transform:
          `translate(${drift}px, ${innerHeight + 60}px) ` +
          `rotate(${rotation}deg)`,
        opacity: 0
      }
    ], {
      duration,
      easing: "ease-out"
    });

    animation.onfinish = () => piece.remove();
  }
}

// Magical floating sparkles.
function sparkleBurst() {
  const symbols = ["✦", "✧", "✨", "♡", "★"];

  for (let i = 0; i < 35; i++) {
    const sparkle = document.createElement("span");

    sparkle.textContent =
      symbols[Math.floor(Math.random() * symbols.length)];

    sparkle.style.position = "fixed";
    sparkle.style.zIndex = "10000";
    sparkle.style.left = 35 + Math.random() * 30 + "vw";
    sparkle.style.top = 35 + Math.random() * 25 + "vh";
    sparkle.style.color = ["#f7cf83", "#f5a8bd", "#fff4df"][i % 3];
    sparkle.style.fontSize = 12 + Math.random() * 24 + "px";
    sparkle.style.pointerEvents = "none";

    document.body.appendChild(sparkle);

    const dx = (Math.random() - 0.5) * innerWidth * 0.8;
    const dy = (Math.random() - 0.5) * innerHeight * 0.8;

    const animation = sparkle.animate([
      { transform: "translate(0, 0) scale(1)", opacity: 1 },
      {
        transform: `translate(${dx}px, ${dy}px) scale(.1) rotate(180deg)`,
        opacity: 0
      }
    ], {
      duration: 1300,
      easing: "ease-out"
    });

    animation.onfinish = () => sparkle.remove();
  }
}

// Animated twinkling stars.
const canvas = document.getElementById("stars");
const ctx = canvas.getContext("2d");

let width = 0;
let height = 0;
let stars = [];

function resizeStars() {
  const dpr = Math.min(window.devicePixelRatio || 1, 2);

  width = window.innerWidth;
  height = window.innerHeight;

  canvas.width = Math.floor(width * dpr);
  canvas.height = Math.floor(height * dpr);
  canvas.style.width = width + "px";
  canvas.style.height = height + "px";

  ctx.setTransform(dpr, 0, 0, dpr, 0, 0);

  const count = Math.min(140, Math.floor(width * height / 7000));

  stars = Array.from({ length: count }, () => ({
    x: Math.random() * width,
    y: Math.random() * height,
    radius: 0.5 + Math.random() * 1.3,
    phase: Math.random() * 6,
    speed: 0.006 + Math.random() * 0.015,
    brightness: 0.3 + Math.random() * 0.7
  }));
}

function drawStars() {
  ctx.clearRect(0, 0, width, height);

  stars.forEach(star => {
    star.phase += star.speed;

    const alpha =
      star.brightness * (0.55 + 0.45 * Math.sin(star.phase));

    ctx.beginPath();
    ctx.arc(star.x, star.y, star.radius, 0, Math.PI * 2);
    ctx.fillStyle = `rgba(255,239,220,${alpha})`;
    ctx.fill();
  });

  requestAnimationFrame(drawStars);
}

window.addEventListener("resize", resizeStars, { passive: true });

resizeStars();
drawStars();
</script>

</body>
</html>

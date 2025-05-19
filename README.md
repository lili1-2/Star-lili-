<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Star Lili</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@600&display=swap');
  body, html {
    margin: 0; padding: 0; height: 100%;
    background: black;
    color: white;
    font-family: 'Poppins', sans-serif;
    overflow-x: hidden;
  }
  .stars {
    position: fixed;
    width: 100%;
    height: 100%;
    background: black;
    z-index: -1;
    overflow: hidden;
  }
  .star {
    position: absolute;
    background: white;
    border-radius: 50%;
    opacity: 0.8;
    animation: twinkle 3s infinite ease-in-out;
  }
  @keyframes twinkle {
    0%, 100% {opacity: 0.8;}
    50% {opacity: 0.2;}
  }
  .container {
    text-align: center;
    padding: 150px 20px 40px;
  }
  .star-name {
    font-size: 5vw;
    font-weight: 700;
    margin-bottom: 10px;
  }
  .subtitle {
    font-size: 1.8vw;
    color: #ccc;
    margin-bottom: 60px;
    font-style: italic;
  }
  .info-section {
    max-width: 600px;
    margin: 0 auto 40px;
    text-align: left;
    font-size: 1.2rem;
    line-height: 1.6;
    background: rgba(255, 255, 255, 0.05);
    padding: 20px 30px;
    border-radius: 10px;
  }
  .info-section h2 {
    margin-top: 0;
    margin-bottom: 15px;
    color: #f0c040;
  }
  iframe {
    display: block;
    margin: 0 auto 60px;
    border: none;
    width: 90vw;
    max-width: 600px;
    height: 400px;
    border-radius: 15px;
    box-shadow: 0 0 20px #f0c040aa;
  }
  @media (max-width: 600px) {
    .star-name {
      font-size: 10vw;
    }
    .subtitle {
      font-size: 4vw;
    }
    .info-section {
      font-size: 1rem;
      padding: 15px 20px;
    }
  }
</style>
</head>
<body>
<div class="stars" id="stars"></div>

<div class="container">
  <div class="star-name">Lili</div>
  <div class="subtitle">Our love is eternal, shining forever through Lili.</div>
</div>

<div class="info-section">
  <h2>About the Star</h2>
  <p>🌟 <strong>Star Name:</strong> Lili</p>
  <p>📍 <strong>Coordinates:</strong> RA 18h 36m 56.3s | Dec +38° 47′ 1″</p>
  <p>📅 <strong>Date of Registration:</strong> Monday, May 27, 2025</p>
  <p>📝 This star was named in honor of Lili, as a symbol of eternal love.</p>
</div>

<iframe src="https://stellarium-web.org/embed.html?object=star&ra=18.61564&dec=38.7836&fov=10" title="Star Location" allowfullscreen></iframe>

<script>
  const starsContainer = document.getElementById('stars');

  function createStar() {
    const star = document.createElement('div');
    star.classList.add('star');
    const size = Math.random() * 2 + 1;
    star.style.width = size + 'px';
    star.style.height = size + 'px';
    star.style.top = Math.random() * 100 + '%';
    star.style.left = Math.random() * 100 + '%';
    star.style.animationDuration = (Math.random() * 3 + 2) + 's';
    starsContainer.appendChild(star);
  }

  for(let i=0; i<100; i++) {
    createStar();
  }
</script>

</body>
</html>

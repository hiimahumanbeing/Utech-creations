<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Utech Creations Entertainment Hub</title>
  <style>
    body {
      background-color: #0a1e3b;
      color: white;
      font-family: 'Arial', sans-serif;
      margin: 0;
      padding: 0;
      text-align: center;
      overflow-x: hidden;
    }

    header {
      background: linear-gradient(45deg, #00264d, #001f3f);
      padding: 40px;
      color: white;
    }

    header h1 {
      font-size: 3rem;
      animation: fadeIn 2s ease-in-out infinite alternate;
    }

    @keyframes fadeIn {
      from {
        opacity: 0.5;
        transform: scale(0.9);
      }
      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    .button {
      background-color: #007bff;
      color: white;
      padding: 15px 30px;
      text-decoration: none;
      font-size: 18px;
      border-radius: 5px;
      margin: 20px;
      display: inline-block;
      transition: transform 0.3s;
    }

    .button:hover {
      transform: scale(1.1);
      background-color: #0056b3;
    }

    .video-gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      margin: 30px 50px;
    }

    .video-gallery iframe {
      width: 100%;
      height: 200px;
      border: 0;
      border-radius: 8px;
    }

    .animated-text {
      font-size: 24px;
      color: yellow;
      animation: bounce 3s infinite;
    }

    @keyframes bounce {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-15px);
      }
    }

    footer {
      background: #001f3f;
      color: white;
      padding: 20px;
      margin-top: 50px;
    }

    input[type="text"] {
      padding: 10px;
      width: 80%;
      max-width: 300px;
      margin: 15px;
      border: none;
      border-radius: 5px;
    }

    #countdown {
      font-size: 24px;
      color: cyan;
    }
  </style>
  <script>
    // Countdown Timer for Next Video Launch
    function startCountdown() {
      const targetDate = new Date().getTime() + 86400000; // 24 hours from now
      const timer = setInterval(function () {
        const now = new Date().getTime();
        const distance = targetDate - now;

        if (distance < 0) {
          clearInterval(timer);
          document.getElementById("countdown").innerHTML = "Video Launched!";
        } else {
          const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
          const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
          const seconds = Math.floor((distance % (1000 * 60)) / 1000);
          document.getElementById("countdown").innerHTML = `Next Video in: ${hours}h ${minutes}m ${seconds}s`;
        }
      }, 1000);
    }

    window.onload = startCountdown;
  </script>
</head>
<body>
  <header>
    <h1>Welcome to Utech Creations Entertainment!</h1>
    <p class="animated-text">Enjoy Our Latest Content and Explore Videos!</p>
  </header>

  <h2>Explore Our Latest Videos!</h2>
  <div class="video-gallery">
    <!-- You can embed more videos here -->
    <iframe src="https://www.youtube.com/embed/eB4m1gzZswk" title="Latest Video"></iframe>
  </div>

  <div id="countdown"></div>

  <h3>Search for Your Favorite Video!</h3>
  <input type="text" placeholder="Search videos...">

  <h3>Contact Me:</h3>
  <p>Email: <a href="mailto:utechcreations507@gmail.com">utechcreations507@gmail.com</a></p>
  <p>Check my YouTube Channel: <a href="https://youtube.com/@utechcreations?si=mDzqH2qpQ6llOIL7" target="_blank">Utech Creations</a></p>

  <footer>
    <p>100% Created by Ukasha - All Rights Reserved.</p>
  </footer>
</body>
</html>

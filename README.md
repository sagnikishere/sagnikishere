<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animated Tech Stack</title>
  <style>
    body {
      background-color: #0f172a; /* Dark background to make colors pop */
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    .stack-container {
      display: flex;
      gap: 24px;
      flex-wrap: wrap;
      justify-content: center;
      padding: 20px;
    }

    .tech-card {
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.1);
      padding: 20px 40px;
      border-radius: 16px;
      color: #ffffff;
      font-size: 1.2rem;
      font-weight: 600;
      letter-spacing: 1px;
      cursor: pointer;
      position: relative;
      overflow: hidden;
      transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      /* Continuous floating animation */
      animation: float 4s ease-in-out infinite;
    }

    /* Staggered animation delays so they don't move in sync */
    .tech-card:nth-child(1) { animation-delay: 0s; }
    .tech-card:nth-child(2) { animation-delay: 0.5s; }
    .tech-card:nth-child(3) { animation-delay: 1s; }

    /* Hover Effects with Unique Colors */
    .tech-card:hover {
      transform: translateY(-15px) scale(1.05);
      background: rgba(255, 255, 255, 0.1);
    }

    .vercel:hover {
      box-shadow: 0 10px 30px -10px #ffffff;
      border-color: #ffffff;
      color: #ffffff;
    }

    .netlify:hover {
      box-shadow: 0 10px 30px -10px #00C7B7;
      border-color: #00C7B7;
      color: #00C7B7;
    }
    
    .react:hover {
      box-shadow: 0 10px 30px -10px #61DAFB;
      border-color: #61DAFB;
      color: #61DAFB;
    }

    /* Keyframes for the floating effect */
    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0px); }
    }

    /* Optional: A subtle sweeping shine effect inside the card */
    .tech-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 50%;
      height: 100%;
      background: linear-gradient(to right, transparent, rgba(255,255,255,0.1), transparent);
      transform: skewX(-20deg);
      transition: 0.5s;
    }

    .tech-card:hover::before {
      left: 150%;
    }
  </style>
</head>
<body>

  <div class="stack-container">
    <div class="tech-card react">React</div>
    <div class="tech-card vercel">Vercel</div>
    <div class="tech-card netlify">Netlify</div>
  </div>

</body>
</html>

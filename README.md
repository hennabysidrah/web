<html>
<head>
  <title>Portfolio Website</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
  
  <style>
    body {
      font-family: 'Courier New', Courier, monospace;
      margin: 0;
      padding: 0;
      background-color: black;
      color: lime;
    }
    
    .navbar {
      background-color: #000033;
      padding: 10px;
      display: flex;
      justify-content: space-between;
      align-items: center; 
    }
    
    .navbar ul {
      list-style-type: none;
      margin: 0;
      padding: 0;
      display: flex;
      align-items: center;
    }
    
    .navbar li {
      margin-right: 10px;
    }
    
    .navbar li:last-child {
      margin-right: 0;
    }
    
    .navbar a {
      display: flex;  
      align-items: center;  
      padding: 10px;
      color: lime;
      text-decoration: none;
      cursor: pointer;
      transition: transform 0.3s;
    }
    
    .navbar a i {
      margin-right: 5px; 
    }
    
    .navbar a:hover {
      color: yellow;
      transform: translateY(-2px);
    }
    
    .container {
      max-width: 800px;
      margin: 0 auto;
      padding: 20px;
    }
    
    .content {
      background-color: #000066;
      padding: 20px;
      border-radius: 5px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      text-align: left;
    }
    
    .button {
      display: inline-block;
      padding: 12px 20px;
      background-color: #000033;
      color: lime;
      text-decoration: none;
      border-radius: 3px;
      margin-right: 20px;
      border: none;
      transition: transform 0.3s;
      position: relative;
      cursor: pointer;
    }
    
    .button:hover {
      color: yellow;
      transform: translateY(-2px);
    }
    
    .portfolio-item {
      display: flex;
      margin-bottom: 20px;
      border: 1px solid lime;
      border-radius: 3px;
      padding: 10px;
    }
    
    .portfolio-item img {
      width: 200px;
      height: 150px;
      margin-right: 10px;
      border: 1px solid lime;
      border-radius: 3px;
    }
    
    .portfolio-item .item-details {
      flex-grow: 1;
    }
    
    .portfolio-item h3 {
      margin-top: 0;
      color: lime;
    }
    
    .portfolio-item p {
      margin-top: 5px;
    }
    
    /* Dropdown Styles */
    .dropdown {
      position: relative;
      display: inline-block;
    }
    
    .dropdown-content {
      display: none;
      position: absolute;
      background-color: #000033;
      min-width: 160px;
      box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
      z-index: 1;
      top: 30px;
      right: 0;
    }

    .dropdown-content a {
      color: lime;
      padding: 12px 16px;
      text-decoration: none;
      display: block;
    }

    .dropdown-content a:hover {
      background-color: #000066;
    }

    .dropdown:hover .dropdown-content {
      display: block;
    }

    .show {
      display: block;
    }
  </style>
</head>
<body>
  <div class="navbar">
    <ul>
      <li><a onclick="scrollToSection('home')" title="Go to Home"><i class="fas fa-home"></i> Home</a></li>
      <li><a onclick="scrollToSection('about')" title="About Me"><i class="fas fa-info-circle"></i> About</a></li>
      <li><a onclick="scrollToSection('portfolio')" title="Portfolio"><i class="fas fa-briefcase"></i> Portfolio</a></li>
      <li><a onclick="scrollToSection('contact')" title="Contact Me"><i class="fas fa-envelope"></i> Contact</a></li>
    </ul>
    <div class="dropdown">
      <a href="#" class="button" onclick="playClickSound(); toggleDropdown()" title="Projects"><i class="fa fa-hammer"></i></a>
      <div id="dropdown" class="dropdown-content">
        <a href="https://www.roblox.com/games/13304409142/Memes-Tower-Defense">Memes Tower Defense</a>
        <a href="https://www.roblox.com/games/16018553783/">Commissions</a>
      </div>
    </div>
  </div>
  <div class="container">
    <div class="content" id="home">
      <h1 style="font-size: 40px;">Welcome to my Portfolio</h1>
      <p style="font-size: 20px;">Hi, This is my portfolio website which will showcase my past work and may also contain some work-in-progress projects.</p>
      <h2 style="font-size: 30px;">About Me</h2>
      <p style="font-size: 20px;">Hi, I'm Zeyan and I'm 14 years old. I do commissions for Roblox! I have coding skills and I'm familiar with OOP. Though I'm not an expert yet, I'm constantly improving and giving my best. 👍</p>
      <h2 style="font-size: 30px;">Portfolio</h2>
      <div class="portfolio-item">
        <img src="image1.png" alt="Portfolio Item 1">
        <div class="item-details">
          <h3 style="font-size: 24px;"> OOP example 1</h3>
          <p style="font-size: 18px;"> Some of my code that contains OOP.</p>
        </div>
      </div>
      <div class="portfolio-item">
        <img src="image2.png" alt="Portfolio Item 2">
        <div class="item-details">
          <h3 style="font-size: 24px;">Player outfit loader</h3>
          <p style="font-size: 18px;">A Script that loads all player outfits.</p>
        </div>
      </div>
    </div>
    <div class="content" id="contact">
      <h2 style="font-size: 30px;">Contact Me</h2>
  
      <ul>
        <li><a href="https://discord.gg/eNHRKZcwUa" class="button" title="Join Discord" style="font-size: 18px;"><i class="fab fa-discord"></i> Discord</a></li>
        <li><a href="https://www.roblox.com/users/3522931236/profile" class="button" title="Visit Roblox Profile" style="font-size: 18px;"><i class="fab fa-roblox"></i> Roblox</a></li>
        <li><a href="https://twitter.com/zeyan99645177" class="button" title="Follow on Twitter" style="font-size: 18px;"><i class="fab fa-twitter"></i> Twitter</a></li>
      </ul>
    </div>
  </div>

  <script>
    function scrollToSection(id) {
      const section = document.getElementById(id);
      section.scrollIntoView({ behavior: 'smooth' });
    }
    
    function toggleDropdown() {
      var dropdown = document.getElementById("dropdown");
      dropdown.classList.toggle("show");
    }
  
    window.onclick = function(event) {
      if (!event.target.matches('.button')) {
        var dropdown = document.getElementById("dropdown");
        if (dropdown.classList.contains('show')) {
          dropdown.classList.remove('show');
        }
      }
    }

    function playClickSound() {
      var audio = new Audio('clicksound.mp3');
      audio.play();
    }
  </script>
</body>
</html>

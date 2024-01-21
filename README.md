
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
      transition: background-color 0.3s, color 0.3s;
    }
    
    body.light-mode {
      background-color: white;
      color: green;
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
    
    /* Toggle Button Styles */
    .toggle-btn {
      position: relative;
      width: 50px;
      height: 25px;
      background-color: #000033;
      border-radius: 15px;
      cursor: pointer;
    }
    
    .toggle-btn .sun-icon {
      position: absolute;
      top: 50%;
      left: 3px;
      transform: translateY(-50%);
      color: lime;
    }
    
    .toggle-btn .circle {
      position: absolute;
      top: 3px;
      left: 25px;
      width: 19px;
      height: 19px;
      border-radius: 50%;
      background-color: lime;
      transition: all 0.3s;
    }
    
    .toggle-btn.light-mode .circle {
      transform: translateX(25px);
      background-color: #000033;
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
    <div class="toggle-btn" onclick="toggleMode()">
      <i class="fas fa-sun sun-icon"></i>
      <div class="circle"></div>
    </div>
  </div>
  <div class="container">
    <div class="content" id="home">
      <h1 style="font-size: 40px;">Welcome to my Portfolio</h1>
      <p style="font-size: 20px;">Hi, This is my portfolio website which will showcase my past work and may also contain some work-in-progress projects.</p>
      <h2 style="font-size: 30px;">About Me</h2>
      <p style="font-size: 20px;">Hi, I'm Zeyan and I'm 14 years old. I do commissions for Roblox! I have coding skills and I'm familiar with various programming languages like HTML, CSS, JavaScript, etc.</p>
      <h2 style="font-size: 30px;">Portfolio</h2>
      <div class="portfolio-item">
        <img src="project1.png" alt="Project 1">
        <div class="item-details">
          <h3>Project 1</h3>
          <p>Description of project 1.</p>
        </div>
      </div>
      <div class="portfolio-item">
        <img src="project2.png" alt="Project 2">
        <div class="item-details">
          <h3>Project 2</h3>
          <p>Description of project 2.</p>
        </div>
      </div>
      <h2 style="font-size: 30px;">Contact</h2>
      <p style="font-size: 20px;">Feel free to contact me via email or through the contact form below:</p>
      <form>
        <input type="text" placeholder="Name">
        <input type="email" placeholder="Email">
        <textarea placeholder="Message"></textarea>
        <button type="submit">Send</button>
      </form>
    </div>
  </div>
  
  <script>
    function toggleMode() {
      const body = document.querySelector('body');
      body.classList.toggle('light-mode');
    }
    
    function toggleDropdown() {
      const dropdown = document.getElementById('dropdown');
      dropdown.classList.toggle('show');
    }
    
    function scrollToSection(sectionId) {
      const section = document.getElementById(sectionId);
      section.scrollIntoView({ behavior: 'smooth' });
    }
    
       function playClickSound() {
      var audio = new Audio('clicksound.mp3');
      audio.play();
    }
  </script>
</body>
</html>

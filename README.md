<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Tavada Mpofu Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    /* General Styles */
    body {
      background-color: #000;
      color: #fff;
      font-family: 'Poppins', sans-serif;
      margin: 0;
      padding: 0;
      overflow-x: hidden;
    }

    /* Header */
    header {
      background: linear-gradient(135deg, #ff007f, #5500ff);
      padding: 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: fixed;
      width: 100%;
      height: 60px;
      top: 0;
      left: 0;
      z-index: 1000;
      box-sizing: border-box;
    }

    .hamburger-menu {
      display: none;
      cursor: pointer;
    }

    .hamburger-menu .bar {
      display: block;
      width: 25px;
      height: 3px;
      margin: 5px auto;
      background-color: #fff;
    }

    #menu-button {
      display: none;
    }

    .main-navbar ul {
      list-style: none;
      padding: 0;
      margin: 0;
      display: flex;
    }

    .main-navbar ul li {
      margin: 0 15px;
    }

    .main-navbar ul li a {
      color: #fff;
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s;
    }

    .main-navbar ul li a:hover {
      color: #ff007f;
    }

    /* Hero Section */
    .section-hero {
      background: url('https://source.unsplash.com/1600x900/?space,stars')
        no-repeat center center/cover;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      margin-top: 60px;
    }

    .hero-section-content h1 {
      font-size: 3rem;
      text-transform: uppercase;
      background: -webkit-linear-gradient(45deg, #ff007f, #5500ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
      margin-bottom: 1rem;
    }
    
    .tag-line {
      font-size: 1.5rem;
      color: #ff007f;
      margin-bottom: 1.5rem;
    }

    /* Social Icons */
    .social-icons-wrapper {
      margin-top: 20px;
    }

    .social-icons-wrapper a {
      color: #ff007f;
      font-size: 2rem;
      margin: 0 10px;
      transition: color 0.3s ease;
    }

    .social-icons-wrapper a:hover {
      color: #5500ff;
    }

    /* Card / Terminal */
    .card {
      padding: 1rem;
      overflow: hidden;
      border: 1px solid #333;
      border-radius: 12px;
      background-color: transparent;
      backdrop-filter: none;
      min-width: 344px;
      max-width: 600px;
      margin: 20px auto;
    }

    .wrap {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      position: relative;
      z-index: 10;
      border: none;
      overflow: hidden;
    }

    .terminal {
      display: flex;
      flex-direction: column;
      background: transparent;
      font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas,
        "Liberation Mono", "Courier New", monospace;
    }

    .head {
      display: flex;
      align-items: center;
      justify-content: space-between;
      overflow: hidden;
      min-height: 40px;
      padding-inline: 12px;
      border-top-left-radius: 8px;
      border-top-right-radius: 8px;
      background-color: #202425;
    }

    .title {
      display: flex;
      align-items: center;
      gap: 8px;
      height: 2.5rem;
      user-select: none;
      font-weight: 600;
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;
      color: #8e8e8e;
    }

    .title > svg {
      height: 18px;
      width: 18px;
      margin-top: 2px;
      color: #006adc;
    }

    .copy_toggle {
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 0.25rem;
      border: 0.65px solid #c1c2c5;
      margin-left: auto;
      border-radius: 6px;
      background-color: #202425;
      color: #8e8e8e;
      cursor: pointer;
    }

    .copy_toggle > svg {
      width: 20px;
      height: 20px;
    }

    .copy_toggle:active > svg > path,
    .copy_toggle:focus-within > svg > path {
      animation: clipboard-check 500ms linear forwards;
    }

    .body {
      display: flex;
      flex-direction: column;
      position: relative;
      border-bottom-right-radius: 8px;
      border-bottom-left-radius: 8px;
      overflow-x: auto;
      padding: 1rem;
      line-height: 19px;
      color: white;
      background-color: black;
      white-space: nowrap;
    }

    .pre {
      display: flex;
      flex-direction: row;
      align-items: center;
      white-space: pre;
      background-color: transparent;
      overflow: hidden;
      box-sizing: border-box;
      font-size: 16px;
    }

    .pre code:nth-child(1) {
      color: #575757;
    }

    .pre code:nth-child(2) {
      color: #e34ba9;
    }

    .cmd {
      height: 19px;
      position: relative;
      display: flex;
      align-items: center;
      flex-direction: row;
    }

    .cmd::before {
      content: attr(data-cmd);
      position: relative;
      display: block;
      white-space: nowrap;
      overflow: hidden;
      background-color: transparent;
      animation: inputs 8s steps(22) infinite;
    }

    .cmd::after {
      content: "";
      position: relative;
      display: block;
      height: 100%;
      overflow: hidden;
      background-color: transparent;
      border-right: 0.15em solid #e34ba9;
      animation: cursor 0.5s step-end infinite alternate,
        blinking 0.5s infinite;
    }

    @keyframes blinking {
      20%, 80% {
        transform: scaleY(1);
      }
      50% {
        transform: scaleY(0);
      }
    }

    @keyframes cursor {
      50% {
        border-right-color: transparent;
      }
    }

    @keyframes inputs {
      0%, 100% {
        width: 0;
      }
      10%, 90% {
        width: 58px;
      }
      30%, 70% {
        width: 215px;
        max-width: max-content;
      }
    }

    @keyframes clipboard-check {
      100% {
        color: #fff;
        d: path("M 9 5 H 7 a 2 2 0 0 0 -2 2 v 12 a 2 2 0 0 0 2 2 h 10 a 2 2 0 0 0 2 -2 V 7 a 2 2 0 0 0 -2 -2 h -2 M 9 5 a 2 2 0 0 0 2 2 h 2 a 2 2 0 0 0 2 -2 M 9 5 a 2 2 0 0 1 2 -2 h 2 a 2 2 0 0 1 2 2 m -6 9 l 2 2 l 4 -4");
      }
    }

    /* Sections */
    .section {
      padding: 50px 10%;
      background-color: black;
      border: none !important;
      margin: 0 !important;
    }

    .section-content {
      background: rgba(255, 0, 127, 0.1);
      padding: 20px;
      border-radius: 10px;
    }

    .about-content {
      background: transparent;
    }

    .text-with-border {
      background: linear-gradient(135deg, #ff007f, #5500ff);
      padding: 20px;
      margin: 20px auto;
      width: 80%;
      max-width: 800px;
      border-radius: 10px;
      box-shadow: 0 0 10px #ff007f;
      color: white;
    }

    .design-section {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      background-color: #1f1f1f;
      min-height: 100vh;
      padding: 100px 0;
      font-family: 'Jost', sans-serif;
    }

    .timeline {
      width: 80%;
      background: #000;
      height: auto;
      max-width: 800px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
    }

    .timeline-content {
      background: #000;
      box-shadow: 5px 5px 10px #111, -5px -5px 10px #222;
      color: white;
      padding: 20px;
      border-radius: 10px;
    }

    .timeline-component {
      margin: 0px 20px 20px 20px;
    }

    .timeline-component h3 {
      color: #ff007f;
      margin-top: 0;
    }

    @media screen and (min-width: 768px) {
      .timeline {
        display: grid;
        grid-template-columns: 1fr 3px 1fr;
      }

      .timeline-middle {
        position: relative;
        background-image: linear-gradient(135deg, #ff007f, #5500ff);
        width: 3px;
        height: 100%;
      }

      .timeline-circle {
        position: absolute;
        top: 0;
        left: 50%;
        width: 15px;
        height: 15px;
        border-radius: 50%;
        background-image: linear-gradient(135deg, #ff007f, #5500ff);
        transform: translateX(-50%);
      }
    }

    /* Project Section */
    #projects {
      padding: 50px 10%;
    }

    .projects h2,
    .contact h2 {
      text-align: center;
      color: #ff007f;
      margin-bottom: 30px;
    }

    .project {
      background: linear-gradient(135deg, #ff007f, #5500ff);
      padding: 20px;
      margin: 20px auto;
      width: 80%;
      max-width: 800px;
      border-radius: 10px;
      box-shadow: 0 0 10px #ff007f;
      color: white;
    }

    .project h3 {
      margin-top: 0;
    }

    /* Contact Section */
    #contact {
      padding: 50px 10%;
      text-align: center;
    }

    .contact p {
      text-align: center;
      font-size: 1.2rem;
      margin: 10px 0;
    }

    .contact a {
      color: #ff007f;
      text-decoration: none;
      font-weight: bold;
    }

    .contact a:hover {
      text-decoration: underline;
    }

    /* Footer */
    footer {
      text-align: center;
      width: 100%;
      position: relative;
      padding: 20px;
      background: linear-gradient(135deg, #ff007f, #5500ff);
      margin-top: 20px;
      box-sizing: border-box;
    }

    /* Mobile Responsiveness */
    @media (max-width: 768px) {
      .hamburger-menu {
        display: block;
      }
      
      .main-navbar {
        position: fixed;
        top: 60px;
        left: -100%;
        width: 100%;
        background: linear-gradient(135deg, #ff007f, #5500ff);
        transition: 0.3s;
        box-shadow: 0 10px 27px rgba(0, 0, 0, 0.05);
      }
      
      .main-navbar ul {
        display: block;
        text-align: center;
        padding: 20px 0;
      }
      
      .main-navbar ul li {
        margin: 15px 0;
      }
      
      #menu-button:checked ~ .main-navbar {
        left: 0;
      }
      
      .hero-section-content h1 {
        font-size: 2rem;
      }
      
      .tag-line {
        font-size: 1.2rem;
      }
      
      .text-with-border,
      .project {
        width: 95%;
      }
      
      .card {
        min-width: auto;
        width: 90%;
      }
    }
  </style>
</head>
<body>
  <header>
    <label class="hamburger-menu" for="menu-button">
      <span class="bar"></span>
      <span class="bar"></span>
      <span class="bar"></span>
    </label>
    <input type="checkbox" id="menu-button" />
    <nav class="main-navbar">
      <ul>
        <li><a href="#home-section">HOME</a></li>
        <li><a href="#about-section">ABOUT</a></li>
        <li><a href="#experience-section">EXPERIENCE</a></li>
        <li><a href="#projects">PROJECTS</a></li>
        <li><a href="#contact">CONTACT</a></li>
      </ul>
    </nav>
  </header>
  <main class="container">
    <section class="section section-hero" id="home-section">
      <div class="hero-section-content">
        <h1>TAVADA (LELO) MPOFU</h1>
        <p class="tag-line">Final year Information Technology Student</p>
        <div class="social-icons-wrapper">
          <a href="#"><i class="fa-brands fa-github"></i></a>
          <a href="#"><i class="fa-brands fa-instagram"></i></a>
          <a href="#"><i class="fa-brands fa-twitter"></i></a>
          <a href="#"><i class="fa-brands fa-linkedin"></i></a>
        </div>
      </div>
    </section>
    <div class="card">
      <div class="wrap">
        <div class="terminal">
          <hgroup class="head">
            <p class="title">
              <svg
                width="16px"
                height="16px"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                stroke-linejoin="round"
                stroke-linecap="round"
                stroke-width="2"
                stroke="currentColor"
                fill="none"
              >
                <path
                  d="M7 15L10 12L7 9M13 15H17M7.8 21H16.2C17.8802 21 18.7202 21 19.362 20.673C19.9265 20.3854 20.3854 19.9265 20.673 19.362C21 18.7202 21 17.8802 21 16.2V7.8C21 6.11984 21 5.27976 20.673 4.63803C20.3854 4.07354 19.9265 3.6146 19.362 3.32698C18.7202 3 17.8802 3 16.2 3H7.8C6.11984 3 5.27976 3 4.63803 3.32698C4.07354 3.6146 3.6146 4.07354 3.32698 4.63803C3 5.27976 3 6.11984 3 7.8V16.2C3 17.8802 3 18.7202 3.32698 19.362C3.6146 19.9265 4.07354 20.3854 4.63803 20.673C5.27976 21 6.11984 21 7.8 21Z"
                ></path>
              </svg>
              Terminal
            </p>
            <button class="copy_toggle" tabindex="-1" type="button">
              <svg
                width="16px"
                height="16px"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                stroke-linejoin="round"
                stroke-linecap="round"
                stroke-width="2"
                stroke="currentColor"
                fill="none"
              >
                <path
                  d="M9 5h-2a2 2 0 0 0 -2 2v12a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-12a2 2 0 0 0 -2 -2h-2"
                ></path>
                <path
                  d="M9 3m0 2a2 2 0 0 1 2 -2h2a2 2 0 0 1 2 2v0a2 2 0 0 1 -2 2h-2a2 2 0 0 1 -2 -2z"
                ></path>
              </svg>
            </button>
          </hgroup>
          <div class="body">
            <pre class="pre"><code>-&nbsp;</code><code>npx&nbsp;</code><code class="cmd" data-cmd="create-react-app@latest"></code></pre>
          </div>
        </div>
      </div>
    </div>
    <section class="section section-about" id="about-section">
      <div class="section-content">
        <div class="text-with-border">
          <p>
            Motivated IT student with a strong foundation in programming, software development, web development, and systems analysis, seeking to apply technical skills and innovative thinking in a challenging role. Passionate about leveraging technology to solve real-world problems and eager to contribute to projects that drive efficiency and innovation while continuing to grow as an IT professional.
          </p>
        </div>
      </div>
    </section>
    <section class="section section-experience" id="experience-section">
      <!-- Timeline -->
      <section class="design-section">
        <div class="timeline">
          <!-- Timeline components -->
          <div class="timeline-empty"></div>
          <div class="timeline-middle">
            <div class="timeline-circle"></div>
          </div>
          <div class="timeline-component timeline-content">
            <h3>Art Jamming Melrose Arch</h3>
            <p>
              Gaining experience in my first ever workplace setting as a salesperson. Learning to work with clientele and in a team environment.
            </p>
            <ul>
              <li>Welcoming customers to the store</li>
              <li>Instructing customers on painting processes and rules</li>
              <li>Ensuring the shop floor is correctly replenished</li>
              <li>General office/administrative duties</li>
              <li>Supporting the store in meeting its sales target</li>
            </ul>
          </div>
          <div class="timeline-component timeline-content">
            <h3>Richfield Graduate Institute of Technology</h3>
            <p>
              Majoring in Computer Science, I gained many skills and learned several programming languages. I also played netball and represented my school's first team.
            </p>
            <ul>
              <li>Python</li>
              <li>JavaScript</li>
              <li>PHP</li>
              <li>C++</li>
              <li>SQL</li>
              <li>HTML</li>
              <li>CSS</li>
            </ul>
          </div>
          <div class="timeline-middle">
            <div class="timeline-circle"></div>
          </div>
          <div class="timeline-empty"></div>
          <div class="timeline-empty"></div>
          <div class="timeline-middle">
            <div class="timeline-circle"></div>
          </div>
          <div class="timeline-component timeline-content">
            <h3>Maramba Technologies</h3>
            <p>
              Reaching into my first ever education-related employment, I developed websites and maintained them while handling general IT duties.
            </p>
            <ul>
              <li>Offer technical support</li>
              <li>Install and update company software and hardware</li>
              <li>Maintaining the company website</li>
              <li>Review diagnostics</li>
              <li>Implement security measures</li>
            </ul>
          </div>
        </div>
      </section>
    </section>
    <!-- Projects Section -->
    <section id="projects" class="projects">
      <h2>Projects</h2>
      <div class="project">
        <h3>Open-source learning management system</h3>
        <p>
          A software application or web-based technology used to plan, implement, and assess a specific learning process. It helps create and deliver content, monitor student participation, and assess student performance.
        </p>
      </div>
    </section>
    <!-- Contact Section -->
    <section id="contact" class="contact">
      <h2>Contact</h2>
      <p>Email: mtavi721@gmail.com</p>
      <p>Phone: 0691550223</p>
      <p>GitHub: <a href="https://github.com/yourgithub" target="_blank">github.com/yourgithub</a></p>
      <p>LinkedIn: <a href="https://www.linkedin.com/in/tavada-mpofu-23a9302a9" target="_blank">linkedin.com/Tavada(lelo)Mpofu</a></p>
    </section>
    <!-- Footer -->
    <footer>
      <p>&copy; 2025 Tavada(lelo) Mpofu. All Rights Reserved.</p>
    </footer>
  </main>
</body>
</html>

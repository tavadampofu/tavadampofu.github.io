<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tavada Mpofu Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
            color: #e0e0e0;
            line-height: 1.6;
        }

        header {
            background: #000;
            padding: 2rem 0;
            border-bottom: 3px solid #ff69b4;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #ff69b4;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            color: #e0e0e0;
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }

        nav a:hover {
            color: #ff69b4;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .hero {
            padding: 6rem 0;
            text-align: center;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            color: #fff;
        }

        .hero .highlight {
            color: #ff69b4;
        }

        .hero p {
            font-size: 1.3rem;
            color: #b0b0b0;
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            padding: 1rem 2rem;
            background: #ff69b4;
            color: #000;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255, 105, 180, 0.3);
        }

        .section {
            padding: 4rem 0;
        }

        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            color: #fff;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background: #ff69b4;
            margin: 1rem auto 0;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background: #2d2d2d;
            padding: 2rem;
            border-radius: 10px;
            border: 2px solid #3d3d3d;
            transition: transform 0.3s, border-color 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-5px);
            border-color: #ff69b4;
        }

        .skill-card h3 {
            color: #ff69b4;
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: #2d2d2d;
            border-radius: 10px;
            overflow: hidden;
            border: 2px solid #3d3d3d;
            transition: transform 0.3s, border-color 0.3s;
        }

        .project-card:hover {
            transform: scale(1.03);
            border-color: #ff69b4;
        }

        .project-header {
            background: #1a1a1a;
            padding: 1.5rem;
            border-bottom: 2px solid #ff69b4;
        }

        .project-header h3 {
            color: #fff;
            font-size: 1.5rem;
        }

        .project-body {
            padding: 1.5rem;
        }

        .project-body p {
            color: #b0b0b0;
            margin-bottom: 1rem;
        }

        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tag {
            background: #3d3d3d;
            color: #ff69b4;
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.85rem;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: #2d2d2d;
            padding: 2rem;
            border-radius: 10px;
            border: 2px solid #3d3d3d;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #ff69b4;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            background: #1a1a1a;
            border: 2px solid #3d3d3d;
            border-radius: 5px;
            color: #e0e0e0;
            font-family: inherit;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #ff69b4;
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        footer {
            background: #000;
            padding: 2rem 0;
            text-align: center;
            border-top: 3px solid #ff69b4;
            margin-top: 4rem;
        }

        footer p {
            color: #b0b0b0;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 1rem;
        }

        .social-links a {
            color: #e0e0e0;
            font-size: 1.5rem;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: #ff69b4;
        }

        .timeline {
            position: relative;
            max-width: 900px;
            margin: 0 auto;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 3px;
            height: 100%;
            background: #ff69b4;
        }

        .timeline-item {
            margin-bottom: 3rem;
            position: relative;
        }

        .timeline-item:nth-child(odd) {
            padding-right: calc(50% + 2rem);
        }

        .timeline-item:nth-child(even) {
            padding-left: calc(50% + 2rem);
        }

        .timeline-content {
            background: #2d2d2d;
            padding: 2rem;
            border-radius: 10px;
            border: 2px solid #3d3d3d;
            position: relative;
            transition: transform 0.3s, border-color 0.3s;
        }

        .timeline-content:hover {
            transform: translateY(-5px);
            border-color: #ff69b4;
        }

        .timeline-item:nth-child(odd) .timeline-content::after {
            content: '';
            position: absolute;
            right: -12px;
            top: 20px;
            width: 0;
            height: 0;
            border-left: 10px solid #3d3d3d;
            border-top: 10px solid transparent;
            border-bottom: 10px solid transparent;
        }

        .timeline-item:nth-child(even) .timeline-content::after {
            content: '';
            position: absolute;
            left: -12px;
            top: 20px;
            width: 0;
            height: 0;
            border-right: 10px solid #3d3d3d;
            border-top: 10px solid transparent;
            border-bottom: 10px solid transparent;
        }

        .timeline-content:hover::after {
            border-left-color: #ff69b4;
            border-right-color: #ff69b4;
        }

        .timeline-dot {
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 20px;
            height: 20px;
            background: #ff69b4;
            border: 4px solid #1a1a1a;
            border-radius: 50%;
            top: 20px;
            z-index: 1;
        }

        .timeline-content h3 {
            color: #ff69b4;
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .timeline-content .company {
            color: #fff;
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }

        .timeline-content .date {
            color: #b0b0b0;
            font-size: 0.9rem;
            margin-bottom: 1rem;
            font-style: italic;
        }

        .timeline-content ul {
            list-style: none;
            padding-left: 0;
        }

        .timeline-content ul li {
            color: #b0b0b0;
            margin-bottom: 0.5rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .timeline-content ul li::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: #ff69b4;
            font-size: 1.2rem;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            nav ul {
                gap: 1rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .timeline::before {
                left: 20px;
            }

            .timeline-item:nth-child(odd),
            .timeline-item:nth-child(even) {
                padding-right: 0;
                padding-left: 60px;
            }

            .timeline-dot {
                left: 20px;
            }

            .timeline-item:nth-child(odd) .timeline-content::after,
            .timeline-item:nth-child(even) .timeline-content::after {
                left: -12px;
                right: auto;
                border-right: 10px solid #3d3d3d;
                border-left: none;
            }

            .timeline-content:hover::after {
                border-right-color: #ff69b4;
            }
        }

        .game-container {
            max-width: 600px;
            margin: 0 auto;
            background: #2d2d2d;
            padding: 2rem;
            border-radius: 10px;
            border: 2px solid #3d3d3d;
            text-align: center;
        }

        .game-info {
            display: flex;
            justify-content: space-between;
            margin-bottom: 2rem;
            font-size: 1.2rem;
        }

        .game-info span {
            color: #ff69b4;
            font-weight: bold;
        }

        #gameCanvas {
            background: #1a1a1a;
            border: 3px solid #ff69b4;
            border-radius: 5px;
            display: block;
            margin: 0 auto;
            cursor: pointer;
        }

        .game-controls {
            margin-top: 1.5rem;
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .game-btn {
            padding: 0.8rem 1.5rem;
            background: #3d3d3d;
            color: #ff69b4;
            border: 2px solid #ff69b4;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
        }

        .game-btn:hover {
            background: #ff69b4;
            color: #000;
        }

        #gameMessage {
            margin-top: 1rem;
            font-size: 1.2rem;
            color: #ff69b4;
            min-height: 30px;
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">&lt;Tavada (Lelo) Mpofu&gt;</div>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#game">Game</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="container">
            <h1>Hi, I'm <span class="highlight">TAVADA MPOFU</span></h1>
            <p>Software Engineer | Full-Stack Developer | Problem Solver</p>
            <a href="#contact" class="btn">Get In Touch</a>
        </div>
    </section>

    <section id="skills" class="section">
        <div class="container">
            <h2 class="section-title">Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>Frontend Development</h3>
                    <p>| HTML | CSS |React | Responsive Design | UI/UX |</p>
                </div>
                <div class="skill-card">
                    <h3>Backend Development</h3>
                    <p>| Android Studio Code | C++ | C# | Java | JavaScript | Node.js | PHP | Python | REST APIs |</p>
                </div>
                <div class="skill-card">
                    <h3>Database & DevOps</h3>
                    <p>| MySQL | MongoD | Git | GitHub | AWS |</p>
                </div>
				<div class="skill-card">
                    <h3>Cybersecurity</h3>
                    <p>| GDPR Compliance Basics Cybersecurity | Encryption |</p>
                </div>
				<div class="skill-card">
                    <h3>Microsoft Packages</h3>
                    <p>| MS Office | Excel | PowerPoint |</p>
                </div>
                <div class="skill-card">
                    <h3>Soft Skills</h3>
                    <p>Fostering relationships | Negotiating and Listening | Interpreting requirements | Energetic and Passionate</p>					
                    <p>Result and value-driven |Resilient and a Problem solver | Well-articulated and Analytical | Trustworthy </p>
                </div>
            </div>
        </div>
    </section>

    <section id="experience" class="section">
        <div class="container">
            <h2 class="section-title">Work Experience</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <h3> IT Specialist </h3>
                        <div class="company">Maramba Technologies</div>
                        <div class="date">Sept 2023 - Sept 2025</div>
                        <ul>
                            <li>Offer technical support to company staff and troubleshoot computer problems. </li>
                            <li>Mentored junior developers and conducted code reviews. </li>
                            <li>Improved application performance by 40% through optimization. </li>
                            <li>Install and update company software and hardware as needed. </li>
							<li>Regularly maintaining the company website, through the addition of requests.</li>
                        </ul>
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <h3>Web Developer</h3>
                        <div class="company">Nunu’s The Artist</div>
                        <div class="date">JSept 2025 – Jan 2026 (on-request)</div>
                        <ul>
                            <li>Built responsive web applications using React and Node.js</li>
                            <li>Collaborated with design team to implement pixel-perfect UIs</li>
                            <li>Front-end Development focusing on user interface, user experience and client-side development. </li>
                            <li>Deals deployment, scaling, and maintenance of web applications.</li>
                        </ul>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <section id="projects" class="section">
        <div class="container">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-header">
                        <h3>CertiFinder</h3>
						<a href="https://certifinder.vercel.app/">CertiFinder</a>
                    </div>
                    <div class="project-body">
                        <p>(AI-Powered Certificate Analysis Application) – Co-Founder / Backend developer / Frontend Developer </p>
                        <div class="tech-tags">
                            <span class="tag">React</span>
                            <span class="tag">Node.js</span>
                            <span class="tag">MongoDB</span>
							<span class="tag">Typescript</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-header">
                        <h3>Nunu’s the Artist</h3>
						<a href="http://wptesting.co.za.dedi1045.jnb2.host-h.net/nunustheartist/">Nunu's the Artist</a>
                    </div>
                    <div class="project-body">
                        <p>(Restaurant Website) – Co-Designer / Backend developer / Frontend Developer </p>
                        <div class="tech-tags">
                            <span class="tag">HTML & CSS</span>
							<span class="tag">Javascript</span>
                            <span class="tag">PHP</span>
                            <span class="tag">MySQL</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-header">
                        <h3>Tavada Mpofu</h3>
						<a href="https://tavadampofu.github.io/">Tavada Mpofu</a>
                    </div>
                    <div class="project-body">
                        <p>(Self-Portfolio Website) – Founder / Designer / Backend developer / Frontend Developer</p>
                        <div class="tech-tags">
                            <span class="tag">HTML</span>
							<span class="tag">Javascript</span>
                            <span class="tag">API</span>
							<span class="tag">PHP</span>
                            <span class="tag">CSS</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="game" class="section">
        <div class="container">
            <h2 class="section-title">Take a Break - Play Snake!</h2>
            <div class="game-container">
                <div class="game-info">
                    <div>Score: <span id="score">0</span></div>
                    <div>High Score: <span id="highScore">0</span></div>
                </div>
                <canvas id="gameCanvas" width="400" height="400"></canvas>
                <div id="gameMessage"></div>
                <div class="game-controls">
                    <button class="game-btn" onclick="startGame()">Start Game</button>
                    <button class="game-btn" onclick="pauseGame()">Pause</button>
                </div>
                <p style="color: #b0b0b0; margin-top: 1rem;">Use Arrow Keys or WASD to control the snake</p>
            </div>
        </div>
    </section>

    <section id="contact" class="section">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <form class="contact-form" method="POST" action="contact.php">
                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" name="message" required></textarea>
                </div>
                <button type="submit" class="btn">Send Message</button>
            </form>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="social-links">
                <a href="tavadampofu.github.io">GitHub</a>
                <a href="linkedin.com/Tavada(lelo)Mpofu">LinkedIn</a>
                <a href="mtavi721@gmail.com">Gmail</a>
            </div>
            <p>&copy; 2026 Tavada Mpofu. All rights reserved.</p>
        </div>
    </footer>

    <script>
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        const scoreElement = document.getElementById('score');
        const highScoreElement = document.getElementById('highScore');
        const messageElement = document.getElementById('gameMessage');

        const gridSize = 20;
        const tileCount = canvas.width / gridSize;

        let snake = [{x: 10, y: 10}];
        let velocity = {x: 0, y: 0};
        let food = {x: 15, y: 15};
        let score = 0;
        let highScore = localStorage.getItem('snakeHighScore') || 0;
        let gameLoop;
        let gameRunning = false;
        let isPaused = false;

        highScoreElement.textContent = highScore;

        function startGame() {
            if (gameRunning && !isPaused) return;
            
            if (!gameRunning) {
                snake = [{x: 10, y: 10}];
                velocity = {x: 1, y: 0};
                score = 0;
                scoreElement.textContent = score;
                placeFood();
                gameRunning = true;
                isPaused = false;
                messageElement.textContent = '';
            } else if (isPaused) {
                isPaused = false;
                messageElement.textContent = '';
            }
            
            if (gameLoop) clearInterval(gameLoop);
            gameLoop = setInterval(update, 100);
        }

        function pauseGame() {
            if (!gameRunning) return;
            isPaused = !isPaused;
            
            if (isPaused) {
                clearInterval(gameLoop);
                messageElement.textContent = 'Game Paused';
            } else {
                gameLoop = setInterval(update, 100);
                messageElement.textContent = '';
            }
        }

        function update() {
            if (isPaused) return;

            const head = {x: snake[0].x + velocity.x, y: snake[0].y + velocity.y};

            if (head.x < 0 || head.x >= tileCount || head.y < 0 || head.y >= tileCount) {
                gameOver();
                return;
            }

            for (let segment of snake) {
                if (head.x === segment.x && head.y === segment.y) {
                    gameOver();
                    return;
                }
            }

            snake.unshift(head);

            if (head.x === food.x && head.y === food.y) {
                score++;
                scoreElement.textContent = score;
                placeFood();
                
                if (score > highScore) {
                    highScore = score;
                    highScoreElement.textContent = highScore;
                    localStorage.setItem('snakeHighScore', highScore);
                }
            } else {
                snake.pop();
            }

            draw();
        }

        function draw() {
            ctx.fillStyle = '#1a1a1a';
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            ctx.fillStyle = '#ff69b4';
            ctx.fillRect(food.x * gridSize, food.y * gridSize, gridSize - 2, gridSize - 2);

            snake.forEach((segment, index) => {
                ctx.fillStyle = index === 0 ? '#ff69b4' : '#b0b0b0';
                ctx.fillRect(segment.x * gridSize, segment.y * gridSize, gridSize - 2, gridSize - 2);
            });
        }

        function placeFood() {
            food = {
                x: Math.floor(Math.random() * tileCount),
                y: Math.floor(Math.random() * tileCount)
            };

            for (let segment of snake) {
                if (food.x === segment.x && food.y === segment.y) {
                    placeFood();
                    return;
                }
            }
        }

        function gameOver() {
            clearInterval(gameLoop);
            gameRunning = false;
            messageElement.textContent = 'Game Over! Score: ' + score;
        }

        document.addEventListener('keydown', (e) => {
            if (!gameRunning || isPaused) return;

            switch(e.key) {
                case 'ArrowUp':
                case 'w':
                case 'W':
                    if (velocity.y === 0) velocity = {x: 0, y: -1};
                    break;
                case 'ArrowDown':
                case 's':
                case 'S':
                    if (velocity.y === 0) velocity = {x: 0, y: 1};
                    break;
                case 'ArrowLeft':
                case 'a':
                case 'A':
                    if (velocity.x === 0) velocity = {x: -1, y: 0};
                    break;
                case 'ArrowRight':
                case 'd':
                case 'D':
                    if (velocity.x === 0) velocity = {x: 1, y: 0};
                    break;
            }
        });

        draw();
    </script>
</body>
</html>

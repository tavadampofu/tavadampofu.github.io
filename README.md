<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
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
            top: 0;
            left: 0;
            z-index: 1000;
        }

        .main-navbar ul {
            list-style: none;
            padding: 0;
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
            background: url('https://source.unsplash.com/1600x900/?space,stars') no-repeat center center/cover;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
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
        }

        /* Card */
        .card {
            position: relative;
            padding: 20px;
            background: #1f1f1f;
            border-radius: 20px;
            box-shadow: 0 0 15px rgba(255, 0, 127, 0.5);
            text-align: center;
            max-width: 300px;
            margin: 40px auto;
            width: 190px;
            height: 254px;
        }

        .card-overlay {
            position: absolute;
            inset: 0;
            pointer-events: none;
            background: repeating-conic-gradient(var(--bg) 0.0000001%, var(--grey) 0.000104%) 60% 60%/600% 600%;
            filter: opacity(10%) contrast(105%);
        }

        .card-inner {
            font-size: 1.5rem;
            font-weight: bold;
            color: white;
        }

        .tag-line {
            font-size: 1.5rem;
            color: #ff007f;
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

        /* Sections */
        .section {
            padding: 50px 10%;
        }

        .section-content {
            background: rgba(255, 0, 127, 0.1);
            padding: 20px;
            border-radius: 10px;
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

        /* Timeline */
        .timeline .card {
            background: linear-gradient(135deg, #ff007f, #5500ff);
            padding: 20px;
            border-left: 4px solid #ff007f;
            margin-bottom: 20px;
        }

        .timeline .card .title {
            color: #ff007f;
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
        }

        .timeline-component {
            margin: 0px 20px 20px 20px;
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
        .projects h2,
        .contact h2 {
            text-align: center;
            color: #ff007f;
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

        /* Contact */
        .contact p {
            text-align: center;
            font-size: 1.2rem;
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
            padding: 20px;
            background: linear-gradient(135deg, #ff007f, #5500ff);
            margin-top: 20px;
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
        <input type="checkbox" id="menu-button">
        <nav class="main-navbar">
            <ul>
                <li><a href="#home-section">HOME</a></li>
                <li><a href="#about-section">ABOUT</a></li>
                <li><a href="#experience-section">EXPERIENCE</a></li>
                <li><a href="#project-section">PROJECT</a></li>
                <li><a href="#contact-section">CONTACT</a></li>
            </ul>
        </nav>
    </header>
    <main class="container">
        <section class="section section-hero" id="home-section">
            <div class="hero-section-content">
                <h1>I AM</h1>
                <h1>TAVADA (LELO) MPOFU</h1>
                <p class="tag-line">Final year Information Technology Student</p>
                <div class="card">
                    <div class="card-overlay"></div>
                    <div class="card-inner">YOUR<br>CONTENT<br>HERE</div>
                </div>
                <div class="social-icons-wrapper">
                    <a href="#"><i class="fa-brands fa-github"></i></a>
                    <a href="#"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#"><i class="fa-brands fa-twitter"></i></a>
                    <a href="#"><i class="fa-brands fa-linkedin"></i></a>
                </div>
            </div>
        </section>

        <section class="section section-about" id="about-section">
            <div class="section-content">
                <div class="text-with-border">
                    <p>
                        Motivated IT student with a strong foundation in programming, software development,
                        web development, and systems analysis, seeking to apply technical skills and
                        innovative thinking in a challenging role. Passionate about leveraging technology
                        to solve real-world problems and eager to contribute to projects that drive
                        efficiency and innovation while continuing to grow as an IT professional.
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
                        <p>Gaining experience in my first ever workplace setting as a salesperson.
                            Learning to work with clientele and in a team environment.</p>
                        <ul>
                            <li>Welcoming customers to the store</li>
                            <li>Instructing customers on painting processes and rules</li>
                            <li>Ensuring the shop floor is correctly replenished</li>
                            <li>General office/administrative duties</li>
                            <li>Supporting the store in meeting its sales target</li>
                        </ul>
                    </div>
                    <!-- Additional timeline components... -->
                </div>
            </section>
        </section>

        <!-- Projects Section -->
        <section id="projects" class="projects">
            <h2>Projects</h2>
            <div class="project">
                <h3>Open-source learning management system</h3>
                <p>A software application or web-based technology used to plan, implement, and assess a specific learning process.
                    It helps create and deliver content, monitor student participation, and assess student performance.</p>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="contact">
            <h2>Contact</h2>
            <p>Email: mtavi721@gmail.com</p>
            <p>Phone: 0691550223</p>
            <p>GitHub: <a href="https://github.com/yourgithub" target="_blank">github.com/yourgithub</a></p>
            <p>LinkedIn: <a href="www.linkedin.com/in/tavada-mpofu-23a9302a9" target="_blank">linkedin.com/Tavada(lelo)Mpofu</a></p>
        </section>

        <!-- Footer -->
        <footer>
            <p>&copy; 2025 Tavada(lelo) Mpofu. All Rights Reserved.</p>
        </footer>
    </main>
</body>

</html>

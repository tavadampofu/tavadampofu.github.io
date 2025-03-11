<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Jost:wght@200;300;400&display=swap');
        body {
            background-color: #000;
            color: #fff;
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }

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
        }

        .tag-line {
            font-size: 1.5rem;
            color: #ff007f;
        }

        .social-icons-wrapper a {
            color: #ff007f;
            font-size: 1.5rem;
            margin: 0 10px;
            transition: transform 0.3s ease-in-out;
        }

        .social-icons-wrapper a:hover {
            transform: scale(1.2);
            color: #fff;
        }

        .section {
            padding: 50px 10%;
        }

        .section-content {
            background: rgba(255, 0, 127, 0.1);
            padding: 20px;
            border-radius: 10px;
        }

        .text-with-border {
            border: 2px solid #ff007f;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px #ff007f;
        }

        .timeline .card {
            background: rgba(255, 0, 127, 0.2);
            padding: 20px;
            border-left: 4px solid #ff007f;
            margin-bottom: 20px;
        }
		
		.timeline .card .title {
    color: #ff007f;
}

@import url('https://fonts.googleapis.com/css2?family=Jost:wght@200;300;400&display=swap');
.design-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #1f1f1f;
  min-height: 100vh;
  padding: 100px 0;
  font-family: Jost;
}

.design {
  display: flex;
  align-items: center;
  justify-content: center;
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
  padding: 20px;
  background: #1f1f1f;
  -webkit-box-shadow: 5px 5px 10px #1a1a1a, -5px -5px 10px #242424;
          box-shadow: 5px 5px 10px #1a1a1a, -5px -5px 10px #242424;
  border-radius: 5px;
  color: white;
  padding: 1.75rem;
  transition: 0.4s ease;
  overflow-wrap: break-word !important;
  margin: 1rem;
  margin-bottom: 20px;
  border-radius: 6px;
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
    background-image: linear-gradient(45deg, #F27121, #E94057, #8A2387);
    width: 3px;
    height: 100%;
  }
  .main-middle {
    opacity: 0;
  }
  .timeline-circle {
    position: absolute;
    top: 0;
    left: 50%;
    width: 15px;
    height: 15px;
    border-radius: 50%;
    background-image: linearlinear-gradient(45deg, #F27121, #E94057, #8A2387);
    -webkit-transform: translateX(-50%);
            transform: translateX(-50%);
  }
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

        .projects h2, .contact h2 {
            text-align: center;
            color: #ff007f;
        }

        .project {
            background: rgba(255, 0, 127, 0.2);
            padding: 20px;
            margin: 20px 0;
            border-radius: 10px;
            box-shadow: 0 0 10px #ff007f;
        }

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

<main>
    <section class="section section-hero" id="home-section">
        <div class="hero-section-content">
            <h1>I AM</h1>
            <h1>TAVADA MPOFU</h1>
            <p class="tag-line">Final year Information Technology Student</p>
        </div>
    </section>

    <section class="section" id="about-section">
        <div class="section-content">
            <div class="text-with-border">
                <p>Motivated IT student with a strong foundation in programming, software development,
                        web development, and systems analysis, seeking to apply technical skills and
                        innovative thinking in a challenging role. Passionate about leveraging technology
                        to solve real-world problems and eager to contribute to projects that drive
                        efficiency and innovation while continuing to grow as an IT professional.</p>
            </div>
        </div>
    </section>

<style>@import url('https://fonts.googleapis.com/css2?family=Jost:wght@200;300;400&display=swap');</style>
<!--This is the main container that contains the whole timeline.-->
<section class="design-section">
<div class="timeline">

                  <div class="timeline-empty">
                  </div>

               <div class="timeline-middle">
                   <div class="timeline-circle"></div>
               </div>
               <div class="timeline-component timeline-content">
                <h3>Art Jamming Melrose Arch</h3>
                <p>Gaining experience in my first ever workplace setting as a salesperson.
                                    Learning to work with clientele and in a team environment.
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
                         <b>TERTIARY EDUCATION</b></p>
                                <p>
                                    Majoring in Computer Science, I gained many skills and learned several
                                    programming languages. I also played netball and represented my school's first team.
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
                <div class="timeline-empty">
                </div>

                <div class="timeline-empty">
                </div>

               <div class="timeline-middle">
                   <div class="timeline-circle"></div>
               </div>
               <div class=" timeline-component timeline-content">
                <h3>Maramba Technologies</h3>
                <p>
                                 Reaching into my first ever education-related employment, I developed
                                    websites and maintained them while handling general IT duties.
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
    </div> 
</section>

    <section class="section" id="projects">
        <h2>Projects</h2>
        <div class="project">
            <h3>Open-source learning management system</h3>
            <p>a software application or web-based technology used to plan, implement and assess a specific learning process,
			a way to create and deliver content, monitor student participation and assess student performance</p>
        </div>
    </section>

    <section class="section" id="contact">
        <h2>Contact</h2>
        <p>Email: mtavi721@gmail.com</p>
        <p>Phone: 0691550223</p><p>LinkedIn: <a href="www.linkedin.com/in/tavada-mpofu-23a9302a9" target="_blank">linkedin.com/Tavada(lelo)Mpofu</a></p><p>GitHub: <a href="https://github.com/yourgithub">github.com/yourgithub</a></p>
    </section>
</main>

<footer>
    <p>&copy; 2025 Tavada(lelo) Mpofu. All Rights Reserved.</p>
</footer>
</body>
</html>

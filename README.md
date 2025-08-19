!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Portfolio</title>
        <style>
            * {
                margin: 0;
                padding: 0;
                box-sizing: border-box;
                font-family: 'Arial', sans-serif;
            }

            body {
                line-height: 1.6;
                color: #333;
                background-color: #f4f4f4;
            }

            nav {
                background-color: #2c3e50;
                padding: 1rem;
                position: fixed;
                width: 100%;
                top: 0;
                z-index: 1000;
            }

            nav ul {
                list-style: none;
                display: flex;
                justify-content: center;
                gap: 2rem;
            }

            nav ul li a {
                color: white;
                text-decoration: none;
                font-weight: bold;
                transition: color 0.3s;
            }

            nav ul li a:hover {
                color: #3498db;
            }

            .container {
                max-width: 800px;
                margin: 80px auto 20px;
                padding: 20px;
                background-color: white;
                border-radius: 8px;
                box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            }

            h1 {
                color: #2c3e50;
                text-align: center;
                margin-bottom: 1rem;
            }

            h3 {
                color: #3498db;
                margin-top: 1.5rem;
                margin-bottom: 0.5rem;
            }

            p {
                margin-bottom: 1rem;
                text-align: justify;
            }

            ul {
                list-style: square;
                margin-left: 20px;
                margin-bottom: 1rem;
            }

            li {
                margin-bottom: 0.5rem;
            }

            footer {
                background-color: #2c3e50;
                color: white;
                text-align: center;
                padding: 1rem;
                position: relative;
                bottom: 0;
                width: 100%;
            }

            #theme-toggle {
                position: fixed;
                top: 1rem;
                right: 1rem;
                padding: 0.5rem 1rem;
                background-color: #3498db;
                color: white;
                border: none;
                border-radius: 5px;
                cursor: pointer;
                transition: background-color 0.3s;
            }

            #theme-toggle:hover {
                background-color: #2980b9;
            }

            .dark-mode {
                background-color: #2c3e50;
                color: #f4f4f4;
            }

            .dark-mode .container {
                background-color: #34495e;
                color: #f4f4f4;
            }

            .dark-mode h1 {
                color: #ecf0f1;
            }

            .dark-mode h3 {
                color: #3498db;
            }

            @media (max-width: 600px) {
                nav ul {
                    flex-direction: column;
                    align-items: center;
                }

                .container {
                    margin: 100px 20px 20px;
                    padding: 15px;
                }
            }
        </style>
    </head>
    <body>
        <nav>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#skills">Skills</a></li>
            </ul>
        </nav>

        <button id="theme-toggle">Toggle Dark Mode</button>

        <div class="container">
            <h1>Karthic E</h1>
            <h3 id="about">About</h3>
            <p>I am E. Karthic, a passionate and driven Electronics and Communication Engineering student at SNS College of Technology, with a strong interest in robotics, embedded systems, and AI-driven solutions. I have hands-on experience in building and mentoring robotics projects, participating in hackathons, and developing innovative applications such as Attendify and Med X. My skills span across Arduino, Python, HTML/CSS/JavaScript, and cross-platform app development, complemented by creative abilities in video editing and Canva design. I am an enthusiastic learner, currently enhancing my expertise in Japanese language and emerging technologies, with a long-term goal of working in Japan at a leading MNC.</p>
            <h3 id="projects">Projects</h3>
            <ul>
                <li>Attendify</li>
                <li>Med X</li>
                <li>Eco Sense</li>
                <li>GTA-Style 2D Open-World Game</li>
                <li>Robotics Mentoring</li>
            </ul>
            <h3 id="skills">Skills</h3>
            <ul>
                <li>Robotics</li>
                <li>Embedded Systems</li>
                <li>Arduino Programming</li>
                <li>Python</li>
                <li>HTML, CSS & JavaScript</li>
                <li>Cross-Platform App Development</li>
                <li>Video Editing</li>
                <li>Canva Design</li>
            </ul>
        </div>

        <footer>
            <p>karthiceaswaran@gmail.com</p>
            <p>9047123344</p>
        </footer>

        <script>
            document.querySelectorAll('nav a').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href').substring(1);
                    const targetElement = document.getElementById(targetId);
                    window.scrollTo({
                        top: targetElement.offsetTop - 70,
                        behavior: 'smooth'
                    });
                });
            });

            const themeToggle = document.getElementById('theme-toggle');
            themeToggle.addEventListener('click', () => {
                document.body.classList.toggle('dark-mode');
                themeToggle.textContent = document.body.classList.contains('dark-mode')
                    ? 'Toggle Light Mode'
                    : 'Toggle Dark Mode';
            });
        </script>
    </body>
</html>


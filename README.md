<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }
        
        a {
            text-decoration: none;
            color: #3498db;
        }
        
        .container {
            max-width: 1100px;
            margin: auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background: #2c3e50;
            color: #fff;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        header h1 {
            font-size: 24px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: #fff;
            font-weight: bold;
        }
        
        nav ul li a:hover {
            color: #3498db;
        }
        
        /* Hero Section */
        #hero {
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://via.placeholder.com/1920x1080') no-repeat center center/cover;
            color: #fff;
            padding-top: 80px;
        }
        
        #hero h2 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        #hero p {
            font-size: 20px;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            background: #3498db;
            color: #fff;
            padding: 10px 30px;
            border-radius: 5px;
            margin: 0 10px;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background: #2980b9;
            transform: scale(1.05);
        }
        
        /* About Section */
        #about {
            padding: 80px 0;
            background: #fff;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 36px;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .about-img {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }
        
        .about-img img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }
        
        .about-text h3 {
            font-size: 24px;
            margin-bottom: 20px;
        }
        
        /* Skills Section */
        #skills {
            padding: 80px 0;
            background: #f4f4f4;
        }
        
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }
        
        .skill {
            background: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
            flex: 1;
            min-width: 200px;
            transition: all 0.3s ease;
        }
        
        .skill:hover {
            transform: translateY(-10px);
        }
        
        .skill i {
            font-size: 40px;
            color: #3498db;
            margin-bottom: 15px;
        }
        
        /* Projects Section */
        #projects {
            padding: 80px 0;
            background: #fff;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: #fff;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }
        
        .project-img {
            height: 200px;
            overflow: hidden;
        }
        
        .project-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: all 0.5s ease;
        }
        
        .project-card:hover .project-img img {
            transform: scale(1.1);
        }
        
        .project-info {
            padding: 20px;
        }
        
        .project-info h3 {
            margin-bottom: 10px;
        }
        
        /* Contact Section */
        #contact {
            padding: 80px 0;
            background: #f4f4f4;
        }
        
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: #fff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        
        .form-group textarea {
            height: 150px;
        }
        
        /* Footer */
        footer {
            background: #2c3e50;
            color: #fff;
            text-align: center;
            padding: 20px 0;
        }
        
        .social-links {
            margin: 20px 0;
        }
        
        .social-links a {
            color: #fff;
            margin: 0 10px;
            font-size: 20px;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            color: #3498db;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            header .container {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 15px;
                justify-content: center;
            }
            
            #hero h2 {
                font-size: 36px;
            }
            
            #hero p {
                font-size: 18px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <h1>My Portfolio</h1>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="hero">
        <div class="container">
            <div>
                <h2>Hi, I'm Pasupathi R</h2>
                <p>A passionate web developer creating beautiful, functional websites and applications.</p>
                <a href="#projects" class="btn">View My Work</a>
                <a href="#contact" class="btn">Contact Me</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-img">
                    <img src="" alt="Profile Image">
                </div>
                <div class="about-text">
                    <h3>Who I Am</h3>
                    <p>I'm a full-stack web developer with building responsive websites and web applications. I specialize in HTML, CSS, JavaScript, and various frameworks.</p>
                    <p>When I'm not coding, you can find me hiking, reading, or experimenting with new technologies. I'm passionate about creating intuitive user experiences and solving complex problems with elegant solutions.</p>
                    <p>My approach to development combines technical expertise with creative problem-solving to deliver high-quality products that meet client needs.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <h2 class="section-title">My Skills</h2>
            <div class="skills-container">
                <div class="skill">
                    <i class="fab fa-html5"></i>
                    <h3>HTML5</h3>
                    <p>Semantic markup, accessibility, SEO optimization</p>
                </div>
                <div class="skill">
                    <i class="fab fa-css3-alt"></i>
                    <h3>CSS3</h3>
                    <p>Responsive design, animations, Flexbox, Grid</p>
                </div>
                <div class="skill">
                    <i class="fab fa-js"></i>
                    <h3>JavaScript</h3>
                    <p>ES6+, DOM manipulation, async programming</p>
                </div>
                <div class="skill">
                    <i class="fab fa-react"></i>
                    <h3>React</h3>
                    <p>Component-based architecture, hooks, state management</p>
                </div>
                <div class="skill">
                    <i class="fab fa-node-js"></i>
                    <h3>Node.js</h3>
                    <p>Server-side development, REST APIs, Express</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <h2 class="section-title">My Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://okcredit-blog-images-prod.storage.googleapis.com/2021/04/ecommerce3-1.jpg" alt="Project 1">
                    </div>
                    <div class="project-info">
                        <h3>E-Commerce Website</h3>
                        <p>A fully responsive e-commerce platform with product filtering, cart functionality, and secure checkout.</p>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSSUVMKSMWSKpgS_eQ398zjUKl3rNzbLWsHsA&s" alt="Project 2">
                    </div>
                    <div class="project-info">
                        <h3>Task Management App</h3>
                        <p>A productivity application for organizing tasks with drag-and-drop functionality and team collaboration.</p>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://png.pngtree.com/png-clipart/20230414/ourmid/pngtree-weather-icon-png-image_6685458.png" alt="Project 3">
                    </div>
                    <div class="project-info">
                        <h3>Weather Dashboard</h3>
                        <p>Real-time weather information with 5-day forecast using API integration and geolocation.</p>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <div class="contact-form">
                <form>
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="subject">Subject</label>
                        <input type="text" id="subject" name="subject" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" name="type..." required></textarea>
                    </div>
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
            <p>&copy; 2023 My Portfolio. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>

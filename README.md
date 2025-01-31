<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aniket Patil | Portfolio</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #121212;
            color: #fff;
            text-align: center;
            overflow: hidden;
        }
        header {
            background: #1f1f1f;
            padding: 40px;
            font-size: 1.5em;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 10;
        }
        nav ul {
            list-style: none;
            padding: 0;
            display: flex;
            justify-content: center;
            gap: 20px;
            background: #1f1f1f;
            padding: 15px;
            position: fixed;
            width: 100%;
            top: 80px;
            z-index: 10;
        }
        nav ul li {
            display: inline;
        }
        nav a {
            text-decoration: none;
            color: #f39c12;
            font-weight: bold;
            transition: color 0.3s;
        }
        nav a:hover {
            color: #e74c3c;
        }
        .slideshow-container {
            position: relative;
            width: 100%;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .slide {
            display: none;
            width: 100%;
            height: 100vh;
            position: absolute;
            padding-top: 150px;
        }
        .active {
            display: block;
        }
        .controls {
            position: absolute;
            bottom: 50px;
            left: 50%;
            transform: translateX(-50%);
        }
        .btn {
            background: #f39c12;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            margin: 5px;
            border-radius: 5px;
        }
        .btn:hover {
            background: #e74c3c;
        }
    </style>
</head>
<body>
    <header>
        <h1>Aniket Patil</h1>
        <p>Data Analyst | Business Intelligence | Power BI</p>
    </header>
    
    <nav>
        <ul>
            <li><a href="#home" onclick="showSlide(0)">Home</a></li>
            <li><a href="#about" onclick="showSlide(1)">About</a></li>
            <li><a href="#resume" onclick="showSlide(2)">Resume</a></li>
            <li><a href="#projects" onclick="showSlide(3)">Projects</a></li>
            <li><a href="#contact" onclick="showSlide(4)">Contact</a></li>
        </ul>
    </nav>
    
    <div class="slideshow-container">
        <section id="home" class="slide active">
            <h2>Welcome</h2>
            <p>Explore my portfolio to know more about my work and skills.</p>
        </section>
        
        <section id="about" class="slide">
            <h2>About Me</h2>
            <p>I'm a data analytics enthusiast with expertise in Power BI, SQL, Tableau, and Python. Passionate about turning data into insights!</p>
        </section>
        
        <section id="resume" class="slide">
            <h2>Resume</h2>
            <p>Download my resume <a href="resume.pdf" target="_blank">here</a>.</p>
        </section>
        
        <section id="projects" class="slide">
            <h2>Projects</h2>
            <ul>
                <li>🔹 Hyundai HRMS & Sales Dashboard</li>
                <li>🔹 Income Tax Analysis Dashboard</li>
                <li>🔹 App Dashboard (Medical, LTC, Tour, Transfer)</li>
            </ul>
        </section>
        
        <section id="contact" class="slide">
            <h2>Contact</h2>
            <p>Email: ani.patil1351@gmail.com</p>
            <p>LinkedIn: <a href="https://linkedin.com/in/yourprofile" target="_blank">Your Profile</a></p>
            <p>GitHub: <a href="https://github.com/aniketpatil1351" target="_blank">github.com/aniketpatil1351</a></p>
        </section>
        
        <div class="controls">
            <button class="btn" onclick="prevSlide()">Previous</button>
            <button class="btn" onclick="nextSlide()">Next</button>
        </div>
    </div>
    
    <script>
        let currentSlide = 0;
        const slides = document.querySelectorAll(".slide");
        
        function showSlide(index) {
            slides[currentSlide].classList.remove("active");
            currentSlide = index;
            if (currentSlide >= slides.length) currentSlide = 0;
            if (currentSlide < 0) currentSlide = slides.length - 1;
            slides[currentSlide].classList.add("active");
        }
        
        function nextSlide() {
            showSlide(currentSlide + 1);
        }
        
        function prevSlide() {
            showSlide(currentSlide - 1);
        }
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phoebe Emile | Data Analyst</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles */
        :root {
            --primary-blue: #1a4b8c;
            --light-blue: #2d8cda;
            --gradient-blue: linear-gradient(135deg, var(--primary-blue) 0%, var(--light-blue) 100%);
            --white: #ffffff;
            --light-gray: #f5f7fa;
            --dark-gray: #333333;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            color: var(--dark-gray);
            line-height: 1.6;
            background-color: var(--white);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary-blue);
            margin-bottom: 15px;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--gradient-blue);
            border-radius: 2px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--gradient-blue);
            color: var(--white);
            text-decoration: none;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        /* Header Styles */
        header {
            background: var(--gradient-blue);
            color: var(--white);
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .nav-links a:hover {
            color: rgba(255, 255, 255, 0.8);
        }
        
        /* Hero Section */
        .hero {
            padding: 180px 0 100px;
            background: var(--gradient-blue);
            color: var(--white);
            text-align: center;
        }
        
        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
        }
        
        .hero-content h2 {
            font-size: 1.8rem;
            margin-bottom: 30px;
            font-weight: 400;
        }
        
        .hero-content p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 40px;
            opacity: 0.9;
        }
        
        /* About Section */
        .about {
            background-color: var(--white);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
         .profile-img {
            flex: 1;
            text-align: center;
        }
         .profile-img img {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--light-blue);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .profile-img .placeholder {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: var(--gradient-blue);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 5rem;
            margin: 0 auto;
            border: 5px solid var(--light-blue);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 2rem;
            color: var(--primary-blue);
            margin-bottom: 20px;
        }
        
        .about-text p {
            margin-bottom: 15px;
        }
        
        /* Skills Section */
        .skills {
            background-color: var(--light-gray);
        }
        
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .skill-category {
            background: var(--white);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .skill-category h3 {
            color: var(--primary-blue);
            margin-bottom: 20px;
            text-align: center;
        }
        
        .skill-level {
            margin-bottom: 25px;
        }
        
        .skill-level h4 {
            color: var(--dark-gray);
            margin-bottom: 10px;
            font-size: 1.2rem;
        }
        
        .skill-item {
            margin-bottom: 10px;
        }
        
        .skill-item span {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }
        
        /* Experience Section */
        .experience {
            background-color: var(--white);
        }
        
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 6px;
            background-color: var(--light-blue);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -3px;
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item:nth-child(odd) {
            left: 0;
        }
        
        .timeline-item:nth-child(even) {
            left: 50%;
        }
        
        .timeline-content {
            padding: 20px;
            background-color: var(--white);
            position: relative;
            border-radius: 6px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .timeline-content h3 {
            color: var(--primary-blue);
            margin-bottom: 10px;
        }
        
        .timeline-content h4 {
            color: var(--light-blue);
            margin-bottom: 10px;
        }
        
        .timeline-content p {
            margin-bottom: 10px;
        }
        
        /* Projects Section */
        .projects {
            background-color: var(--light-gray);
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: var(--white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
        }
        
        .project-info {
            padding: 20px;
        }
        
        .project-info h3 {
            color: var(--primary-blue);
            margin-bottom: 10px;
        }
        
        .project-info h4 {
            color: var(--light-blue);
            margin-bottom: 10px;
            font-size: 1rem;
        }
        
        .project-info p {
            margin-bottom: 15px;
        }
        
        /* Contact Section */
        .contact {
            background: var(--gradient-blue);
            color: var(--white);
            text-align: center;
        }
        
        .contact-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .contact-content h2 {
            margin-bottom: 30px;
        }
        
        .contact-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .contact-item i {
            font-size: 1.5rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark-gray);
            color: var(--white);
            text-align: center;
            padding: 20px 0;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
            }
            
            .nav-links {
                margin-top: 20px;
            }
            
            .nav-links li {
                margin-left: 15px;
                margin-right: 15px;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .hero-content h2 {
                font-size: 1.5rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">Phoebe Emile</div>
            <ul class="nav-links">
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container hero-content">
            <h1>Phoebe Emile</h1>
            <h2>Mechatronics Engineer & Data Analyst</h2>
            <p>I'm a data analyst with a passion for transforming raw data into clear, actionable insights. Using tools like Python, Excel, and Power BI, I specialize in cleaning datasets, uncovering trends, and building visualizations that support smarter decisions.</p>
            <a href="#contact" class="btn">Get In Touch</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="profile-img">
               <div class="placeholder">
                  <img src="[me.jpg](https://github.com/PhoebeEmile/phoebeEmile.github.io/blob/main/me.jpg)" alt="Phoebe Emile">
              </div>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Transforming Data into Impactful Stories</h3>
                    <p>I enjoy solving complex problems, simplifying information, and helping teams see the story behind the numbers. For me, data isn't just numbers—it's a powerful tool for impact.</p>
                    <p>My vision is to empower smarter decisions through data-driven storytelling. I envision a world where data isn't just collected—it's understood, trusted, and used to solve real problems.</p>
                    <p>As a data analyst, my goal is to bridge the gap between raw information and strategic insight, helping organizations unlock their full potential through clarity, precision, and innovation.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="skills">
        <div class="container">
            <div class="section-title">
                <h2>My Skills</h2>
            </div>
            <div class="skills-container">
                <!-- Technical Skills -->
                <div class="skill-category">
                    <h3>Technical Skills</h3>
                    
                    <div class="skill-level">
                        <h4>Expert</h4>
                        <div class="skill-item">
                            <span>Python</span>
                        </div>
                        <div class="skill-item">
                            <span>Data Visualization</span>
                        </div>
                        <div class="skill-item">
                            <span>SolidWorks</span>
                        </div>
                    </div>
                    
                    <div class="skill-level">
                        <h4>Intermediate</h4>
                        <div class="skill-item">
                            <span>Excel</span>
                        </div>
                        <div class="skill-item">
                            <span>SQL</span>
                        </div>
                        <div class="skill-item">
                            <span>PCB Design (Altium)</span>
                        </div>
                    </div>
                    
                    <div class="skill-level">
                        <h4>Basic</h4>
                        <div class="skill-item">
                            <span>Power BI</span>
                        </div>
                    </div>
                </div>
                
                <!-- Soft Skills -->
                <div class="skill-category">
                    <h3>Soft Skills</h3>
                    
                    <div class="skill-level">
                        <h4>Expert</h4>
                        <div class="skill-item">
                            <span>Problem Solving</span>
                        </div>
                        <div class="skill-item">
                            <span>Technical Presentation</span>
                        </div>
                    </div>
                    
                    <div class="skill-level">
                        <h4>Intermediate</h4>
                        <div class="skill-item">
                            <span>Team Leadership</span>
                        </div>
                        <div class="skill-item">
                            <span>Client Communication</span>
                        </div>
                    </div>
                    
                    <div class="skill-level">
                        <h4>Basic</h4>
                        <div class="skill-item">
                            <span>Project Management</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="experience">
        <div class="container">
            <div class="section-title">
                <h2>Education & Experience</h2>
            </div>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Faculty of Engineering</h3>
                        <h4>2022 - Present</h4>
                        <p>projects:</p>
                        <p>Arduino project | Smart parking system Garage</p>
                        <p>AVR project | Timer using Atmega32, using Assembly language</p>
                        <p>Design project | Designed and Fabricated Pick & place mechanisms</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>AI & Data Engineer - DEPI</h3>
                        <h4>2025 - Present</h4>
                        <!--<p>Currently enrolled in a hands-on program focused on machine learning, data preprocessing, and scalable model deployment. The course emphasizes practical skills in Python, SQL, and cloud technologies.</p>-->
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Summer Internship</h3>
                        <h4>Alstom |Railway company</h4>
                        <p>Internship at the Quality Department.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>AGUAPHOTON ACADEMY - Hardware Engineer, Head presentation</h3>
                        <p>Tools| Altium </p>
                        <p>Designed and Fabricated the communication board of the ROV.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Technical Sales Engineer</h3>
                        <h4>Focus Company</h4>
                        <!--<p></p>-->
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Team Mentor</h3>
                        <h4>M&P Robotics</h4>
                        <p>My team Competed in FLL competition. Made a LEGO robot and programmed it.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <div class="section-title">
                <h2>Professional Projects</h2>
            </div>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-info">
                        <h3>Faculty of Engineering</h3>
                        <h4>Role: Mechatronics student | Tools: Matlab</h4>
                        <p>We studied 2 datasets using different numerical methods to find the best way to represent the data numerically. Using methods like linear regression.</p>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-info">
                        <h3>ROBO-TECH ROV Rangers</h3>
                        <h4>Role: Mechanical Engineer | Tools: SolidWorks, Fabrication</h4>
                        <p>Worked on the mechanical design of the ROV. Was responsible for the fabrication of the design and sealing of the electrical components.</p>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-info">
                        <h3>Aquaphoton Academy</h3>
                        <h4>Role: Hardware Engineer | Tools: Altium, PCB Design</h4>
                        <p>Worked on the main board of the ROV</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Let's Work Together</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                     <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Phone</h3>
                            <p>+201211812211</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Email</h3>
                            <p>Femile2004@gmail.com</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Location</h3>
                            <p>Alexandria, Egypt</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <input type="text" placeholder="Your Name" required>
                        <input type="email" placeholder="Your Email" required>
                        <input type="text" placeholder="Subject" required>
                        <textarea placeholder="Your Message" rows="5" required></textarea>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" class="social-link"><i class="fab fa-github"></i></a>
            </div>
            <p>&copy; 2023 Phoebe Emile. All Rights Reserved.</p>
        </div>
    </footer>
</body>
</html>

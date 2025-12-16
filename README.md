<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shivani Jadhav | Celestial Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Orbitron:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Space Grotesk', sans-serif;
            background: #0a0a14;
            color: #e0e0ff;
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }

        /* Celestial Background */
        .cosmic-bg {
            position: fixed;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(ellipse at 20% 20%, rgba(103, 58, 183, 0.15) 0%, transparent 50%),
                radial-gradient(ellipse at 80% 80%, rgba(0, 150, 136, 0.1) 0%, transparent 50%),
                radial-gradient(ellipse at 40% 60%, rgba(233, 30, 99, 0.1) 0%, transparent 50%),
                linear-gradient(180deg, #0a0a14 0%, #1a1a2e 100%);
            z-index: -2;
        }

        .stars {
            position: fixed;
            width: 100%;
            height: 100%;
            background-image: 
                radial-gradient(2px 2px at 20px 30px, #eee, rgba(0,0,0,0)),
                radial-gradient(2px 2px at 40px 70px, #fff, rgba(0,0,0,0)),
                radial-gradient(1px 1px at 90px 40px, #ddd, rgba(0,0,0,0)),
                radial-gradient(1px 1px at 130px 80px, #fff, rgba(0,0,0,0));
            background-repeat: repeat;
            background-size: 200px 200px;
            z-index: -1;
            animation: twinkle 3s infinite alternate;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.7; }
            50% { opacity: 1; }
        }

        /* Aurora Effect */
        .aurora {
            position: fixed;
            width: 100%;
            height: 300px;
            background: linear-gradient(0deg, transparent, rgba(103, 58, 183, 0.1), transparent);
            filter: blur(40px);
            z-index: -1;
            animation: auroraFlow 10s infinite alternate ease-in-out;
        }

        @keyframes auroraFlow {
            0% { transform: translateY(0) rotate(0deg); opacity: 0.3; }
            100% { transform: translateY(-50px) rotate(1deg); opacity: 0.7; }
        }

        /* Main Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
            position: relative;
            z-index: 1;
        }

        /* Header Section */
        .header {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }

        .cosmic-title {
            font-family: 'Orbitron', sans-serif;
            font-size: 4.5rem;
            background: linear-gradient(90deg, #673ab7, #00bcd4, #e91e63);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 15px;
            letter-spacing: 2px;
            position: relative;
            display: inline-block;
        }

        .cosmic-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 200px;
            height: 3px;
            background: linear-gradient(90deg, transparent, #673ab7, #00bcd4, #e91e63, transparent);
            border-radius: 2px;
        }

        .subtitle {
            font-size: 1.8rem;
            color: #a0a0ff;
            margin-bottom: 30px;
            font-weight: 300;
            letter-spacing: 3px;
        }

        /* Nebula Animation */
        .nebula-container {
            width: 100%;
            height: 300px;
            margin: 40px auto;
            position: relative;
            overflow: hidden;
            border-radius: 20px;
            background: rgba(16, 20, 31, 0.5);
            border: 1px solid rgba(103, 58, 183, 0.3);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
        }

        .nebula {
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 30% 50%, rgba(103, 58, 183, 0.4) 0%, transparent 50%),
                radial-gradient(circle at 70% 30%, rgba(0, 188, 212, 0.3) 0%, transparent 50%),
                radial-gradient(circle at 50% 70%, rgba(233, 30, 99, 0.3) 0%, transparent 50%);
            animation: nebulaFloat 15s infinite alternate ease-in-out;
        }

        @keyframes nebulaFloat {
            0% { transform: scale(1) rotate(0deg); }
            100% { transform: scale(1.1) rotate(1deg); }
        }

        /* Social Links */
        .cosmic-links {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin: 40px 0;
        }

        .cosmic-link {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: rgba(26, 26, 46, 0.8);
            border: 1px solid rgba(103, 58, 183, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #a0a0ff;
            font-size: 1.5rem;
            text-decoration: none;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .cosmic-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, rgba(103, 58, 183, 0.2), rgba(0, 188, 212, 0.2));
            opacity: 0;
            transition: opacity 0.3s;
        }

        .cosmic-link:hover {
            transform: translateY(-5px);
            border-color: #673ab7;
            box-shadow: 0 10px 30px rgba(103, 58, 183, 0.3);
            color: #fff;
        }

        .cosmic-link:hover::before {
            opacity: 1;
        }

        /* About Section */
        .about-container {
            background: rgba(26, 26, 46, 0.6);
            border-radius: 20px;
            padding: 40px;
            margin: 60px 0;
            border: 1px solid rgba(103, 58, 183, 0.3);
            position: relative;
            overflow: hidden;
        }

        .about-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(103, 58, 183, 0.05), transparent);
            z-index: -1;
        }

        .section-title {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.2rem;
            color: #00bcd4;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .section-title::before {
            content: '✦';
            color: #e91e63;
        }

        .about-text {
            font-size: 1.2rem;
            line-height: 1.8;
            color: #c0c0ff;
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        /* Tech Galaxy */
        .tech-galaxy {
            margin: 80px 0;
        }

        .galaxy-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .galaxy-sector {
            background: rgba(26, 26, 46, 0.7);
            border-radius: 15px;
            padding: 30px;
            border: 1px solid rgba(0, 188, 212, 0.3);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .galaxy-sector::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, #673ab7, #00bcd4);
        }

        .galaxy-sector:hover {
            transform: translateY(-10px);
            border-color: #673ab7;
            box-shadow: 0 15px 40px rgba(103, 58, 183, 0.2);
        }

        .sector-title {
            font-size: 1.5rem;
            color: #e91e63;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .sector-title i {
            color: #00bcd4;
        }

        .tech-planets {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        .tech-planet {
            background: rgba(103, 58, 183, 0.2);
            border: 1px solid rgba(103, 58, 183, 0.4);
            color: #a0a0ff;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            transition: all 0.3s;
        }

        .tech-planet:hover {
            background: rgba(103, 58, 183, 0.4);
            transform: scale(1.05);
            color: #fff;
        }

        /* Project Constellations */
        .project-constellations {
            margin: 80px 0;
        }

        .constellation-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .constellation {
            background: rgba(26, 26, 46, 0.7);
            border-radius: 15px;
            padding: 30px;
            border: 1px solid rgba(233, 30, 99, 0.3);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .constellation::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(233, 30, 99, 0.05), transparent);
            opacity: 0;
            transition: opacity 0.3s;
        }

        .constellation:hover {
            transform: translateY(-10px);
            border-color: #e91e63;
            box-shadow: 0 15px 40px rgba(233, 30, 99, 0.2);
        }

        .constellation:hover::before {
            opacity: 1;
        }

        .project-title {
            font-size: 1.5rem;
            color: #00bcd4;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .project-title i {
            color: #e91e63;
        }

        .project-role {
            color: #673ab7;
            font-weight: 600;
            margin-bottom: 15px;
            font-size: 1rem;
        }

        .project-desc {
            color: #c0c0ff;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .tech-star {
            background: rgba(0, 188, 212, 0.2);
            border: 1px solid rgba(0, 188, 212, 0.4);
            color: #a0a0ff;
            padding: 6px 12px;
            border-radius: 15px;
            font-size: 0.85rem;
        }

        /* GitHub Universe */
        .github-universe {
            margin: 80px 0;
        }

        .universe-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .stat-card {
            background: rgba(26, 26, 46, 0.7);
            border-radius: 15px;
            padding: 30px;
            border: 1px solid rgba(103, 58, 183, 0.3);
            text-align: center;
            transition: all 0.3s;
        }

        .stat-card:hover {
            border-color: #00bcd4;
            transform: translateY(-5px);
        }

        .stat-value {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.5rem;
            color: #e91e63;
            margin-bottom: 10px;
        }

        .stat-label {
            color: #a0a0ff;
            font-size: 1rem;
        }

        /* Exploration Nebula */
        .exploration-nebula {
            background: rgba(26, 26, 46, 0.7);
            border-radius: 20px;
            padding: 40px;
            margin: 80px 0;
            border: 1px solid rgba(0, 188, 212, 0.3);
            position: relative;
            overflow: hidden;
        }

        .exploration-nebula::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 30% 50%, rgba(0, 188, 212, 0.1) 0%, transparent 70%);
        }

        .exploration-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .exploration-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 15px;
            background: rgba(103, 58, 183, 0.1);
            border-radius: 10px;
            border: 1px solid rgba(103, 58, 183, 0.3);
            transition: all 0.3s;
        }

        .exploration-item:hover {
            background: rgba(103, 58, 183, 0.2);
            transform: translateX(10px);
            border-color: #673ab7;
        }

        .exploration-icon {
            width: 40px;
            height: 40px;
            background: rgba(0, 188, 212, 0.2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #00bcd4;
            font-size: 1.2rem;
        }

        /* Footer */
        .cosmic-footer {
            text-align: center;
            padding: 60px 0 40px;
            margin-top: 80px;
            border-top: 1px solid rgba(103, 58, 183, 0.3);
            position: relative;
        }

        .cosmic-footer::before {
            content: '';
            position: absolute;
            top: -1px;
            left: 50%;
            transform: translateX(-50%);
            width: 200px;
            height: 2px;
            background: linear-gradient(90deg, transparent, #673ab7, #00bcd4, #e91e63, transparent);
        }

        .footer-text {
            color: #a0a0ff;
            font-size: 1.1rem;
            margin: 20px 0;
            line-height: 1.6;
        }

        .view-counter {
            display: inline-block;
            background: rgba(233, 30, 99, 0.2);
            color: #e91e63;
            padding: 8px 20px;
            border-radius: 20px;
            font-family: 'Orbitron', sans-serif;
            font-size: 0.9rem;
            border: 1px solid rgba(233, 30, 99, 0.4);
        }

        /* Particle Animation */
        .particles {
            position: fixed;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .cosmic-title {
                font-size: 3rem;
            }
            
            .subtitle {
                font-size: 1.4rem;
            }
            
            .nebula-container {
                height: 200px;
            }
            
            .about-container,
            .exploration-nebula {
                padding: 30px 20px;
            }
            
            .galaxy-grid,
            .constellation-grid,
            .universe-stats {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            .cosmic-title {
                font-size: 2.5rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .cosmic-links {
                gap: 15px;
            }
            
            .cosmic-link {
                width: 50px;
                height: 50px;
                font-size: 1.2rem;
            }
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }

        ::-webkit-scrollbar-track {
            background: rgba(26, 26, 46, 0.5);
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(45deg, #673ab7, #00bcd4);
            border-radius: 5px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(45deg, #5e35b1, #00acc1);
        }
    </style>
</head>
<body>
    <!-- Cosmic Background -->
    <div class="cosmic-bg"></div>
    <div class="stars"></div>
    <div class="aurora"></div>
    
    <!-- Main Container -->
    <div class="container">
        <!-- Header -->
        <header class="header">
            <h1 class="cosmic-title">SHIVANI JADHAV</h1>
            <p class="subtitle">WEB DEVELOPER & DEVOPS ENGINEER</p>
            
            <!-- Nebula Animation -->
            <div class="nebula-container">
                <div class="nebula"></div>
            </div>
            
            <!-- Social Links -->
            <div class="cosmic-links">
                <a href="https://github.com/Shivpjadhav" class="cosmic-link">
                    <i class="fab fa-github"></i>
                </a>
                <a href="https://www.linkedin.com/in/shivani-jadhav-8b4b67251" class="cosmic-link">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="mailto:jadhavshivani332@gmail.com" class="cosmic-link">
                    <i class="fas fa-envelope"></i>
                </a>
                <a href="#" class="cosmic-link">
                    <i class="fas fa-globe"></i>
                </a>
            </div>
        </header>
        
        <!-- About Section -->
        <section class="about-container">
            <h2 class="section-title">CELESTIAL PROFILE</h2>
            <p class="about-text">
                A passionate developer focused on creating elegant backend solutions and efficient DevOps pipelines. 
                I enjoy building systems that are both beautiful in architecture and reliable in production. 
                Like a cosmic architect, I weave code into constellations of functionality across the digital universe.
            </p>
        </section>
        
        <!-- Tech Galaxy -->
        <section class="tech-galaxy">
            <h2 class="section-title">TECH GALAXY</h2>
            <div class="galaxy-grid">
                <!-- Frontend Sector -->
                <div class="galaxy-sector">
                    <h3 class="sector-title"><i class="fas fa-palette"></i> FRONTEND</h3>
                    <div class="tech-planets">
                        <span class="tech-planet">HTML</span>
                        <span class="tech-planet">CSS</span>
                        <span class="tech-planet">JavaScript</span>
                        <span class="tech-planet">React.js</span>
                        <span class="tech-planet">Bootstrap</span>
                        <span class="tech-planet">Tailwind CSS</span>
                    </div>
                </div>
                
                <!-- Backend Sector -->
                <div class="galaxy-sector">
                    <h3 class="sector-title"><i class="fas fa-server"></i> BACKEND</h3>
                    <div class="tech-planets">
                        <span class="tech-planet">PHP</span>
                        <span class="tech-planet">CodeIgniter 4</span>
                        <span class="tech-planet">Node.js</span>
                        <span class="tech-planet">MySQL</span>
                        <span class="tech-planet">MongoDB</span>
                        <span class="tech-planet">REST APIs</span>
                    </div>
                </div>
                
                <!-- DevOps Sector -->
                <div class="galaxy-sector">
                    <h3 class="sector-title"><i class="fas fa-cloud"></i> DEVOPS</h3>
                    <div class="tech-planets">
                        <span class="tech-planet">AWS</span>
                        <span class="tech-planet">Azure</span>
                        <span class="tech-planet">Terraform</span>
                        <span class="tech-planet">Linux</span>
                        <span class="tech-planet">Git</span>
                        <span class="tech-planet">Docker</span>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Project Constellations -->
        <section class="project-constellations">
            <h2 class="section-title">PROJECT CONSTELLATIONS</h2>
            <div class="constellation-grid">
                <!-- Project 1 -->
                <div class="constellation">
                    <h3 class="project-title"><i class="fas fa-briefcase"></i> Job Portal</h3>
                    <div class="project-role">Naukri-style platform</div>
                    <p class="project-desc">Engineered backend modules for candidate workflows, authentication, and job lifecycle management.</p>
                    <div class="project-tech">
                        <span class="tech-star">PHP</span>
                        <span class="tech-star">CodeIgniter 4</span>
                        <span class="tech-star">MySQL</span>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="constellation">
                    <h3 class="project-title"><i class="fas fa-hotel"></i> Hotel Management</h3>
                    <div class="project-role">Full-stack system</div>
                    <p class="project-desc">Delivered frontend UI, backend APIs, and complete admin dashboard ecosystem with real-time booking.</p>
                    <div class="project-tech">
                        <span class="tech-star">PHP</span>
                        <span class="tech-star">React.js</span>
                        <span class="tech-star">MySQL</span>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="constellation">
                    <h3 class="project-title"><i class="fas fa-building"></i> Office Management</h3>
                    <div class="project-role">Workplace coordination</div>
                    <p class="project-desc">Built role-based access modules and admin workflows for operational automation and team coordination.</p>
                    <div class="project-tech">
                        <span class="tech-star">PHP</span>
                        <span class="tech-star">CodeIgniter 4</span>
                        <span class="tech-star">MySQL</span>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- GitHub Universe -->
        <section class="github-universe">
            <h2 class="section-title">GITHUB UNIVERSE</h2>
            <div class="universe-stats">
                <div class="stat-card">
                    <div class="stat-value">15+</div>
                    <div class="stat-label">Projects</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">5k+</div>
                    <div class="stat-label">Code Commits</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">10+</div>
                    <div class="stat-label">Technologies</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">24/7</div>
                    <div class="stat-label">Learning Mode</div>
                </div>
            </div>
        </section>
        
        <!-- Exploration Nebula -->
        <section class="exploration-nebula">
            <h2 class="section-title">EXPLORATION NEBULA</h2>
            <div class="exploration-grid">
                <div class="exploration-item">
                    <div class="exploration-icon">
                        <i class="fas fa-infinity"></i>
                    </div>
                    <div>
                        <h4>Advanced DevOps</h4>
                        <p style="color: #a0a0ff; font-size: 0.9rem;">Workflows & Automation</p>
                    </div>
                </div>
                
                <div class="exploration-item">
                    <div class="exploration-icon">
                        <i class="fas fa-code-branch"></i>
                    </div>
                    <div>
                        <h4>Infrastructure as Code</h4>
                        <p style="color: #a0a0ff; font-size: 0.9rem;">Terraform Mastery</p>
                    </div>
                </div>
                
                <div class="exploration-item">
                    <div class="exploration-icon">
                        <i class="fas fa-cloud"></i>
                    </div>
                    <div>
                        <h4>Cloud Native</h4>
                        <p style="color: #a0a0ff; font-size: 0.9rem;">Scalable Architectures</p>
                    </div>
                </div>
                
                <div class="exploration-item">
                    <div class="exploration-icon">
                        <i class="fas fa-network-wired"></i>
                    </div>
                    <div>
                        <h4>Microservices</h4>
                        <p style="color: #a0a0ff; font-size: 0.9rem;">Design Patterns</p>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Footer -->
        <footer class="cosmic-footer">
            <div class="footer-text">
                Thank you for exploring my cosmic digital garden.<br>
                Let's create constellations of innovation together.
            </div>
            <div class="view-counter">
                <i class="fas fa-eye"></i> Cosmic Views: Loading...
            </div>
        </footer>
    </div>

    <!-- Particles Script -->
    <script>
        // Create floating particles
        function createParticles() {
            const container = document.createElement('div');
            container.className = 'particles';
            document.body.appendChild(container);
            
            const colors = ['#673ab7', '#00bcd4', '#e91e63', '#8bc34a'];
            
            for (let i = 0; i < 50; i++) {
                const particle = document.createElement('div');
                const size = Math.random() * 5 + 2;
                const color = colors[Math.floor(Math.random() * colors.length)];
                
                particle.style.cssText = `
                    position: absolute;
                    width: ${size}px;
                    height: ${size}px;
                    background: ${color};
                    border-radius: 50%;
                    top: ${Math.random() * 100}vh;
                    left: ${Math.random() * 100}vw;
                    opacity: ${Math.random() * 0.5 + 0.2};
                    box-shadow: 0 0 10px ${color};
                    pointer-events: none;
                `;
                
                container.appendChild(particle);
                
                // Animate particle
                animateParticle(particle);
            }
        }
        
        function animateParticle(particle) {
            let x = parseFloat(particle.style.left);
            let y = parseFloat(particle.style.top);
            let dx = (Math.random() - 0.5) * 0.5;
            let dy = (Math.random() - 0.5) * 0.5;
            
            function move() {
                x += dx;
                y += dy;
                
                // Bounce off edges
                if (x <= 0 || x >= 100) dx = -dx;
                if (y <= 0 || y >= 100) dy = -dy;
                
                particle.style.left = x + 'vw';
                particle.style.top = y + 'vh';
                
                requestAnimationFrame(move);
            }
            
            move();
        }
        
        // Initialize particles
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            
            // Animate elements on scroll
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, observerOptions);
            
            // Observe all sections
            document.querySelectorAll('.galaxy-sector, .constellation, .stat-card').forEach(el => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(20px)';
                el.style.transition = 'opacity 0.6s, transform 0.6s';
                observer.observe(el);
            });
            
            // Simulate view counter
            const viewCounter = document.querySelector('.view-counter');
            let views = 1274;
            setInterval(() => {
                views += Math.floor(Math.random() * 3);
                viewCounter.innerHTML = `<i class="fas fa-eye"></i> Cosmic Views: ${views}`;
            }, 3000);
        });
        
        // Add keyboard navigation effects
        document.addEventListener('keydown', (e) => {
            if (e.key === 'ArrowDown' || e.key === 'ArrowUp') {
                e.preventDefault();
                const sections = document.querySelectorAll('section');
                const currentScroll = window.scrollY;
                const windowHeight = window.innerHeight;
                
                let targetSection;
                if (e.key === 'ArrowDown') {
                    sections.forEach(section => {
                        if (section.offsetTop > currentScroll + 100) {
                            if (!targetSection || section.offsetTop < targetSection.offsetTop) {
                                targetSection = section;
                            }
                        }
                    });
                } else {
                    sections.forEach(section => {
                        if (section.offsetTop < currentScroll - 100) {
                            if (!targetSection || section.offsetTop > targetSection.offsetTop) {
                                targetSection = section;
                            }
                        }
                    });
                }
                
                if (targetSection) {
                    window.scrollTo({
                        top: targetSection.offsetTop - 100,
                        behavior: 'smooth'
                    });
                }
            }
        });
    </script>
</body>
</html>

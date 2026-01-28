<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Innocent Niyonzima - Full-Stack Developer</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #e4e4e7;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            margin: 0;
            padding: 0;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .hero {
            text-align: center;
            padding: 80px 20px;
            background: radial-gradient(circle at center, rgba(0, 114, 255, 0.1) 0%, transparent 70%);
            border-radius: 20px;
            margin-bottom: 50px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(0, 114, 255, 0.05), transparent);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            background: linear-gradient(135deg, #00d4ff, #0072ff, #6a85b6, #bac8e0);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
            animation: fadeInUp 1s ease-out;
            position: relative;
            z-index: 1;
        }

        .hero p {
            font-size: 1.3rem;
            color: #a1a1aa;
            max-width: 700px;
            margin: 0 auto 30px;
            animation: fadeInUp 1s ease-out 0.2s both;
            position: relative;
            z-index: 1;
        }

        .hero .subtitle {
            font-size: 1.1rem;
            color: #60a5fa;
            font-weight: 500;
            animation: fadeInUp 1s ease-out 0.4s both;
            position: relative;
            z-index: 1;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .section {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 16px;
            padding: 40px;
            margin-bottom: 30px;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 114, 255, 0.1);
        }

        .section h2 {
            color: #60a5fa;
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section h2::before {
            content: '';
            font-size: 1.5rem;
        }

        .tech-stack {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .tech-category {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .tech-category h3 {
            color: #fbbf24;
            font-size: 1.2rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .tech-category h3::before {
            content: '';
            font-size: 1rem;
        }

        .badge-container {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 114, 255, 0.2);
        }

        .project-card h3 {
            color: #34d399;
            margin-bottom: 10px;
        }

        .project-card p {
            color: #a1a1aa;
            font-size: 0.9rem;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .stats img {
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .contact-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(255, 255, 255, 0.05);
            color: #60a5fa;
            text-decoration: none;
            padding: 12px 20px;
            border-radius: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .contact-link:hover {
            background: rgba(96, 165, 250, 0.1);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(96, 165, 250, 0.3);
        }

        .footer {
            text-align: center;
            padding: 40px 0;
            color: #71717a;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            .hero p {
                font-size: 1.1rem;
            }
            .section {
                padding: 20px;
            }
            .tech-stack {
                grid-template-columns: 1fr;
            }
            .projects {
                grid-template-columns: 1fr;
            }
            .stats {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Hero Section -->
        <div class="hero">
            <h1>Hi, I'm Innocent Niyonzima</h1>
            <p>CS Graduate Student @ CUA • Full-Stack & Backend Developer</p>
            <p class="subtitle">Building scalable systems, APIs, and automation tools with a focus on secure, maintainable, and ethical engineering.</p>
        </div>

        <!-- About Section -->
        <div class="section">
            <h2>About Me</h2>
            <p>Passionate about creating innovative solutions that make a difference. I specialize in full-stack development with expertise in modern web technologies, cloud architecture, and DevOps practices. Always learning, always building!</p>
        </div>

        <!-- Tech Stack Section -->
        <div class="section">
            <h2>Tech Stack</h2>
            <div class="tech-stack">
                <div class="tech-category">
                    <h3>Languages</h3>
                    <div class="badge-container">
                        <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/>
                        <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white"/>
                        <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
                        <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white"/>
                        <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black"/>
                        <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white"/>
                    </div>
                </div>
                <div class="tech-category">
                    <h3>Frontend</h3>
                    <div class="badge-container">
                        <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black"/>
                        <img src="https://img.shields.io/badge/TailwindCSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white"/>
                    </div>
                </div>
                <div class="tech-category">
                    <h3>Backend & Frameworks</h3>
                    <div class="badge-container">
                        <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white"/>
                        <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white"/>
                        <img src="https://img.shields.io/badge/ASP.NET-512BD4?style=for-the-badge&logo=.net&logoColor=white"/>
                        <img src="https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white"/>
                    </div>
                </div>
                <div class="tech-category">
                    <h3>Databases</h3>
                    <div class="badge-container">
                        <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white"/>
                        <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"/>
                        <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
                        <img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white"/>
                    </div>
                </div>
                <div class="tech-category">
                    <h3>DevOps & Tools</h3>
                    <div class="badge-container">
                        <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
                        <img src="https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=nginx&logoColor=white"/>
                        <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white"/>
                        <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white"/>
                    </div>
                </div>
            </div>
        </div>

        <!-- Projects Section -->
        <div class="section">
            <h2>Featured Projects</h2>
            <div class="projects">
                <div class="project-card">
                    <h3>Ibyapa.com</h3>
                    <p>MERN platform for driving exam preparation with interactive quizzes and progress tracking.</p>
                    <a href="https://ibyapa.com" class="contact-link">View Project →</a>
                </div>
                <div class="project-card">
                    <h3>Budget Planner (.NET)</h3>
                    <p>Personal finance management app built with ASP.NET Core for expense tracking and budgeting.</p>
                </div>
                <div class="project-card">
                    <h3>PublishEveryDay API</h3>
                    <p>Robust blogging backend with REST APIs, authentication, and content management.</p>
                    <a href="https://pedbackend.onrender.com/api-docs/" class="contact-link">API Docs →</a>
                </div>
                <div class="project-card">
                    <h3>COVID-19 Explorer</h3>
                    <p>Real-time dashboard for COVID-19 data visualization using Node.js and external APIs.</p>
                    <a href="https://github.com/Rwandantechy/covid-19-updates-explorer-using-nodejs" class="contact-link">View on GitHub →</a>
                </div>
            </div>
        </div>

        <!-- Certifications & Languages -->
        <div class="section">
            <h2>Certifications & Languages</h2>
            <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px;">
                <div>
                    <h3 style="color: #fbbf24;">Certifications</h3>
                    <ul style="color: #a1a1aa; padding-left: 20px;">
                        <li>ALX Back-End Pro</li>
                        <li>Aspire Leaders (2024)</li>
                        <li>Andela TLP (2023)</li>
                        <li>Oracle SQL (2022)</li>
                    </ul>
                </div>
                <div>
                    <h3 style="color: #fbbf24;">Languages</h3>
                    <p style="color: #a1a1aa;">English • Kinyarwanda • French</p>
                </div>
            </div>
        </div>

        <!-- Contact Links -->
        <div class="section">
            <h2>Let's Connect</h2>
            <div class="contact-links">
                <a href="https://innocent-niyonzima.vercel.app" class="contact-link">
                    Portfolio
                </a>
                <a href="https://www.linkedin.com/in/innocent-niyonziima" class="contact-link">
                    LinkedIn
                </a>
                <a href="https://x.com/Innocentus8" class="contact-link">
                    Twitter
                </a>
                <a href="mailto:your.email@example.com" class="contact-link">
                    Email
                </a>
            </div>
        </div>

        <!-- GitHub Stats -->
        <div class="section">
            <h2>GitHub Stats</h2>
            <div class="stats">
                <img src="https://github-readme-stats.vercel.app/api?username=Rwandantechy&show_icons=true&theme=dark&bg_color=0f0f23&border_color=1a1a2e&title_color=60a5fa&icon_color=34d399&text_color=e4e4e7" alt="GitHub Stats"/>
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=Rwandantechy&theme=dark&background=0f0f23&border=1a1a2e&stroke=60a5fa&ring=34d399&fire=34d399&currStreakLabel=60a5fa&sideLabels=60a5fa&dates=60a5fa&currStreakNum=e4e4e7&sideNums=e4e4e7" alt="GitHub Streak"/>
            </div>
            <div style="text-align: center; margin-top: 20px;">
                <img src="https://github-profile-trophy.vercel.app/?username=Rwandantechy&theme=dark&no-frame=true&no-bg=true&margin-w=10&row=1&column=6" alt="GitHub Trophies"/>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p>Thanks for visiting! Feel free to explore my repositories and reach out for collaborations.</p>
        </div>
    </div>
</body>
</html>

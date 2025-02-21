<!DOCTYPE html>
<html>
<head>
  <style>
    :root {
      --primary: #2193b0;
      --gradient: linear-gradient(135deg, #2193b0 0%, #6dd5ed 100%);
      --dark: #1a1a1a;
      --light: #ffffff;
      --card-bg: rgba(255, 255, 255, 0.05);
    }

    body {
      background: var(--dark);
      color: var(--light);
      font-family: 'Inter', sans-serif;
      margin: 0;
      padding: 40px;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
    }

    .hero {
      display: flex;
      align-items: center;
      gap: 40px;
      padding: 60px 0;
      border-radius: 20px;
      background: var(--gradient);
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      width: 100%;
      height: 100%;
      background: url('/api/placeholder/1200/400') center/cover;
      opacity: 0.1;
      animation: pulse 4s infinite;
    }

    @keyframes pulse {
      0% { opacity: 0.1; }
      50% { opacity: 0.2; }
      100% { opacity: 0.1; }
    }

    .profile-img {
      width: 200px;
      height: 200px;
      border-radius: 20px;
      border: 4px solid var(--light);
      box-shadow: 0 10px 30px rgba(0,0,0,0.3);
      margin-left: 40px;
      position: relative;
      z-index: 1;
    }

    .hero-content {
      position: relative;
      z-index: 1;
    }

    .hero-title {
      font-size: 3em;
      margin: 0;
      font-weight: 800;
      background: var(--light);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .hero-subtitle {
      font-size: 1.5em;
      margin: 10px 0;
      opacity: 0.9;
    }

    .social-links {
      display: flex;
      gap: 20px;
      margin-top: 20px;
    }

    .social-btn {
      padding: 10px 25px;
      border: 2px solid var(--light);
      border-radius: 10px;
      color: var(--light);
      text-decoration: none;
      font-weight: 600;
      transition: all 0.3s ease;
    }

    .social-btn:hover {
      background: var(--light);
      color: var(--primary);
      transform: translateY(-2px);
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
      margin: 60px 0;
    }

    .skill-card {
      background: var(--card-bg);
      border-radius: 15px;
      padding: 30px;
      border: 1px solid rgba(255,255,255,0.1);
      transition: transform 0.3s ease;
    }

    .skill-card:hover {
      transform: translateY(-5px);
    }

    .skill-title {
      color: var(--primary);
      font-size: 1.2em;
      margin: 0 0 15px 0;
    }

    .skill-list {
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .skill-list li {
      margin: 10px 0;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .skill-list li::before {
      content: '▹';
      color: var(--primary);
    }

    .projects-section {
      margin: 60px 0;
    }

    .section-title {
      font-size: 2em;
      margin-bottom: 30px;
      color: var(--primary);
    }

    .project-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
    }

    .project-card {
      background: var(--card-bg);
      border-radius: 15px;
      padding: 30px;
      border: 1px solid rgba(255,255,255,0.1);
      transition: all 0.3s ease;
    }

    .project-card:hover {
      transform: translateY(-5px);
      border-color: var(--primary);
    }

    .project-title {
      color: var(--light);
      margin: 0 0 15px 0;
      font-size: 1.4em;
    }

    .project-desc {
      color: rgba(255,255,255,0.7);
      margin: 0 0 20px 0;
      line-height: 1.6;
    }

    .tech-stack {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .tech-tag {
      padding: 5px 15px;
      background: rgba(33, 147, 176, 0.1);
      border-radius: 20px;
      font-size: 0.9em;
      color: var(--primary);
    }

    .stats-section {
      margin: 60px 0;
      text-align: center;
    }

    .stats-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 30px;
      margin-top: 30px;
    }

    .stat-card {
      background: var(--card-bg);
      border-radius: 15px;
      padding: 30px;
      border: 1px solid rgba(255,255,255,0.1);
    }

    .stat-number {
      font-size: 2.5em;
      color: var(--primary);
      font-weight: 700;
    }

    .stat-label {
      margin-top: 10px;
      color: rgba(255,255,255,0.7);
    }

    footer {
      text-align: center;
      margin-top: 60px;
      padding: 20px;
      color: rgba(255,255,255,0.5);
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="hero">
      <img src="/api/placeholder/200/200" alt="Profile" class="profile-img">
      <div class="hero-content">
        <h1 class="hero-title">Akshay Kumar</h1>
        <p class="hero-subtitle">Full-Stack Developer • Ex-IISc Research Intern</p>
        <div class="social-links">
          <a href="https://ak517ay.vercel.app/" class="social-btn">Portfolio</a>
          <a href="https://www.linkedin.com/in/akshay-kumar-7a8857255/" class="social-btn">LinkedIn</a>
          <a href="https://github.com/ak517ayakshay" class="social-btn">GitHub</a>
        </div>
      </div>
    </div>

    <div class="skills-grid">
      <div class="skill-card">
        <h3 class="skill-title">Languages</h3>
        <ul class="skill-list">
          <li>Python</li>
          <li>C++</li>
          <li>C</li>
        </ul>
      </div>
      <div class="skill-card">
        <h3 class="skill-title">Frontend</h3>
        <ul class="skill-list">
          <li>HTML5</li>
          <li>CSS3</li>
          <li>Bootstrap</li>
          <li>Tailwind</li>
        </ul>
      </div>
      <div class="skill-card">
        <h3 class="skill-title">Backend</h3>
        <ul class="skill-list">
          <li>Django</li>
          <li>MySQL</li>
          <li>REST APIs</li>
        </ul>
      </div>
    </div>

    <div class="projects-section">
      <h2 class="section-title">Featured Projects</h2>
      <div class="project-grid">
        <div class="project-card">
          <h3 class="project-title">C.L.A.S.S</h3>
          <p class="project-desc">Advanced learning management system with analytics and personalized learning paths.</p>
          <div class="tech-stack">
            <span class="tech-tag">Django</span>
            <span class="tech-tag">MySQL</span>
            <span class="tech-tag">Analytics</span>
          </div>
        </div>
        <div class="project-card">
          <h3 class="project-title">PRECISION-VISION</h3>
          <p class="project-desc">Computer vision system for real-time object detection and analysis.</p>
          <div class="tech-stack">
            <span class="tech-tag">Python</span>
            <span class="tech-tag">OpenCV</span>
            <span class="tech-tag">Deep Learning</span>
          </div>
        </div>
        <div class="project-card">
          <h3 class="project-title">SCHOLATA</h3>
          <p class="project-desc">Educational platform with integrated assessment tools.</p>
          <div class="tech-stack">
            <span class="tech-tag">Django</span>
            <span class="tech-tag">MySQL</span>
            <span class="tech-tag">Bootstrap</span>
          </div>
        </div>
      </div>
    </div>

    <div class="stats-section">
      <h2 class="section-title">Achievement Highlights</h2>
      <div class="stats-grid">
        <div class="stat-card">
          <div class="stat-number">10+</div>
          <div class="stat-label">Projects Completed</div>
        </div>
        <div class="stat-card">
          <div class="stat-number">1000+</div>
          <div class="stat-label">Contributions</div>
        </div>
        <div class="stat-card">
          <div class="stat-number">5+</div>
          <div class="stat-label">Technologies Mastered</div>
        </div>
      </div>
    </div>

    <footer>
      <p>© 2024 Akshay Kumar. All rights reserved.</p>
    </footer>
  </div>
</body>
</html>

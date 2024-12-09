<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Onest:wght@100..900&display=swap" rel="stylesheet">
  <title>Fredrick Otieno</title>
  <style>
    :root {
      --bg-dark: #1a1a1a;
      --text-dark: #ffffff;
      --bg-light: #f5f5f5;
      --text-light: #1a1a1a;
      --accent: #50c878;
    }

    body {
      font-family: Onest, sans-serif;
      margin: 0;
      padding: 0;
      background-color: var(--bg-dark);
      color: var(--text-dark);
      transition: background-color 0.3s ease, color 0.3s ease;
    }

    .container {
      max-width: 800px;
      margin: 2rem auto;
      padding: 1rem;
    }

    h1 {
      font-size: 2rem;
      color: var(--accent);
      text-align: center;
      margin-bottom: 50px;
      margin-top: 200px;
    }

    .section {
      margin: 1.5rem 0;
     
    }

    .section h2 {
      border-bottom: 2px solid var(--accent);
      padding-bottom: 0.5rem;
      
    }

    .section p {
      margin: 0.5rem 0;
      line-height: 1.6;
       
    }

    .theme-toggle {
      display: flex;
      justify-content: center;
      margin-top: 1rem;
    }

    .theme-toggle button {
      background-color: var(--accent);
      border: none;
      color: var(--text-dark);
      padding: 0.5rem 1rem;
      font-size: 1rem;
      cursor: pointer;
      border-radius: 5px;
      transition: background-color 0.3s ease;
    }

    .theme-toggle button:hover {
      background-color: #3ca65e;
    }
    .intro{
      color: #50c878;
      margin-bottom: 250px;
    }
    span{
      color: #50c878;
    }
    .counter {
      text-align: center;
      font-size: 1rem;
      color: var(--accent);
      margin-top: 0.5rem;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Hi, I'm Fred</h1>
    <div class="counter" id="viewCounter">Viewed 0 times</div>
    <p>The Cloud is my office.</p>
    <p class="intro">AWS Cloud Engineer | Specializing in Cloud Architecture & Automation Certified AWS Cloud Engineer | Building Scalable Cloud Solutions</p>
    <div class="section">
      <h2>About Me</h2>
      <p>Hello, I’m Fredrick Otieno, an enthusiastic AWS Cloud Engineer with a passion for leveraging cloud technology to drive innovation and efficiency. With a solid foundation in infrastructure management and a knack for problem-solving, I thrive in dynamic environments where I can contribute to impactful projects.

         Over the course of my career, I have developed a deep expertise in a wide range of AWS services, enabling me to <span>design</span>, <span>deloy</span>deploy, and <span>manage robust cloud solutions</span>. My hands-on experience includes:
         
         Amazon EC2: Proficient in provisioning and configuring virtual servers to deliver scalable compute capacity tailored to application needs.
         AWS S3: Skilled in using Amazon S3 for secure and durable data storage, implementing policies for data lifecycle management and cost optimization.
         AWS Lambda: Experienced in serverless architecture, designing event-driven applications that reduce operational overhead while enhancing scalability.
         Amazon RDS: Well-versed in deploying and managing relational databases, ensuring high availability and performance through automated backups and scaling.
         CloudWatch & CloudTrail: Adept at monitoring applications and resources to ensure performance and security compliance, utilizing insights for proactive maintenance.
         I enjoy collaborating with cross-functional teams to define cloud strategies that align with business goals. My approach combines technical expertise with strong communication skills, allowing me to convey complex concepts in an understandable manner. I am driven by a desire to continuously learn and stay updated with the latest industry trends and AWS offerings.
         
         Whether optimizing cloud infrastructure or implementing best practices for security and compliance, I am committed to delivering high-quality solutions that empower organizations to realize the full potential of cloud technology.</p>
    </div>
    <div class="section">
      <h2>Experience</h2>
      <h2>Junior Cloud Engineer - Intern</h2>
      <h3>Airtel Kenya</h3>
      <h3>Oct 2024 - Present · 3 mos</h3>
      <h3>Nairobi County, Kenya · Hybrid</h3>
      <p><strong>Software Engineer</strong> - Tech Corp (2022 - Present)</p>
      <p>Developed and deployed cloud-based applications, improving system performance by 30%.</p>
    </div>
    <div class="section">
      <h2>Skills</h2>
      <p>Python, JavaScript, AWS, React, Node.js</p>
    </div>
    <div class="theme-toggle">
      <button onclick="toggleTheme()">Toggle Theme</button>
    </div>
  </div>

  <script>
    const root = document.documentElement;

    function toggleTheme() {
      if (root.style.getPropertyValue('--bg-dark') === '#1a1a1a') {
        root.style.setProperty('--bg-dark', '#f5f5f5');
        root.style.setProperty('--text-dark', '#1a1a1a');
        root.style.setProperty('--bg-light', '#1a1a1a');
        root.style.setProperty('--text-light', '#ffffff');
      } else {
        root.style.setProperty('--bg-dark', '#1a1a1a');
        root.style.setProperty('--text-dark', '#ffffff');
        root.style.setProperty('--bg-light', '#f5f5f5');
        root.style.setProperty('--text-light', '#1a1a1a');
      }
    }

     // Counter logic
     function updateViewCounter() {
      let views = localStorage.getItem('resumeViews') || 0;
      views = parseInt(views) + 1;
      localStorage.setItem('resumeViews', views);
      document.getElementById('viewCounter').textContent = `Viewed ${views} times`;
    }

    // Initialize counter on page load
    updateViewCounter();
  </script>
</body>
</html>

# Ex01 Portfolio
## Date:

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Haripriya | Portfolio</title>
  <meta name="description" content="Portfolio of Haripriya - IT Student, AI & ML Enthusiast" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #ffe6f0;
      --muted: #333333;
      --text: #000000;
      --brand: #cc3366;
      --brand-2: #ff6699;
      --ring: rgba(204,51,102,.3);
      --maxw: 900px;
    }

    * { box-sizing: border-box; }
    html, body { height: 100%; margin: 0; padding: 0; }
    body{
      font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial;
      color: var(--text);
      background: var(--bg);
      line-height: 1.7;
      font-size: 16px;
      scroll-behavior: smooth;
      text-align: center;
    }

    header{
      position: sticky; top:0; z-index: 20;
      backdrop-filter: blur(10px);
      background: #ffd6e8;
      border-bottom: 1px solid #f5b6c9;
    }
    .nav{
      max-width: var(--maxw);
      margin: 0 auto;
      display:flex; align-items:center; justify-content:space-between;
      padding: 14px 20px;
    }
    .logo{ display:flex; align-items:center; gap:10px; font-weight:700; }
    .logo-mark{ width:28px; height:28px; border-radius:8px; background: linear-gradient(135deg, var(--brand), var(--brand-2)); }
    nav a{
      color: var(--muted); text-decoration:none; font-weight:500; font-size: 15px;
      padding: 8px 12px; border-radius: 8px; transition: .2s ease;
    }
    nav a:hover, nav a.active{ color: var(--brand); background: rgba(204,51,102,.1); }

    .container{ max-width: var(--maxw); margin: 0 auto; padding: 40px 20px; }
    .section{ padding: 40px 0; }
    h1,h2,h3{ line-height:1.3; margin:0 0 16px; }
    h1{ font-size: clamp(32px, 4vw, 46px); font-weight: 700; }
    h2{ font-size: clamp(24px, 3vw, 34px); color: var(--brand); font-weight: 600; }
    h3{ font-size: 20px; font-weight: 600; }
    p.lead{ color: var(--text); font-size: 17px; max-width: 70ch; margin: 0 auto; }

    .hero{ padding: 40px 20px; }
    .pill{ display:inline-block; background: rgba(204,51,102,.1); border:1px solid rgba(204,51,102,.25); color: var(--brand); padding: 6px 12px; border-radius: 999px; font-size: 12px; font-weight: 600; text-transform: uppercase; margin-bottom: 12px; }
    .cta{ display:flex; gap:12px; justify-content:center; margin-top: 20px; }
    .btn{ border-radius: 8px; border:1px solid rgba(204,51,102,.3); background: var(--brand); color: #fff; text-decoration:none; padding: 12px 18px; font-weight: 600; font-size: 15px; transition:.2s; }
    .btn:hover{ transform: translateY(-2px); box-shadow: 0 6px 16px rgba(204,51,102,.25); }
    .btn.alt{ background: transparent; color: var(--brand); }

    .skills-row { display: flex; justify-content: center; gap: 30px; margin: 20px 0; flex-wrap: wrap; }
    .skill { width: 250px; }
    .bar{ height: 8px; background: #fcd6e5; border-radius: 999px; overflow: hidden; width: 100%; margin: 6px auto; }
    .bar > span{ display:block; height:100%; background: linear-gradient(90deg, var(--brand), var(--brand-2)); width: var(--value, 50%); }

    ul.projects-list { list-style: none; padding: 0; margin: 20px auto; display:inline-block; text-align: left; }
    ul.projects-list li { margin-bottom: 14px; font-size: 17px; }
    ul.projects-list li::before { content: "• "; color: var(--brand); font-size: 20px; }

    form{ display:grid; gap:12px; max-width: 500px; margin: 0 auto; }
    label{ font-size: 14px; color: var(--text); }
    input, textarea{
      width: 100%; padding: 12px 14px; border-radius: 8px; color: var(--text);
      background: #fff; border:1px solid #f5b6c9;
      outline: none; transition: .2s ease; font: inherit;
    }
    input:focus, textarea:focus{ border-color: var(--ring); box-shadow: 0 0 0 4px rgba(204,51,102,.08); }
    textarea{ min-height: 140px; resize: vertical; }

    footer{ border-top: 1px solid #f5b6c9; color: var(--text); background: #ffd6e8; }
    .foot{ max-width: var(--maxw); margin: 0 auto; padding: 24px 20px; display:flex; justify-content:space-between; gap: 12px; flex-wrap: wrap; font-size: 14px; }
  </style>
</head>
<body>
  <header>
    <div class="nav">
      <div class="logo"><span class="logo-mark"></span> <span>Haripriya</span></div>
      <nav>
        <a href="#about" class="active">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero" id="home">
      <span class="pill">IT Student | AI & ML Enthusiast</span>
      <h1>Hi, I’m <span style="color:var(--brand)">Haripriya</span></h1>
      <p class="lead">I am a passionate third-year Information Technology student at Saveetha Engineering College. I enjoy exploring emerging technologies and working on ideas that bring innovation and impact. Currently, I’m learning Artificial Intelligence and Machine Learning step by step, aiming to build intelligent solutions that are efficient, practical, and beneficial for real-world applications.</p>
      <div class="cta">
        <a class="btn" href="#projects">View Projects</a>
        <a class="btn alt" href="#contact">Contact Me</a>
      </div>
    </section>

    <section class="container section" id="about">
      <h2>About</h2>
      <p class="lead">I am Haripriya, a third-year IT student passionate about AI and ML. I focus on strengthening my coding and analytical skills to apply these concepts effectively, while aiming to create solutions that can positively impact the world.</p>
    </section>

    <section class="container section" id="skills">
      <h2>Skills</h2>
      <p class="lead">I have been building a strong foundation in programming with Python, C, and Java. Along with this, I am developing knowledge in Artificial Intelligence and Machine Learning. I also enjoy problem-solving, logical thinking, and improving coding efficiency. In addition to technical skills, I value teamwork, communication, and adaptability.</p>
      
      <div class="skills-row">
        <div class="skill"><strong>Python</strong><div class="bar" style="--value: 85%"><span></span></div></div>
        <div class="skill"><strong>Java</strong><div class="bar" style="--value: 75%"><span></span></div></div>
      </div>
      <div class="skills-row">
        <div class="skill"><strong>C</strong><div class="bar" style="--value: 80%"><span></span></div></div>
        <div class="skill"><strong>AI & ML Basics</strong><div class="bar" style="--value: 70%"><span></span></div></div>
      </div>
    </section>

    <section class="container section" id="projects">
      <h2>Projects</h2>
      <p class="lead">As part of my learning journey, I have explored projects that apply my technical skills in practical scenarios. These projects help me understand algorithms better and connect theory with real-world needs.</p>
      <ul class="projects-list">
        <li>Predictive Model for Basic Data Analysis</li>
        <li>Simple Machine Learning Application</li>
        <li>Exploring AI-based Solutions for Real-world Problems</li>
      </ul>
    </section>

    <section class="container section" id="contact">
      <h2>Contact</h2>
      <p class="lead">Want to collaborate or connect with me? Feel free to reach out using the form below.</p>
      <form onsubmit="event.preventDefault(); alert('Thank you! Your message has been sent. (Demo)')">
        <div>
          <label for="name">Name</label>
          <input id="name" name="name" placeholder="Your full name" required />
        </div>
        <div>
          <label for="email">Email</label>
          <input id="email" name="email" type="email" placeholder="you@example.com" required />
        </div>
        <div>
          <label for="message">Message</label>
          <textarea id="message" name="message" placeholder="Write your message here..." required></textarea>
        </div>
        <div class="cta">
          <button class="btn" type="submit">Send Message</button>
          <a class="btn alt" href="mailto:haripriya@example.com">Email Directly</a>
        </div>
      </form>
    </section>
  </main>

  <footer>
    <div class="foot">
      <span>© <span id="year"></span> Haripriya</span>
      <div>
        <a href="#about">About</a> | <a href="#skills">Skills</a> | <a href="#projects">Projects</a> | <a href="#contact">Contact</a>
      </div>
    </div>
  </footer>

  <script>
    const links = Array.from(document.querySelectorAll('nav a'));
    const ids = links.map(a => a.getAttribute('href'));
    const sections = ids.map(id => document.querySelector(id));
    const setActive = () => {
      let idx = 0, fromTop = scrollY + 120;
      for (let i=0; i<sections.length; i++) {
        const s = sections[i]; if (!s) continue;
        const top = s.offsetTop, bottom = top + s.offsetHeight;
        if (fromTop >= top && fromTop < bottom) { idx = i; break; }
      }
      links.forEach((a,i)=>a.classList.toggle('active', i===idx));
    }
    addEventListener('scroll', setActive, { passive: true });
    setActive();
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
```

## OUTPUT
<img width="1884" height="911" alt="image" src="https://github.com/user-attachments/assets/d194c06f-cadf-4535-be18-51108e9910a4" />
<img width="1873" height="906" alt="image" src="https://github.com/user-attachments/assets/605f690d-694d-4324-8218-7dfae97c95e6" />
<img width="1881" height="911" alt="image" src="https://github.com/user-attachments/assets/31250055-bebe-42f0-a221-6bf0bac41978" />



## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.

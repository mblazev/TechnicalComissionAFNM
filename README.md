<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Mario Blazevski's Personal Website">
  <title>Mario Blazevski | Portfolio</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <div class="container">
      <h1>Mario Blazevski</h1>
      <p>Aerospace Engineer | STEM Advocate | Motorsport Visionary</p>
    </div>
  </header>

  <nav>
    <ul>
      <li><a href="#about">About Me</a></li>
      <li><a href="#professional_experience">Professional Experience</a></li>
      <li><a href="#portfolio">Portfolio</a></li>
      <li><a href="#blog">Blog</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <main>
    <section id="about">
      <h2>About Me</h2>
      <img src="mario.jpg" alt="Photo of Mario Blazevski" style="width:200px; height:auto; border-radius:50%;">
      
      
      <p>Hello! Welcome to my portfolio! I'm Mario Blazevski, 
      a dedicated innovator and team leader from North Macedonia. With a profound interest in STEM, engineering, and motorsport, I have committed my career to merging these fields to create impactful projects and inspire future generations. 
      I am the President and Founder of Aerth Racing, an organization aimed at promoting STEM education through motorsport. As a leader, I have successfully managed teams that participated in prestigious global competitions, including F1 in Schools and Formula Student.
      My work emphasizes innovation, environmental sustainability, and hands-on learning experiences.</p>
    </section>

    <section id="professional_experience">
      <h2>Professional Experience</h2>

      <h3>President and Founder</h3>
      <h4>Aerth Racing (2022–Present)</h4>
      <p>Established and led Aerth Racing, North Macedonia's first team to compete in the F1 in Schools World Finals.
Focused on promoting STEM education and sustainability through innovative racing projects.
Secured sponsorships, cultivated partnerships, and advanced the team's capabilities in engineering and project management.</p>

      <h3>President, Technical Commission</h3>
      <h4>Automobile Federation of North Macedonia (2023–Present)</h4>
      <p>Led technical policy development in line with international FIA standards.
Championed environmental campaigns and road safety initiatives.</p>

      <h3>Chief Mechanical Scrutineer</h3>
      <h4>Formula Student Alpe Adria, Czech Republic, and Portugal (2023–Present)</h4>
      <p>Ensured compliance with technical and safety standards in international student motorsport competitions.</p>
    </section>

    <section id="portfolio">
  <h2>Portfolio</h2>
  <div class="project-container">
    <div class="project-card">
      <h3>Formula Student Macedonia</h3>
      <p>Founded the first Formula Student team in North Macedonia, focusing on building competitive race cars while promoting engineering excellence.</p>
      <div class="project-card-footer">2022 - Present</div>
    </div>
    <div class="project-card">
      <h3>Aerth Racing</h3>
      <p>Led multiple innovative campaigns and designs that showcased the potential of youth talent in STEM and engineering.</p>
      <div class="project-card-footer">2021 - Present</div>
    </div>
    <div class="project-card">
      <h3>H2O Colligo</h3>
      <p>Designed a water collection and electricity production system, recognized by the Fund for Innovations and Technology.</p>
      <div class="project-card-footer">2020</div>
    </div>
  </div>
</section>


    <section id="blog">
      <h2>Blog</h2>
      <article>
        <h3>[Blog Post Title]</h3>
        <p>[Brief introduction to the blog post content, sharing insights or experiences relevant to your field.]</p>
      </article>
    </section>

    <section id="contact">
      <h2>Contact</h2>
      <p>Email: <a href="mailto:blazevskimario1@gmail.com">blazevskimario1@gmail.com</a></p>

      <button class="redirect-button" onclick="window.location.href='https://www.linkedin.com/in/mario-blazevski-774a31196/';">
        LinkedIn Mario Blazevski
      </button>

      <form>
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>

        <label for="message">Message:</label>
        <textarea id="message" name="message" required></textarea>

        <button type="submit">Send</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Mario Blazevski. All Rights Reserved.</p>
  </footer>
</body>
</html>

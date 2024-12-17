<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Mario Blazevski's Personal Website">
  <title>Mario Blazevski | Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
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
      <li><a href="#about" class="active">About Me</a></li>
      <li><a href="#professional_experience">Experience</a></li>
      <li><a href="#portfolio">Portfolio</a></li>
      <li><a href="#rocket_trajectory">C Program</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <main>
    <section id="about">
      <h2>About Me</h2>
      <img src="mario.jpg" alt="Photo of Mario Blazevski">
      <p>I'm Mario Blazevski, a dedicated innovator and team leader from North Macedonia. With a profound interest in STEM, engineering, and motorsport, I have successfully led projects, promoted STEM education, and inspired future generations through Aerth Racing and other initiatives.</p>
    </section>

    <section id="portfolio">
      <h2>Portfolio</h2>
      <div class="project-container">
        <div class="project-card">
          <h3>Formula Student Macedonia</h3>
          <p>Founded the first student team in North Macedonia to build competitive race cars.</p>
        </div>
        <div class="project-card">
          <h3>Aerth Racing</h3>
          <p>Led innovative campaigns to showcase youth talent in STEM and engineering.</p>
        </div>
        <div class="project-card">
          <h3>H2O Colligo</h3>
          <p>Designed a water collection and electricity production system recognized for innovation.</p>
        </div>
      </div>
    </section>

    <section id="rocket_trajectory">
      <h2>Rocket Trajectory Simulation (C Program)</h2>
      <p>This is a simple C program that calculates the trajectory of a rocket using basic physics equations.</p>
      <pre class="code-block">
<pre class="code-block">
<code>
#include &lt;stdio.h&gt;
#include &lt;math.h&gt;

#define GRAVITY 9.81

int main() {
    double velocity, angle, time, x, y;
    printf("Enter launch velocity (m/s): ");
    scanf("%lf", &velocity);
    printf("Enter launch angle (degrees): ");
    scanf("%lf", &angle);

    angle = angle * M_PI / 180.0; // Convert angle to radians
    time = 0.0;

    printf("\nTrajectory Points:\n");
    printf("Time (s)\tX (m)\t\tY (m)\n");

    while (1) {
        x = velocity * cos(angle) * time;
        y = velocity * sin(angle) * time - 0.5 * GRAVITY * time * time;

        if (y &lt; 0) break; // Rocket has hit the ground

        printf("%.2f\t\t%.2f\t\t%.2f\n", time, x, y);
        time += 0.1;
    }

    printf("Rocket trajectory simulation complete.\n");
    return 0;
}
</code>
</pre>
    

    <section id="contact">
      <h2>Contact</h2>
      <p>Email: <a href="mailto:blazevskimario1@gmail.com">blazevskimario1@gmail.com</a></p>
      <form>
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
        <label for="message">Message:</label>
        <textarea id="message" name="message" rows="5" required></textarea>
        <button type="submit">Send</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Mario Blazevski. All Rights Reserved.</p>
  </footer>
</body>
</html>

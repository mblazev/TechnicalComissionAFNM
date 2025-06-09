<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Serres 2025 - Official Notice Board</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      margin: 0;
      padding: 0;
    }
    header {
      background: #222;
      color: white;
      padding: 20px;
      text-align: center;
    }
    header img {
      width: 120px;
      display: block;
      margin: 0 auto 10px;
    }
    nav {
      background: #333;
      padding: 10px;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    nav a {
      color: white;
      text-decoration: none;
      margin: 0 15px;
      font-weight: bold;
    }
    main {
      max-width: 900px;
      margin: auto;
      background: white;
      padding: 20px;
    }
    .notice {
      background: #eef;
      border-left: 4px solid #0055aa;
      margin-bottom: 20px;
      padding: 10px 20px;
    }
    footer {
      text-align: center;
      padding: 15px;
      background: #222;
      color: white;
    }
    .download-link {
      display: inline-block;
      margin-top: 10px;
      padding: 10px 15px;
      background-color: #0055aa;
      color: white;
      text-decoration: none;
      border-radius: 5px;
    }
    .download-link:hover {
      background-color: #003e80;
    }
  </style>
</head>
<body>
  <div style="background-color: #ffcc00; color: #000; text-align: center; padding: 10px; font-weight: bold;">
    🔔 Notification: <a href="https://docs.google.com/forms/d/1DSF5dxeb91_d1okZPqDh-hJF0cUHdqEudYTZYVjf4Co/preview" target="_blank" style="color: #000; text-decoration: underline;">Entry Form is now open — CLOSING DATE: Monday, 30th June 2025</a>
  </div>
  <header>
    <img src="ea48b0a3-b8c0-467f-838e-23affb25fd13.png" alt="Automobile Federation of North Macedonia Logo" />
    <h1>Serres 2025 - Official Press & Notice Board</h1>
    <p>Automobile Federation of North Macedonia - Technical Commission</p>
    <div style="display: flex; justify-content: center; gap: 20px; align-items: center; margin-top: 10px;">
      <img src="fia_wordmakr.png" alt="Member of FIA Logo" style="width: 100px;" />
      <img src="Central_European_Zone_logo.jpg" alt="CEZ Logo" style="width: 100px;" />
    </div>
  </header>

  <nav>
    <a href="#home">Home</a>
    <a href="#documents">Documents</a>
    <a href="#schedule">Schedule</a>
    <a href="#media">Media</a>
    <a href="bulletins.html">Bulletins Archive</a>
  </nav>

  <main>
    <section id="home">
      <h2>Latest Notices</h2>
      <div id="bulletin-container">
        <p>Loading bulletins...</p>
      </div>
    </section>

    <script>
      fetch('bulletins.json')
        .then(response => response.json())
        .then(bulletins => {
          const container = document.getElementById('bulletin-container');
          container.innerHTML = '';
          bulletins.reverse().slice(0, 4).forEach((b, i) => {
            container.innerHTML += `
              <div class="notice">
                <strong>Bulletin ${String(i + 1).padStart(2, '0')} - ${b.title} <span style='font-weight:normal;'>(Posted: ${b.timestamp})</span></strong>
                <p>${b.content}</p>
              </div>`;
          });
        })
        .catch(error => {
          document.getElementById('bulletin-container').innerHTML = '<p>Failed to load bulletins.</p>';
          console.error('Error loading bulletins:', error);
        });
    </script>
  </main>

  <footer>
    <p>&copy; 2025 Automobile Federation of North Macedonia</p>
  </footer>
</body>
</html>

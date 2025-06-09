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

    <section id="documents">
      <h2>Official Documents</h2>
      <p>Click below to download the latest regulations and bulletins.</p>
      <a class="download-link" href="https://afm.com.mk/wp-content/uploads/2025/06/Supplementary-Regulation-SERRES-2025.docx.pdf" target="_blank">Download Supplementary Regulation</a>
    </section>

    <section id="schedule">
      <h2>Event Schedule</h2>
      <p>The full time schedule will be uploaded soon. Please check back regularly for updates.</p>
    </section>

    <section id="media">
      <h2>Media</h2>
      <p>Photos and videos from the event will appear here.</p>
      <img src="poster.png" alt="FIA Central European Zone Championship Poster" style="width:100%; max-width:700px; display:block; margin:auto; margin-top:20px;" />
    </section>

    <section id="weather">
      <h2>Current Weather at Serres Circuit</h2>
      <div style="height:400px;width:100%;">
        <iframe
          width="100%"
          height="100%"
          src="https://embed.windy.com/embed2.html?lat=41.078&lon=23.550&detailLat=41.078&detailLon=23.550&width=650&height=450&zoom=10&level=surface&overlay=wind&menu=&message=true&marker=true&calendar=12&pressure=true&type=map&location=coordinates&detail=&metricWind=default&metricTemp=default&radarRange=-1"
          frameborder="0"
        ></iframe>
      </div>
    </section>

    <section id="info">
      <h2>Event Information</h2>
      <div class="notice">
        <strong>🏁 Name of the Event</strong>
        <p><strong>CIRCUIT RACE AK PERFORMANS</strong></p>
        <p>📍 Place: Automotodrom Serres, Greece</p>
        <p>📅 Date: 05th – 06th July 2025</p>
      </div>

      <div class="notice">
        <strong>📦 Organizer</strong>
        <p>
          AK PERFORMANS<br>
          Post address: ul: Franklin Ruzvelt br: 40/1-12<br>
          Telephone: +38976431880<br>
          E-mail: <a href="mailto:akperformans@gmail.com">akperformans@gmail.com</a>
        </p>
      </div>

      <div class="notice">
        <strong>🧑‍⚖️ Officials</strong>
        <p>
          Stewards Panel President: Pavle Donevski<br>
          Steward: Ranko Stanojkovski<br>
          Steward: Dean Grbac<br>
          Clerk of the Course: Kiril Karanakov<br>
          Chief of the Marshals: Autodrom SERRES<br>
          Secretary: Stefka Valeva<br>
          Chief Scrutineer: Autodrom SERRES<br>
          Scrutineering Assistant: Autodrom SERRES<br>
          Administrative Checks Manager: Stefka Valeva<br>
          Park Ferme and Paddock Manager: Mario Blazevski<br>
          Chief Timekeeper: Autodrom SERRES<br>
          Chief Medical Officer: Prim. Dr. Spec. Vasilaki Karabasev
        </p>
      </div>

      <div class="notice">
        <strong>📌 Locations</strong>
        <p>
          Race Control: Main Building, 1st Floor<br>
          Race Office: Main Building, 1st Floor<br>
          Stewards’ Office: Main Building, 1st Floor<br>
          Official Notice Board: Main Entrance of the Press Center, Ground Floor
        </p>
      </div>

      <div class="notice">
        <strong>📢 Status of the Event</strong>
        <p>
          - FIA CEZ Circuit and Endurance Championship<br>
          - Championship for North Macedonia<br>
          - TWINGO CUP<br>
          - CLIO CUP<br>
          - HONDA CUP<br>
          - BG CUP
        </p>
      </div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Automobile Federation of North Macedonia</p>
  </footer>
</body>
</html>

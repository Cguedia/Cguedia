<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>{{Tu Nombre}} — Portafolio / Desarrollo Web</title>

  <!-- Google Font (puedes cambiarla si prefieres) -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg:#0f1724;
      --card:#0b1220;
      --muted:#9aa4b2;
      --accent:#7c5cff;
      --glass: rgba(255,255,255,0.03);
      --radius:14px;
      --maxw:1100px;
      color-scheme: dark;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: linear-gradient(180deg, #061025 0%, #071428 50%, #08142a 100%);
      color:#e6eef8;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding:40px 20px;
      display:flex;
      justify-content:center;
    }
    .container{
      width:100%;
      max-width:var(--maxw);
    }

    header{
      display:flex;
      gap:20px;
      align-items:center;
      margin-bottom:24px;
    }
    .avatar{
      width:96px;
      height:96px;
      border-radius:16px;
      background:linear-gradient(135deg,var(--accent),#3bb89f);
      display:flex;
      align-items:center;
      justify-content:center;
      font-weight:700;
      font-size:34px;
      color:white;
      box-shadow:0 6px 18px rgba(124,92,255,0.18);
      flex-shrink:0;
    }
    .header-info h1{
      margin:0;
      font-size:24px;
      letter-spacing:-0.2px;
    }
    .header-info p{
      margin:6px 0 0;
      color:var(--muted);
      font-size:14px;
    }

    .grid{
      display:grid;
      grid-template-columns: 1fr 360px;
      gap:20px;
      align-items:start;
    }

    /* Left column */
    .card{
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:var(--radius);
      padding:18px;
      box-shadow: 0 6px 20px rgba(2,6,23,0.6);
      border: 1px solid rgba(255,255,255,0.03);
    }
    .hero{
      display:flex;
      gap:18px;
      align-items:flex-start;
    }
    .bio{
      line-height:1.6;
      color:var(--muted);
      font-size:15px;
    }

    .btn-row{
      margin-top:14px;
      display:flex;
      gap:10px;
    }
    .button{
      background:var(--accent);
      color:white;
      padding:10px 14px;
      border-radius:10px;
      text-decoration:none;
      font-weight:600;
      font-size:14px;
      display:inline-flex;
      gap:8px;
      align-items:center;
      box-shadow:0 6px 18px rgba(124,92,255,0.12);
    }
    .ghost{
      background:transparent;
      border:1px solid rgba(255,255,255,0.06);
      color:var(--muted);
      padding:10px 12px;
      border-radius:10px;
      text-decoration:none;
      font-size:14px;
    }

    h2.section-title{
      margin:0 0 12px 0;
      font-size:18px;
      display:flex;
      align-items:center;
      gap:10px;
    }

    /* Projects */
    .projects{
      display:grid;
      gap:12px;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    }
    .project-card{
      background:var(--card);
      padding:12px;
      border-radius:12px;
      border:1px solid rgba(255,255,255,0.03);
      min-height:120px;
      display:flex;
      flex-direction:column;
      justify-content:space-between;
    }
    .project-card h3{
      margin:0;
      font-size:16px;
    }
    .project-card p{
      margin:8px 0 0;
      color:var(--muted);
      font-size:13px;
      flex:1;
    }
    .project-links{
      margin-top:10px;
      display:flex;
      gap:8px;
    }
    .chip{
      background:var(--glass);
      padding:6px 8px;
      border-radius:999px;
      font-size:12px;
      color:var(--muted);
      border:1px solid rgba(255,255,255,0.02);
    }

    /* Right column (sidebar) */
    .sidebar .box{
      margin-bottom:12px;
    }
    .skills{
      display:flex;
      flex-wrap:wrap;
      gap:8px;
      margin-top:6px;
    }
    .skill{
      background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.02));
      padding:8px 10px;
      border-radius:10px;
      font-size:13px;
      color:var(--muted);
      border:1px solid rgba(255,255,255,0.02);
    }
    .contact-list{
      display:flex;
      flex-direction:column;
      gap:8px;
      margin-top:8px;
    }
    .contact-item{
      display:flex;
      gap:10px;
      align-items:center;
      color:var(--muted);
      font-size:14px;
      text-decoration:none;
    }

    footer{
      margin-top:22px;
      color:var(--muted);
      font-size:13px;
      text-align:center;
    }

    /* Responsive */
    @media (max-width:980px){
      .grid{grid-template-columns:1fr}
      .avatar{width:80px;height:80px;font-size:28px}
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- Header -->
    <header>
      <div class="avatar" aria-hidden="true">
        <!-- Iniciales o icono; reemplaza con <img> si quieres -->
        {{IN}}
      </div>
      <div class="header-info">
        <h1>{{Tu Nombre Completo}}</h1>
        <p>Estudiante de <strong>Desarrollo Web</strong> • Frontend • HTML | CSS | JavaScript</p>
        <div style="margin-top:10px">
          <a class="button" href="https://github.com/{{GITHUB_USERNAME}}" target="_blank" rel="noopener noreferrer">
            <!-- Simple GitHub SVG icon -->
            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" aria-hidden="true" xmlns="http://www.w3.org/2000/svg">
              <path d="M8 0.5C3.865 0.5 0.5 3.865 0.5 8C0.5 11.318 2.613 13.977 5.388 15.053C5.888 15.133 6.053 14.838 6.053 14.588C6.053 14.368 6.044 13.576 6.04 12.567C3.878 13.182 3.34 11.69 3.34 11.69C2.913 10.611 2.22 10.33 2.22 10.33C1.278 9.766 2.288 9.778 2.288 9.778C3.33 9.838 3.86 10.86 3.86 10.86C4.78 12.39 6.183 11.976 6.76 11.74C6.84 11.06 7.11 10.63 7.408 10.38C5.06 10.12 2.58 9.11 2.58 6.03C2.58 4.24 3.2 2.79 4.2 1.78C4.06 1.53 3.54 0.88 4.34 0.09C4.34 0.09 5.2 -0.08 6.04 0.55C6.86 0.31 7.73 0.19 8.6 0.19C9.47 0.19 10.34 0.31 11.16 0.55C12  -0.08 12.86 0.09 12.86 0.09C13.66 0.88 13.14 1.53 13 1.78C14 2.79 14.62 4.24 14.62 6.03C14.62 9.12 12.14 10.11 9.78 10.37C10.17 10.7 10.52 11.36 10.52 12.33C10.52 13.72 10.51 14.84 10.51 14.58C10.51 14.84 10.67 15.14 11.18 15.05C13.95 13.98 16.06 11.318 16.06 8C16.06 3.865 12.695 0.5 8.56 0.5H8Z" fill="white" opacity="0.9"/>
            </svg>
            Ver mi GitHub
          </a>
          <a class="ghost" href="#contacto">Contactar</a>
        </div>
      </div>
    </header>

    <div class="grid">
      <!-- LEFT: main content -->
      <main>
        <section class="card hero">
          <div style="flex:1">
            <h2 class="section-title">Sobre mí</h2>
            <p class="bio">
              <!-- Reemplaza este párrafo con tu presentación -->
              Hola, soy <strong>{{Tu Nombre}}</strong>, estudiante de <em>Desarrollo Web</em>. Me apasiona crear interfaces limpias y accesibles, aprender nuevas tecnologías y construir proyectos que resuelvan problemas reales. Actualmente estoy profundizando en JavaScript, HTML5, CSS3 y frameworks modernos.
            </p>

            <div class="btn-row">
              <a class="button" href="https://github.com/{{GITHUB_USERNAME}}" target="_blank" rel="noopener">Mi GitHub</a>
              <a class="ghost" href="#proyectos">Ver Proyectos</a>
            </div>
          </div>
          <div style="width:150px; text-align:center; opacity:0.95;">
            <!-- Área para foto o ilustración -->
            <div style="background: linear-gradient(135deg,#0b2540,#07243a); border-radius:12px; padding:12px;">
              <img src="{{URL_DE_TU_IMAGEN_OPCIONAL}}" alt="Foto" style="width:100%;border-radius:8px; display:block" onerror="this.style.display='none'">
              <div style="margin-top:8px; color:var(--muted); font-size:13px">Estudiante • Frontend</div>
            </div>
          </div>
        </section>

        <section id="proyectos" class="card" style="margin-top:16px">
          <h2 class="section-title">Proyectos destacados</h2>
          <p style="color:var(--muted); margin-top:0; font-size:14px">
            Aquí algunos proyectos que he subido a GitHub. Reemplaza cada tarjeta con tus proyectos reales.
          </p>

          <div class="projects" style="margin-top:12px">
            <!-- Proyecto 1 -->
            <article class="project-card">
              <div>
                <h3>Proyecto 1 — {{Nombre Proyecto}}</h3>
                <p>Breve descripción del proyecto: qué hace, tecnologías (HTML, CSS, JS, React...), y tu rol.</p>
              </div>
              <div class="project-links">
                <a class="chip" href="https://github.com/{{GITHUB_USERNAME}}/{{REPO1}}" target="_blank">Código</a>
                <a class="chip" href="{{LINK_PROYECTO1_WEBSITE}}" target="_blank">Demo</a>
                <span class="chip">HTML • CSS • JS</span>
              </div>
            </article>

            <!-- Proyecto 2 -->
            <article class="project-card">
              <div>
                <h3>Proyecto 2 — {{Nombre Proyecto}}</h3>
                <p>Breve descripción del proyecto 2. Explica la idea y por qué es relevante.</p>
              </div>
              <div class="project-links">
                <a class="chip" href="https://github.com/{{GITHUB_USERNAME}}/{{REPO2}}" target="_blank">Código</a>
                <a class="chip" href="{{LINK_PROYECTO2_WEBSITE}}" target="_blank">Demo</a>
                <span class="chip">React • API</span>
              </div>
            </article>

            <!-- Proyecto 3 (opcional) -->
            <article class="project-card">
              <div>
                <h3>Proyecto 3 — {{Nombre Proyecto}}</h3>
                <p>Describe aquí otro proyecto (portafolio, clon, pequeña app, etc.).</p>
              </div>
              <div class="project-links">
                <a class="chip" href="https://github.com/{{GITHUB_USERNAME}}/{{REPO3}}" target="_blank">Código</a>
                <span class="chip">Vanilla JS</span>
              </div>
            </article>
          </div>
        </section>

        <section class="card" style="margin-top:16px">
          <h2 class="section-title">Experiencia y formación</h2>
          <p style="color:var(--muted); margin-top:6px">
            <!-- Rellena con tus estudios/cursos -->
            Curso: {{Nombre del Curso o Bootcamp}} • Centro: {{Nombre del Centro}} • Fecha: {{Fecha}}.
          </p>

          <h2 class="section-title" style="margin-top:12px">Metas</h2>
          <p style="color:var(--muted); margin-top:6px">
            Convertirme en desarrollador/a frontend, trabajar en proyectos UX-friendly y seguir aprendiendo sobre accesibilidad y performance web.
          </p>
        </section>
      </main>

      <!-- RIGHT: sidebar -->
      <aside class="sidebar">
        <div class="card box">
          <h2 class="section-title">Habilidades</h2>
          <div class="skills" style="margin-top:8px">
            <div class="skill">HTML5</div>
            <div class="skill">CSS3</div>
            <div class="skill">JavaScript</div>
            <div class="skill">Responsive</div>
            <div class="skill">Git</div>
            <div class="skill">Bootstrap</div>
            <div class="skill">React (básico)</div>
            <!-- Añade o quita según necesites -->
          </div>
        </div>

        <div class="card box">
          <h2 class="section-title">Contacto</h2>
          <div class="contact-list">
            <a class="contact-item" href="mailto:{{TU_EMAIL}}" id="contacto">
              <!-- email icon -->
              <svg width="14" height="14" viewBox="0 0 24 24" fill="none" style="margin-right:6px"><path d="M4 6h16v12H4z" stroke="white" stroke-opacity="0.6" stroke-width="1.2" stroke-linejoin="round" stroke-linecap="round"/></svg>
              {{TU_EMAIL}}
            </a>
            <a class="contact-item" href="https://github.com/{{GITHUB_USERNAME}}" target="_blank" rel="noopener">
              <svg width="14" height="14" viewBox="0 0 24 24" fill="none" style="margin-right:6px"><path d="M12 .5C5.648.5.5 5.648.5 12c0 5.092 3.292 9.407 7.872 10.94.576.106.78-.25.78-.556 0-.274-.01-1.003-.015-1.97-3.203.697-3.88-1.54-3.88-1.54-.523-1.33-1.277-1.684-1.277-1.684-1.044-.713.08-.699.08-.699 1.154.082 1.76 1.184 1.76 1.184 1.025 1.756 2.688 1.249 3.343.955.104-.742.402-1.249.732-1.536-2.556-.29-5.244-1.278-5.244-5.686 0-1.256.448-2.283 1.184-3.089-.119-.29-.512-1.46.112-3.043 0 0 .964-.309 3.16 1.18.917-.255 1.9-.382 2.877-.387.977.005 1.96.132 2.877.387 2.196-1.488 3.158-1.18 3.158-1.18.626 1.583.234 2.753.115 3.043.74.806 1.182 1.833 1.182 3.089 0 4.42-2.693 5.392-5.256 5.677.413.355.78 1.057.78 2.13 0 1.538-.014 2.776-.014 3.153 0 .31.203.67.787.556C20.708 21.405 24 17.089 24 12c0-6.352-5.148-11.5-12-11.5z" fill="white" opacity="0.9"/></svg>
              github.com/{{GITHUB_USERNAME}}
            </a>
            <a class="contact-item" href="{{LINK_LINKEDIN}}" target="_blank" rel="noopener">
              <svg width="14" height="14" viewBox="0 0 24 24" fill="none" style="margin-right:6px"><path d="M4.98 3.5C4.98 4.88 3.86 6 2.48 6S0 4.88 0 3.5 1.12 1 2.5 1 4.98 2.12 4.98 3.5zM0 24h5V7H0v17zM7.5 7h4.7v2.2h.1c.66-1.25 2.28-2.56 4.7-2.56C22 6.64 24 9.04 24 13.8V24h-5v-9.4c0-2.24-.04-5.12-3.12-5.12-3.12 0-3.6 2.44-3.6 4.96V24h-5V7z" fill="white" opacity="0.9"/></svg>
              LinkedIn
            </a>
          </div>
        </div>

        <div class="card box">
          <h2 class="section-title">Repositorios recientes</h2>
          <p style="color:var(--muted); font-size:13px; margin-top:6px">
            <!-- Si quieres, aquí puedes pegar manualmente tus repos favoritos -->
            - {{REPO1}}<br>
            - {{REPO2}}<br>
            - {{REPO3}}
          </p>
        </div>

        <div class="card box">
          <h2 class="section-title">Disponibilidad</h2>
          <p style="color:var(--muted); font-size:13px; margin-top:6px">
            Buscando prácticas / proyectos freelance • Disponible para colaborar.
          </p>
        </div>
      </aside>
    </div>

    <footer>
      © <span id="year"></span> {{Tu Nombre}} — Portafolio generado con ❤️ • <a href="https://github.com/{{GITHUB_USERNAME}}" target="_blank" style="color:var(--muted); text-decoration:none">Mi GitHub</a>
    </footer>
  </div>

  <script>
    // Pequeños scripts para mejorar la plantilla
    document.getElementById('year').textContent = new Date().getFullYear();

    // si no quieres la imagen, pon el src vacío o borra la etiqueta <img> en el HTML
    // Reemplaza las {{PLACEHOLDER}} por tu información real:
    // - {{Tu Nombre}}, {{GITHUB_USERNAME}}, {{TU_EMAIL}}, {{LINK_LINKEDIN}}
    // - Repos: {{REPO1}}, {{REPO2}}, {{REPO3}}
    // También puedes cambiar colores en :root al comienzo del CSS.
  </script>
</body>
</html>

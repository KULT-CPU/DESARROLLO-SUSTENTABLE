<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Desarrollo Sustentable en el Ámbito Académico</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg-light: #f4fef6;
      --bg-dark: #121212;
      --text-light: #1a1a1a;
      --text-dark: #f0f0f0;
      --accent: #4caf50;
      --accent-dark: #388e3c;
      --card-bg-light: #ffffff;
      --card-bg-dark: #1e1e1e;
    }
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: 'Inter', sans-serif;
      background: var(--bg-light);
      color: var(--text-light);
      transition: background 0.4s ease, color 0.4s ease;
    }
    .dark-mode {
      background: var(--bg-dark);
      color: var(--text-dark);
    }
    header {
      background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                  url('https://images.unsplash.com/photo-1501004318641-b39e6451bec6') no-repeat center center/cover;
      text-align: center;
      padding: 6rem 1rem;
      color: white;
    }
    header h1 {
      font-size: 3rem;
      margin-bottom: 0.5rem;
    }
    header p {
      font-size: 1.3rem;
      font-style: italic;
      color: #d9f5d2;
    }
    .btn {
      padding: 0.9rem 2rem;
      background: var(--accent);
      border: none;
      color: white;
      font-weight: 700;
      border-radius: 8px;
      font-size: 1rem;
      margin-top: 2rem;
      cursor: pointer;
      transition: background 0.3s ease, transform 0.2s ease;
    }
    .btn:hover {
      background: var(--accent-dark);
      transform: scale(1.05);
    }
    .toggle-mode {
      position: fixed;
      top: 1rem;
      right: 1rem;
      background: var(--accent);
      color: white;
      border: none;
      padding: 0.6rem 1rem;
      border-radius: 20px;
      font-size: 1rem;
      cursor: pointer;
      z-index: 999;
      box-shadow: 0 2px 10px rgba(0,0,0,0.2);
      transition: background 0.3s ease;
    }
    .toggle-mode:hover {
      background: var(--accent-dark);
    }
    .section {
      padding: 4rem 1rem;
      max-width: 1100px;
      margin: auto;
    }
    .section h2 {
      text-align: center;
      font-size: 2.2rem;
      margin-bottom: 2rem;
    }
    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
    }
    .card {
      background: var(--card-bg-light);
      border-radius: 16px;
      padding: 1.5rem;
      box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
      cursor: pointer;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .card:hover {
      transform: translateY(-8px);
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.15);
    }
    .dark-mode .card {
      background: var(--card-bg-dark);
    }
    .card h3 {
      margin-top: 0;
      margin-bottom: 0.5rem;
      font-size: 1.2rem;
      color: var(--accent);
    }
    .detail {
      display: none;
      margin-top: 1rem;
      font-size: 0.95rem;
      line-height: 1.5;
      border-top: 1px solid #ccc;
      padding-top: 1rem;
      animation: expand 0.3s ease-in-out forwards;
    }
    @keyframes expand {
      from { opacity: 0; max-height: 0; }
      to { opacity: 1; max-height: 1000px; }
    }
    footer {
      text-align: center;
      padding: 2rem 1rem;
      background: #e0f2e9;
      color: #333;
      font-size: 0.9rem;
    }
    .dark-mode footer {
      background: #1a1a1a;
      color: #aaa;
    }
  </style>
</head>
<body>
  <button class="toggle-mode" onclick="document.body.classList.toggle('dark-mode')">🌙/☀️</button>

  <header>
    <h1>Desarrollo Sustentable en el Ámbito Académico</h1>
    <p>"No heredamos la Tierra de nuestros padres, la tomamos prestada de nuestros hijos."</p>
    <button class="btn" onclick="document.getElementById('subtemas').scrollIntoView({ behavior: 'smooth' });">Explorar subtemas</button>
  </header>

<section class="section" id="subtemas">
  <h2>temas</h2>
  <div class="cards">
    <div class="card" onclick="toggleDetail(this)">
      <h3>Biología</h3>
      <div class="detail"><p>Explica la biodiversidad y los ecosistemas, promoviendo prácticas de conservación.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Historia de México</h3>
      <div class="detail"><p>Analiza cómo los movimientos sociales han influido en la protección ambiental.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Inglés</h3>
      <div class="detail"><p>Vocabulario ambiental y sustentabilidad global.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Filosofía</h3>
      <div class="detail"><p>Reflexión ética sobre el impacto de nuestras acciones en el planeta.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Expresión oral y escrita</h3>
      <div class="detail"><p>Comunicación efectiva de ideas sustentables.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Geometría y trigonometría</h3>
      <div class="detail"><p>Diseño de estructuras ecológicas con herramientas matemáticas.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Computación</h3>
      <div class="detail"><p>Herramientas digitales para el análisis ambiental.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Orientación profesional y juvenil</h3>
      <div class="detail"><p>Integrar la sustentabilidad en la vida profesional y personal.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Apreciación artística</h3>
      <div class="detail"><p>Creación de arte con mensaje ecológico.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Transporte sostenible</h3>
      <div class="detail"><p>Promoción del transporte público y medios que no contaminen.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Hidroponía escolar</h3>
      <div class="detail"><p>Cultivo sin tierra en espacios escolares para fomentar el autoabastecimiento.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Reciclaje activo</h3>
      <div class="detail"><p>Concursos, separación y reuso creativo de materiales.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Moda sustentable</h3>
      <div class="detail"><p>Recolección y reutilización de ropa usada con fines ecológicos.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Gastronomía ecológica</h3>
      <div class="detail"><p>Recetas saludables, sostenibles y reducción del desperdicio alimentario.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Infraestructura verde</h3>
      <div class="detail"><p>Diseño de construcciones que respeten al medio ambiente.</p></div>
    </div>
    <div class="card" onclick="toggleDetail(this)">
      <h3>Turismo sostenible</h3>
      <div class="detail"><p>Fomentar el turismo educativo que conserve recursos naturales.</p></div>
    </div>
  </div>
</section>
</div>
      </div>
      <!-- Puedes mantener los demás bloques como los tenías -->
      <!-- ... (Resto de las tarjetas igual) -->
    </div>
  </section>

  <footer>
    © 2025 CECyT 4 - Proyecto Aula 2IM14
  </footer>

  <script>
    function toggleDetail(card) {
      const detail = card.querySelector('.detail');
      const all = document.querySelectorAll('.detail');
      all.forEach(d => { if (d !== detail) d.style.display = 'none'; });
      detail.style.display = detail.style.display === 'block' ? 'none' : 'block';
    }
  </script>
</body>
</html>

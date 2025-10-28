<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mahdi Tavakol — C/C++ Software Engineering Portfolio</title>
  <meta name="description" content="Mahdi Tavakol — C/C++ Software Engineering Portfolio: RAII, Parallelism, Numerical Software, Linux toolchains. Links to CVs, slides, GitHub repos, and Kaggle Python projects." />
  <style>
    :root {
      --bg: #0b0c10;
      --panel: #121316;
      --text: #eaeef2;
      --muted: #b6bec9;
      --brand: #60a5fa;
      --accent: #a78bfa;
      --card: #15171b;
      --border: #262a33;
      --link: #93c5fd;
    }
    @media (prefers-color-scheme: light) {
      :root { --bg:#ffffff; --panel:#f7f8fa; --text:#0f172a; --muted:#465366; --brand:#2563eb; --accent:#7c3aed; --card:#ffffff; --border:#e5e7eb; --link:#1d4ed8; }
    }
    * { box-sizing: border-box; }
    html, body { margin: 0; padding: 0; }
    body {
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, Noto Sans, Helvetica Neue, Arial, "Apple Color Emoji", "Segoe UI Emoji";
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }
    a { color: var(--link); text-decoration: none; }
    a:hover { text-decoration: underline; }
    .container { max-width: 980px; margin: 0 auto; padding: 16px; }
    header {
      position: sticky; top: 0; z-index: 40;
      background: linear-gradient(to bottom, rgba(0,0,0,.45), rgba(0,0,0,0));
      backdrop-filter: blur(6px);
    }
    .nav { display:flex; gap:12px; align-items:center; padding:10px 16px; border-bottom:1px solid var(--border); background: rgba(0,0,0,0.25); }
    .nav a { font-size: 14px; font-weight: 600; color: var(--muted); }
    .nav a:hover { color: var(--text); }

    .hero { padding: 22px 0 12px; text-align:center; }
    .hero h1 { margin: 0 0 6px; font-size: clamp(20px, 3vw, 28px); letter-spacing: .2px; }
    .hero p { margin: 4px 0 12px; color: var(--muted); font-size: 14px; }

    .badges { display:flex; flex-wrap: wrap; gap:6px 8px; justify-content:center; align-items:center; margin: 6px 0 12px; }
    .badge-img { display:inline-block; vertical-align: middle; }

    .section { margin: 18px 0 10px; padding: 14px; background: var(--panel); border: 1px solid var(--border); border-radius: 12px; }
    .section h2 { margin: 0 0 10px; font-size: 18px; }

    .grid { display:grid; grid-template-columns: 1fr; gap: 12px; }
    @media (min-width: 720px) { .grid { grid-template-columns: repeat(2, 1fr); } }

    .card { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 14px; }
    .card h3 { margin: 0 0 6px; font-size: 16px; }
    .card p { margin: 0; font-size: 14px; color: var(--muted); }
    .card a.btn { display:inline-block; margin-top: 8px; font-size: 13px; padding: 6px 10px; border-radius: 8px; border:1px solid var(--border); background: #0f172a22; }

    .mono { font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace; font-size: 12px; color: var(--muted); background: #00000020; border: 1px solid var(--border); border-radius: 8px; padding: 8px 10px; overflow:auto; }

    footer { margin: 24px 0 40px; text-align:center; color: var(--muted); font-size: 13px; }
    .pill { display:inline-block; border:1px solid var(--border); padding: 2px 8px; border-radius: 999px; font-size: 12px; color: var(--muted); }
  </style>
</head>
<body>
  <header>
    <nav class="nav container">
      <div class="pill">Mahdi Tavakol</div>
      <div style="flex:1"></div>
      <a href="#about">About</a>
      <a href="#highlights">Highlights</a>
      <a href="#repos">Projects</a>
      <a href="#kaggle">Python</a>
      <a href="#docs">CV & Slides</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main class="container">
    <!-- HERO -->
    <section class="hero" aria-label="Intro">
      <h1>🧭 Mahdi Tavakol — C++ Software Engineering Portfolio</h1>
      <p><strong>Modern C++ • Parallelism • RAII • Numerical Algorithms • Linux Toolchains</strong></p>

      <!-- Tech badges (kept exactly as requested) -->
      <div class="badges" aria-label="Tech stack badges">
        <a href="https://en.cppreference.com/w/" target="_blank" class="badge-img">
          <img alt="C++" src="https://img.shields.io/badge/C%2B%2B-17%2F20-00599C?logo=c%2B%2B&logoColor=white&style=flat" />
        </a>
        <a href="https://eigen.tuxfamily.org/" target="_blank" class="badge-img">
          <img alt="Eigen" src="https://img.shields.io/badge/Eigen-Linear%20Algebra-7E57C2?style=flat" />
        </a>
        <a href="https://www.openmp.org/" target="_blank" class="badge-img">
          <img alt="OpenMP" src="https://img.shields.io/badge/OpenMP-Parallelism-1E88E5?style=flat" />
        </a>
        <a href="https://www.mpi-forum.org/" target="_blank" class="badge-img">
          <img alt="MPI" src="https://img.shields.io/badge/MPI-Distributed-00838F?style=flat" />
        </a>
        <a href="https://cmake.org/" target="_blank" class="badge-img">
          <img alt="CMake" src="https://img.shields.io/badge/CMake-Build-064F8C?logo=cmake&style=flat" />
        </a>
        <a href="https://www.kernel.org/linux.html" target="_blank" class="badge-img">
          <img alt="Linux" src="https://img.shields.io/badge/Linux-Dev%20Env-242938?logo=linux&logoColor=white&style=flat" />
        </a>
      </div>

      <!-- Doc badges (kept) -->
      <div class="badges" aria-label="Document links">
        <a href="CV.pdf" class="badge-img">
          <img alt="Professional CV" src="https://img.shields.io/badge/Professional%20CV-0F766E?style=flat&logo=adobeacrobatreader&logoColor=white" />
        </a>
        <a href="CV-academic.pdf" class="badge-img">
          <img alt="Academic CV" src="https://img.shields.io/badge/Academic%20CV-2563EB?style=flat&logo=adobeacrobatreader&logoColor=white" />
        </a>
        <a href="C++-Overview.pdf" class="badge-img">
          <img alt="Portfolio Slides" src="https://img.shields.io/badge/Portfolio%20Slides-7C3AED?style=flat&logo=googledrive&logoColor=white" />
        </a>
        <a href="C++-Overview.pptx" class="badge-img">
          <img alt="PowerPoint" src="https://img.shields.io/badge/PowerPoint-9333EA?style=flat&logo=microsoftpowerpoint&logoColor=white" />
        </a>
        <a href="https://www.linkedin.com/in/mahditavakol/" target="_blank" class="badge-img">
          <img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" />
        </a>
        <a href="https://www.kaggle.com/mahditavakol/code" target="_blank" class="badge-img">
          <img alt="Python" src="https://img.shields.io/badge/Python-Kaggle%20Projects-3776AB?logo=python&logoColor=white&style=flat" />
        </a>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="section">
      <h2>🧩 About</h2>
      <p>
        I build high‑performance numerical software in Modern C++ (C++17/20), with a focus on <strong>RAII</strong>,
        parallel execution models (<strong>OpenMP</strong>/<strong>MPI</strong>), and clean <strong>CMake</strong> builds.
        This site hosts my CV, portfolio slides, and links to key repositories.
      </p>
    </section>

    <!-- HIGHLIGHTS -->
    <section id="highlights" class="section">
      <h2>✨ Highlights</h2>
      <ul style="margin: 0; padding-left: 18px;">
        <li>Modern C++ (C++17/20) with <strong>RAII</strong> and const‑correct APIs</li>
        <li><strong>Eigen</strong> for high‑performance linear algebra (<code class="mono">noalias()</code> aware)</li>
        <li><strong>OpenMP</strong> and <strong>MPI</strong> for parallel execution</li>
        <li><strong>CMake</strong> builds with Debug/Release & cross‑compiler support</li>
        <li>Scientific software patterns: <strong>Factory</strong>, <strong>Strategy</strong>, <strong>Interface</strong></li>
        <li>Linux‑first workflow (GCC/Clang, Intel oneAPI, Git)</li>
      </ul>
    </section>

    <!-- PROJECTS -->
    <section id="repos" class="section">
      <h2>🗂 Featured Repositories</h2>
      <div class="grid">
        <div class="card">
          <h3>🌀 ModernCppProjects</h3>
          <p>C++ projects demonstrating architecture, parallelism, and performance (e.g. Mandelbrot renderer).</p>
          <a class="btn" href="https://github.com/MahdiTavakol/ModernCppProjects" target="_blank">View repository</a>
        </div>
        <div class="card">
          <h3>🧪 LAMMPS-Constant-pH</h3>
          <p>C++ extensions for constant‑pH MD with robust HPC integration (LAMMPS ecosystem).</p>
          <a class="btn" href="https://github.com/MahdiTavakol/LAMMPS-Constant-pH" target="_blank">View repository</a>
        </div>
        <div class="card">
          <h3>⛰️ MetaDynamics / TI</h3>
          <p>Adaptive biasing and thermodynamic integration methods for molecular simulations.</p>
          <a class="btn" href="https://github.com/MahdiTavakol/lammps-metaAR-10Sep2025" target="_blank">View repository</a>
        </div>
        <div class="card">
          <h3>🧠 NeuralNetwork (C++)</h3>
          <p>Eigen‑powered neural network with RAII and OpenMP/MPI acceleration.</p>
          <a class="btn" href="https://github.com/MahdiTavakol/ModernCppProjects/tree/master/NeuralNetwork/NeuralNetwork" target="_blank">View subfolder</a>
        </div>
      </div>
    </section>

    <!-- KAGGLE / PYTHON -->
    <section id="kaggle" class="section">
      <h2>🐍 Python & Kaggle</h2>
      <p>
        While my core focus is C/C++, I also publish Python notebooks (data analysis, visualization, and ML) on Kaggle.
        Browse them here:
      </p>
      <p>
        <a class="btn" href="https://www.kaggle.com/mahditavakol/code" target="_blank">View my Kaggle Python projects</a>
      </p>
      <div class="mono" aria-label="Typical stack">
        pandas · numpy · matplotlib · scikit‑learn · SciPy · Jupyter
      </div>
    </section>

    <!-- DOCS -->
    <section id="docs" class="section">
      <h2>📄 CV & Slides</h2>
      <p>Download my latest CVs and portfolio slides.</p>
      <div class="badges">
        <a href="CV.pdf" class="badge-img">
          <img alt="Professional CV" src="https://img.shields.io/badge/Professional%20CV-0F766E?style=flat&logo=adobeacrobatreader&logoColor=white" />
        </a>
        <a href="CV-academic.pdf" class="badge-img">
          <img alt="Academic CV" src="https://img.shields.io/badge/Academic%20CV-2563EB?style=flat&logo=adobeacrobatreader&logoColor=white" />
        </a>
        <a href="C++-Overview.pdf" class="badge-img">
          <img alt="Portfolio Slides" src="https://img.shields.io/badge/Portfolio%20Slides-7C3AED?style=flat&logo=googledrive&logoColor=white" />
        </a>
        <a href="C++-Overview.pptx" class="badge-img">
          <img alt="PowerPoint" src="https://img.shields.io/badge/PowerPoint-9333EA?style=flat&logo=microsoftpowerpoint&logoColor=white" />
        </a>
      </div>
      <div class="mono" style="margin-top:8px;">
        Place the files <code>CV.pdf</code>, <code>CV-academic.pdf</code>, <code>C++-Overview.pdf</code>, and <code>C++-Overview.pptx</code> next to this <code>index.html</code>.
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="section">
      <h2>🗣️ Contact</h2>
      <p style="margin:0 0 8px;">
        <strong>Mahdi Tavakol</strong><br/>
        <em>Postdoctoral Researcher • Computational Scientist</em>
      </p>
      <div class="mono">mahditavakol90 [at] gmail [dot] com</div>
      <p style="margin-top:8px;">I’m keen to bring my <strong>C</strong>, <strong>Modern C++</strong>, <strong>CUDA C</strong>, and <strong>numerical simulation</strong> experience to software development roles.</p>
    </section>

    <!-- BUILD HINTS -->
    <section class="section">
      <h2>🛠️ Build Snippets</h2>
      <pre class="mono"># Configure & build (Release)
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build -j

# Debug build with symbols
cmake -S . -B build-debug -DCMAKE_BUILD_TYPE=Debug
cmake --build build-debug -j</pre>
    </section>
  </main>

  <footer>
    <p>© <span id="year"></span> Mahdi Tavakol • <a href="https://github.com/MahdiTavakol" target="_blank">GitHub</a> • <a href="https://www.linkedin.com/in/mahditavakol/" target="_blank">LinkedIn</a></p>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>

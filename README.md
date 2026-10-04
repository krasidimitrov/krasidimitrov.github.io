<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Portfolio of Krasimir Dimitrov — Senior Java Software Engineer specializing in backend systems, Spring, APIs, messaging, cloud and enterprise applications." />
  <title>Krasimir Dimitrov — Senior Java Software Engineer</title>
  <style>
    :root {
      --bg: #07090d;
      --panel: #0d1118;
      --panel-2: #111722;
      --text: #edf2f7;
      --muted: #9aa7b7;
      --line: rgba(255,255,255,.09);
      --accent: #7dd3fc;
      --accent-2: #a78bfa;
      --max: 1180px;
      --radius: 22px;
    }
    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      color: var(--text);
      background:
        radial-gradient(circle at 80% 0%, rgba(125,211,252,.10), transparent 30rem),
        radial-gradient(circle at 10% 20%, rgba(167,139,250,.08), transparent 28rem),
        var(--bg);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.6;
    }
    a { color: inherit; text-decoration: none; }
    .wrap { width: min(calc(100% - 40px), var(--max)); margin: 0 auto; }
    .nav {
      position: sticky; top: 0; z-index: 10;
      backdrop-filter: blur(16px);
      background: rgba(7,9,13,.72);
      border-bottom: 1px solid var(--line);
    }
    .nav-inner { height: 72px; display:flex; align-items:center; justify-content:space-between; }
    .brand { font-weight: 750; letter-spacing: -.03em; }
    .brand span { color: var(--accent); }
    .nav-links { display:flex; gap: 24px; color: var(--muted); font-size: .92rem; }
    .nav-links a:hover { color: var(--text); }
    .hero { min-height: 760px; display:grid; align-items:center; padding: 90px 0 110px; }
    .eyebrow { display:inline-flex; gap:9px; align-items:center; color:var(--accent); font-size:.78rem; font-weight:800; letter-spacing:.13em; text-transform:uppercase; }
    .dot { width:7px; height:7px; border-radius:50%; background:var(--accent); box-shadow:0 0 18px rgba(125,211,252,.8); }
    h1 { font-size: clamp(4rem, 8.5vw, 7.2rem); line-height:.88; letter-spacing:-.08em; max-width: 1050px; margin: 18px 0 14px; }
    h1 em { font-style:normal; color:var(--accent); }
    .hero-tagline { font-size: clamp(2rem, 4.5vw, 4.2rem); line-height:.98; letter-spacing:-.06em; max-width: 850px; margin: 0 0 26px; font-weight: 720; }
    .hero-copy { max-width: 720px; color:var(--muted); font-size: clamp(1.05rem, 2vw, 1.25rem); }
    .hero-actions { display:flex; flex-wrap:wrap; gap:12px; margin-top:32px; }
    .btn { display:inline-flex; align-items:center; justify-content:center; gap:10px; padding:13px 18px; border:1px solid var(--line); border-radius:999px; font-weight:700; transition:.2s ease; }
    .btn.primary { color:#061019; background:var(--text); border-color:var(--text); }
    .btn:hover { transform:translateY(-2px); border-color:rgba(125,211,252,.5); }
    .meta { margin-top: 44px; display:flex; flex-wrap:wrap; gap:10px; }
    .pill { padding:9px 12px; border:1px solid var(--line); border-radius:999px; color:#c7d1dc; background:rgba(255,255,255,.025); font-size:.86rem; }
    section { padding: 105px 0; border-top:1px solid var(--line); }
    .section-head { display:grid; grid-template-columns: .65fr 1.35fr; gap:50px; margin-bottom:48px; }
    .kicker { color:var(--accent); font-weight:800; font-size:.78rem; letter-spacing:.12em; text-transform:uppercase; }
    h2 { font-size:clamp(2.2rem,5vw,4.2rem); letter-spacing:-.06em; line-height:.98; margin: 0; }
    .lead { color:var(--muted); max-width:700px; margin:0; font-size:1.08rem; }
    .skills { display:grid; grid-template-columns: repeat(3, 1fr); gap:14px; }
    .skill { background:linear-gradient(145deg, rgba(255,255,255,.045), rgba(255,255,255,.018)); border:1px solid var(--line); border-radius:var(--radius); padding:25px; min-height:180px; }
    .skill h3 { margin:0 0 14px; font-size:1rem; }
    .skill p { color:var(--muted); margin:0; }
    .projects { display:grid; gap:18px; }
    .project { display:grid; grid-template-columns: 90px 1fr auto; gap:26px; align-items:start; padding:28px 0; border-top:1px solid var(--line); }
    .project:last-child { border-bottom:1px solid var(--line); }
    .num { color:var(--accent); font-weight:800; font-variant-numeric:tabular-nums; }
    .project h3 { font-size:1.45rem; margin:0 0 8px; letter-spacing:-.025em; }
    .project p { color:var(--muted); max-width:760px; margin:0; }
    .tags { max-width:300px; display:flex; flex-wrap:wrap; justify-content:flex-end; gap:7px; }
    .tag { font-size:.75rem; color:#bac5d1; padding:6px 8px; border:1px solid var(--line); border-radius:999px; white-space:nowrap; }
    .contrib-grid { display:grid; grid-template-columns:1fr 1fr; gap:12px; }
    .contrib { padding:18px 20px; border:1px solid var(--line); border-radius:16px; color:#c7d1dc; background:rgba(255,255,255,.018); }
    .timeline { display:grid; gap:18px; }
    .edu { display:grid; grid-template-columns: 160px 1fr; gap:25px; padding:24px 0; border-top:1px solid var(--line); }
    .date { color:var(--accent); font-size:.86rem; font-weight:750; }
    .edu h3 { margin:0 0 4px; font-size:1.08rem; }
    .edu p { margin:0; color:var(--muted); }
    .contact { padding:115px 0 125px; }
    .contact-box { position:relative; overflow:hidden; border:1px solid var(--line); border-radius:30px; padding:55px; background:linear-gradient(135deg, rgba(125,211,252,.08), rgba(167,139,250,.06) 55%, rgba(255,255,255,.025)); }
    .contact-box:after { content:""; position:absolute; width:330px; height:330px; right:-100px; top:-130px; border:1px solid rgba(125,211,252,.18); border-radius:50%; box-shadow:0 0 0 60px rgba(125,211,252,.025), 0 0 0 120px rgba(125,211,252,.015); }
    .contact-box > * { position:relative; z-index:1; }
    .contact-box h2 { max-width:780px; }
    .contact-details { display:flex; flex-wrap:wrap; gap:12px; margin-top:30px; }
    footer { padding:25px 0 45px; color:#657180; font-size:.82rem; display:flex; justify-content:space-between; gap:20px; }
    @media (max-width: 850px) {
      .nav-links { display:none; }
      .hero { min-height:auto; padding:90px 0 100px; }
      .section-head, .skills { grid-template-columns:1fr; }
      .section-head { gap:20px; }
      .project { grid-template-columns:50px 1fr; }
      .tags { grid-column:2; justify-content:flex-start; max-width:none; }
      .contrib-grid { grid-template-columns:1fr; }
      .edu { grid-template-columns:1fr; gap:7px; }
      .contact-box { padding:34px 25px; }
      footer { flex-direction:column; }
    }
    @media (max-width: 520px) {
      .wrap { width:min(calc(100% - 28px), var(--max)); }
      h1 { font-size:3.65rem; }
      .hero-tagline { font-size:2rem; }
      section { padding:80px 0; }
    }
  </style>
</head>
<body>
  <nav class="nav">
    <div class="wrap nav-inner">
      <a class="brand" href="#top">Krasimir<span>.</span></a>
      <div class="nav-links">
        <a href="#about">About</a><a href="#skills">Skills</a><a href="#projects">Projects</a><a href="#experience">Strengths</a><a href="#contact">Contact</a>
      </div>
    </div>
  </nav>

  <main id="top">
    <header class="hero wrap">
      <div>
        <div class="eyebrow"><span class="dot"></span> Senior Java Software Engineer</div>
        <h1>Building backend systems that <em>hold up.</em></h1>
        <p class="hero-copy">Backend-focused engineer with around a decade of experience developing and maintaining enterprise applications with Java and Spring — from technical design and implementation to testing, deployment and production support.</p>
        <div class="hero-actions">
          <a class="btn primary" href="#projects">View featured projects ↓</a>
          <a class="btn" href="mailto:kpackapgo@gmail.com">Get in touch ↗</a>
        </div>
        <div class="meta">
          <span class="pill">Java · Spring · Spring Boot</span>
          <span class="pill">APIs · Kafka · Microservices</span>
          <span class="pill">AWS · Docker · Kubernetes</span>
        </div>
      </div>
    </header>

    <section id="about">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">01 / About</div>
          <p class="lead">I work across the software development lifecycle: understanding requirements, shaping technical solutions, implementing features, testing them, supporting deployments and investigating production issues. My main strength is backend engineering, with practical experience contributing to the frontend when a project needs it.</p>
        </div>
        <div class="skills" id="skills">
          <article class="skill"><h3>Backend</h3><p>Java up to Java 25, Spring Framework, Spring Boot, JPA / Hibernate, REST APIs and SQL.</p></article>
          <article class="skill"><h3>Messaging & integration</h3><p>Kafka, Kafka Streams, OpenAPI and Kong, with experience integrating distributed services and legacy systems.</p></article>
          <article class="skill"><h3>Cloud & delivery</h3><p>AWS, Docker, Kubernetes, Terraform, Jenkins, Maven, Gradle and Git.</p></article>
          <article class="skill"><h3>Databases</h3><p>PostgreSQL, MySQL, MongoDB, DynamoDB and Google Bigtable.</p></article>
          <article class="skill"><h3>Testing</h3><p>JUnit 5, Mockito, TestNG, JMock and Cypress across unit, integration and end-to-end testing.</p></article>
          <article class="skill"><h3>Frontend</h3><p>Angular, AngularJS, GWT, Thymeleaf, IceFaces, PrimeFaces, JavaScript, HTML/CSS and Bootstrap.</p></article>
        </div>
      </div>
    </section>

    <section id="projects">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">02 / Featured Projects</div>
          <p class="lead">A selection of projects I've worked on throughout my career.</p>
        </div>
        <div class="projects">
          <article class="project">
            <div class="num">01</div>
            <div><h3>Enterprise Messaging Platform</h3><p>Contributed to a microservice-based messaging platform and web applications used to create message flows and manage customers. Implemented backend and UI features, REST integrations, automated tests and production fixes, while collaborating with customers and QA.</p></div>
            <div class="tags"><span class="tag">Java</span><span class="tag">Spring Boot</span><span class="tag">Kafka</span><span class="tag">AWS</span><span class="tag">DynamoDB</span><span class="tag">Cypress</span></div>
          </article>
          <article class="project">
            <div class="num">02</div>
            <div><h3>Project Management Platform</h3><p>Developed a large CMS covering funded-project lifecycles: teams, budgets, reports, expenses, time booking and completion tracking. Designed business features and UI mockups, refactored legacy modules, built tests, supported deployments and supervised interns.</p></div>
            <div class="tags"><span class="tag">Java</span><span class="tag">Spring Boot</span><span class="tag">PostgreSQL</span><span class="tag">IceFaces</span><span class="tag">Freemarker</span></div>
          </article>
          <article class="project">
            <div class="num">03</div>
            <div><h3>Public Renewable Energy API</h3><p>Built a customer-facing unified API for creating and managing energy sites, changing device settings and retrieving operational metrics. Integrated several microservices and a legacy monolith behind one interface.</p></div>
            <div class="tags"><span class="tag">Java</span><span class="tag">Spring Boot</span><span class="tag">REST</span><span class="tag">Docker</span><span class="tag">Kubernetes</span><span class="tag">Grafana</span></div>
          </article>
          <article class="project">
            <div class="num">04</div>
            <div><h3>E-commerce Integration Platform</h3><p>Helped take an application from early stages through production rollout, providing a unified way for customers to connect internal and external service providers. Contributed to requirements, architecture discussions, implementation and production monitoring.</p></div>
            <div class="tags"><span class="tag">Java</span><span class="tag">Spring Boot</span><span class="tag">MySQL</span><span class="tag">Angular</span><span class="tag">Terraform</span><span class="tag">Jenkins</span></div>
          </article>
          <article class="project">
            <div class="num">05</div>
            <div><h3>Smart Building Alarm Monitoring</h3><p>An independently built end-to-end lightweight system that monitored smart-building alarms and sent email notifications to configured recipients when events occurred. Included the browser interface and automated notification flow.</p></div>
            <div class="tags"><span class="tag">Java</span><span class="tag">Spring</span><span class="tag">AngularJS</span><span class="tag">Bootstrap</span></div>
          </article>
        </div>
      </div>
    </section>

    <section id="experience">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">03 / How I work</div>
          <p class="lead">Beyond implementation, I contribute to the engineering process around the code: technical decisions, estimation, documentation, reviews, mentoring and production support.</p>
        </div>
        <div class="contrib-grid">
          <div class="contrib">Design and implement REST APIs and backend services.</div>
          <div class="contrib">Integrate internal and external systems across monolithic and microservice architectures.</div>
          <div class="contrib">Research and propose technical solutions for new features and implementation challenges.</div>
          <div class="contrib">Estimate development work and break features into implementation tasks.</div>
          <div class="contrib">Participate in architecture and technical design discussions.</div>
          <div class="contrib">Create and maintain technical and API documentation.</div>
          <div class="contrib">Review code and provide support to junior developers.</div>
          <div class="contrib">Investigate production issues and develop automated tests.</div>
          <div class="contrib">Participate in technical interviews and candidate evaluation.</div>
          <div class="contrib">Work directly with customers to clarify requirements.</div>
        </div>
      </div>
    </section>

    <section id="education">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">04 / Education</div>
          <p class="lead">A background in informatics and IT systems, with studies at St. Cyril and St. Methodius University of Veliko Tarnovo.</p>
        </div>
        <div class="timeline">
          <article class="edu"><div class="date">2013 — 2015</div><div><h3>Master's Degree in IT Systems</h3><p>St. Cyril and St. Methodius University of Veliko Tarnovo</p></div></article>
          <article class="edu"><div class="date">2008 — 2012</div><div><h3>Bachelor's Degree in Informatics</h3><p>St. Cyril and St. Methodius University of Veliko Tarnovo</p></div></article>
          <article class="edu"><div class="date">2004 — 2008</div><div><h3>Mathematics and Informatics</h3><p>High School of Mathematics and Natural Sciences “Vasil Drumev”</p></div></article>
        </div>
      </div>
    </section>

    <section class="contact" id="contact">
      <div class="wrap">
        <div class="contact-box">
          <div class="kicker">05 / Contact</div>
          <h2>Have a backend problem worth solving?</h2>
          <p class="lead">For professional opportunities, technical discussions or project collaboration, feel free to get in touch.</p>
          <div class="contact-details">
            <a class="btn primary" href="mailto:kpackapgo@gmail.com">kpackapgo@gmail.com ↗</a>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer class="wrap">
    <span>© 2026 Krasimir Dimitrov</span>
    <span>Senior Java Software Engineer · Bulgaria</span>
  </footer>
</body>
</html>

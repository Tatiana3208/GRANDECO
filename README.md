<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>GRANDECO | Language Mastery Hub</title>
  <!-- Google Fonts + Font Awesome Icons -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: linear-gradient(145deg, #fefaf5 0%, #fff7f0 100%);
      color: #1e2a3e;
      scroll-behavior: smooth;
      line-height: 1.5;
    }

    /* custom scrollbar */
    ::-webkit-scrollbar {
      width: 8px;
    }
    ::-webkit-scrollbar-track {
      background: #f0e3d4;
      border-radius: 10px;
    }
    ::-webkit-scrollbar-thumb {
      background: #c7ad8f;
      border-radius: 10px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: #a8835e;
    }

    /* navigation */
    .navbar {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(255, 248, 240, 0.92);
      backdrop-filter: blur(16px);
      border-bottom: 1px solid rgba(224, 198, 168, 0.4);
      padding: 1rem 2rem;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.02);
    }

    .logo h1 {
      font-size: 1.9rem;
      font-weight: 800;
      background: linear-gradient(135deg, #cb7b43, #a55828);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      letter-spacing: -0.5px;
      transition: transform 0.2s ease;
    }
    .logo h1:hover {
      transform: scale(1.02);
    }

    .nav-links {
      display: flex;
      flex-wrap: wrap;
      gap: 1.2rem;
      list-style: none;
    }
    .nav-links a {
      text-decoration: none;
      font-weight: 600;
      color: #2c3e2f;
      background: rgba(235, 215, 190, 0.4);
      padding: 0.5rem 1rem;
      border-radius: 60px;
      font-size: 0.9rem;
      transition: all 0.25s;
      backdrop-filter: blur(4px);
    }
    .nav-links a:hover {
      background: #d8b48c;
      color: white;
      transform: translateY(-2px);
      box-shadow: 0 6px 12px rgba(0, 0, 0, 0.05);
    }

    /* hero area (contextual, not counting as extra section) */
    .hero {
      text-align: center;
      padding: 3rem 1.5rem 2rem;
      max-width: 1100px;
      margin: 0 auto;
    }
    .hero h2 {
      font-size: 2.2rem;
      font-weight: 700;
      background: linear-gradient(120deg, #5f4330, #b87a4b);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      margin-bottom: 0.75rem;
    }
    .hero p {
      font-size: 1.1rem;
      color: #4a5b5e;
      max-width: 680px;
      margin: 0 auto;
    }

    /* grid container for the 5 sections (cards) */
    .sections-grid {
      max-width: 1280px;
      margin: 2rem auto 4rem;
      padding: 0 1.5rem;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
      gap: 2rem;
    }

    /* individual section card */
    .section-card {
      background: #ffffffea;
      backdrop-filter: blur(2px);
      border-radius: 2rem;
      box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.08), 0 1px 2px rgba(0,0,0,0.02);
      transition: all 0.3s cubic-bezier(0.2, 0, 0, 1);
      overflow: hidden;
      border: 1px solid rgba(199, 163, 119, 0.25);
      display: flex;
      flex-direction: column;
    }
    .section-card:hover {
      transform: translateY(-6px);
      box-shadow: 0 28px 36px -14px rgba(82, 50, 23, 0.12);
      border-color: rgba(199, 163, 119, 0.5);
    }

    .card-header {
      padding: 1.5rem 1.5rem 0.75rem 1.5rem;
      border-bottom: 2px solid #f3e5d5;
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .card-header i {
      font-size: 2.2rem;
      color: #cb7b43;
      background: #fef1e6;
      padding: 0.6rem;
      border-radius: 1.2rem;
      box-shadow: inset 0 0 0 1px rgba(255,255,240,0.8);
    }
    .card-header h3 {
      font-size: 1.75rem;
      font-weight: 800;
      letter-spacing: -0.3px;
      background: linear-gradient(130deg, #3b2a1f, #8b5a2e);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
    }

    /* CONTENT AREA — user will replace this inner HTML with their own content */
    .content-area {
      padding: 1.5rem 1.5rem 2rem;
      flex: 1;
      background: #fefcf9;
      margin: 0.5rem 0.8rem 1.2rem 0.8rem;
      border-radius: 1.5rem;
      transition: background 0.2s;
      border: 1px dashed #e2cfb9;
    }
    .content-area:hover {
      background: #fffaf3;
      border-color: #cfb387;
    }

    .placeholder-text {
      color: #4f3e2e;
      font-size: 0.95rem;
      line-height: 1.5;
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    .placeholder-text i {
      color: #cb7b43;
      margin-right: 6px;
    }
    .edit-badge {
      display: inline-block;
      background: #f2e4d8;
      font-size: 0.7rem;
      font-weight: 500;
      padding: 0.2rem 0.7rem;
      border-radius: 40px;
      color: #a16536;
      margin-top: 10px;
      letter-spacing: 0.3px;
    }

    /* footer & info */
    .info-footer {
      text-align: center;
      background: #f1e9e0;
      padding: 2rem 1rem;
      margin-top: 1.5rem;
      border-top: 1px solid #e5d5c2;
      font-size: 0.9rem;
      color: #5b4a38;
    }
    .info-footer a {
      color: #bf7c48;
      text-decoration: none;
      font-weight: 600;
    }
    .info-footer a:hover {
      text-decoration: underline;
    }

    /* back to top button */
    .back-to-top {
      position: fixed;
      bottom: 2rem;
      right: 1.5rem;
      background: #cb7b43e0;
      backdrop-filter: blur(8px);
      color: white;
      width: 44px;
      height: 44px;
      border-radius: 60px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-decoration: none;
      font-size: 1.5rem;
      box-shadow: 0 6px 14px rgba(0,0,0,0.2);
      transition: 0.2s;
      opacity: 0.8;
    }
    .back-to-top:hover {
      opacity: 1;
      transform: translateY(-4px);
      background: #9f623a;
    }

    /* responsive */
    @media (max-width: 680px) {
      .navbar {
        flex-direction: column;
        text-align: center;
        padding: 1rem;
      }
      .nav-links {
        justify-content: center;
        gap: 0.7rem;
      }
      .card-header h3 {
        font-size: 1.5rem;
      }
      .hero h2 {
        font-size: 1.8rem;
      }
      .sections-grid {
        gap: 1.5rem;
        padding: 0 1rem;
      }
    }

    /* subtle animation for cards */
    @keyframes fadeSlide {
      0% { opacity: 0; transform: translateY(20px);}
      100% { opacity: 1; transform: translateY(0);}
    }
    .section-card {
      animation: fadeSlide 0.45s ease-out forwards;
    }
  </style>
</head>
<body>

<nav class="navbar">
  <div class="logo">
    <h1>GRANDECO</h1>
  </div>
  <ul class="nav-links">
    <li><a href="#section-A1A2"><i class="fas fa-arrow-right" style="margin-right: 6px;"></i>A1-A2</a></li>
    <li><a href="#section-A2B1"><i class="fas fa-arrow-right" style="margin-right: 6px;"></i>A2-B1</a></li>
    <li><a href="#section-B1B2"><i class="fas fa-arrow-right" style="margin-right: 6px;"></i>B1-B2</a></li>
    <li><a href="#section-Speaking"><i class="fas fa-comments" style="margin-right: 6px;"></i>Speaking circle</a></li>
    <li><a href="#section-Grammar"><i class="fas fa-book-open" style="margin-right: 6px;"></i>Grammar</a></li>
  </ul>
</nav>

<div class="hero">
  <h2>Elevate your language journey</h2>
  <p>GRANDECO provides structured levels, speaking communities, and a focused grammar hub. Each section below is fully editable: replace the placeholder with your own lessons, materials, or resources.</p>
</div>

<!-- 5 CORE SECTIONS: each corresponds to a specific language level/theme -->
<div class="sections-grid">

  <!-- Section 1: A1-A2 -->
  <div class="section-card" id="section-A1A2">
    <div class="card-header">
      <i class="fas fa-seedling"></i>
      <h3>A1 - A2</h3>
    </div>
    <div class="content-area">
      <!-- USER CONTENT ZONE: replace everything inside this div with your own content (text, images, lists, videos) -->
      <div class="placeholder-text">
        <i class="fas fa-pen-fancy"></i> <strong>Foundational stage – build your base</strong><br>
        ✅ Essential vocabulary & everyday expressions<br>
        ✅ Simple sentence structures & basic greetings<br>
        ✅ Listening drills, A1/A2 reading tasks<br>
        <div class="edit-badge"><i class="fas fa-edit"></i>  YOU CAN EDIT THIS BLOCK → replace with your own PDFs, quizzes, notes</div>
        <!-- example: add images or links -->
        <div style="margin-top: 12px; background:#f1e9e0; border-radius: 28px; padding: 8px 12px; font-size:0.85rem;">
          <i class="fas fa-cloud-upload-alt"></i> 📂 <em>Your custom content goes here (grammar tables, flashcards, welcome video)</em>
        </div>
      </div>
      <!-- END OF EDITABLE ZONE: The whole .placeholder-text block can be replaced with any HTML you like -->
    </div>
  </div>

  <!-- Section 2: A2-B1 -->
  <div class="section-card" id="section-A2B1">
    <div class="card-header">
      <i class="fas fa-chart-line"></i>
      <h3>A2 - B1</h3>
    </div>
    <div class="content-area">
      <div class="placeholder-text">
        <i class="fas fa-rocket"></i> <strong>Breakthrough to intermediate</strong><br>
        ✨ Narrate experiences & describe dreams<br>
        ✨ Understand main points of clear standard input<br>
        ✨ Interactive tasks & short articles<br>
        <div class="edit-badge"><i class="fas fa-edit"></i>  Replace with your own lessons, audio exercises, role-play scenarios</div>
        <div style="margin-top: 12px; background:#e9dfd1; border-radius: 28px; padding: 8px 12px;">
          📖 <em>Upload your content: PDF worksheets, video playlists, or practice tests → simply edit HTML</em>
        </div>
      </div>
    </div>
  </div>

  <!-- Section 3: B1-B2 -->
  <div class="section-card" id="section-B1B2">
    <div class="card-header">
      <i class="fas fa-globe"></i>
      <h3>B1 - B2</h3>
    </div>
    <div class="content-area">
      <div class="placeholder-text">
        <i class="fas fa-microphone-alt"></i> <strong>Upper intermediate mastery</strong><br>
        🎯 Express opinions & handle complex arguments<br>
        🎯 Nuanced writing, debates & authentic materials<br>
        🎯 Real-world listening & fluency boosters<br>
        <div class="edit-badge"><i class="fas fa-edit"></i>  Add your CEFR B1/B2 resources — essays, podcasts, grammar deep dives</div>
        <div style="margin-top: 12px;">
          📌 <em>Content showcase slot: you can embed links, Google Drive materials, or interactive quizzes</em>
        </div>
      </div>
    </div>
  </div>

  <!-- Section 4: Speaking circle -->
  <div class="section-card" id="section-Speaking">
    <div class="card-header">
      <i class="fas fa-comments"></i>
      <h3>Speaking circle</h3>
    </div>
    <div class="content-area">
      <div class="placeholder-text">
        <i class="fas fa-users"></i> <strong>Conversation hub – speak with confidence</strong><br>
        🗣️ Weekly speaking prompts & roleplay<br>
        🗣️ Discussion topics, guided dialogues<br>
        🗣️ Voice recording tips & partner activities<br>
        <div class="edit-badge"><i class="fas fa-edit"></i>  Replace with your own speaking tasks, meeting schedules, pronunciation guides</div>
        <div style="margin-top: 16px; background:#f6ede3; border-radius: 20px; padding: 10px;">
          🎙️ <em>"Insert speaking circle materials: conversation starters, realia, group projects, or audio prompts."</em>
        </div>
      </div>
    </div>
  </div>

  <!-- Section 5: Grammar -->
  <div class="section-card" id="section-Grammar">
    <div class="card-header">
      <i class="fas fa-book"></i>
      <h3>Grammar</h3>
    </div>
    <div class="content-area">
      <div class="placeholder-text">
        <i class="fas fa-table-list"></i> <strong>Grammar hub – rules & practice</strong><br>
        📖 Tenses, clauses, prepositions, and more<br>
        📖 Interactive tables & exercises<br>
        📖 Error correction drills & quick references<br>
        <div class="edit-badge"><i class="fas fa-edit"></i>  Replace placeholders with your grammar charts, worksheets, or slides</div>
        <div style="margin-top: 12px; background:#ecdccd; border-radius: 28px; padding: 8px 12px;">
          ✍️ <em>Custom grammar zone — you can embed videos, downloadable cheat sheets, or live exercises.</em>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- How to customise section (user guidance) -->
<div class="info-footer">
  <p><i class="fas fa-code-branch"></i> <strong>How to upload your own content:</strong> Open this <code>index.html</code> file, locate each section (A1-A2, A2-B1, B1-B2, Speaking circle, Grammar). Inside each <code>.content-area</code>, replace the placeholder <code>.placeholder-text</code> block with your desired HTML (text, images, iframes, lists, buttons).<br>  
  🌟 Save, commit & push to GitHub Pages → your updated material will go live instantly.<br>
  📌 <a href="#" id="scrollHint"><i class="fas fa-arrow-up"></i> Back to top</a> &nbsp;|&nbsp; <i class="fas fa-palette"></i> GRANDECO — Designed for intuitive language growth</p>
</div>

<a href="#" class="back-to-top" aria-label="Back to top">
  <i class="fas fa-chevron-up"></i>
</a>

<script>
  // smooth scroll for navbar links and back to top
  document.querySelectorAll('.nav-links a, .back-to-top, #scrollHint').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      if(this.getAttribute('href') && this.getAttribute('href').startsWith('#')) {
        const targetId = this.getAttribute('href').substring(1);
        const targetElement = document.getElementById(targetId);
        if(targetElement) {
          e.preventDefault();
          targetElement.scrollIntoView({
            behavior: 'smooth',
            block: 'start'
          });
          // optional: small focus outline
          targetElement.style.transition = "box-shadow 0.2s";
          targetElement.style.boxShadow = "0 0 0 3px #fea66e80";
          setTimeout(() => { targetElement.style.boxShadow = ""; }, 800);
        } else if(this.getAttribute('href') === '#') {
          // back-to-top default
          e.preventDefault();
          window.scrollTo({ top: 0, behavior: 'smooth' });
        }
      }
    });
  });

  // add highlight when nav link clicked (extra polish)
  const navLinks = document.querySelectorAll('.nav-links a');
  navLinks.forEach(link => {
    link.addEventListener('click', function() {
      navLinks.forEach(l => l.style.background = "");
      this.style.background = "#d8b48c";
      this.style.color = "white";
      setTimeout(() => {
        this.style.background = "";
        this.style.color = "";
      }, 400);
    });
  });

  // provide a small console note for developers
  console.log("GRANDECO landing page — each section's content area is fully editable. Replace placeholder with your own lessons, media, or resources.");
</script>

<!-- ADDITIONAL INFO: All 5 sections are ready for content injection, all ids properly structured. 
     Designed for GitHub Pages: lightweight, accessible, modern -->
</body>
</html>

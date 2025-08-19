[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/jecSxI3G)
# 📘 Assignment: HTML5 + Accessibility & SEO Basics

## Overview

This assignment will help you solidify your understanding of modern HTML5 structure while applying foundational concepts of web accessibility and search engine optimization (SEO). You’ll create a simple, semantically correct web page that prioritizes both human and machine readability—two pillars of great web design.

## Objective

Build a basic web page using HTML5 semantic tags, applying accessibility best practices and beginner-friendly SEO principles. Your final output should demonstrate a well-structured layout that supports screen readers and is optimized for discoverability.

## Guidelines

Use only HTML5. No CSS or JavaScript is required at this stage. Focus on using meaningful semantic elements to structure your page. Avoid using `<div>` or `<span>` unless absolutely necessary. Ensure your page has clearly defined sections such as a header, navigation, main content, and a footer.

Incorporate accessibility by using proper HTML5 landmarks and attributes that improve navigation for assistive technologies. Your HTML should reflect thoughtful planning of hierarchy and readability, both for users and search engines.

For SEO, emphasize the use of heading tags in the correct order, provide descriptive text, and ensure your content is both human-readable and crawler-friendly. Consider how a search engine would interpret your page in terms of structure and content clarity.

## Deliverables

A single HTML file named `index.html`. It should include:

* A semantic structure using appropriate HTML5 elements.
* Clear headings in a logical hierarchy.
* Accessibility enhancements using proper tags and attributes.
* SEO-friendly metadata and content.

## Tips

* Use HTML5 semantic tags appropriately.
* Organize content with accessibility in mind.
* Apply basic on-page SEO techniques.
* Follow clean, readable HTML code structure.

## ANSWER BELOW
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>PLP ➜ Graduate | Enhanced HTML5 Content & Forms</title>
  <meta name="description" content="An HTML5 assignment page themed around completing the PLP Software Development program and graduating. Includes semantic content, lists, tables, media, and a fully validated form." />
  <style>
    :root{
      --bg:#0f172a;        /* slate-900 */
      --panel:#111827;     /* gray-900 */
      --ink:#e5e7eb;       /* gray-200 */
      --muted:#9ca3af;     /* gray-400 */
      --accent:#22d3ee;    /* cyan-400 */
      --accent-2:#a78bfa;  /* violet-400 */
      --ok:#10b981;        /* emerald-500 */
      --warn:#f59e0b;      /* amber-500 */
      --err:#ef4444;       /* red-500 */
      --shadow: 0 10px 25px rgba(0,0,0,.35);
      --radius: 18px;
    }
    html,body{height:100%}
    body{
      margin:0; font:16px/1.55 system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, Noto Sans, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
      background: radial-gradient(1200px 1200px at 10% 10%, rgba(34,211,238,.12), transparent 50%),
                  radial-gradient(900px 900px at 90% 20%, rgba(167,139,250,.12), transparent 50%),
                  var(--bg);
      color:var(--ink);
    }
    header{
      max-width: 1100px; margin: 40px auto 24px; padding: 24px; background: linear-gradient(180deg, rgba(255,255,255,.03), rgba(255,255,255,.02)); border:1px solid rgba(255,255,255,.08); border-radius: var(--radius); box-shadow: var(--shadow);
    }
    header h1{margin:0 0 8px; font-size: clamp(1.5rem, 2.5vw, 2.25rem); letter-spacing:.3px}
    header p{margin:0; color:var(--muted)}
    .wrap{max-width:1100px; margin:0 auto 80px; padding:0 24px 24px;}

    section{background:var(--panel); border:1px solid rgba(255,255,255,.08); border-radius: var(--radius); padding: 22px; margin: 18px 0; box-shadow: var(--shadow);}
    section h2{margin:0 0 12px; font-size: 1.35rem}
    section h3{margin:18px 0 8px; font-size: 1.05rem; color: var(--accent)}
    p, li{color: var(--ink)}
    a{color:var(--accent)}
    code,kbd{background:rgba(255,255,255,.08); padding:.15rem .35rem; border-radius:8px}

    /* lists */
    ul.check{list-style:none; padding-left:0}
    ul.check li{position:relative; padding-left:28px; margin:8px 0}
    ul.check li::before{content:"✔"; position:absolute; left:0; top:0; color:var(--ok)}

    /* table */
    table{width:100%; border-collapse:collapse; border-spacing:0; overflow:hidden; border-radius:12px;}
    thead th{background:rgba(167,139,250,.12); color:var(--ink); text-align:left; padding:10px}
    tbody td{padding:10px; border-top:1px solid rgba(255,255,255,.08);}
    tbody tr:nth-child(even) td{background:rgba(255,255,255,.03)}

    figure{margin:0;}
    figcaption{color:var(--muted); font-size:.9rem; margin-top:6px}

    /* form */
    form{display:grid; gap:18px}
    fieldset{border:1px solid rgba(255,255,255,.12); border-radius: 14px; padding: 16px}
    legend{padding:0 8px; color:var(--accent-2); font-weight:600}

    .grid{display:grid; gap:12px}
    .grid.two{grid-template-columns: repeat(auto-fit, minmax(240px,1fr))}

    label{display:block; font-weight:600; margin-bottom:6px}
    .control{display:flex; align-items:center; gap:10px}
    input, select, textarea{width:100%; padding:10px 12px; border-radius: 12px; border:1px solid rgba(255,255,255,.15); background: rgba(255,255,255,.06); color:var(--ink)}
    input::placeholder, textarea::placeholder{color:rgba(229,231,235,.55)}
    input:focus, select:focus, textarea:focus{outline:2px solid var(--accent); border-color:transparent}

    .hint{color:var(--muted); font-size:.9rem}
    .req{color:var(--warn)}

    .actions{display:flex; gap:12px; flex-wrap:wrap}
    button{cursor:pointer; border:none; border-radius: 14px; padding:12px 16px; font-weight:700; box-shadow: var(--shadow)}
    .primary{background: linear-gradient(180deg, var(--accent), #0ea5b6); color:#0b1220}
    .ghost{background: transparent; color: var(--ink); border:1px solid rgba(255,255,255,.18)}

    .note{background:rgba(16,185,129,.12); border:1px solid rgba(16,185,129,.35); padding:10px 12px; border-radius:12px}
    .sr-only{position:absolute; left:-9999px}
  </style>
</head>
<body>
  <header>
    <h1>PLP ➜ Graduate — My Path to the Cap & Gown</h1>
    <p>This page demonstrates advanced HTML5 content elements and a fully validated form. Theme: I am studying the <strong>PLP Software Development Program</strong> and I am here to graduate.</p>
  </header>

  <main class="wrap">
    <!-- OVERVIEW SECTION WITH LISTS -->
    <section aria-labelledby="overview-title">
      <h2 id="overview-title">Overview</h2>
      <p>The journey from <em>PLP learner</em> to <strong>graduate</strong> involves organized study, consistent practice, and clear milestones. Below are the focus areas for my graduation plan.</p>
      <div class="grid two">
        <div>
          <h3>Focus Areas</h3>
          <ul class="check">
            <li>Master semantic HTML5 structure</li>
            <li>Design accessible, native-validated forms</li>
            <li>Create clean layouts with tables and lists</li>
            <li>Embed meaningful media content</li>
            <li>Prepare a professional portfolio for graduation</li>
          </ul>
        </div>
        <div>
          <h3>Graduation Milestones</h3>
          <ol>
            <li>Finish core modules (<time datetime="2025-09-15">15 Sep 2025</time>)</li>
            <li>Submit capstone project (<time datetime="2025-10-10">10 Oct 2025</time>)</li>
            <li>Mock interviews & career prep (<time datetime="2025-10-22">22 Oct 2025</time>)</li>
            <li>Final assessments (<time datetime="2025-11-05">05 Nov 2025</time>)</li>
            <li>PLP Graduation 🎓 (<time datetime="2025-11-20">20 Nov 2025</time>)</li>
          </ol>
        </div>
      </div>
      <p class="note" role="status" aria-live="polite">Purpose: <strong>PLP to Graduate</strong> — everything on this page is geared toward successfully completing the program.</p>
    </section>

    <!-- TABLE SECTION -->
    <section aria-labelledby="schedule-title">
      <h2 id="schedule-title">Weekly Study Schedule (Sample)</h2>
      <table aria-describedby="schedule-note">
        <thead>
          <tr>
            <th scope="col">Day</th>
            <th scope="col">Module</th>
            <th scope="col">Activity</th>
            <th scope="col">Planned Hours</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Mon</td>
            <td>HTML5 & Accessibility</td>
            <td>Semantic tags, forms, validation</td>
            <td>2</td>
          </tr>
          <tr>
            <td>Tue</td>
            <td>CSS Layouts</td>
            <td>Flexbox, Grid, responsive design</td>
            <td>2</td>
          </tr>
          <tr>
            <td>Wed</td>
            <td>JavaScript Fundamentals</td>
            <td>ES modules, DOM essentials</td>
            <td>2</td>
          </tr>
          <tr>
            <td>Thu</td>
            <td>APIs & JSON</td>
            <td>Fetch patterns, error handling</td>
            <td>2</td>
          </tr>
          <tr>
            <td>Fri</td>
            <td>Capstone</td>
            <td>Feature implementation & testing</td>
            <td>3</td>
          </tr>
        </tbody>
      </table>
      <p id="schedule-note" class="hint">This table demonstrates accessible headings and a clear tabular structure.</p>
    </section>

    <!-- MEDIA SECTION (image + audio + video) -->
    <section aria-labelledby="media-title">
      <h2 id="media-title">Media: My PLP Story</h2>
      <div class="grid two">
        <figure>
          <!-- Inline SVG ensures the image displays even offline -->
          <svg viewBox="0 0 600 360" role="img" aria-labelledby="svgTitle svgDesc" style="width:100%; border-radius:14px; display:block; background:linear-gradient(135deg, rgba(34,211,238,.25), rgba(167,139,250,.25))">
            <title id="svgTitle">PLP to Graduate — Progress Illustration</title>
            <desc id="svgDesc">A stylized path with milestones leading to a graduation cap.</desc>
            <rect x="0" y="0" width="600" height="360" fill="transparent"/>
            <path d="M40 300 C 120 240, 240 280, 320 220 S 520 120, 560 140" fill="none" stroke="white" stroke-width="6" opacity=".7"/>
            <circle cx="120" cy="240" r="10" fill="white"/>
            <circle cx="260" cy="260" r="10" fill="white"/>
            <circle cx="360" cy="200" r="10" fill="white"/>
            <circle cx="480" cy="160" r="10" fill="white"/>
            <g transform="translate(470,70)">
              <polygon points="0,20 60,0 120,20 60,40" fill="white"/>
              <rect x="52" y="40" width="16" height="16" fill="white"/>
              <line x1="120" y1="20" x2="135" y2="38" stroke="white" stroke-width="4"/>
              <circle cx="138" cy="42" r="6" fill="white"/>
            </g>
          </svg>
          <figcaption>Inline SVG image: <em>Path to Graduation</em>.</figcaption>
        </figure>
        <div>
          <figure>
            <audio controls aria-label="Short audio reflection about PLP journey">
              <source src="https://cdn.jsdelivr.net/gh/mdn/webaudio-examples/audio-basics/techno.wav" type="audio/wav" />
              Your browser does not support the audio element.
            </audio>
            <figcaption>Audio clip: study focus background sample.</figcaption>
          </figure>
          <figure style="margin-top:12px">
            <video controls width="100%" poster="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 600 360'%3E%3Crect width='600' height='360' fill='%230f172a'/%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' fill='%23a78bfa' font-size='24'%3EPLP Portfolio Teaser%3C/text%3E%3C/svg%3E">
              <source src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.mp4" type="video/mp4" />
              Your browser does not support the video tag.
            </video>
            <figcaption>Video clip: placeholder demo (will add my graduation vidoe here once completed).</figcaption>
          </figure>
        </div>
      </div>
        </section>

    <!-- FORM SECTION -->
    <section aria-labelledby="form-title">
      <h2 id="form-title">PLP Graduation Readiness Form</h2>
      <p class="hint">This form uses native HTML5 validation and accessible labels/fieldsets. Fields marked <span class="req">*</span> are required.</p>
      <form action="#" method="post" novalidate>
        <fieldset>
          <legend>Personal Details</legend>
          <div class="grid two">
            <div>
              <label for="fullName">Full Name <span class="req" aria-hidden="true">*</span></label>
              <input id="fullName" name="fullName" type="text" placeholder="e.g., Jane Mwila" required minlength="3" autocomplete="name" />
            </div>
            <div>
              <label for="email">Email <span class="req" aria-hidden="true">*</span></label>
              <input id="email" name="email" type="email" placeholder="you@example.com" required autocomplete="email" />
            </div>
            <div>
              <label for="phone">Phone (Zambia format) <span class="req" aria-hidden="true">*</span></label>
              <input id="phone" name="phone" type="tel" placeholder="09XX123456" required pattern="^0\d{9}$" title="Enter a 10-digit Zambian phone number starting with 0" autocomplete="tel" />
            </div>
            <div>
              <label for="studentId">PLP Student ID <span class="req" aria-hidden="true">*</span></label>
              <input id="studentId" name="studentId" type="text" placeholder="PLP-2025-001" required pattern="^PLP-\d{4}-\d{3}$" title="Format: PLP-YYYY-XXX (e.g., PLP-2025-001)" autocomplete="off" />
            </div>
          </div>
        </fieldset>

        <fieldset>
          <legend>Program Information</legend>
          <div class="grid two">
            <div>
              <label for="program">Program</label>
              <input id="program" name="program" type="text" value="PLP Software Development" readonly aria-readonly="true" />
              <p class="hint" id="program-hint">This field is read-only to reflect the page theme.</p>
            </div>
            <div>
              <label for="cohort">Cohort <span class="req" aria-hidden="true">*</span></label>
              <input id="cohort" name="cohort" list="cohortList" placeholder="Select or type" required />
              <datalist id="cohortList">
                <option value="2024/2025"/>
                <option value="2025/2026"/>
                <option value="2026/2027"/>
              </datalist>
            </div>
            <div>
              <label for="track">Primary Track</label>
              <select id="track" name="track" autocomplete="off">
                <option value="frontend">Frontend</option>
                <option value="backend">Backend</option>
                <option value="fullstack" selected>Full‑Stack</option>
                <option value="mobile">Mobile</option>
              </select>
            </div>
            <div>
              <label for="gradDate">Target Graduation Date <span class="req" aria-hidden="true">*</span></label>
              <input id="gradDate" name="gradDate" type="date" required />
            </div>
          </div>
        </fieldset>

        <fieldset>
          <legend>Progress & Portfolio</legend>
          <div class="grid two">
            <div>
              <label for="portfolioUrl">Portfolio URL <span class="req" aria-hidden="true">*</span></label>
              <input id="portfolioUrl" name="portfolioUrl" type="url" placeholder="https://your-portfolio.example" required pattern="https?://.+" title="Enter a valid URL starting with http:// or https://" autocomplete="url" />
            </div>
            <div>
              <label for="repos">Public Repos (0–100)</label>
              <input id="repos" name="repos" type="number" min="0" max="100" step="1" value="5" />
            </div>
            <div>
              <label for="confidence">Graduation Confidence</label>
              <input id="confidence" name="confidence" type="range" min="0" max="100" value="70" />
            </div>
            <div>
              <label for="skills">Key Skills (comma‑separated) <span class="req" aria-hidden="true">*</span></label>
              <input id="skills" name="skills" type="text" placeholder="HTML5, CSS, JS, Git" required pattern="^[^,]+(,[^,]+)*$" title="Provide a comma-separated list of skills" />
            </div>
          </div>
          <div>
            <label for="bio">Short Bio</label>
            <textarea id="bio" name="bio" rows="4" placeholder="A brief summary of my PLP journey and goals."></textarea>
          </div>
        </fieldset>

        <fieldset>
          <legend>Account Security</legend>
          <div class="grid two">
            <div>
              <label for="password">Create Password <span class="req" aria-hidden="true">*</span></label>
              <input id="password" name="password" type="password" required minlength="8" pattern="^(?=.*[A-Z])(?=.*[a-z])(?=.*\d).{8,}$" title="At least 8 characters, including upper, lower, and a number" autocomplete="new-password" />
            </div>
            <div>
              <label for="confirm">Confirm Password <span class="req" aria-hidden="true">*</span></label>
              <input id="confirm" name="confirm" type="password" required minlength="8" pattern="^(?=.*[A-Z])(?=.*[a-z])(?=.*\d).{8,}$" title="Must match the created password" autocomplete="new-password" />
            </div>
          </div>
          <p class="hint">Passwords uses uppercase and lower case and is case sensitive</p>
        </fieldset>

        <fieldset>
          <legend>Agreements</legend>
          <div class="control">
            <input id="terms" name="terms" type="checkbox" required />
            <label for="terms">I confirm the information provided is accurate and I am committed to graduating from PLP.</label>
          </div>
          <div class="control">
            <input id="updates" name="updates" type="checkbox" />
            <label for="updates">Send me updates about career opportunities and alumni events.</label>
          </div>
          <div class="control">
            <input id="contact" name="contact" type="radio" value="email" checked />
            <label for="contact">Preferred contact: Email</label>
          </div>
          <div class="control">
            <input id="contact2" name="contact" type="radio" value="phone" />
            <label for="contact2">Preferred contact: Phone</label>
          </div>
        </fieldset>

        <div class="actions">
          <button class="primary" type="submit">Submit Readiness</button>
          <button class="ghost" type="reset">Reset</button>
        </div>
      </form>
    </section>
  </main>

  <footer class="wrap" style="opacity:.85; text-align:center; color:var(--muted); padding-bottom:48px">
    Built for the <strong>PLP to Graduate</strong> theme — clean, semantic HTML5 with native form validation.
  </footer>
</body>
</html>


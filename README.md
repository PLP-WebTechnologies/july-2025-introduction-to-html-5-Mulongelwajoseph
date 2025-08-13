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

<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>PLPtoGraduate</title>
    <meta name="description" content="An example HTML5-only, accessible and SEO-friendly page for a telemedicine service. Demonstrates semantic structure, landmarks, and headings." />
    <meta name="author" content="TeleHealth Hub" />
    <meta name="robots" content="index, follow" />
  </head>
  <body>
 <header>
      <h1>PLPtoGraduate</h1>
      <p>Your trusted online clinic for secure, convenient care.</p>
<nav aria-label="Primary">
        <ul>
          <li><a href="#services" aria-current="page">Services</a></li>
          <li><a href="#how-it-works">How It Works</a></li>
          <li><a href="#doctors">Our Doctors</a></li>
          <li><a href="#news">News</a></li>
          <li><a href="#contact">Contact</a></li>
            <li><a href="#about">About Us</a></li>
        </ul>
      </nav>
 <form action="#search" method="get" role="search" aria-label="Site search">
        <label for="q">Search PLPtoGraduate Hub:</label>
        <input id="q" name="q" type="search" placeholder="e.g., dermatology, cardiology" />
        <button type="submit">Search</button>
      </form>
 <nav aria-label="Breadcrumb">
        <ol>
          <li><a href="#">Home</a></li>
          <li><a href="#services">Services</a></li>
          <li aria-current="page">Telemedicine</li>
        </ol>
      </nav>
    </header>
<main id="main-content">
      <section id="intro" aria-labelledby="intro-heading">
        <h2 id="intro-heading">Welcome to PLPtoGraduate</h2>
        <p>
          We provide confidential consultations, prescriptions, and follow‑ups via secure video. No app needed—just your browser and an internet connection.
        </p>
        <figure>
          <svg viewBox="0 0 300 120" role="img" aria-labelledby="hero-title hero-desc" width="100%" height="120">
            <title id="hero-title">Doctor speaking with a patient on a laptop</title>
            <desc id="hero-desc">Simple illustrative banner showing remote healthcare.</desc>
            <rect x="0" y="0" width="300" height="120" fill="#e6f2ff" />
            <circle cx="60" cy="60" r="30" fill="#b3d7ff" />
            <rect x="120" y="35" width="150" height="50" fill="#cce6ff" />
            <rect x="125" y="40" width="70" height="40" fill="#ffffff" />
            <rect x="200" y="40" width="65" height="40" fill="#ffffff" />
          </svg>
          <figcaption>PLPtoGraduate Hub connects you to clinicians wherever you are.</figcaption>
        </figure>
      </section>

  <section id="services" aria-labelledby="services-heading">
        <h2 id="services-heading">Services</h2>
        <article aria-labelledby="gp-care">
          <h3 id="gp-care">General Practice</h3>
          <p>Same‑day virtual appointments for common conditions and ongoing care.</p>
        </article>
        <article aria-labelledby="mental-health">
          <h3 id="mental-health">Mental Health Support</h3>
          <p>Licensed counsellors provide therapy and check‑ins from the privacy of your home.</p>
        </article>
        <article aria-labelledby="chronic-care">
          <h3 id="chronic-care">Chronic Care Management</h3>
          <p>Personalised plans for diabetes, hypertension, and asthma with remote monitoring.</p>
        </article>
      </section>

   <section id="how-it-works" aria-labelledby="how-heading">
        <h2 id="how-heading">How It Works</h2>
        <ol>
          <li>Choose a service and a time slot.</li>
          <li>Complete a short pre‑visit questionnaire.</li>
          <li>Join your secure video visit from any modern browser.</li>
          <li>Receive your care plan and, when needed, e‑prescriptions.</li>
        </ol>
        <details>
          <summary>What do I need for a visit?</summary>
          <p>A charged device, a stable internet connection, and a quiet space.</p>
        </details>
        <details>
          <summary>Is my data secure?</summary>
          <p>We follow strict privacy standards and use encrypted connections for all sessions.</p>
        </details>
      </section>

   <section id="doctors" aria-labelledby="doctors-heading">
        <h2 id="doctors-heading">Our Doctors</h2>
        <article aria-labelledby="dr-lee">
          <h3 id="dr-lee">Dr. A. Lee, MD</h3>
          <p>Family physician with 10+ years of telemedicine experience.</p>
        </article>
        <article aria-labelledby="dr-patel">
          <h3 id="dr-patel">Dr. R. Patel, PsyD</h3>
          <p>Clinical psychologist specialising in anxiety and workplace stress.</p>
        </article>
      </section>

  <section id="news" aria-labelledby="news-heading">
        <h2 id="news-heading">News &amp; Updates</h2>
        <article aria-labelledby="news-item-1">
          <header>
            <h3 id="news-item-1">Extended Hours Launch</h3>
            <p>
              <time datetime="2025-08-01">August 1, 2025</time>
            </p>
          </header>
          <p>We now offer consultations from <time datetime="08:00">08:00</time> to <time datetime="20:00">20:00</time> daily.</p>
          <footer>
            <p>Filed under: service updates</p>
          </footer>
        </article>
      </section>

  <aside aria-labelledby="hours-heading">
        <h2 id="hours-heading">Clinic Hours</h2>
        <table>
          <caption>Standard operating hours by day</caption>
          <thead>
            <tr>
              <th scope="col">Day</th>
              <th scope="col">Open</th>
              <th scope="col">Close</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">Monday–Friday</th>
              <td><time datetime="08:00">08:00</time></td>
              <td><time datetime="20:00">20:00</time></td>
            </tr>
            <tr>
              <th scope="row">Saturday</th>
              <td><time datetime="09:00">09:00</time></td>
              <td><time datetime="17:00">17:00</time></td>
            </tr>
            <tr>
              <th scope="row">Sunday</th>
              <td colspan="2">Closed</td>
            </tr>
          </tbody>
        </table>
      </aside>

  <section id="contact" aria-labelledby="contact-heading">
        <h2 id="contact-heading">Contact Us</h2>
        <article aria-labelledby="contact-form-heading">
          <h3 id="contact-form-heading">Send a Message</h3>
          <form action="#thanks" method="post" aria-describedby="contact-help">
            <p id="contact-help">Fields marked with * are required.</p>
            <fieldset>
              <legend>Your Details</legend>
              <label for="name">Full Name *</label>
              <input id="name" name="name" type="text" autocomplete="name" required />

  <label for="email">Email *</label>
   <input id="email" name="email" type="email" autocomplete="email" required />

  <label for="phone">Phone</label>
              <input id="phone" name="phone" type="tel" autocomplete="tel" />
            </fieldset>

   <fieldset>
              <legend>Your Message</legend>
              <label for="topic">Topic *</label>
              <select id="topic" name="topic" required>
                <option value="">Select a topic</option>
                <option>General enquiry</option>
                <option>Book an appointment</option>
                <option>Technical support</option>
              </select>

   <label for="message">Message *</label>
              <textarea id="message" name="message" rows="6" required></textarea>
            </fieldset>

  <button type="submit">Send</button>
          </form>
        </article>

 <article aria-labelledby="address-heading">
          <h3 id="address-heading">Address</h3>
          <address>
            TeleHealth Hub<br />
            123 Health Street<br />
            Ndola, Zambia<br />
            Phone: <a href="tel:+260000000000">+260 00 000 0000</a><br />
            Email: <a href="mailto:mulongelwajoseph@gmail.com">mulongelwajoseph@gmail.com</a>
          </address>
        </article>
      </section>
    </main>

  <footer>
      <nav aria-label="Footer">
        <ul>
          <li><a href="#privacy">Privacy</a></li>
          <li><a href="#terms">Terms</a></li>
          <li><a href="#accessibility">Accessibility</a></li>
        </ul>
      </nav>
      <p>&copy; <time datetime="2025">2025</time> PLPtoGraduate Hub. All rights reserved.</p>
    </footer>
  </body>
</html>



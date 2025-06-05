# Karton CSS

A lightweight, classless CSS framework inspired by cardboard-style design and Sakura CSS.  
Designed to work beautifully with the [Karton web component framework](https://github.com/biensurerodezee/karton-css).

---

## CDN Usage

Include Karton CSS in your HTML via CDN:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/karton-css/karton.css" type="text/css">
```

Features

    Classless styling: write semantic HTML without needing extra classes.

    Warm, organic tones with a cardboard-inspired aesthetic.

    Responsive typography and layouts optimized for readability.

    Styles for common HTML elements: headings, paragraphs, lists, tables, code, forms, alerts, modals, media, and more.

    Accessible modal and alert styles included.

    Works great standalone or with the Karton web component framework.

Quick Start Example
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Karton Component Showcase</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/karton-css/karton.css" type="text/css">
</head>
<body>
  <header>
    <h1>Karton Component Showcase</h1>
    <nav>
      <a href="#glossary">Glossary</a> |
      <a href="#media">Media</a> |
      <a href="#form">Contact</a>
    </nav>
  </header>

  <main>
    <article id="glossary">
      <h2>Glossary</h2>
      <dl>
        <dt>Karton</dt>
        <dd>A lightweight web component framework inspired by cardboard-style design.</dd>
        <dt>Unboxed</dt>
        <dd>A special render mode for Karton components when activated via URL.</dd>
        <dt>State</dt>
        <dd>An internal reactive data storage mechanism.</dd>
      </dl>
    </article>

    <aside>
      <h3>Did You Know?</h3>
      <p>Karton uses URL-based routing to switch between render modes.</p>
    </aside>

    <article id="media">
      <h2>Media Examples</h2>
      <section>
        <h2>Video Demo</h2>
        <div class="media-wrapper">
          <iframe 
            src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
            title="Demo Video" 
            frameborder="0" 
            allowfullscreen></iframe>
        </div>

        <h2>Sample Video</h2>
        <video controls>
          <source src="sample-video.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </section>
    </article>

    <section id="form">
      <h2>Contact Form</h2>
      <form>
        <label for="email">Email (required):</label>
        <input type="email" id="email" name="email" required placeholder="you@example.com" />

        <label for="age">Age (18+):</label>
        <input type="number" id="age" name="age" min="18" required />

        <label for="bio">Short Bio:</label>
        <textarea id="bio" name="bio" rows="4" placeholder="Tell us about yourself..."></textarea>

        <button type="submit">Submit</button>
      </form>
    </section>
  </main>

  <div class="alert alert-info">This is an info message.</div>
  <div class="alert alert-warning">Warning! Something needs your attention.</div>
  
  <button id="openDialogBtn">Open Dialog</button>

  <dialog id="myDialog" role="dialog" aria-modal="true" aria-labelledby="dialogTitle">
    <button class="close" aria-label="Close dialog">&times;</button>
    <h2 id="dialogTitle">Modal Title</h2>
    <p>This is the modal content.</p>
  </dialog>

  <script>
    const dialog = document.getElementById('myDialog');
    const openBtn = document.getElementById('openDialogBtn');
    const closeBtn = dialog.querySelector('button.close');

    openBtn.addEventListener('click', () => {
      dialog.showModal();
    });

    closeBtn.addEventListener('click', () => {
      dialog.close();
    });

    dialog.addEventListener('keydown', (event) => {
      if (event.key === 'Escape') {
        dialog.close();
      }
    });
  </script>

  <footer>
    <p>© 2025 Karton Framework. Made with care and cardboard.</p>
  </footer>
</body>
</html>

Element Styling Examples
Headings & Paragraphs

<h1>Header level 1</h1>
<h2>Header level 2</h2>
<p>This is a paragraph with <em>italic</em>, <strong>bold</strong>, and <code>monospace</code> text.</p>

Lists

<ul>
  <li>Unordered list item 1</li>
  <li>Unordered list item 2</li>
</ul>

<ol>
  <li>Ordered list item 1</li>
  <li>Ordered list item 2</li>
</ol>

Tables

<table>
  <caption>Sample Table</caption>
  <thead>
    <tr><th>Size</th><th>Material</th><th>Color</th></tr>
  </thead>
  <tbody>
    <tr><td>9</td><td>Leather</td><td>Brown</td></tr>
    <tr><td>10</td><td>Canvas</td><td>Natural</td></tr>
  </tbody>
</table>

Code Blocks

<pre><code>function greet() {
  console.log("Welcome to Karton!");
}</code></pre>

Forms

<form>
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required placeholder="you@example.com" />

  <label for="age">Age:</label>
  <input type="number" id="age" name="age" min="18" required />

  <label for="message">Message:</label>
  <textarea id="message" name="message" rows="4"></textarea>

  <button type="submit">Submit</button>
</form>

Alerts

<div class="alert alert-info">Information message</div>
<div class="alert alert-warning">Warning message</div>
<div class="alert alert-error">Error message</div>
<div class="alert alert-success">Success message</div>

Modal Dialog

<button id="openDialogBtn">Open Dialog</button>

<dialog id="myDialog" role="dialog" aria-modal="true" aria-labelledby="dialogTitle">
  <button class="close" aria-label="Close dialog">&times;</button>
  <h2 id="dialogTitle">Modal Title</h2>
  <p>This is the modal content.</p>
</dialog>

<script>
  const dialog = document.getElementById('myDialog');
  const openBtn = document.getElementById('openDialogBtn');
  const closeBtn = dialog.querySelector('button.close');

  openBtn.addEventListener('click', () => dialog.showModal());
  closeBtn.addEventListener('click', () => dialog.close());

  dialog.addEventListener('keydown', (event) => {
    if (event.key === 'Escape') dialog.close();
  });
</script>
```
Development & Contribution

Contributions and suggestions are very welcome! Please open issues or pull requests on the GitHub repository.
License

This project is licensed under the MIT License.

© 2025 Karton Framework by biensurerodezee.
Made with care and cardboard.


Let me know if you want it split into sections or formatted differently!
# karton-css
# karton-js

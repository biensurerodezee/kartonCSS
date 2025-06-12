# Karton CSS

A lightweight, classless CSS framework inspired by cardboard-style design and Sakura CSS.  
Designed to work beautifully with the [Karton web component framework](https://github.com/biensurerodezee/kartoncss).

---


## CDN Usage

Include Karton CSS in your HTML via CDN:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/kartoncss/karton.css" type="text/css">
```

Or minified:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/kartoncss/karton.min.css" type="text/css">
```


# Features

    Classless styling: write semantic HTML without needing extra classes.

    Warm, organic tones with a cardboard-inspired aesthetic.

    Responsive typography and layouts optimized for readability.

    Styles for common HTML elements: headings, paragraphs, lists, tables, code, forms, alerts, modals, media, and more.

    Accessible modal and alert styles included.

    Works great standalone or with the Karton web component framework.


# Example 

[Surge Live Example](https://kartoncss.surge.sh)
[JSDelivr Live Example](https://cdn.jsdelivr.net/npm/kartoncss/index.html)

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Karton CSS</title>
    <link rel="icon" type="image/svg+xml" href="karton-element.svg" />
    <link href='karton.css' id="karton-css" rel='stylesheet' type='text/css'>
  </head>
  <body>
    <span id="top"><span>
  
    <!-- semantic -->
    <header>
      <h1>Karton CSS Showcase</h1>
      <!-- navigation -->
      <nav>
        <a href="#glossary">Glossary</a>
        <a href="#media">Media</a>
        <a href="#form">Contact</a>
        <a href="#paragraphs">Paragraphs</a>
        <a href="#form-elements">Form Elements</a>
        <a href="#an-h3-header">List</a>
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
        <!-- media -->
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
  
    <!-- alerts -->
    <div class="alert alert-info">This is an info message.</div>
    <div class="alert alert-warning">Warning! Something needs your attention.</div>
    <div class="alert alert-error">Error! Something needs your attention badly.</div>
    
    <!-- modal -->
    <button id="openDialogBtn">Open Dialog</button>

    <dialog id="myDialog" role="dialog" aria-modal="true" aria-labelledby="dialogTitle">
      <button class="close" aria-label="Close dialog">&times;</button>
      <h2 id="dialogTitle">Modal Title</h2>
      <p>This is the modal content.</p>
      <p>This is the modal content.</p>
      <p>This is the modal content.</p>
      <p>This is the modal content.</p>
      <p>This is the modal content.</p>
      <p>This is the modal content.</p>
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

      // Optional: Close dialog on pressing Escape key
      dialog.addEventListener('keydown', (event) => {
        if (event.key === 'Escape') {
          dialog.close();
        }
      });
    </script>

    <!-- sakura test -->
    <div id="paragraphs">
      <p>Paragraphs look like this. Font size along with line height and maximum width are optimized for reading.</p>

      <p><em>Italic</em>, <strong>bold</strong>, and <code>monospace</code>. Itemized lists look like:</p>
      <ul>
        <li>this one</li>
        <li>that one</li>
        <li>the other one</li>
      </ul>

      <p><strong>Here's a block quote</strong>:</p>
      <blockquote>
        <p>Man surprised me most about humanity. Because he sacrifices his health in order to make money. Then he sacrifices money to recuperate his health. And then he is so anxious about the future that he does not enjoy the present; the result being that he does not live in the present or the future; he lives as if he is never going to die, and then dies having never really lived. -James J Lachard</p>
      </blockquote>

      <h2 id="an-h2-header">An h2 header</h2>
      <p><strong>Some code blocks</strong></p>
      <pre><code>define foobar() {
      print &quot;Welcome to flavor country!&quot;;
  }</code></pre>
      <div class="sourceCode">
        <pre class="sourceCode python"><code class="sourceCode python"><span class="im">import</span> time
        <span class="co"># Quick, count to ten!</span>
        <span class="cf">for</span> i <span class="op">in</span> <span class="bu">range</span>(<span class="dv">10</span>):
         <span class="co"># (but not *too* quick)</span>
      time.sleep(<span class="fl">0.5</span>)
        <span class="bu">print</span> i</code></pre>
      </div>

      <h3 id="an-h3-header">An h3 header</h3>
      <p>A nested list:</p>
      <ol style="list-style-type: decimal">
        <li>
          <p>First, get these ingredients:</p>
          <ul>
            <li>carrots</li>
            <li>celery</li>
            <li>lentils</li>
          </ul>
        </li>
        <li>
          <p>Boil some water.</p>
        </li>
        <li>
          <p>Dump everything in the pot and follow this algorithm:</p>
          <pre><code>find wooden spoon
    uncover pot
    stir
    cover pot
    balance wooden spoon precariously on pot handle
    wait 10 minutes
    goto first step (or shut off burner when done)</code></pre>
          <p>Do not bump wooden spoon or it will fall.</p>
        </li>
      </ol>

      <h1 id="header-level-1">Header level 1</h1>
      <h2 id="header-level-2">Header level 2</h2>
      <h3 id="header-level-3">Header level 3</h3>
      <h4 id="header-level-4">Header level 4</h4>
      <h5 id="header-level-5">Header level 5</h5>
      <h6 id="header-level-6">Header level 6</h6>

      <p>A horizontal line:</p>
      <hr>

      <p>Here's a link to <a href="http://foo.bar">a website</a>, to a <a href="local-doc.html">local doc</a>, and to a <a href="#an-h2-header">section heading in the current doc</a>. Here's a footnote <a href="#fn1" id="fnref1"><sup>1</sup></a>.</p>
      <p>Tables can look like this:</p>

      <table>
        <caption>
          Shoes, their sizes, and what they're made of
        </caption>
        <thead>
          <tr >
            <th align="left">size</th>
            <th align="left">material</th>
            <th align="left">color</th>
          </tr>
        </thead>
        <tbody>
          <tr >
            <td align="left">9</td>
            <td align="left">leather</td>
            <td align="left">brown</td>
          </tr>
          <tr >
            <td align="left">10</td>
            <td align="left">hemp canvas</td>
            <td align="left">natural</td>
          </tr>
          <tr >
            <td align="left">11</td>
            <td align="left">glass</td>
            <td align="left">transparent</td>
          </tr>
        </tbody>
      </table>
      <p>Multi-line tables:</p>
      <table style="width:46%;">
        <colgroup>
          <col width="13%">
          <col width="31%">
        </colgroup>
        <thead>
          <tr>
            <th align="left">keyword</th>
            <th align="left">text</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td align="left">red</td>
            <td align="left">Sunsets, apples, and other red or reddish things.</td>
          </tr>
          <tr>
            <td align="left">green</td>
            <td align="left">Leaves, grass, frogs and other things it's not easy being.</td>
          </tr>
        </tbody>
      </table>

      <p>A horizontal rule follows.</p>
      <hr>
      <p>Images are responsive by default:</p>
      <div>
        <img alt="example image" src="sakura.png" title="An exemplary image">
        <p>example image</p>
      </div>

      <hr>

      <h1 id="form-elements">Form Elements</h1>
      <form>
        <div id="forms__input">
          <h3>Input fields</h3>
          <p><label for="input__text">Text Input</label> <input id="input__text" placeholder="Text Input" type="text"></p>
          <p><label for="input__password">Password</label> <input id="input__password" placeholder="Type your Password" type="password"></p>
          <p><label for="input__webaddress">Web Address</label> <input id="input__webaddress" placeholder="http://yoursite.com" type="url"></p>
          <p><label for="input__emailaddress">Email Address</label> <input id="input__emailaddress" placeholder="name@email.com" type="email"></p>
          <p><label for="input__phone">Phone Number</label> <input id="input__phone" placeholder="(999) 999-9999" type="tel"></p>
          <p><label for="input__search">Search</label> <input id="input__search" placeholder="Enter Search Term" type="search"></p>
          <p><label for="input__text2">Number Input</label> <input id="input__text2" placeholder="Enter a Number" type="number"></p>
          <p><label for="input__text3">Error</label> <input id="input__text3" placeholder="Text Input" type="text"></p>
          <p><label for="input__text4">Valid</label> <input id="input__text4" placeholder="Text Input" type="text"></p>
        </div>
        <p><a href="#top">[Top]</a></p>
        <div id="forms__select">
          <h3>Select menus</h3>
          <p><label for="select">Select</label> <select id="select">
              <optgroup label="Option Group">
                <option>
                  Option One
                </option>
                <option>
                  Option Two
                </option>
                <option>
                  Option Three
                </option>
              </optgroup>
          </select></p>
        </div>
        <p><a href="#top">[Top]</a></p>
        <div id="forms__checkbox">
          <h3>Checkboxes</h3>
          <ul style="list-style:none;">
            <li><label for="checkbox1"><input checked="checked" id="checkbox1" name="checkbox" type="checkbox"> Choice A</label></li>
            <li><label for="checkbox2"><input id="checkbox2" name="checkbox" type="checkbox"> Choice B</label></li>
            <li><label for="checkbox3"><input id="checkbox3" name="checkbox" type="checkbox"> Choice C</label></li>
          </ul>
        </div>
        <p><a href="#top">[Top]</a></p>
        <div id="forms__textareas">
          <h3>Textareas</h3>
          <p><label for="textarea">Textarea</label>
            <textarea cols="48" id="textarea" placeholder="Enter your message here" rows="8"></textarea></p>
        </div>
        <p><a href="#top">[Top]</a></p>
        <div id="forms__html5">
          <div id="forms__action">
            <h3>Action buttons</h3>
            <p><input type="submit" value="input type=submit"> <input type="button" value="input type=button"> <input type="reset" value="input type=reset"> <input disabled type="submit" value="input disabled"></p>
            <p><button type="submit">&lt;button type=submit&gt;</button> <button type="button">&lt;button type=button&gt;</button> <button type="reset">&lt;button type=reset&gt;</button> <button disabled type="button">&lt;button disabled&gt;</button></p>
          </div>
          <p><a href="#top">[Top]</a></p>
        </div>
      </form>
      <div>
        <hr>
        <ol>
          <li id="fn1"><p>Footnote text goes here.<a href="#fnref1">↩</a></p></li>
        </ol>
      </div>
    </div>
    <!-- footer -->
    <footer>
      <p>© 2025 Karton Framework. Made with care and cardboard.</p>
    </footer>

  </body>
</html>
```


# Development & Contribution

Contributions and suggestions are very welcome! Please open issues or pull requests on the GitHub repository.


# License

This project is licensed under the MIT License.

© 2025 Karton Framework by biensurerodezee.
Made with care and cardboard.


##### kartonJS
The [KartonJS](https://github.com/biensurerodezee/kartonJS) WebComponent Framework using KartonCSS by default

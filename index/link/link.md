---
# This is a generated file
title: "Link Examples"
ref: /aria-practices/

github:
  repository: w3c/aria-practices
  path: aria-practices.html
permalink: /index/link/link

lang: en
---
<script src="../js/examples.js"></script>
<script src="../js/highlight.pack.js"></script>
<script src="../js/app.js"></script>

<link href="css/link.css" rel="stylesheet" />
<script src="js/link.js" type="text/javascript"></script>


<link rel="stylesheet" href="/assets/styles.css">
<!-- Code highlighting styles -->
<link rel="stylesheet" href="/index/css/github.css">

<div>

        <div class="sidebar-container">
          <aside class="sidebar-left" aria-describedby="sidebar-toc">
            <h2 id="sidebar-toc" class="sidebar-headline">Table of Contents</h2>
            <ul class="sidebar-list">
              
                    <li>
                      <a href="#ex_label">Examples</a>
                    </li>
                   
                    <li>
                      <a href="#kbd_label">Keyboard Support</a>
                    </li>
                   
                    <li>
                      <a href="#rps_label">Role, Property, State, and Tabindex  Attributes</a>
                    </li>
                   
                    <li>
                      <a href="#javascript-and-css-source-code">Javascript and CSS Source Code</a>
                    </li>
                   
                    <li>
                      <a href="#html-source-code">HTML Source Code</a>
                    </li>
                  
            </ul>
            
    <ul class="sidebar-list sidebar-list-yellow">
      <li><a href="/about/#browser_and_AT_support">Browser and Assistive Technology Support</a></li>
      <li><a href="https://github.com/w3c/aria-practices/issues/new">Report Issue</a></li>
      <li><a href="https://github.com/w3c/aria-practices/projects/21">Related Issues</a></li>
      <li><a href="/patterns/link/">Design Pattern</a></li>
    </ul>
  
          </aside>
          <div class="sidebar-right"><h2 class="followed-by-support-notice">About This Example</h2><img alt=""
        src="/assets/img/link.svg"
        class="example-page-example-icon"
      >
  
  <div>
  
  <p>
    The examples below demonstrate three variations of the
    <a href="/patterns/link/">design pattern for link</a>.
     The link pattern is used when it is necessary for elements other than the HTML <code>a</code> element to have link behaviors.
  </p>
  <p>
    <strong>Note:</strong> Use the HTML <code>a</code> element to create links whenever possible.
    Browsers provide valuable functionality for native HTML links, e.g., open the target in a new window and copy the target URL to the system clipboard.
  </p>
  <section>
    <h2 id="ex_label" tabindex="-1">Examples</h2>
    <div role="separator" id="ex_start_sep" aria-labelledby="ex_start_sep ex_label" aria-label="Start of"></div>
    <div class="table-wrap"><table class="data">
      <thead>
        <tr>
          <th>Number</th>
          <th>Description</th>
          <th>Link</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>
            <div class="example-header"><span id="ex1_label">1</span></div>
          </th>
          <td>
            <code>span</code> element with text content.
          </td>
          <td id="ex1">
            <span tabindex="0"
                role="link"
                onclick="goToLink(event, 'https://www.w3.org/')"
                onkeydown="goToLink(event, 'https://www.w3.org/')">
              W3C website
            </span>
          </td>
        </tr>
        <tr>
          <th>
            <div class="example-header"><span id="ex2_label">2</span></div>
          </th>
          <td>
            <code>img</code> element with <code>alt</code> attribute.
          </td>
          <td id="ex2">
            <img tabindex="0"
              role="link"
              onclick="goToLink(event, 'https://www.w3.org/')"
              onkeydown="goToLink(event, 'https://www.w3.org/')"
              src="images/w3c-logo.svg"
              alt="W3C Website">
          </td>
        </tr>
        <tr>
          <th>
            <div class="example-header"><span id="ex3_label">3</span></div>
          </th>
          <td>
            CSS <code>:before</code> content property on a <code>span</code> element.
          </td>
          <td id="ex3">
            <span tabindex="0"
              role="link"
              class="link3"
              onclick="goToLink(event, 'https://www.w3.org/TR/wai-aria-practices/')"
              onkeydown="goToLink(event, 'https://www.w3.org/TR/wai-aria-practices/')"
              aria-label="W3C website"></span>
          </td>
        </tr>
      </tbody>
    </table></div>
    <div role="separator" id="ex_end_sep" aria-labelledby="ex_end_sep ex_label" aria-label="End of"></div>
  </section>
  <section>
    <h2 id="kbd_label" tabindex="-1">Keyboard Support</h2>
    <div class="table-wrap"><table aria-labelledby="kbd_label" class="def">
      <thead>
        <tr>
          <th>Key</th>
          <th>Function</th>
        </tr>
      </thead>
      <tbody>
        <tr data-test-id="key-enter">
          <th><kbd>enter</kbd></th>
          <td>
          Activates the link.
          </td>
        </tr>
      </tbody>
    </table></div>
  </section>

  <section>
    <h2 id="rps_label" tabindex="-1">Role, Property, State, and Tabindex  Attributes</h2>
    <div class="table-wrap"><table aria-labelledby="rps_label" class="data attributes">
      <thead>
        <tr>
          <th scope="col">Role</th>
          <th scope="col">Attribute</th>
          <th scope="col">Element</th>
          <th scope="col">Usage</th>
        </tr>
      </thead>
      <tbody>
        <tr data-test-id="link-role">
          <th scope="row"><code>link</code></th>
          <td>
          </td>
          <td><code>span</code><br><code>img</code></td>
          <td>
            <ul>
            <li>Examples 1 and 3: Identifies the <code>span</code> element as a <code>link</code>.</li>
            <li>Example 2: Identifies the <code>img</code> element as a <code>link</code>.</li>
            </ul>
          </td>
        </tr>
        <tr data-test-id="tabindex">
          <td></td>
          <th scope="row"><code>tabindex=&quot;0&quot;</code></th>
          <td><code>span</code>, <br><code>img</code></td>
          <td>Includes the link element in the page tab sequence.</td>
        </tr>
        <tr data-test-id="alt">
          <td></td>
          <th scope="row"><code>alt</code></th>
          <td><code>img</code></td>
          <td>
                Example 2: Defines the accessible name of the link.
          </td>
        </tr>
        <tr data-test-id="aria-label">
          <td></td>
          <th scope="row"><code>aria-label</code></th>
          <td><code>span</code></td>
          <td>
            Example 3: Defines the accessible name of the link.
          </td>
        </tr>
      </tbody>
    </table></div>
  </section>

  <section>
    <h2 tabindex="-1" id="javascript-and-css-source-code">Javascript and CSS Source Code</h2>
    <ul id="css_js_files">
      <li>
        CSS:
        <a href="css/link.css" type="tex/css">link.css</a>
      </li>
      <li>
        Javascript:
        <a href="js/link.js" type="text/javascript">link.js</a>
      </li>
    </ul>
  </section>

  <section>
    <h2 tabindex="-1" id="html-source-code">HTML Source Code</h2>
    <h3 id="sc1_label">Link 1</h3>
    <div role="separator" id="sc1_start_sep" aria-labelledby="sc1_start_sep sc1_label" aria-label="Start of"></div>
    <pre><code id="sc1"></code></pre>
    <div role="separator" id="sc1_end_sep" aria-labelledby="sc1_end_sep sc1_label" aria-label="End of"></div>
    <h3 id="sc2_label">Link 2</h3>
    <div role="separator" id="sc2_start_sep" aria-labelledby="sc2_start_sep sc2_label" aria-label="Start of"></div>
    <pre><code id="sc2"></code></pre>
    <div role="separator" id="sc2_end_sep" aria-labelledby="sc2_end_sep sc2_label" aria-label="End of"></div>
    <h3 id="sc3_label">Link 3</h3>
    <div role="separator" id="sc3_start_sep" aria-labelledby="sc3_start_sep sc3_label" aria-label="Start of"></div>
    <pre><code id="sc3"></code></pre>
    <div role="separator" id="sc3_end_sep" aria-labelledby="sc3_end_sep sc3_label" aria-label="End of"></div>
    <script>
      sourceCode.add('sc1', 'ex1', 'ex1_label', 'css_js_files');
      sourceCode.add('sc2', 'ex2', 'ex2_label', 'css_js_files');
      sourceCode.add('sc3', 'ex3', 'ex3_label', 'css_js_files');
      sourceCode.make();
    </script>
  </section>
  </div>
  <nav>
    <a href="/patterns/link/">Link Design Pattern in WAI-ARIA Authoring Practices 1.2</a>
  </nav>
</div>
        </div>
      
</div>
<script>
  var SkipToConfig = {
    settings: {
      skipTo: {
        displayOption: 'popup',
        attachElement: '#site-header',
        colorTheme: 'aria'
      }
    }
  };
</script>
<script src="/assets/skipto.min.js"></script>
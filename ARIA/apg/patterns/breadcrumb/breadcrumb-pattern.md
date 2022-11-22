---
# This file was generated by scripts/pre-build/library/formatForJekyll.js
title: "Breadcrumb Pattern"
ref: /ARIA/apg/patterns/breadcrumb/

github:
  repository: w3c/aria-practices
  branch: main
  path: content/patterns/breadcrumb/breadcrumb-pattern.html
feedbackmail: public-aria-practices@w3.org
permalink: /ARIA/apg/patterns/breadcrumb/

sidebar: true



# Context here: https://github.com/w3c/wai-aria-practices/issues/31
type_of_guidance: APG

lang: en
---
<meta charset="UTF-8" />
<meta content="width=device-width, initial-scale=1.0" name="viewport" />
<title>Breadcrumb Pattern</title>

<script src="../../shared/js/highlight.pack.js"></script>
<script src="../../shared/js/app.js"></script>
<script src="../../shared/js/skipto.js"></script>


<link 
  rel="stylesheet"
  href="{{ '/content-assets/wai-aria-practices/styles.css' | relative_url }}"
>
<!-- Code highlighting styles -->
<link 
  rel="stylesheet"
  href="{{ '/ARIA/apg/shared/css/github.css' | relative_url }}"
>

<script>
const addBodyClass = undefined;
const enableSidebar = true;
if (addBodyClass) document.body.classList.add(addBodyClass);
if (enableSidebar) document.body.classList.add('has-sidebar');
</script>
    

<script>
    const parentPage = window.location.pathname.match(
      /\/(patterns|practices)\//
    )?.[1];
    if (parentPage) {
      const parentHref = 'a[href*="' + parentPage + '"]';
      document.querySelector(parentHref).classList.add('active');
    }
  </script>
<div>

    <div>
      

      <section id="about">
        <h2>About This Pattern</h2>
        <p>
          A breadcrumb trail consists of a list of links to the parent pages of the current page in hierarchical order.
          It helps users find their place within a website or web application.
          Breadcrumbs are often placed horizontally before a page's main content.
        </p>
      </section>

      <section id="examples" class="examples-section"><img alt="" 
      src="{{ '/content-images/wai-aria-practices/img/breadcrumb.svg' | relative_url }}"
    >
        <h2>Example</h2>
        <p><a href="examples/breadcrumb/">Breadcrumb design pattern example</a></p>
      </section>

      <section id="keyboard_interaction">
        <h2>Keyboard Interaction</h2>
        <p>Not applicable.</p>
      </section>

      <section id="roles_states_properties">
        <h2>WAI-ARIA Roles, States, and Properties</h2>
        <ul>
          <li>Breadcrumb trail is contained within a navigation landmark region.</li>
          <li>The landmark region is labelled via <a href="https://w3c.github.io/aria/#aria-label" class="property-reference">aria-label</a> or <a href="https://w3c.github.io/aria/#aria-labelledby" class="property-reference">aria-labelledby</a>.</li>
          <li>
            The link to the current page has <a href="https://w3c.github.io/aria/#aria-current" class="property-reference">aria-current</a> set to <code>page</code>.
            If the element representing the current page is not a link, aria-current is optional.
          </li>
        </ul>
      </section>
    </div>
  
</div>
<script 
  src="{{ '/ARIA/apg/shared/js/skipto.js' | relative_url }}"
></script>
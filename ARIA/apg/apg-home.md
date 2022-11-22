---
# This file was generated by scripts/pre-build/library/formatForJekyll.js
title: "ARIA Authoring Practices Guide"
ref: /ARIA/apg/

github:
  repository: w3c/aria-practices
  branch: main
  path: content/apg-home.html
feedbackmail: public-aria-practices@w3.org
permalink: /ARIA/apg/

sidebar: false



# Context here: https://github.com/w3c/wai-aria-practices/issues/31
type_of_guidance: APG

lang: en
---


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
    const parentPage = window.location.pathname.match(
      /\/(patterns|practices)\//
    )?.[1];
    if (parentPage) {
      const parentHref = 'a[href*="' + parentPage + '"]';
      document.querySelector(parentHref).classList.add('active');
    }
  </script>
<div>

    <link 
      rel="stylesheet"
      href="{{ '/content-assets/wai-aria-practices/homepage.css' | relative_url }}"
    >
    <div class="off-white-section">
      <div class="contained top-contained margin-fix">
        <div class="top-section">
          <div class="top-box">
            <div class="top-detail-1 detail-1"></div>
            <div class="detail-2"></div>
            <h1>ARIA Authoring Practices Guide (APG) Home</h1>
            <p>
        Learn to use the accessibility semantics defined by the Accessible Rich Internet Application (ARIA) specification to create accessible web experiences.
        This guide describes how to apply accessibility semantics to common design patterns and widgets.
        It provides design patterns and functional examples complemented by in-depth guidance for fundamental practices.
      </p>
            <a href="patterns/" class="button-link button-link-white">View Patterns</a>
          </div>
          <img alt="A laptop screen fills with an accessibility icon and emits a checkmark." src="images/index-1.svg">
        </div>
      </div>
      <div class="detail-3"></div>
      <div class="top-grid-pattern grid-pattern"></div>
    </div>
    <div class="white-section">
      <div class="centered">
        <div class="resource-detail-4 detail-4"></div>
        <h2>APG Resources</h2>
        <p>Building blocks that help you make the web accessible</p>
      </div>
      <div class="contained margin-fix">
        <div class="resource-item">
                <div class="resource-item-content">
                  <h3>Design Patterns and Examples</h3>
                  <p>
                    
            Learn how to make accessible web components and widgets with ARIA roles, states and properties and by implementing keyboard support.
            One or more ways of implementing each pattern is demonstrated with a functional example.
          
                  </p>
                  <a href="patterns/" aria-label="Learn more about APG patterns and examples" class="button-link">Learn More</a>
                </div>
                <div class="resource-item-img">
                  <img alt="A menagerie of widgets." src="images/index-2.svg">
                </div>
              </div><div class="resource-item">
                <div class="resource-item-content">
                  <h3>Use ARIA Landmarks</h3>
                  <p>
                    Learn how to use HTML sectioning elements and ARIA landmark roles to make it easy for assistive technology users to understand the meaning of the layout of a page.
                  </p>
                  <a href="practices/landmark-regions/" aria-label="Learn more about ARIA landmarks" class="button-link">Learn More</a>
                </div>
                <div class="resource-item-img">
                  <img alt="A document flies apart into chunks." src="images/index-3.svg">
                </div>
              </div><div class="resource-item">
                <div class="resource-item-content">
                  <h3>Providing Accessible Names and Descriptions</h3>
                  <p>
                    Providing elements with accessible names and, where appropriate, accessible descriptions is one of the most important responsibilities authors have when developing accessible web experiences.
                  </p>
                  <a href="practices/names-and-descriptions/" aria-label="Learn more about accessible names and descriptions" class="button-link">Learn More</a>
                </div>
                <div class="resource-item-img">
                  <img alt="Indicators delve inside a document." src="images/index-4.svg">
                </div>
              </div><div class="resource-item">
                <div class="resource-item-content">
                  <h3>And So Much More...</h3>
                  <p>
                    Learn about other fundamental practices related to correctly using accessibility semantics, developing keyboard interfaces, and more.
                  </p>
                  <a class="button-link" href="practices/" aria-label="Learn more about APG practices">Learn More</a>
                </div>
                <div class="resource-item-img">
                  <img alt="A box with an accessibility label is chock full of widgets and document bits." src="images/index-5.svg">
                </div>
              </div>
      </div>
      <div class="collaboration-grid-pattern grid-pattern"></div>
    </div>
    <div class="white-section">
      <div class="centered margin-fix">
        <h2 class="collaboration-h2">
          Get Involved
        </h2>
        <p class="collaboration-p">
          
        The APG Task Force relies on broad community representation and participation to continuously improve the usefulness and quality of the APG.
        There are a variety of ways you can get involved and help promote development of accessible experiences.
      
        </p>
      </div>
      <div class="collaboration-items">
        
                  <div class="collaboration-item">
                    <img alt="An icon showing three nodes connecting." src="images/index-6.svg">
                    <h3>Join the Task Force</h3>
                    <p>
            To join the APG Task Force, individuals need to first join the W3C ARIA Working Group.
            Participants are expected to actively contribute to the work of the task force.
          </p>
                    <a rel="noopener noreferrer" target="_blank" href="https://www.w3.org/WAI/ARIA/task-forces/practices/">Learn more about the work of the task force and how to join</a>
                  </div>
                
                  <div class="collaboration-item">
                    <img alt="An icon showing two human shapes carrying a burden." src="images/index-7.svg">
                    <h3>Contribute via GitHub</h3>
                    <p>
            Many valuable contributions are made by people who find or raise issues of interest in our GitHub repository and then submit proposed changes via a GitHub pull request.
            If you choose this path, please start by studying our guidelines for contributing to the repository and maintaining code quality.
          </p>
                    <a rel="noopener noreferrer" target="_blank" href="https://github.com/w3c/aria-practices">View ReadMe in the GitHub repository</a>
                  </div>
                

        <div class="collaboration-item mailing-list-item">
          <div class="collaboration-detail-4 detail-4"></div>
          <img alt="A notification bell icon appears over an email icon." src="images/index-8.svg">
          <div>
            <h3>Mailing Lists</h3>
            <p>
            The APG Task Force uses the public aria-practices mailing list for email discussion.
            Meeting announcements, agendas, and links to minutes are sent to the mailing list.
            While GitHub issues are the preferred place to discuss APG content, the mailing list is available to anyone who would prefer to communicate with the APG Task Force via email.
          </p><p><a rel="noopener noreferrer" target="_blank" href="https://lists.w3.org/Archives/Public/public-aria-practices/">View the aria-practices mailing list archive</a></p>
          </div>
        </div>
      </div>
      <div class="bottom-grid-pattern grid-pattern"></div>
    </div>
    <div class="bottom-off-white-section off-white-section"></div>
  
</div>
<script 
  src="{{ '/ARIA/apg/shared/js/skipto.js' | relative_url }}"
></script>
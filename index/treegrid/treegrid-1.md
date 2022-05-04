---
# This is a generated file
title: "Treegrid Email Inbox Example"
ref: /aria-practices/

github:
  repository: w3c/aria-practices
  path: aria-practices.html
permalink: /index/treegrid/treegrid-1

lang: en
---
<script src="../js/examples.js"></script>
<script src="../js/highlight.pack.js"></script>
<script src="../js/app.js"></script>

<link href="css/treegrid-1.css" rel="stylesheet" />
<style>
  /* Style the current cell focus option so user know what they're getting */
  [aria-current] {
    position: relative;
    outline: 2px solid green;
    outline-offset: 3px;
    background-color: #fffff8;
  }
  [aria-current] > a::before {
    display: inline-block;
    position: absolute;
    content: "Current";
    font-size: 80%;
    right: -3px;
    top: -3px;
    padding: 3px 1ch;
    background-color: green;
    color: white;
    font-weight: bold;
  }
</style>
<script src="js/treegrid-1.js" type="text/javascript"></script>


<link rel="stylesheet" href="/assets/styles.css">
<!-- Code highlighting styles -->
<link rel="stylesheet" href="/index/css/github.css">

<div>

        <div class="sidebar-container">
          <aside class="sidebar-left" aria-describedby="sidebar-toc">
            <h2 id="sidebar-toc" class="sidebar-headline">Table of Contents</h2>
            <ul class="sidebar-list">
              
                    <li>
                      <a href="#example-usage-options">Example Usage Options</a>
                    </li>
                   
                    <li>
                      <a href="#ex_label">Example</a>
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
                      <a href="#sc1_label">HTML Source Code</a>
                    </li>
                  
            </ul>
            
    <ul class="sidebar-list sidebar-list-yellow">
      <li><a href="/about/#browser_and_AT_support">Browser and Assistive Technology Support</a></li>
      <li><a href="https://github.com/w3c/aria-practices/issues/new">Report Issue</a></li>
      <li><a href="https://github.com/w3c/aria-practices/projects/17">Related Issues</a></li>
      <li><a href="/patterns/treegrid/">Treegrid Design Pattern</a></li>
    </ul>

          </aside>
          <div class="sidebar-right"><h2 class="followed-by-support-notice">About This Example</h2><img alt=""
        src="/assets/img/treegrid.svg"
        class="example-page-example-icon"
      >
  
  <div>
  
  <p>
    <strong>NOTE:</strong> This example is new in APG 1.1 release 2.
    Please provide feedback in
    <a href="https://github.com/w3c/aria-practices/issues/790">issue 790.</a>
  </p>
  <p>
    The following example demonstrates how the
    <a href="/patterns/treegrid/">treegrid design pattern</a>
    can be used to make an interactive tree that enables users to both navigate the hierarchical structure of email conversations
    and also navigate elements that describe each email, such as subject and sender.
  </p>
  <p>Similar examples include: </p>
  <ul>
    <li><a href="../grid/dataGrids.html">Data Grid Examples</a>: Three example implementations of grid that include features relevant to presenting tabular information, such as content editing, sort, and column hiding.</li>
    <li><a href="../treeview/treeview-1/treeview-1a.html">File Directory Treeview using <em>computed</em> properties</a></li>
    <li><a href="../treeview/treeview-1/treeview-1b.html">File Directory Treeview using <em>declared</em> properties</a></li>
    <li><a href="../treeview/treeview-2/treeview-2a.html">Navigation Treeview using <em>computed</em> properties</a></li>
    <li><a href="../treeview/treeview-2/treeview-2b.html">Navigation Treeview using <em>declared</em> properties</a></li>
  </ul>
  <h2 tabindex="-1" id="example-usage-options">Example Usage Options</h2>
  <p>
    This example demonstrates three different ways of implementing the keyboard navigation specified in the treegrid pattern.
    The following links change the behavior of the navigation keys :
  </p>
  <ul>
    <li id="option-cell-focus-allow">
      <a href="treegrid-1.html">Rows are focused first, but cells can be focused</a>:<br>
      Useful when the desired experience is for the treegrid to act primarily like a tree where each row is treated like a node in a tree,
      but it is still possible for users to navigate across the cells in a row.
    </li>
    <li id="option-cell-focus-start">
      <a href="treegrid-1.html?cell=start">Cells are focused first, but rows can be focused</a>:<br>
      Useful when the desired experience is for the treegrid to act primarily like a grid where arrow keys move among cells,
      but it is still possible for users to focus a row and then start navigating the structure like a tree.
    </li>
    <li id="option-cell-focus-force">
      <a href="treegrid-1.html?cell=force">Only cells can be focused</a>:<br>
      Useful when the desired experience is that the treegrid act primarily like a grid and there is no need to focus complete rows.
    </li>
  </ul>
  <p>
    Note: A row-only option is not provided.
    A treegrid where cells cannot be focused would be implemented as a <a href="/patterns/treeview/">tree view</a>.
    A treeview that has columns in its visual presentation may be appropriate when all the following conditions are present:
  </p>
  <ul>
    <li>Columns are guaranteed to fit horizontally (no horizontal scrolling necessary).</li>
    <li>Columns are merely for attractive presentation; there is no need to navigate them individually.</li>
    <li>A screen reader user can easily understand the UI when all information in a row is announced as a single string without any separation.</li>
  </ul>
  <section>
    <div class="example-header">
      <h2 id="ex_label" tabindex="-1">Example</h2>
    </div>
    <div role="separator" id="ex_start_sep" aria-labelledby="ex_start_sep ex_label" aria-label="Start of"></div>
    
    <div id="ex1">
      <div class="table-wrap"><table id="treegrid" role="treegrid" aria-label="Inbox">
        <colgroup>
          <col id="treegrid-col1">
          <col id="treegrid-col2">
          <col id="treegrid-col3">
        </colgroup>
        <thead>
          <tr>
            <th scope="col">Subject</th>
            <th scope="col">Summary</th>
            <th scope="col">Email</th>
          </tr>
        </thead>
        <tbody>
          <tr role="row" aria-level="1" aria-posinset="1" aria-setsize="1" aria-expanded="true">
            <td role="gridcell">Treegrids are awesome</td>
            <td role="gridcell">Want to learn how to use them?</td>
            <td role="gridcell"><a href="mailto:aaron@thegoogle.rocks">aaron@thegoogle.rocks</a></td>
          </tr>
          <tr role="row" aria-level="2" aria-posinset="1" aria-setsize="3">
             <td role="gridcell">re: Treegrids are awesome</td>
             <td role="gridcell">I agree with you, they are the shizzle</td>
             <td role="gridcell"><a href="mailto:joe@blahblahblah.blahblah">joe@blahblahblah.blahblah</a></td>
          </tr>
          <tr role="row" aria-level="2" aria-posinset="2" aria-setsize="3" aria-expanded="false">
             <td role="gridcell">re: Treegrids are awesome</td>
             <td role="gridcell">They are great for showing a lot of data, like a grid</td>
             <td role="gridcell"><a href="mailto:billy@dangerous.fish">billy@dangerous.fish</a></td>
          </tr>
          <tr role="row" aria-level="3" aria-posinset="1" aria-setsize="1" class="hidden">
             <td role="gridcell">re: Treegrids are awesome</td>
             <td role="gridcell">Cool, we've been needing an example and documentation</td>
             <td role="gridcell"><a href="mailto:doris@rufflazydogs.sleep">doris@rufflazydogs.sleep</a></td>
          </tr>
          <tr role="row" aria-level="2" aria-posinset="3" aria-setsize="3" aria-expanded="false">
             <td role="gridcell">re: Treegrids are awesome</td>
             <td role="gridcell">I hear the Fancytree library is going to align with this example!</td>
             <td role="gridcell"><a href="mailto:someone@please-do-it.company">someone@please-do-it.company</a></td>
          </tr>
          <tr role="row" aria-level="3" aria-posinset="1" aria-setsize="1" aria-expanded="false" class="hidden">
             <td role="gridcell">re: Treegrids are awesome</td>
             <td role="gridcell">Sometimes they are more like trees, others are more like grids</td>
             <td role="gridcell"><a href="mailto:mari@beingpractical.com">mari@beingpractical.com</a></td>
          </tr>
          <tr role="row" aria-level="4" aria-posinset="1" aria-setsize="2" class="hidden">
             <td role="gridcell">re: Treegrids are awesome</td>
             <td role="gridcell">Cool, when it's a tree, let's keep left/right to collapse/expand</td>
             <td role="gridcell"><a href="mailto:issie@imadeadcatsadly.wascute">issie@imadeadcatsadly.wascute</a></td>
          </tr>
          <tr role="row" aria-level="4" aria-posinset="2" aria-setsize="2" class="hidden">
             <td role="gridcell">re: Treegrids are awesome</td>
             <td role="gridcell">I see, sometimes right arrow moves by column</td>
             <td role="gridcell"><a href="mailto:kitten@kittenseason.future">kitten@kittenseason.future</a></td>
          </tr>
        </tbody>
      </table></div>
    </div>

    <div role="separator" id="ex_end_sep" aria-labelledby="ex_end_sep ex_label" aria-label="End of"></div>

  </section>

  <section>
    <h2 id="kbd_label" tabindex="-1">Keyboard Support</h2>
    <p>
      <strong>NOTE:</strong> The following table includes descriptions of how keyboard commands move focus among cells and rows in the treegrid implementation on this page.
      In the example on this page, some cells contain a single focusable widget, and if a cell contains a widget, the cell is not focusable; the widget receives focus instead of the cell.
      So, when a keyboard command description says a command moves focus to a cell, the command may either focus the cell or a widget inside the cell.
    </p>
     <div class="table-wrap"><table aria-labelledby="kbd_label" class="def">
      <thead>
        <tr>
          <th>Key</th>
          <th>Function</th>
        </tr>
      </thead>
      <tbody>
      <tr data-test-id="key-right-arrow">
        <th scope="row">
          <kbd>Right Arrow</kbd>
        </th>
        <td>
          <ul>
            <li>If a row is focused, and it is collapsed, expands the current row.</li>
            <li>If a row is focused, and it is expanded, focuses the first cell in the row.</li>
            <li>If a cell is focused, moves one cell to the right.</li>
            <li>If focus is on the right most cell, focus does not move.</li>
          </ul>
        </td>
      </tr>
      <tr data-test-id="key-left-arrow">
        <th scope="row">
          <kbd>Left Arrow</kbd>
        </th>
        <td>
          <ul>
            <li>If a row is focused, and it is expanded, collapses the current row.</li>
            <li>If a row is focused, and it is collapsed, moves to the parent row (if there is one).</li>
            <li>If a cell in the first column is focused, focuses the row.</li>
            <li>If a cell in a different column is focused, moves focus one cell to the left.</li>
          </ul>
        </td>
      </tr>
      <tr data-test-id="key-down-arrow">
        <th scope="row">
          <kbd>Down Arrow</kbd>
        </th>
        <td>
          <ul>
            <li>Moves focus one row or one cell down, depending on whether a row or cell is currently focused.</li>
            <li>If focus is on the bottom row, focus does not move.</li>
          </ul>
        </td>
      </tr>
      <tr data-test-id="key-up-arrow">
        <th scope="row">
          <kbd>Up Arrow</kbd>
        </th>
        <td>
          <ul>
            <li>Moves focus one row or one cell up, depending on whether a row or cell is currently focused.</li>
            <li>If focus is on the top row, focus does not move.</li>
          </ul>
        </td>
      </tr>
      <tr data-test-id="key-tab">
        <th scope="row">
          <kbd>Tab</kbd>
        </th>
        <td>
          <ul>
            <li>Moves focus to the next interactive widget in the current row.</li>
            <li>If there are no more interactive widgets in the current row, moves focus out of the treegrid.</li>
          </ul>
        </td>
      </tr>
      <tr data-test-id="key-shift-tab">
        <th scope="row">
          <kbd>Shift + Tab</kbd>
        </th>
        <td>
          <ul>
            <li>If a cell is focused, moves focus to the previous interactive widget in the current row.</li>
            <li>If a row is focused, moves focus out of the treegrid.</li>
          </ul>
        </td>
      </tr>
      <tr data-test-id="key-home">
        <th scope="row">
          <kbd>Home</kbd>
        </th>
        <td>
          <ul>
            <li>If a row is focused, moves to the first row.</li>
            <li>If a cell is focused, moves focus to the first cell in the row containing focus.</li>
          </ul>
        </td>
      </tr>
      <tr data-test-id="key-end">
        <th scope="row">
          <kbd>End</kbd>
        </th>
        <td>
          <ul>
            <li>If a row is focused, moves to the last row.</li>
            <li>If a cell is focused, moves focus to the last cell in the row containing focus.</li>
          </ul>
        </td>
      </tr>
      <tr data-test-id="key-control-home">
        <th scope="row">
          <kbd>Control + Home</kbd>
        </th>
        <td>
          <ul>
            <li>If a row has focus, moves focus to the first row.</li>
            <li>If a cell has focus, moves focus to the cell in the first row in the same column as the cell that had focus.</li>
          </ul>
        </td>
      </tr>
      <tr data-test-id="key-control-end">
        <th scope="row">
          <kbd>Control + End</kbd>
        </th>
        <td>
          <ul>
            <li>If a row has focus, moves focus to the last row.</li>
            <li>If a cell has focus, moves focus to the cell in the last row in the same column as the cell that had focus.</li>
          </ul>
        </td>
      </tr>
      <tr data-test-id="key-enter">
        <th scope="row">
          <kbd>Enter</kbd>
        </th>
        <td>
          <ul>
            <li>Performs default action associated with row or cell that has focus, e.g. opens message or navigate to link.</li>
            <li>If focus is on the cell with the expand/collapse button, and there is no other action, will toggle expansion of the current row.</li>
          </ul>
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
        <tr data-test-id="treegrid-role">
          <th scope="row"><code>treegrid</code></th>
          <td></td>
          <td><code>table</code></td>
          <td>Identifies the element as a <code>treegrid</code>.</td>
        </tr>
        <tr data-test-id="treegrid-aria-label">
          <td>
          </td>
          <th scope="row"><code>aria-label="Inbox"</code></th>
          <td><code>table</code></td>
          <td>Provides an accessible name for the <code>treegrid</code>.</td>
        </tr>
        <tr data-test-id="row-role">
          <th scope="row"><code>row</code></th>
          <td></td>
          <td><code>tr</code></td>
          <td>
            <ul>
              <li>Identifies the element as a <code>row</code>.</li>
              <li>The <code>row</code> role is not an implicit semantic for the <code>tr</code> element when in a <code>treegrid</code>.</li>
            </ul>
          </td>
        </tr>
        <tr data-test-id="row-tabindex">
          <td></td>
          <th scope="row"><code>tabindex="-1"</code></th>
          <td><code>tr</code> or <code>td</code></td>
          <td>
            <ul>
              <li>Makes the element focusable without including it in the tab sequence of the page.</li>
              <li>All <code>row</code> and <code>gridcell</code> elements are focusable, but only one is included in the tab sequence.</li>
             </ul>
          </td>
        </tr>
        <tr data-test-id="row-tabindex">
          <td></td>
          <th scope="row"><code>tabindex="0"</code></th>
          <td><code>tr</code> or <code>td</code></td>
          <td>
            <ul>
              <li>Includes the element in the tab sequence.</li>
              <li>Only one <code>row</code> or <code>gridcell</code> in the <code>treegrid</code> has <code>tabindex=&quot;0&quot;</code>.</li>
              <li>In this implementation, the first <code>row</code> in the <code>treegrid</code> is included in the tab sequence when the page loads.</li>
              <li>
                When the user moves focus in the <code>treegrid</code>, the element included in the tab sequence changes to the element with focus as described in the section on
                <a href="/fundamentals/keyboard-interface/#kbd_roving_tabindex">roving tabindex.</a>
              </li>
             </ul>
          </td>
        </tr>
        <tr data-test-id="row-aria-expanded">
          <td>
          </td>
          <th scope="row"><code>aria-expanded="false"</code></th>
          <td><code>tr</code> or <code>td</code></td>
          <td>
            <ul>
              <li>Applied only to parent row or first cell of parent row, i.e., next set of rows are responses to the message in this row</li>
              <li>Indicates the parent row is closed, i.e., the descendant rows are not visible.</li>
              <li>The visual indication of the collapsed state is synchronized by a CSS attribute selector.</li>
              <li>When the treegrid is configured to support focus on rows <code>aria-expanded</code> is on the <code>tr</code> elements, but when the treegrid is configured to support focus on cells only, <code>aria-expanded</code> is on the first <code>td</code> element contained in each row.</li>
            </ul>
          </td>
        </tr>
        <tr data-test-id="row-aria-expanded">
          <td>
          </td>
          <th scope="row"><code>aria-expanded="true"</code></th>
          <td><code>tr</code> or <code>td</code></td>
          <td>
            <ul>
              <li>Applied only to parent rows or the first cell in parent rows, i.e., next set of rows are responses to the message in this row</li>
              <li>Indicates the parent row is open, i.e., the descendant rows are visible.</li>
              <li>The visual indication of the open state is synchronized by a CSS attribute selector.</li>
              <li>When the treegrid is configured to support focus on rows <code>aria-expanded</code> is on the <code>tr</code> elements, but when the treegrid is configured to support focus on cells only, <code>aria-expanded</code> is on the first <code>td</code> element contained in each row.</li>
            </ul>
          </td>
        </tr>
        <tr data-test-id="row-aria-level">
          <td>
          </td>
          <th scope="row"><code>aria-level="<em>number</em>"</code></th>
          <td><code>tr</code></td>
          <td>
            <ul>
              <li>Defines the level of the row in the hierarchical treegrid structure.</li>
              <li>Counting is one-based.</li>
              <li>Root rows have aria-level=“1”.</li>
            </ul>
          </td>
        </tr>
        <tr data-test-id="row-aria-setsize">
          <td>
          </td>
          <th scope="row"><code>aria-setsize="<em>number</em>"</code></th>
          <td><code>tr</code></td>
          <td>
            Defines the number of rows in the set of rows that are in the same branch and at the same level within the hierarchy.
          </td>
        </tr>
        <tr data-test-id="row-aria-posinset">
          <td>
          </td>
          <th scope="row"><code>aria-posinset="<em>number</em>"</code></th>
          <td><code>tr</code></td>
          <td>
            <ul>
              <li>Defines the position of the row within the set of other rows that are in the same branch and at the same level within the hierarchy.</li>
              <li>Counting is one-based, not zero-based.</li>
            </ul>
          </td>
        </tr>
        <tr data-test-id="gridcell-role">
          <th scope="row"><code>gridcell</code></th>
          <td></td>
          <td><code>td</code></td>
          <td>
            <ul>
              <li>Identifies the element as a <code>gridcell</code>.</li>
              <li>The <code>gridcell</code> role is not an implicit semantic for the <code>td</code> element when in a <code>treegrid</code>.</li>
            </ul>
          </td>
        </tr>
              </tbody>
    </table></div>
    <p>
      <strong>NOTE:</strong> Due to an error in the ARIA 1.1 specification, the <code>aria-posinset</code> and <code>aria-setsize</code> properties are not supported on row elements.
      This is being corrected in ARIA 1.2.
      Consequently, when validating the HTML in this example, errors are generated.
    </p>
  </section>

  <section>
    <h2 tabindex="-1" id="javascript-and-css-source-code">Javascript and CSS Source Code</h2>
    
    <ul id="css_js_files">
      <li>
        CSS:
        <a href="css/treegrid-1.css" type="text/css">treegrid-1.css</a>
      </li>
      <li>
        Javascript:
        <a href="js/treegrid-1.js" type="text/javascript">treegrid-1.js</a>
      </li>
    </ul>
  </section>

  <section>
    <h2 id="sc1_label" tabindex="-1">HTML Source Code</h2>
    <div role="separator" id="sc1_start_sep" aria-labelledby="sc1_start_sep sc1_label" aria-label="Start of"></div>
    <pre><code id="sc1"></code></pre>
    <div role="separator" id="sc1_end_sep" aria-labelledby="sc1_end_sep sc1_label" aria-label="End of"></div>
    
    <script>
      sourceCode.add('sc1', 'ex1', 'ex_label', 'css_js_files');
      sourceCode.make();
    </script>
  </section>
  </div>
  <nav>
    
    <a href="/patterns/treegrid/">Treegrid Design Pattern in WAI-ARIA Authoring Practices 1.2</a>
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
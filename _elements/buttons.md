---
layout: styleguide
type: element
title: Buttons
lead: Use buttons to signal actions. 
---

<div class="preview">

  <h6>Orange Primary Buttons</h6>
  <div class="button_wrapper">
    <button class="fd-button-orange">Default</button>
    <button class="fd-button-orange fd-button-orange-active">Active</button>
    <button class="fd-button-orange fd-button-orange-hover">Hover</button>
  </div>

  <h6>Green Primary Buttons</h6>
  <div class="button_wrapper">
    <button class="fd-button-green">Default</button>
    <button class="fd-button-green fd-button-green-active">Active</button>
    <button class="fd-button-green fd-button-green-hover">Hover</button>
  </div>

  <h6>Button Focus</h6>
  <div class="button_wrapper">
    <button class="fd-button-green fd-button-focus">Default</button>
  </div>

  <h6>Disabled Button</h6>
  <div class="button_wrapper">
    <button class="fd-button-disabled">Default</button>
  </div>

  <h6>Button Sizes</h6>
  <div class="button_wrapper">
    <button class="fd-button-small fd-button-green">Small</button>
    <button class="fd-button-green">Medium</button>
    <button class="fd-button-large fd-button-green">Large</button>
  </div> 
</div>

<div class="css-preview">

<style type="text/css">

  /* Basic Button Styles */
  button,
  button:visited{
    display: inline-block;
    appearance: none;
    border: 0;
    border-radius: 3px;
    color: #ffffff;
    cursor: pointer;
    display: inline-block;
    font-size: 14px;
    font-weight: bold;
    font-family: verdana;
    line-height: 1;
    margin: .5em;
    outline: none;
    padding: 10px 20px;
    text-align: center;
    text-decoration: none;
    width: auto;
    -webkit-font-smoothing: antialiased;  
  }

  /* Button Sizes */
  .fd-button-large{
    font-size: 16px;
    padding: 15px 30px;
  }
  .fd-button-small{
    font-size: 12px;
    padding: 7px 14px;
  }  

  /* Other Button States */
  .fd-button-focus,
  button:focus{
    box-shadow: 0 0 6px #666666;
  }

  .fd-button-disabled{
    background-color: #d6d7d9;
    color: #666666;  
  }

  /* Green Button: Default, Hover, Active */
  .fd-button-green{
    background-color: #4fa157;  
  }
  .fd-button-green-hover,
  .fd-button-green:hover{
    background-color: #458d4e;
  }
  .fd-button-green-active,
  .fd-button-green:active{
    background-color: #3a7741;
  }

  /* Orange Button: Default, Hover, Active */
  .fd-button-orange{
    background-color: #ffba53;
    color: #3c2400;
  }
  .fd-button-orange-hover,
  .fd-button-orange:hover{
    background-color: #ffa113;
  }
  .fd-button-orange-active,
  .fd-button-orange:active{
    background-color: #ed8f00;
  }

  /* Alt Orange Button: Default, Hover, Active */
  .fd-button-orange-alt{
    background-color: #f59300;
    color: #ffffff;
  }
  .fd-button-orange-alt-hover,
  .fd-button-orange-alt:hover{
    background-color: #ffa113;
  }
  .fd-button-orange-alt-active,
  .fd-button-orange-alt:active{
    background-color: #de8600;
  }

</style>

</div>


<div class="usa-accordion-bordered usa-accordion-docs">
  <button class="usa-button-unstyled usa-accordion-button"
      aria-expanded="true" aria-controls="collapsible-0">
    Documentation
  </button>
  <div id="collapsible-0" aria-hidden="false" class="usa-accordion-content">
    <!-- <h4 class="usa-heading">Implementation</h4>
    <p>The examples demonstrate how to use button elements. To use a button style on an anchor link, add the <code>usa-button</code> class to your anchor link. 
    <p>To use a different style button on your anchor link, add the special button class in addition to <code>usa-button</code>:</p>
    <ul>
      <li><code>usa-button-primary-alt</code></li>
      <li><code>usa-button-secondary</code></li>
      <li><code>usa-button-gray</code></li>
      <li><code>usa-button-outline</code></li>
      <li><code>usa-button-outline-inverse</code></li>
      <li><code>usa-button-disabled</code></li>
      <li><code>usa-button-big</code></li>
    </ul>
    <p>For example, a secondary button style would use the following code:
    <code>&lt;a class="usa-button usa-button-secondary" href="/my-link"&gt;My button&lt;/a&gt;</code></p> -->
    <h4 class="usa-heading">Accessibility</h4>
    <ul class="usa-content-list">
      <li>Use <em class="em-yellow-bg"><code>&lt;button&gt;</code></em> tags to create buttons</li>
      <li>Buttons should display a visible focus state when users tab to them.</li>
      <li>Avoid using <em class="em-yellow-bg"><code>&lt;div&gt;</code></em> or <em class="em-yellow-bg"><code>&lt;img&gt;</code></em> tags to create buttons. Screen readers don't automatically know either is an usable button.</li>
      <li>When styling links to look like buttons, remember that screen readers handle links slightly differently than they do buttons. Pressing the Space key triggers a button, but pressing the Enter key triggers a link.</li>
    </ul>
    <!-- <h4 class="usa-heading">Usability</h4>
    <h5>When to use</h5>
    <ul class="usa-content-list">
      <li>Use buttons for the most important actions you want users to take on your site, such as "download," "sign up," or "log out."</li>
    </ul>
    <h5>When to consider something else</h5>
    <ul class="usa-content-list">
      <li>If you want to lead users between pages of a website. Use links instead.</li>
      <li>Less popular or less important actions may be visually styled as links.</li>
    </ul>
    <h5>Guidance</h5>
    <ul class="usa-content-list">
      <li>Generally, use primary buttons for actions that go to the next step and use secondary buttons for actions that happen on the current page.</li>
      <li>Style the button most users should click in a way that distinguishes from other buttons on the page. Try using the  “large button” or the most visually distinct fill color.</li>
      <li>Make sure buttons should look clickable—use color variations to distinguish static, hover and active states.</li>
      <li>Avoid using too many buttons on a page.</li>
      <li>Use sentence case for button labels. </li>
      <li>Button labels should be as short as possible with “trigger words” that your users will recognize to clearly explain what will happen when the button is clicked (for example, “download,” “view” or “sign up”).</li>
      <li>Make the first word of the button’s label a verb. For example, instead of “Complaint Filing” label the button “File a complaint.”</li>
      <li>At times, consider adding an icon to signal specific actions (“download”, “open in a new window”, etc). </li>
    </ul> -->
  </div>
</div>

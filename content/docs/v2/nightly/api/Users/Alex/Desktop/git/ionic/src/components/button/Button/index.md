---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "button"
title: "Button"
header_sub_title: "Ionic API Documentation"
doc: "Button"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/src/button/basic"
angular_controller: APIDemoCtrl 
---









<h1 class="api-title">
<a class="anchor" name="button" href="#button"></a>

Button
<h3><code>[ion-button]</code></h3>






</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/components/button/button.ts#L4">
Improve this doc
</a>






<p>Buttons are simple components that are optimized to handle touch
events on mobile. Buttons can contain text and icons, and can 
be customized with one or more input properties. For a complete list of
input properties, see <a href="#input-properties">Input Properties</a> below.</p>
<p>To use the Button component, add the <code>ion-button</code> directive to an
HTML <code>&lt;button&gt;</code>.</p>




<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<pre><code class="lang-html">&lt;!-- Basic button --&gt;
&lt;button ion-button&gt;Default&lt;/button&gt;

&lt;!-- Custom Color --&gt;
&lt;button ion-button ion-color color=&quot;secondary&quot;&gt;Secondary&lt;/button&gt;

&lt;!-- Shapes --&gt;
&lt;button ion-button full&gt;Full Button&lt;/button&gt;

&lt;button ion-button block&gt;Block Button&lt;/button&gt;

&lt;button ion-button round&gt;Round Button&lt;/button&gt;

&lt;!-- Outline --&gt;
&lt;button ion-button full outline&gt;Outline + Full&lt;/button&gt;

&lt;!-- Sizes --&gt;
&lt;button ion-button large&gt;Large&lt;/button&gt;

&lt;button ion-button&gt;Default&lt;/button&gt;

&lt;button ion-button small&gt;Small&lt;/button&gt;
</code></pre>
<h3 id="styling-buttons-dynamically">Styling Buttons Dynamically</h3>
<p>All of the <a href="#input-properties">input properties</a> that determine a buttons appearance can be 
set dynamically by binding them to a value on the component&#39;s model. For example, most attributes
can be toggled by binding them to a <code>boolean</code> value on the model:</p>
<pre><code class="lang-html">&lt;!-- Dynamically set rounded corners --&gt;
&lt;button ion-button [round]=&quot;isRound&quot;&gt;Round Button&lt;/button&gt;

&lt;!-- Dynamically set clear background --&gt;
&lt;button ion-button [clear]=&quot;isClear&quot;&gt;Clear Button&lt;/button&gt;
</code></pre>
<p>To set the color of a button, bind the <code>color</code> property to a value on the model
of the component. Any string that corresponds to a Sass variable defined in your 
<a href="/docs/v2/theming/theming-your-app/">$color map</a> is valid for the <code>color</code> property.  </p>
<pre><code class="lang-html">&lt;!-- Bind the color to a variable --&gt;
&lt;button ion-button ion-color [color]=&quot;isDanger&quot;&gt;
  Dangerous?
&lt;/button&gt;

&lt;!-- Bind the color to a ternary expression --&gt;
&lt;button ion-button ion-color [color]=&quot;isDanger ? &#39;danger&#39; : &#39;primary&#39;&quot;&gt;
  Also Dangerous?
&lt;/button&gt;
</code></pre>
<h2 id="common-usage-patterns">Common Usage Patterns</h2>
<h3 id="using-icons-in-buttons">Using Icons in Buttons</h3>
<p>To add icons to a button, add an <code>ion-icon</code> component inside of it and either the <code>icon-left</code>
or <code>icon-right</code> position attribute. If you want a button with only an icon in it, you can also
use the <code>icon-only</code> attribute, which will increase the size of the icon to better fill the button:</p>
<pre><code class="lang-html">&lt;!-- Float the icon left --&gt;
&lt;button ion-button icon-left&gt;
  &lt;ion-icon name=&quot;home&quot;&gt;&lt;/ion-icon&gt;
  Left Icon
&lt;/button&gt;

&lt;!-- Float the icon right --&gt;
&lt;button ion-button icon-right&gt;
  Right Icon
  &lt;ion-icon name=&quot;home&quot;&gt;&lt;/ion-icon&gt;
&lt;/button&gt;

&lt;!-- Only icon (no text) --&gt;
&lt;button ion-button icon-only&gt;
  &lt;ion-icon name=&quot;home&quot;&gt;&lt;/ion-icon&gt;
&lt;/button&gt;
</code></pre>
<h3 id="using-buttons-in-components">Using Buttons In Components</h3>
<p>Although buttons can be used on their own, they can easily be used within other components. 
For example, the following positions buttons on the left and right side of the navbar:</p>
<pre><code class="lang-html">&lt;ion-header&gt;
  &lt;ion-navbar&gt;
    &lt;ion-buttons start&gt;
      &lt;button ion-button icon-only&gt;
        &lt;ion-icon name=&quot;contact&quot;&gt;&lt;/ion-icon&gt;
      &lt;/button&gt;
    &lt;/ion-buttons&gt;

    &lt;ion-buttons end&gt;
      &lt;button ion-button icon-only&gt;
        &lt;ion-icon name=&quot;search&quot;&gt;&lt;/ion-icon&gt;
      &lt;/button&gt;
    &lt;/ion-buttons&gt;
  &lt;/ion-navbar&gt;
&lt;/ion-header&gt;
</code></pre>
<p>Similarly, the following positions a button on the right side of a list item:</p>
<pre><code class="lang-html">&lt;ion-list&gt;
  &lt;ion-item&gt;
    Left Icon Button
    &lt;button ion-button outline item-right icon-left&gt;
      &lt;ion-icon name=&quot;star&quot;&gt;&lt;/ion-icon&gt;
      Left Icon
    &lt;/button&gt;
  &lt;/ion-item&gt;
&lt;/ion-list&gt;
</code></pre>




<!-- @property tags -->



<!-- instance methods on the class -->
<!-- input methods on the class -->
<h2><a class="anchor" name="input-properties" href="#input-properties"></a>Input Properties</h2>
<table class="table param-table" style="margin:0;">
  <thead>
    <tr>
      <th>Attr</th>
      <th>Type</th>
      <th>Details</th>
    </tr>
  </thead>
  <tbody>
    
    <tr>
      <td>large</td>
      <td><code>boolean</code></td>
      <td><p> Whether the button should be larger.</p>
</td>
    </tr>
    
    <tr>
      <td>small</td>
      <td><code>boolean</code></td>
      <td><p> Whether the button should be smaller.</p>
</td>
    </tr>
    
    <tr>
      <td>default</td>
      <td><code>boolean</code></td>
      <td><p> Whether the button should be the default size.</p>
</td>
    </tr>
    
    <tr>
      <td>outline</td>
      <td><code>boolean</code></td>
      <td><p> Whether the button should be button transparent with a border.</p>
</td>
    </tr>
    
    <tr>
      <td>clear</td>
      <td><code>boolean</code></td>
      <td><p> Whether the button should be transparent without a border.</p>
</td>
    </tr>
    
    <tr>
      <td>solid</td>
      <td><code>boolean</code></td>
      <td><p> Whether the button should be solid. Useful for buttons within an item.</p>
</td>
    </tr>
    
    <tr>
      <td>round</td>
      <td><code>boolean</code></td>
      <td><p> Whether the button should have rounded corners.</p>
</td>
    </tr>
    
    <tr>
      <td>block</td>
      <td><code>boolean</code></td>
      <td><p> Whether the button should fill its parent container with a border-radius.</p>
</td>
    </tr>
    
    <tr>
      <td>full</td>
      <td><code>boolean</code></td>
      <td><p> Whether the button should fill its parent container. Button will have no border-radius or left/right borders.</p>
</td>
    </tr>
    
    <tr>
      <td>strong</td>
      <td><code>boolean</code></td>
      <td><p> Whether the button should have a strong visual appearance, ie. it represents an important action.</p>
</td>
    </tr>
    
    <tr>
      <td>mode</td>
      <td><code>string</code></td>
      <td><p> The mode to apply to this component. Mode can be <code>ios</code>, <code>wp</code>, or <code>md</code>.</p>
</td>
    </tr>
    
    <tr>
      <td>color</td>
      <td><code>string</code></td>
      <td><p> The default color to use. For most buttons this will set the background color,
for outline buttons it will set the border color. For example: <code>&quot;primary&quot;</code>, <code>&quot;secondary&quot;</code>, <code>&quot;danger&quot;</code>.</p>
</td>
    </tr>
    
  </tbody>
</table>


  <h2 id="sass-variable-header"><a class="anchor" name="sass-variables" href="#sass-variables"></a>Sass Variables</h2>
  <div id="sass-variables" ng-controller="SassToggleCtrl">
  <div class="sass-platform-toggle">
    
      
      
      <a ng-init="setSassPlatform('base')" ng-class="{ active: active === 'base' }" ng-click="setSassPlatform('base')" >All</a>
      
      
      
      <a ng-class="{ active: active === 'ios' }" ng-click="setSassPlatform('ios')">iOS</a>
      
      
      
      <a ng-class="{ active: active === 'md' }" ng-click="setSassPlatform('md')">Material Design</a>
      
      
      
      <a ng-class="{ active: active === 'wp' }" ng-click="setSassPlatform('wp')">Windows Platform</a>
      
      
    
  </div>


  
  <table ng-show="active === 'base'" id="sass-base" class="table param-table" style="margin:0;">
    <thead>
      <tr>
        <th>Property</th>
        <th>Default</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      
      <tr>
        <td><code>$button-round-padding</code></td>
        
          <td><code>0 2.6rem</code></td>
        
        <td><p>Padding of the round button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-round-border-radius</code></td>
        
          <td><code>64px</code></td>
        
        <td><p>Border radius of the round button</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
  <table ng-show="active === 'ios'" id="sass-ios" class="table param-table" style="margin:0;">
    <thead>
      <tr>
        <th>Property</th>
        <th>Default</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      
      <tr>
        <td><code>$button-ios-margin</code></td>
        
          <td><code>.4rem .2rem</code></td>
        
        <td><p>Margin of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-padding</code></td>
        
          <td><code>0 1em</code></td>
        
        <td><p>Padding of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-height</code></td>
        
          <td><code>2.8em</code></td>
        
        <td><p>Height of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-border-radius</code></td>
        
          <td><code>4px</code></td>
        
        <td><p>Border radius of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-font-size</code></td>
        
          <td><code>1.6rem</code></td>
        
        <td><p>Font size of the button text</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-background-color</code></td>
        
          <td><code>color($colors-ios, primary)</code></td>
        
        <td><p>Background color of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-text-color</code></td>
        
          <td><code>color-contrast($colors-ios, $button-ios-background-color)</code></td>
        
        <td><p>Text color of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-background-color-activated</code></td>
        
          <td><code>color-shade($button-ios-background-color)</code></td>
        
        <td><p>Background color of the activated button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-opacity-activated</code></td>
        
          <td><code>1</code></td>
        
        <td><p>Opacity of the activated button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-opacity-hover</code></td>
        
          <td><code>.8</code></td>
        
        <td><p>Opacity of the button on hover</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-large-padding</code></td>
        
          <td><code>0 1em</code></td>
        
        <td><p>Padding of the large button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-large-height</code></td>
        
          <td><code>2.8em</code></td>
        
        <td><p>Height of the large button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-large-font-size</code></td>
        
          <td><code>2rem</code></td>
        
        <td><p>Font size of the large button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-small-padding</code></td>
        
          <td><code>0 .9em</code></td>
        
        <td><p>Padding of the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-small-height</code></td>
        
          <td><code>2.1em</code></td>
        
        <td><p>Height of the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-small-font-size</code></td>
        
          <td><code>1.3rem</code></td>
        
        <td><p>Font size of the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-small-icon-font-size</code></td>
        
          <td><code>1.3em</code></td>
        
        <td><p>Font size of an icon in the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-outline-border-width</code></td>
        
          <td><code>1px</code></td>
        
        <td><p>Border width of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-outline-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-outline-border-radius</code></td>
        
          <td><code>$button-ios-border-radius</code></td>
        
        <td><p>Border radius of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-outline-border-color</code></td>
        
          <td><code>$button-ios-background-color</code></td>
        
        <td><p>Border color of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-outline-text-color</code></td>
        
          <td><code>$button-ios-background-color</code></td>
        
        <td><p>Text color of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-outline-background-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-outline-text-color-activated</code></td>
        
          <td><code>color-contrast($colors-ios, $button-ios-background-color)</code></td>
        
        <td><p>Text color of the activated outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-outline-background-color-activated</code></td>
        
          <td><code>$button-ios-background-color</code></td>
        
        <td><p>Background color of the activated outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-outline-opacity-activated</code></td>
        
          <td><code>1</code></td>
        
        <td><p>Opacity of the activated outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-clear-border-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Border color of the clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-clear-background-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-clear-background-color-activated</code></td>
        
          <td><code>$button-ios-clear-background-color</code></td>
        
        <td><p>Background color of the activated clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-clear-opacity-activated</code></td>
        
          <td><code>.4</code></td>
        
        <td><p>Opacity of the activated clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-clear-text-color-hover</code></td>
        
          <td><code>$button-ios-background-color</code></td>
        
        <td><p>Text color of the clear button on hover</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-clear-opacity-hover</code></td>
        
          <td><code>.6</code></td>
        
        <td><p>Opacity of the clear button on hover</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-round-padding</code></td>
        
          <td><code>$button-round-padding</code></td>
        
        <td><p>Padding of the round button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-round-border-radius</code></td>
        
          <td><code>$button-round-border-radius</code></td>
        
        <td><p>Border radius of the round button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-ios-strong-font-weight</code></td>
        
          <td><code>600</code></td>
        
        <td><p>Font weight of the strong button</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
  <table ng-show="active === 'md'" id="sass-md" class="table param-table" style="margin:0;">
    <thead>
      <tr>
        <th>Property</th>
        <th>Default</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      
      <tr>
        <td><code>$button-md-margin</code></td>
        
          <td><code>.4rem .2rem</code></td>
        
        <td><p>Margin of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-padding</code></td>
        
          <td><code>0 1.1em</code></td>
        
        <td><p>Padding of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-height</code></td>
        
          <td><code>3.6rem</code></td>
        
        <td><p>Height of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-border-radius</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border radius of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-font-size</code></td>
        
          <td><code>1.4rem</code></td>
        
        <td><p>Font size of the button text</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-font-weight</code></td>
        
          <td><code>500</code></td>
        
        <td><p>Font weight of the button text</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-text-transform</code></td>
        
          <td><code>uppercase</code></td>
        
        <td><p>Capitalization of the button text</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-background-color</code></td>
        
          <td><code>color($colors-md, primary)</code></td>
        
        <td><p>Background color of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-text-color</code></td>
        
          <td><code>color-contrast($colors-md, $button-md-background-color)</code></td>
        
        <td><p>Text color of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-box-shadow</code></td>
        
          <td><code>0 2px 2px 0 rgba(0, 0, 0, .14), 0 3px 1px -2px rgba(0, 0, 0, .2), 0 1px 5px 0 rgba(0, 0, 0, .12)</code></td>
        
        <td><p>Box shadow of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-transition-duration</code></td>
        
          <td><code>300ms</code></td>
        
        <td><p>Duration of the transition of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-transition-timing-function</code></td>
        
          <td><code>cubic-bezier(.4, 0, .2, 1)</code></td>
        
        <td><p>Speed curve of the transition of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-background-color-hover</code></td>
        
          <td><code>$button-md-background-color</code></td>
        
        <td><p>Background color of the button on hover</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-background-color-activated</code></td>
        
          <td><code>color-shade($button-md-background-color)</code></td>
        
        <td><p>Background color of the activated button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-opacity-activated</code></td>
        
          <td><code>1</code></td>
        
        <td><p>Opacity of the activated button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-box-shadow-activated</code></td>
        
          <td><code>0 3px 5px rgba(0, 0, 0, .14), 0 3px 5px rgba(0, 0, 0, .21)</code></td>
        
        <td><p>Box shadow of the activated button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-ripple-background-color</code></td>
        
          <td><code>#555</code></td>
        
        <td><p>Background color of the ripple on the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-large-padding</code></td>
        
          <td><code>0 1em</code></td>
        
        <td><p>Padding of the large button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-large-height</code></td>
        
          <td><code>2.8em</code></td>
        
        <td><p>Height of the large button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-large-font-size</code></td>
        
          <td><code>2rem</code></td>
        
        <td><p>Font size of the large button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-small-padding</code></td>
        
          <td><code>0 .9em</code></td>
        
        <td><p>Padding of the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-small-height</code></td>
        
          <td><code>2.1em</code></td>
        
        <td><p>Height of the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-small-font-size</code></td>
        
          <td><code>1.3rem</code></td>
        
        <td><p>Font size of the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-small-icon-font-size</code></td>
        
          <td><code>1.4em</code></td>
        
        <td><p>Font size of an icon in the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-outline-border-width</code></td>
        
          <td><code>1px</code></td>
        
        <td><p>Border width of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-outline-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-outline-border-color</code></td>
        
          <td><code>$button-md-background-color</code></td>
        
        <td><p>Border color of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-outline-text-color</code></td>
        
          <td><code>$button-md-background-color</code></td>
        
        <td><p>Text color of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-outline-background-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-outline-box-shadow</code></td>
        
          <td><code>none</code></td>
        
        <td><p>Box shadow of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-outline-background-color-hover</code></td>
        
          <td><code>rgba(158, 158, 158, .1)</code></td>
        
        <td><p>Background color of the outline button on hover</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-outline-background-color-activated</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the activated outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-outline-box-shadow-activated</code></td>
        
          <td><code>none</code></td>
        
        <td><p>Box shadow of the activated outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-outline-opacity-activated</code></td>
        
          <td><code>1</code></td>
        
        <td><p>Opacity of the activated outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-outline-ripple-background-color</code></td>
        
          <td><code>$button-md-background-color</code></td>
        
        <td><p>Background color of the ripple on the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-clear-border-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Border color of the clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-clear-text-color</code></td>
        
          <td><code>$button-md-background-color</code></td>
        
        <td><p>Text color of the clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-clear-background-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-clear-box-shadow</code></td>
        
          <td><code>none</code></td>
        
        <td><p>Box shadow of the clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-clear-opacity</code></td>
        
          <td><code>1</code></td>
        
        <td><p>Opacity of the clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-clear-background-color-activated</code></td>
        
          <td><code>rgba(158, 158, 158, .2)</code></td>
        
        <td><p>Background color of the activated clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-clear-box-shadow-activated</code></td>
        
          <td><code>$button-md-clear-box-shadow</code></td>
        
        <td><p>Box shadow of the activated clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-clear-background-color-hover</code></td>
        
          <td><code>rgba(158, 158, 158, .1)</code></td>
        
        <td><p>Background color of the clear button on hover</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-clear-ripple-background-color</code></td>
        
          <td><code>#999</code></td>
        
        <td><p>Background color of the ripple on the clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-round-padding</code></td>
        
          <td><code>$button-round-padding</code></td>
        
        <td><p>Padding of the round button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-round-border-radius</code></td>
        
          <td><code>$button-round-border-radius</code></td>
        
        <td><p>Border radius of the round button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-md-strong-font-weight</code></td>
        
          <td><code>bold</code></td>
        
        <td><p>Font weight of the strong button</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
  <table ng-show="active === 'wp'" id="sass-wp" class="table param-table" style="margin:0;">
    <thead>
      <tr>
        <th>Property</th>
        <th>Default</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      
      <tr>
        <td><code>$button-wp-margin</code></td>
        
          <td><code>.4rem .2rem</code></td>
        
        <td><p>Margin of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-padding</code></td>
        
          <td><code>0 1.1em</code></td>
        
        <td><p>Padding of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-height</code></td>
        
          <td><code>3.6rem</code></td>
        
        <td><p>Height of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-border-width</code></td>
        
          <td><code>3px</code></td>
        
        <td><p>Border width of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-border-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Border color of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-border-radius</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Border radius of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-font-size</code></td>
        
          <td><code>1.4rem</code></td>
        
        <td><p>Font size of the button text</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-background-color</code></td>
        
          <td><code>color($colors-wp, primary)</code></td>
        
        <td><p>Background color of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-text-color</code></td>
        
          <td><code>color-contrast($colors-wp, $button-wp-background-color)</code></td>
        
        <td><p>Text color of the button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-background-color-activated</code></td>
        
          <td><code>color-shade($button-wp-background-color)</code></td>
        
        <td><p>Background color of the activated button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-large-padding</code></td>
        
          <td><code>0 1em</code></td>
        
        <td><p>Padding of the large button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-large-height</code></td>
        
          <td><code>2.8em</code></td>
        
        <td><p>Height of the large button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-large-font-size</code></td>
        
          <td><code>2rem</code></td>
        
        <td><p>Font size of the large button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-small-padding</code></td>
        
          <td><code>0 .9em</code></td>
        
        <td><p>Padding of the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-small-height</code></td>
        
          <td><code>2.1em</code></td>
        
        <td><p>Height of the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-small-font-size</code></td>
        
          <td><code>1.3rem</code></td>
        
        <td><p>Font size of the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-small-icon-font-size</code></td>
        
          <td><code>1.4em</code></td>
        
        <td><p>Font size of an icon in the small button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-outline-border-width</code></td>
        
          <td><code>1px</code></td>
        
        <td><p>Border width of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-outline-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-outline-border-color</code></td>
        
          <td><code>$button-wp-background-color</code></td>
        
        <td><p>Border color of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-outline-text-color</code></td>
        
          <td><code>$button-wp-background-color</code></td>
        
        <td><p>Text color of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-outline-background-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-outline-background-color-activated</code></td>
        
          <td><code>$button-wp-background-color</code></td>
        
        <td><p>Background color of the activated outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-outline-background-color-opacity-activated</code></td>
        
          <td><code>.16</code></td>
        
        <td><p>Opacity of the background color of the activated outline button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-clear-text-color</code></td>
        
          <td><code>$button-wp-background-color</code></td>
        
        <td><p>Text color of the clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-clear-background-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-clear-background-color-activated</code></td>
        
          <td><code>rgba(158, 158, 158, .2)</code></td>
        
        <td><p>Background color of the activated clear button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-clear-background-color-hover</code></td>
        
          <td><code>rgba(158, 158, 158, .1)</code></td>
        
        <td><p>Background color of the clear button on hover</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-round-padding</code></td>
        
          <td><code>$button-round-padding</code></td>
        
        <td><p>Padding of the round button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-round-border-radius</code></td>
        
          <td><code>$button-round-border-radius</code></td>
        
        <td><p>Border radius of the round button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$button-wp-strong-font-weight</code></td>
        
          <td><code>bold</code></td>
        
        <td><p>Font weight of the strong button</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
</div>



<!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='/docs/v2/components#buttons'>Button Component Docs</a>,
<a href='/docs/v2/components#fabs'>FabButton Docs</a>,
<a href='../../fab/FabButton'>FabButton API Docs</a>,
<a href='../../fab/FabContainer'>FabContainer API Docs</a><!-- end content block -->


<!-- end body block -->


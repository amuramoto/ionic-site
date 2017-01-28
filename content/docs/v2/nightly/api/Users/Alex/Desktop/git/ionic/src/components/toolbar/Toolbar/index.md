---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "toolbar"
title: "Toolbar"
header_sub_title: "Ionic API Documentation"
doc: "Toolbar"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/src/toolbar/basic"
angular_controller: APIDemoCtrl 
---









<h1 class="api-title">
<a class="anchor" name="toolbar" href="#toolbar"></a>

Toolbar
<h3><code>ion-toolbar</code></h3>






</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/components/toolbar/toolbar.ts#L120">
Improve this doc
</a>






<p>A Toolbar is a generic bar that is positioned above or below content.
Unlike a <a href="../../navbar/Navbar">Navbar</a>, a toolbar can be used as a subheader.
When toolbars are placed within an <code>&lt;ion-header&gt;</code> or <code>&lt;ion-footer&gt;</code>,
the toolbars stay fixed in their respective location. When placed within
<code>&lt;ion-content&gt;</code>, toolbars will scroll with the content.</p>
<h3 id="buttons-in-a-toolbar">Buttons in a Toolbar</h3>
<p>Buttons placed in a toolbar should be placed inside of the <code>&lt;ion-buttons&gt;</code>
element. An exception to this is a <a href="../../menu/MenuToggle">menuToggle</a> button.
It should not be placed inside of the <code>&lt;ion-buttons&gt;</code> element. Both the
<code>&lt;ion-buttons&gt;</code> element and the <code>menuToggle</code> can be positioned inside of the
toolbar using different properties. The below chart has a description of each
property.</p>




<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<pre><code class="lang-html">&lt;ion-header no-border&gt;

  &lt;ion-toolbar&gt;
    &lt;ion-title&gt;My Toolbar Title&lt;/ion-title&gt;
  &lt;/ion-toolbar&gt;

  &lt;ion-toolbar&gt;
    &lt;ion-title&gt;I&#39;m a subheader&lt;/ion-title&gt;
  &lt;/ion-toolbar&gt;

&lt;ion-header&gt;


&lt;ion-content&gt;

  &lt;ion-toolbar&gt;
    &lt;ion-title&gt;Scrolls with the content&lt;/ion-title&gt;
  &lt;/ion-toolbar&gt;

&lt;/ion-content&gt;


&lt;ion-footer no-border&gt;

  &lt;ion-toolbar&gt;
    &lt;ion-title&gt;I&#39;m a footer&lt;/ion-title&gt;
  &lt;/ion-toolbar&gt;

&lt;/ion-footer&gt;
</code></pre>
<h3 id="changing-the-color">Changing the Color</h3>
<p>You can change the toolbars color by changing the property on the element.</p>
<pre><code class="lang-typescript">@Component({
  template: `
    &lt;ion-toolbar color=&quot;primary&quot;&gt;
      &lt;ion-title&gt;Toolbar&lt;/ion-title&gt;
    &lt;/ion-toolbar&gt;


    &lt;ion-toolbar color=&quot;secondary&quot;&gt;
      &lt;ion-title&gt;Toolbar&lt;/ion-title&gt;
    &lt;/ion-toolbar&gt;

    &lt;ion-toolbar color=&quot;danger&quot;&gt;
      &lt;ion-title&gt;Toolbar&lt;/ion-title&gt;
    &lt;/ion-toolbar&gt;


    &lt;ion-toolbar color=&quot;dark&quot;&gt;
      &lt;ion-title&gt;Toolbar&lt;/ion-title&gt;
    &lt;/ion-toolbar&gt;
  `
  })
</code></pre>
<p>You can also change the navbar&#39;s color the same way. This will allow you to have 
a different color navbar per page in your app.</p>
<pre><code class="lang-html">&lt;ion-header&gt;
  &lt;ion-navbar color=&quot;dark&quot;&gt;
    &lt;ion-title&gt;Dark&lt;/ion-title&gt;
  &lt;/ion-navbar&gt;
&lt;/ion-header&gt;


&lt;ion-header&gt;
  &lt;ion-navbar color=&quot;danger&quot;&gt;
    &lt;ion-title&gt;Danger&lt;/ion-title&gt;
  &lt;/ion-navbar&gt;
&lt;/ion-header&gt;

&lt;ion-header&gt;
  &lt;ion-navbar color=&quot;secondary&quot;&gt;
    &lt;ion-title&gt;Secondary&lt;/ion-title&gt;
  &lt;/ion-navbar&gt;
&lt;/ion-header&gt;
</code></pre>
<h2 id="common-usage-patterns">Common Usage Patterns</h2>
<h3 id="header">Header</h3>
<p>One of the best uses of the toolbar is as a header.</p>
<pre><code class="lang-html">&lt;ion-header&gt;
  &lt;ion-toolbar color=&quot;primary&quot;&gt;
    &lt;ion-buttons start&gt;
      &lt;button ion-button icon-only&gt;
        &lt;ion-icon name=&quot;content&quot;&gt;&lt;/ion-icon&gt;
      &lt;/button&gt;
    &lt;/ion-buttons&gt;

    &lt;ion-title&gt;Header&lt;/ion-title&gt;

    &lt;ion-buttons end&gt;
      &lt;button ion-button icon-only&gt;
        &lt;ion-icon name=&quot;search&quot;&gt;&lt;/ion-icon&gt;
      &lt;/button&gt;
    &lt;/ion-buttons&gt;

  &lt;/ion-toolbar&gt;
&lt;/ion-header&gt;

&lt;ion-content&gt;
  &lt;p&gt;There is a header above me!&lt;/p&gt;
&lt;/ion-content&gt;
</code></pre>
<h3 id="buttons-in-toolbars">Buttons in Toolbars</h3>
<p>Buttons can be added to both header and footer toolbars. To add a button 
to a toolbar, we need to first add an <code>ion-buttons</code> component. This component 
wraps one or more buttons, and can be positioned using one of following attributes:</p>
<table>
<thead>
<tr>
<th>Property</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>start</code></td>
<td>Positions element to the left of the content in <code>ios</code> mode, and directly to the right in <code>md</code> and <code>wp</code> mode.</td>
</tr>
<tr>
<td><code>end</code></td>
<td>Positions element to the right of the content in <code>ios</code> mode, and to the far right in <code>md</code> and <code>wp</code> mode.</td>
</tr>
<tr>
<td><code>left</code></td>
<td>Positions element to the left of all other elements.</td>
</tr>
<tr>
<td><code>right</code></td>
<td>Positions element to the right of all other elements. </td>
</tr>
</tbody>
</table>
<pre><code class="lang-html">&lt;ion-header&gt;
  &lt;ion-toolbar&gt;
    &lt;ion-buttons start&gt;
      &lt;button ion-button icon-only color=&quot;royal&quot;&gt;
        &lt;ion-icon name=&quot;search&quot;&gt;&lt;/ion-icon&gt;
      &lt;/button&gt;
    &lt;/ion-buttons&gt;
    &lt;ion-title&gt;Send To...&lt;/ion-title&gt;
    &lt;ion-buttons end&gt;
      &lt;button ion-button icon-only color=&quot;royal&quot;&gt;
        &lt;ion-icon name=&quot;person-add&quot;&gt;&lt;/ion-icon&gt;
      &lt;/button&gt;
    &lt;/ion-buttons&gt;
  &lt;/ion-toolbar&gt;
&lt;/ion-header&gt;

&lt;ion-content&gt;&lt;/ion-content&gt;

&lt;ion-footer&gt;
  &lt;ion-toolbar&gt;
    &lt;p&gt;Ash, Misty, Brock&lt;/p&gt;
    &lt;ion-buttons end&gt;
      &lt;button ion-button icon-right color=&quot;royal&quot;&gt;
        Send
        &lt;ion-icon name=&quot;send&quot;&gt;&lt;/ion-icon&gt;
      &lt;/button&gt;
    &lt;/ion-buttons&gt;
  &lt;/ion-toolbar&gt;
&lt;/ion-footer&gt;
</code></pre>
<h3 id="segment-in-toolbars">Segment in Toolbars</h3>
<p><a href="#segment">Segments</a> are a great way to allow users to switch between different 
sets of data. Use the following markup to add a segment to a toolbar:</p>
<pre><code class="lang-html">&lt;ion-header&gt;
  &lt;ion-toolbar&gt;
    &lt;ion-buttons start&gt;
      &lt;button ion-button icon-only&gt;
        &lt;ion-icon name=&quot;create&quot;&gt;&lt;/ion-icon&gt;
      &lt;/button&gt;
    &lt;/ion-buttons&gt;
    &lt;ion-segment&gt;
      &lt;ion-segment-button value=&quot;new&quot;&gt;
        New
      &lt;/ion-segment-button&gt;
      &lt;ion-segment-button value=&quot;hot&quot;&gt;
        Hot
      &lt;/ion-segment-button&gt;
    &lt;/ion-segment&gt;
    &lt;ion-buttons end&gt;
      &lt;button ion-button icon-only&gt;
        &lt;ion-icon name=&quot;more&quot;&gt;&lt;/ion-icon&gt;
      &lt;/button&gt;
    &lt;/ion-buttons&gt;
  &lt;/ion-toolbar&gt;
&lt;/ion-header&gt;
</code></pre>
<h3 id="searchbar-in-toolbars">Searchbar in Toolbars</h3>
<p>Another common design paradigm is to include a searchbar inside your toolbar.</p>
<pre><code class="lang-html">&lt;ion-header&gt;
  &lt;ion-toolbar color=&quot;primary&quot;&gt;
    &lt;ion-searchbar (input)=&quot;getItems($event)&quot;&gt;&lt;/ion-searchbar&gt;
  &lt;/ion-toolbar&gt;
&lt;/ion-header&gt;

&lt;ion-content&gt;
  &lt;ion-list&gt;
    &lt;ion-item *ngFor=&quot;let item of items&quot;&gt;
      {% raw %}{{ item }}{% endraw %}
    &lt;/ion-item&gt;
  &lt;/ion-list&gt;
&lt;/ion-content&gt;
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
      <td>color</td>
      <td><code>string</code></td>
      <td><p> The predefined color to use. For example: <code>&quot;primary&quot;</code>, <code>&quot;secondary&quot;</code>, <code>&quot;danger&quot;</code>.</p>
</td>
    </tr>
    
    <tr>
      <td>mode</td>
      <td><code>string</code></td>
      <td><p> The mode to apply to this component. Mode can be <code>ios</code>, <code>wp</code>, or <code>md</code>.</p>
</td>
    </tr>
    
  </tbody>
</table>


  <h2 id="sass-variable-header"><a class="anchor" name="sass-variables" href="#sass-variables"></a>Sass Variables</h2>
  <div id="sass-variables" ng-controller="SassToggleCtrl">
  <div class="sass-platform-toggle">
    
      
      
      <a ng-init="setSassPlatform('ios')" ng-class="{ active: active === 'ios' }" ng-click="setSassPlatform('ios')" >iOS</a>
      
      
      
      <a ng-class="{ active: active === 'md' }" ng-click="setSassPlatform('md')">Material Design</a>
      
      
      
      <a ng-class="{ active: active === 'wp' }" ng-click="setSassPlatform('wp')">Windows Platform</a>
      
      
    
  </div>


  
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
        <td><code>$toolbar-order-ios</code></td>
        
          <td><code>(&#10;  back-button: 0,&#10;  menu-toggle-start: 1,&#10;  buttons-left: 2,&#10;  buttons-start: 3,&#10;  content: 4,&#10;  buttons-end: 5,&#10;  buttons-right: 6,&#10;  menu-toggle-end: 7,&#10;)</code></td>
        
        <td><p>Order of the toolbar elements</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-ios-button-font-size</code></td>
        
          <td><code>1.7rem</code></td>
        
        <td><p>Font size of the toolbar button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-ios-title-font-size</code></td>
        
          <td><code>1.7rem</code></td>
        
        <td><p>Font size of the toolbar title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-ios-title-font-weight</code></td>
        
          <td><code>600</code></td>
        
        <td><p>Font weight of the toolbar title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-ios-title-text-align</code></td>
        
          <td><code>center</code></td>
        
        <td><p>Text alignment of the toolbar title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-ios-title-text-color</code></td>
        
          <td><code>color-contrast($colors-ios, $toolbar-ios-background)</code></td>
        
        <td><p>Text color of the toolbar title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-ios-button-color</code></td>
        
          <td><code>color-contrast($colors-ios, $toolbar-ios-background, ios)</code></td>
        
        <td><p>Text color of the toolbar button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-ios-button-border-radius</code></td>
        
          <td><code>4px</code></td>
        
        <td><p>Border radius of the toolbar button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$navbar-ios-height</code></td>
        
          <td><code>$toolbar-ios-height</code></td>
        
        <td><p>Height of the navigation bar</p>
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
        <td><code>$toolbar-order-md</code></td>
        
          <td><code>(&#10;  back-button: 0,&#10;  menu-toggle-start: 1,&#10;  buttons-left: 2,&#10;  content: 3,&#10;  buttons-start: 4,&#10;  buttons-end: 5,&#10;  buttons-right: 6,&#10;  menu-toggle-end: 7,&#10;)</code></td>
        
        <td><p>Order of the toolbar elements</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-md-title-font-size</code></td>
        
          <td><code>2rem</code></td>
        
        <td><p>Font size of the toolbar title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-md-title-text-color</code></td>
        
          <td><code>color-contrast($colors-md, $toolbar-md-background, md)</code></td>
        
        <td><p>Text color of the toolbar title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-md-button-font-size</code></td>
        
          <td><code>1.4rem</code></td>
        
        <td><p>Font size of the toolbar button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-md-button-color</code></td>
        
          <td><code>$toolbar-md-title-text-color</code></td>
        
        <td><p>Text color of the toolbar button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-md-button-border-radius</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border radius of the toolbar button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$navbar-md-height</code></td>
        
          <td><code>$toolbar-md-height</code></td>
        
        <td><p>Height of the navigation bar</p>
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
        <td><code>$toolbar-order-wp</code></td>
        
          <td><code>(&#10;  back-button: 0,&#10;  menu-toggle-start: 1,&#10;  buttons-left: 2,&#10;  content: 3,&#10;  buttons-start: 4,&#10;  buttons-end: 5,&#10;  buttons-right: 6,&#10;  menu-toggle-end: 7,&#10;)</code></td>
        
        <td><p>Order of the toolbar elements</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-wp-title-padding</code></td>
        
          <td><code>0 6px</code></td>
        
        <td><p>Padding of the toolbar title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-wp-title-font-size</code></td>
        
          <td><code>1.5rem</code></td>
        
        <td><p>Font size of the toolbar title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-wp-title-font-weight</code></td>
        
          <td><code>bold</code></td>
        
        <td><p>Font weight of the toolbar title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-wp-title-text-transform</code></td>
        
          <td><code>uppercase</code></td>
        
        <td><p>Text transform of the toolbar title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-wp-title-text-color</code></td>
        
          <td><code>color-contrast($colors-wp, $toolbar-wp-background, wp)</code></td>
        
        <td><p>Text color of the toolbar title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-wp-button-font-size</code></td>
        
          <td><code>1.4rem</code></td>
        
        <td><p>Font size of the toolbar button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-wp-button-color</code></td>
        
          <td><code>color-contrast($colors-wp, $toolbar-wp-background, wp)</code></td>
        
        <td><p>Text color of the toolbar button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toolbar-wp-button-border-radius</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border radius of the toolbar button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$navbar-wp-height</code></td>
        
          <td><code>$toolbar-wp-height</code></td>
        
        <td><p>Height of the navigation bar</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
</div>



<!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='../../navbar/Navbar/'>Navbar API Docs</a>,
<a href='../Header/'>Header API Docs</a>,
<a href='../Footer/'>Footer API Docs</a><!-- end content block -->


<!-- end body block -->


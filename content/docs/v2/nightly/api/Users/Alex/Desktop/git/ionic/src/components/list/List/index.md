---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "list"
title: "List"
header_sub_title: "Ionic API Documentation"
doc: "List"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/src/list/basic"
angular_controller: APIDemoCtrl 
additional_preview_device_urls:
  - inset-list: /docs/v2/demos/src/list/inset/
  - list-headers: /docs/v2/demos/src/list/headers/
  - list-dividers: /docs/v2/demos/src/list/dividers/
  - icon-list: /docs/v2/demos/src/list/icon/
  - avatar-list: /docs/v2/demos/src/list/avatar/
  - multi-line-list: /docs/v2/demos/src/list/multiline/
  - sliding-list: /docs/v2/demos/src/list/sliding/
  - thumbnail-list: /docs/v2/demos/src/list/thumbnail/
---









<h1 class="api-title">
<a class="anchor" name="list" href="#list"></a>

List
<h3><code>ion-list</code></h3>






</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/components/list/list.ts#L8">
Improve this doc
</a>






<p>The List is a widely used interface element in almost any mobile app,
and can include content ranging from basic text all the way to
buttons, toggles, icons, and thumbnails.</p>
<p>Both the list, which contains items, and the list items themselves
can be any HTML element.</p>
<p>Using the List and Item components make it easy to support various
interaction modes such as swipe to edit, drag to reorder, and
removing items.</p>




<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<pre><code class="lang-html">&lt;ion-list&gt;
  &lt;ion-item *ngFor=&quot;let contact of contacts&quot;&gt;
    {% raw %}{{contact.firstName}} {{contact.lastName}}{% endraw %}
  &lt;/ion-item&gt;
&lt;/ion-list&gt;
</code></pre>
<h2 id="common-usage-patterns">Common Usage Patterns</h2>
<h3 id="inset-list">Inset List</h3>
<p>Lists don’t have an outside margin by default.  To add one, add the <code>inset</code> 
attribute to the <code>ion-list</code> component.</p>
<pre><code class="lang-html">&lt;ion-list inset&gt;
  &lt;button ion-item *ngFor=&quot;let item of items&quot;&quot;&gt;
    {% raw %}{{ item }}{% endraw %}
  &lt;/button&gt; 
&lt;/ion-list&gt;
</code></pre>
<h3 id="list-dividers">List Dividers</h3>
<p>To divide groups of items, use <code>&lt;ion-item-group&gt;</code> instead of <code>&lt;ion-list&gt;</code>, then 
use <code>&lt;ion-item-divider&gt;</code> components to divide the group in to multiple sections:</p>
<pre><code class="lang-html">&lt;ion-item-group&gt;
  &lt;ion-item-divider color=&quot;light&quot;&gt;A&lt;/ion-item-divider&gt;
  &lt;ion-item&gt;Angola&lt;/ion-item&gt;
  &lt;ion-item&gt;Argentina&lt;/ion-item&gt;
&lt;/ion-item-group&gt;
</code></pre>
<h3 id="list-headers">List Headers</h3>
<p>Each list can include a header at the top of the list by including
<code>&lt;ion-list-header&gt;</code>:</p>
<pre><code class="lang-html">&lt;ion-list&gt;
  &lt;ion-list-header&gt;
    Action
  &lt;/ion-list-header&gt;
  &lt;ion-item&gt;Terminator II&lt;/ion-item&gt;
  &lt;ion-item&gt;The Empire Strikes Back&lt;/ion-item&gt;
  &lt;ion-item&gt;Blade Runner&lt;/ion-item&gt;
&lt;/ion-list&gt;
</code></pre>
<h3 id="icon-list">Icon List</h3>
<p>Adding icons to list items is a great way to hint about the contents of each item. 
The position of the icon can be set using the <code>item-left</code> and <code>item-right</code> attributes. 
The size of the icon defaults to <code>small</code>, and can be made larger with the <code>large</code> attribute.</p>
<pre><code class="lang-html">&lt;ion-list&gt;
  &lt;ion-item&gt;
    &lt;ion-icon name=&quot;leaf&quot; item-left&gt;&lt;/ion-icon&gt;
      Herbology
    &lt;ion-icon name=&quot;rose&quot; item-right&gt;&lt;/ion-icon&gt;
  &lt;/ion-item&gt;
&lt;/ion-list&gt;
</code></pre>
<h3 id="avatar-list">Avatar List</h3>
<p>Item avatars showcase an image larger than an icon, but smaller than a thumbnail. 
To use an avatar, add an <code>&lt;ion-avatar&gt;</code> component inside of an item. The position 
of the avatar can be set using the <code>item-left</code> and <code>item-right</code> attributes:</p>
<pre><code class="lang-html">&lt;ion-list&gt;
  &lt;ion-item&gt;
    &lt;ion-avatar item-left&gt;
      &lt;img src=&quot;img/avatar-cher.png&quot;&gt;
    &lt;/ion-avatar&gt;
    &lt;h2&gt;Cher&lt;/h2&gt;
    &lt;p&gt;Ugh. As if.&lt;/p&gt;
  &lt;/ion-item&gt;
&lt;/ion-list&gt;
</code></pre>
<h3 id="multi-line-list">Multi-line List</h3>
<p>Multi-line lists are identical to regular lists, except items have multiple lines 
of text. When an <code>&lt;ion-item</code>&gt; component contains multiple header or paragraph elements, 
it will automatically expand it’s height to fit the new lines of text. Below is an 
example with three lines of text:</p>
<pre><code class="lang-html">&lt;ion-list&gt;
  &lt;ion-item&gt;
    &lt;ion-avatar item-left&gt;
      &lt;img src=&quot;img/avatar-finn.png&quot;&gt;
    &lt;/ion-avatar&gt;
    &lt;h2&gt;Finn&lt;/h2&gt;
    &lt;h3&gt;Don&#39;t Know What To Do!&lt;/h3&gt;
    &lt;p&gt;I&#39;ve had a pretty messed up day. If we just...&lt;/p&gt;
  &lt;/ion-item&gt;
&lt;/ion-list&gt;
</code></pre>
<h3 id="sliding-list">Sliding List</h3>
<p>Sliding items can be swiped to the left or right to reveal a hidden set of buttons.  To 
use a sliding item, add an <code>ion-item-sliding</code> component inside of an <code>ion-list</code> component. 
Next, add an <code>&lt;ion-item-options&gt;</code> component inside of the sliding item to contain the 
buttons.</p>
<p>For more information, Check out the <a href="../../item/ItemSliding">API docs</a>.</p>
<pre><code class="lang-html">&lt;ion-list&gt;
  &lt;ion-item-sliding&gt;
    &lt;ion-item&gt;
      &lt;ion-avatar item-left&gt;
        &lt;img src=&quot;img/slimer.png&quot;&gt;
      &lt;/ion-avatar&gt;
      &lt;h2&gt;Slimer&lt;/h2&gt;
    &lt;/ion-item&gt;
    &lt;ion-item-options side=&quot;left&quot;&gt;
      &lt;button ion-button color=&quot;primary&quot;&gt;
        &lt;ion-icon name=&quot;text&quot;&gt;&lt;/ion-icon&gt;
        Text
      &lt;/button&gt;
      &lt;button ion-button color=&quot;secondary&quot;&gt;
        &lt;ion-icon name=&quot;call&quot;&gt;&lt;/ion-icon&gt;
        Call
      &lt;/button&gt;
    &lt;/ion-item-options&gt;
    &lt;ion-item-options side=&quot;right&quot;&gt;
      &lt;button ion-button color=&quot;primary&quot;&gt;
        &lt;ion-icon name=&quot;mail&quot;&gt;&lt;/ion-icon&gt;
        Email
      &lt;/button&gt;
    &lt;/ion-item-options&gt;
  &lt;/ion-item-sliding&gt;
&lt;/ion-list&gt;
</code></pre>
<h3 id="thumbnail-list">Thumbnail List</h3>
<p>Item thumbnails showcase an image that takes up the entire height of an item. To use 
a thumbnail, add an <code>&lt;ion-thumbnail&gt;</code> component inside of an item. The position of 
the thumbnail can be set using the <code>item-left</code> and <code>item-right</code> attributes:</p>
<pre><code class="lang-html">&lt;ion-list&gt;
  &lt;ion-item&gt;
    &lt;ion-thumbnail item-left&gt;
      &lt;img src=&quot;img/thumbnail-totoro.png&quot;&gt;
    &lt;/ion-thumbnail&gt;
    &lt;h2&gt;My Neighbor Totoro&lt;/h2&gt;
    &lt;p&gt;Hayao Miyazaki • 1988&lt;/p&gt;
    &lt;button ion-button clear item-right&gt;View&lt;/button&gt;
  &lt;/ion-item&gt;
&lt;/ion-list&gt;
</code></pre>




<!-- @property tags -->

<h2><a class="anchor" name="attributes" href="#attributes"></a>Attributes:</h2>
<table class="table" style="margin:0;">
<thead>
<tr>
<th>Attribute</th>







<th>Description</th>
</tr>
</thead>
<tbody>

<tr>
<td>
no-lines
</td>



<td>
Removes the dividing line between items in the list.

</td>
</tr>

</tbody>
</table>



<!-- instance methods on the class -->

<h2><a class="anchor" name="instance-members" href="#instance-members"></a>Instance Members</h2>

<div id="closeSlidingItems"></div>

<h3>
<a class="anchor" name="closeSlidingItems" href="#closeSlidingItems"></a>
<code>closeSlidingItems()</code>
  

</h3>

Closes any sliding items that are open.










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
      <td>mode</td>
      <td><code>string</code></td>
      <td><p> The platform mode to apply to this component. Mode can be <code>ios</code>, <code>wp</code>, or <code>md</code>.</p>
</td>
    </tr>
    
    <tr>
      <td>sliding</td>
      <td><code>boolean</code></td>
      <td><p> Sets whether item sliding is enabled</p>
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
        <td><code>$list-ios-margin-top</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Margin top of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-ios-margin-right</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Margin right of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-ios-margin-bottom</code></td>
        
          <td><code>32px</code></td>
        
        <td><p>Margin bottom of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-ios-margin-left</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Margin left of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-ios-margin-top</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin top of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-ios-margin-right</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin right of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-ios-margin-bottom</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin bottom of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-ios-margin-left</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin left of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-ios-border-radius</code></td>
        
          <td><code>4px</code></td>
        
        <td><p>Border radius of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-ios-header-padding-left</code></td>
        
          <td><code>$item-ios-padding-left</code></td>
        
        <td><p>Padding left of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-ios-header-border-bottom</code></td>
        
          <td><code>$hairlines-width solid $list-ios-border-color</code></td>
        
        <td><p>Border bottom of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-ios-header-font-size</code></td>
        
          <td><code>1.2rem</code></td>
        
        <td><p>Font size of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-ios-header-font-weight</code></td>
        
          <td><code>500</code></td>
        
        <td><p>Font weight of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-ios-header-letter-spacing</code></td>
        
          <td><code>.1rem</code></td>
        
        <td><p>Letter spacing of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-ios-header-text-transform</code></td>
        
          <td><code>uppercase</code></td>
        
        <td><p>Text transform of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-ios-header-color</code></td>
        
          <td><code>#333</code></td>
        
        <td><p>Text color of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-ios-header-background-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the header in a list</p>
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
        <td><code>$list-md-margin-top</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin top of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-md-margin-right</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Margin right of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-md-margin-bottom</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin bottom of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-md-margin-left</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Margin left of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-md-margin-top</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin top of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-md-margin-right</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin right of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-md-margin-bottom</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin bottom of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-md-margin-left</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin left of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-md-border-radius</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border radius of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-md-header-margin-bottom</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Margin bottom of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-md-header-padding-left</code></td>
        
          <td><code>$item-md-padding-left</code></td>
        
        <td><p>Padding left of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-md-header-min-height</code></td>
        
          <td><code>4.5rem</code></td>
        
        <td><p>Minimum height of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-md-header-border-top</code></td>
        
          <td><code>1px solid $list-md-border-color</code></td>
        
        <td><p>Border top of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-md-header-font-size</code></td>
        
          <td><code>1.4rem</code></td>
        
        <td><p>Font size of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-md-header-color</code></td>
        
          <td><code>#757575</code></td>
        
        <td><p>Text color of the header in a list</p>
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
        <td><code>$list-wp-margin-top</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin top of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-wp-margin-right</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Margin right of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-wp-margin-bottom</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin bottom of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-wp-margin-left</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Margin left of the list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-wp-margin-top</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin top of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-wp-margin-right</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin right of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-wp-margin-bottom</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin bottom of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-wp-margin-left</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Margin left of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-inset-wp-border-radius</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border radius of the inset list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-wp-header-padding-left</code></td>
        
          <td><code>$item-wp-padding-left</code></td>
        
        <td><p>Padding left of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-wp-header-border-bottom</code></td>
        
          <td><code>1px solid $list-wp-border-color</code></td>
        
        <td><p>Border bottom of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-wp-header-font-size</code></td>
        
          <td><code>2rem</code></td>
        
        <td><p>Font size of the header in a list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$list-wp-header-color</code></td>
        
          <td><code>$list-wp-text-color</code></td>
        
        <td><p>Text color of the header in a list</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
</div>



<!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='/docs/v2/components#lists'>List Component Docs</a>,
<a href='../../item/Item'>Item API Docs</a>,
<a href='../../item/ItemSliding'>ItemSliding API Docs</a><!-- end content block -->


<!-- end body block -->


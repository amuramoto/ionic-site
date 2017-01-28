---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "card"
title: "Card"
header_sub_title: "Ionic API Documentation"
doc: "Card"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/src/card/basic"
angular_controller: APIDemoCtrl 
additional_preview_device_urls:
  - using-components-in-cards: /docs/v2/demos/src/card/list/
  - card-headers: /docs/v2/demos/src/card/header/
  - header-image: /docs/v2/demos/src/card/image/
  - background-image: /docs/v2/demos/src/card/background/
  - social-cards: /docs/v2/demos/src/card/advanced-social/
  - map-cards: /docs/v2/demos/src/card/advanced-map/
---









<h1 class="api-title">
<a class="anchor" name="card" href="#card"></a>

Card
<h3><code>ion-card</code></h3>






</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/components/card/card.ts#L3">
Improve this doc
</a>






<p>Cards are a common user interface element for mobile apps, and act as a formatted container
for displaying content. Cards are commonly used to display lists of items, similar to <code>ion-item</code>.</p>
<h3 id="card-headers">Card Headers</h3>
<p>Just like a normal page, cards can be customized to include headers. To add a header 
to a card, add the <code>ion-card-header</code> component, then include the card&#39;s body content
inside the <code>ion-card-content</code> component:</p>
<pre><code class="lang-html">&lt;ion-card&gt;
  &lt;ion-card-header&gt;
    Header
  &lt;/ion-card-header&gt;
  &lt;ion-card-content&gt;
    The British use the term &quot;header&quot;, but the American term &quot;head-shot.&quot;
  &lt;/ion-card-content&gt;
&lt;/ion-card&gt;
</code></pre>
<h3 id="card-titles">Card Titles</h3>
<p>Card titles are similar to card headers, but are styled with less top and bottom margin so 
that they have less emphasis. Generally, a title is used to label the contents of <code>ion-card-content</code>, 
while a header is used to label the entire Card. To add a title, add the <code>ion-card-title</code> component:</p>
<pre><code class="lang-html">&lt;ion-card&gt;
  &lt;ion-card-content&gt;
    &lt;ion-card-title&gt;Header or Headshot?&lt;/ion-card-title&gt;
    The British use the term &quot;header&quot;, but the American term &quot;head-shot.&quot;
  &lt;/ion-card-content&gt;
&lt;/ion-card&gt;
</code></pre>
<h3 id="using-components-in-cards">Using Components in Cards</h3>
<p>Many different components can be nested inside a Card. For example, a card can contain a list of items:</p>
<pre><code class="lang-html">&lt;ion-card&gt;
  &lt;ion-card-header&gt;
    Explore Nearby
  &lt;/ion-card-header&gt;

  &lt;ion-list&gt;
    &lt;button ion-item&gt;
      &lt;ion-icon name=&quot;cart&quot; item-left&gt;&lt;/ion-icon&gt;
      Shopping
    &lt;/button&gt;

    &lt;button ion-item&gt;
      &lt;ion-icon name=&quot;medical&quot; item-left&gt;&lt;/ion-icon&gt;
      Hospital
    &lt;/button&gt;
  &lt;/ion-list&gt;
&lt;/ion-card&gt;
</code></pre>
<h2 id="common-usage-patterns">Common Usage Patterns</h2>
<h3 id="header-image">Header Image</h3>
<p>Images in cards will automatically be scaled to display full-width. A common layout is to
use an image along with the <code>ion-card-content</code> component to create the look of a card with 
a header image:</p>
<pre><code class="lang-html">&lt;ion-card&gt;
  &lt;img src=&quot;img/nin-live.png&quot;/&gt;
  &lt;ion-card-content&gt;
    &lt;ion-card-title&gt;
      Nine Inch Nails Live
    &lt;/ion-card-title&gt;
    &lt;p&gt;
      The most popular industrial group ever, and largely
      responsible for bringing the music to a mass audience.
    &lt;/p&gt;
  &lt;/ion-card-content&gt;
&lt;/ion-card&gt;
</code></pre>
<h3 id="background-image">Background Image</h3>
<p>Cards can be used to achieve a multitude of designs. We provide many of the elements to achieve 
common designs, but sometimes it will be necessary to add custom styles. Adding background 
images to cards is a perfect example of how adding custom styles can achieve a completely different look.</p>
<pre><code class="lang-html">&lt;ion-card&gt;
  &lt;img src=&quot;img/card-saopaolo.png&quot;/&gt;
  &lt;div class=&quot;card-title&quot;&gt;São Paulo&lt;/div&gt;
  &lt;div class=&quot;card-subtitle&quot;&gt;41 Listings&lt;/div&gt;
&lt;/ion-card&gt;
</code></pre>
<p>Then, in the Sass file for the page:</p>
<pre><code class="lang-scss">ion-card {
  position: relative;
  text-align: center;
}

.card-title {
  position: absolute;
  top: 36%;
  font-size: 2.0em;
  width: 100%;
  font-weight: bold;
  color: #fff;
}

.card-subtitle {
  font-size: 1.0em;
  position: absolute;
  top: 52%;
  width: 100%;
  color: #fff;
}
</code></pre>
<h3 id="social-cards">Social Cards</h3>
<p>It&#39;s often necessary to create social cards within an application. Using a combination of different 
items in a card you can achieve this.</p>
<pre><code class="lang-html">&lt;ion-card&gt;

  &lt;ion-item&gt;
    &lt;ion-avatar item-left&gt;
      &lt;img src=&quot;img/marty-avatar.png&quot;&gt;
    &lt;/ion-avatar&gt;
    &lt;h2&gt;Marty McFly&lt;/h2&gt;
    &lt;p&gt;November 5, 1955&lt;/p&gt;
  &lt;/ion-item&gt;

  &lt;img src=&quot;img/advance-card-bttf.png&quot;&gt;

  &lt;ion-card-content&gt;
    &lt;p&gt;Wait a minute. Wait a minute, Doc. Uhhh... Are you telling me that you built a time machine...&lt;/p&gt;
  &lt;/ion-card-content&gt;

  &lt;ion-row&gt;
    &lt;ion-col&gt;
      &lt;button ion-button icon-left clear small&gt;
        &lt;ion-icon name=&quot;thumbs-up&quot;&gt;&lt;/ion-icon&gt;
        &lt;div&gt;12 Likes&lt;/div&gt;
      &lt;/button&gt;
    &lt;/ion-col&gt;
    &lt;ion-col&gt;
      &lt;button ion-button icon-left clear small&gt;
        &lt;ion-icon name=&quot;text&quot;&gt;&lt;/ion-icon&gt;
        &lt;div&gt;4 Comments&lt;/div&gt;
      &lt;/button&gt;
    &lt;/ion-col&gt;
    &lt;ion-col center text-center&gt;
      &lt;ion-note&gt;
        11h ago
      &lt;/ion-note&gt;
    &lt;/ion-col&gt;
  &lt;/ion-row&gt;

&lt;/ion-card&gt;
</code></pre>
<h3 id="map-cards">Map Cards</h3>
<p>A combination of Ionic components can be used to create a card that appears as a map.</p>
<pre><code class="lang-html">&lt;ion-card&gt;

  &lt;img src=&quot;img/advance-card-map-madison.png&quot;&gt;
  &lt;ion-fab right top&gt;
    &lt;button ion-fab&gt;
      &lt;ion-icon name=&quot;pin&quot;&gt;&lt;/ion-icon&gt;
    &lt;/button&gt;
  &lt;/ion-fab&gt;

  &lt;ion-item&gt;
    &lt;ion-icon name=&quot;football&quot; item-left large&gt;&lt;/ion-icon&gt;
    &lt;h2&gt;Museum of Football&lt;/h2&gt;
    &lt;p&gt;11 N. Way St, Madison, WI 53703&lt;/p&gt;
  &lt;/ion-item&gt;

  &lt;ion-item&gt;
    &lt;ion-icon name=&quot;wine&quot; item-left large &gt;&lt;/ion-icon&gt;
    &lt;h2&gt;Institute of Fine Cocktails&lt;/h2&gt;
    &lt;p&gt;14 S. Hop Avenue, Madison, WI 53703&lt;/p&gt;
  &lt;/ion-item&gt;

  &lt;ion-item&gt;
    &lt;span item-left&gt;18 min&lt;/span&gt;
    &lt;span item-left&gt;(2.6 mi)&lt;/span&gt;
    &lt;button ion-button icon-left clear item-right&gt;
      &lt;ion-icon name=&quot;navigate&quot;&gt;&lt;/ion-icon&gt;
      Start
    &lt;/button&gt;
  &lt;/ion-item&gt;

&lt;/ion-card&gt;
</code></pre>
<!-- <h3 class="section-nav" id="card-advanced-weather">Weather Cards</h3>
<a target="_blank" class="component-doc-demo" href="https://github.com/driftyco/ionic-preview-app/tree/master/app/pages/cards/advanced-weather">
  Demo Source
</a>

Coming soon.* -->



<!-- @usage tag -->


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
        <td><code>$card-ios-margin-top</code></td>
        
          <td><code>12px</code></td>
        
        <td><p>Margin top of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-margin-right</code></td>
        
          <td><code>12px</code></td>
        
        <td><p>Margin right of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-margin-bottom</code></td>
        
          <td><code>12px</code></td>
        
        <td><p>Margin bottom of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-margin-left</code></td>
        
          <td><code>12px</code></td>
        
        <td><p>Margin left of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-padding-top</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Padding top of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-padding-right</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Padding right of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-padding-bottom</code></td>
        
          <td><code>14px</code></td>
        
        <td><p>Padding bottom of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-padding-left</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Padding left of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-padding-media-top</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Padding top of the media on the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-padding-media-bottom</code></td>
        
          <td><code>9px</code></td>
        
        <td><p>Padding bottom of the media on the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-background-color</code></td>
        
          <td><code>$list-ios-background-color</code></td>
        
        <td><p>Background color of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-box-shadow-color</code></td>
        
          <td><code>rgba(0, 0, 0, .3)</code></td>
        
        <td><p>Box shadow color of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-box-shadow</code></td>
        
          <td><code>0 1px 2px $card-ios-box-shadow-color</code></td>
        
        <td><p>Box shadow of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-border-radius</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border radius of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-font-size</code></td>
        
          <td><code>1.4rem</code></td>
        
        <td><p>Font size of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-text-color</code></td>
        
          <td><code>#666</code></td>
        
        <td><p>Color of the card text</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-title-font-size</code></td>
        
          <td><code>1.8rem</code></td>
        
        <td><p>Font size of the card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-title-padding</code></td>
        
          <td><code>8px 0 8px 0</code></td>
        
        <td><p>Padding of the card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-title-margin</code></td>
        
          <td><code>2px 0 2px</code></td>
        
        <td><p>Margin of the card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-title-text-color</code></td>
        
          <td><code>#222</code></td>
        
        <td><p>Color of the card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-header-font-size</code></td>
        
          <td><code>1.6rem</code></td>
        
        <td><p>Font size of the card header</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-header-font-weight</code></td>
        
          <td><code>500</code></td>
        
        <td><p>Font weight of the card header</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-header-padding</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Padding of the card header</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-ios-header-color</code></td>
        
          <td><code>#333</code></td>
        
        <td><p>Color of the card header</p>
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
        <td><code>$card-md-margin-top</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Margin top of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-margin-right</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Margin right of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-margin-bottom</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Margin bottom of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-margin-left</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Margin left of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-padding-top</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Padding top of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-padding-right</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Padding right of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-padding-bottom</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Padding bottom of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-padding-left</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Padding left of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-padding-media-top</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Padding top of the media on the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-padding-media-bottom</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Padding bottom of the media on the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-avatar-size</code></td>
        
          <td><code>4rem</code></td>
        
        <td><p>Size of the card avatar</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-thumbnail-size</code></td>
        
          <td><code>8rem</code></td>
        
        <td><p>Size of the card thumbnail</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-background-color</code></td>
        
          <td><code>$list-md-background-color</code></td>
        
        <td><p>Background color of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-box-shadow</code></td>
        
          <td><code>0 2px 2px 0 rgba(0, 0, 0, .14), 0 3px 1px -2px rgba(0, 0, 0, .2), 0 1px 5px 0 rgba(0, 0, 0, .12)</code></td>
        
        <td><p>Box shadow of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-border-radius</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border radius of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-font-size</code></td>
        
          <td><code>1.4rem</code></td>
        
        <td><p>Font size of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-line-height</code></td>
        
          <td><code>1.5</code></td>
        
        <td><p>Line height of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-text-color</code></td>
        
          <td><code>#222</code></td>
        
        <td><p>Color of the card text</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-title-font-size</code></td>
        
          <td><code>2.4rem</code></td>
        
        <td><p>Font size of the card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-title-padding</code></td>
        
          <td><code>8px 0 8px 0</code></td>
        
        <td><p>Padding of the card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-title-margin</code></td>
        
          <td><code>2px 0 2px</code></td>
        
        <td><p>Margin of the card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-title-text-color</code></td>
        
          <td><code>#222</code></td>
        
        <td><p>Color of the card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-header-font-size</code></td>
        
          <td><code>1.6rem</code></td>
        
        <td><p>Font size of the card header</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-header-padding</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Padding of the card header</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-md-header-color</code></td>
        
          <td><code>#222</code></td>
        
        <td><p>Color of the card header</p>
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
        <td><code>$card-wp-margin-top</code></td>
        
          <td><code>8px</code></td>
        
        <td><p>Margin top of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-margin-right</code></td>
        
          <td><code>8px</code></td>
        
        <td><p>Margin right of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-margin-bottom</code></td>
        
          <td><code>8px</code></td>
        
        <td><p>Margin bottom of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-margin-left</code></td>
        
          <td><code>8px</code></td>
        
        <td><p>Margin left of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-padding-top</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Padding top of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-padding-right</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Padding right of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-padding-bottom</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Padding bottom of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-padding-left</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Padding left of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-padding-media-top</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Padding top of the media on the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-padding-media-bottom</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Padding bottom of the media on the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-avatar-size</code></td>
        
          <td><code>4rem</code></td>
        
        <td><p>Size of the card avatar</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-thumbnail-size</code></td>
        
          <td><code>8rem</code></td>
        
        <td><p>Size of the card thumbnail</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-background-color</code></td>
        
          <td><code>$list-wp-background-color</code></td>
        
        <td><p>Background color of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-box-shadow-color</code></td>
        
          <td><code>rgba(0, 0, 0, .2)</code></td>
        
        <td><p>Box shadow color of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-box-shadow</code></td>
        
          <td><code>0 1px 1px 1px $card-wp-box-shadow-color</code></td>
        
        <td><p>Box shadow of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-border-radius</code></td>
        
          <td><code>1px</code></td>
        
        <td><p>Border radius of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-font-size</code></td>
        
          <td><code>1.4rem</code></td>
        
        <td><p>Font size of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-line-height</code></td>
        
          <td><code>1.5</code></td>
        
        <td><p>Line height of the card</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-text-color</code></td>
        
          <td><code>#222</code></td>
        
        <td><p>Color of the card text</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-title-font-size</code></td>
        
          <td><code>2.4rem</code></td>
        
        <td><p>Font size of card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-title-padding</code></td>
        
          <td><code>8px 0 8px 0</code></td>
        
        <td><p>Padding of the card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-title-margin</code></td>
        
          <td><code>2px 0</code></td>
        
        <td><p>Margin of the card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-title-text-color</code></td>
        
          <td><code>#222</code></td>
        
        <td><p>Color of the card title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-header-font-size</code></td>
        
          <td><code>1.6rem</code></td>
        
        <td><p>Font size of the card header</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-header-padding</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Padding of the card header</p>
</td>
      </tr>
      
      <tr>
        <td><code>$card-wp-header-color</code></td>
        
          <td><code>#222</code></td>
        
        <td><p>Color of the card header</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
</div>



<!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='/docs/v2/components/#cards'>Card Component Docs</a><!-- end content block -->


<!-- end body block -->


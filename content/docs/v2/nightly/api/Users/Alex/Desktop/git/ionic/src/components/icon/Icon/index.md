---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "icon"
title: "Icon"
header_sub_title: "Ionic API Documentation"
doc: "Icon"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/src/icon/basic"
angular_controller: APIDemoCtrl 
---









<h1 class="api-title">
<a class="anchor" name="icon" href="#icon"></a>

Icon
<h3><code>ion-icon</code></h3>






</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/components/icon/icon.ts#L4">
Improve this doc
</a>






<p>The Icon component is used to include Ionicons in an app. Icons can be used 
on their own or inside of a number of Ionic components, and are styled 
differently depending on the mode the app is running in (iOS, MD, WP). 
For example, by setting the icon name of <code>alarm</code>, on iOS the
icon will automatically apply <code>ios-alarm</code>, and on Material Design it will
automatically apply <code>md-alarm</code>.</p>
<p>For a full list of available icons, check out the
<a href="../../../../ionicons">Ionicons docs</a>.</p>




<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<pre><code class="lang-html">&lt;!-- automatically uses the correct &quot;star&quot; icon depending on the mode --&gt;
&lt;ion-icon name=&quot;star&quot;&gt;&lt;/ion-icon&gt;

&lt;!-- explicity set the icon for each mode --&gt;
&lt;ion-icon ios=&quot;ios-home&quot; md=&quot;md-home&quot;&gt;&lt;/ion-icon&gt;

&lt;!-- always use the same icon, no matter what the mode --&gt;
&lt;ion-icon name=&quot;ios-clock&quot;&gt;&lt;/ion-icon&gt;
&lt;ion-icon name=&quot;logo-twitter&quot;&gt;&lt;/ion-icon&gt;
</code></pre>
<h3 id="active-inactive-icons">Active / Inactive Icons</h3>
<p>All icons have both <code>active</code> and <code>inactive</code> states. Active icons are typically 
full and thick, where as inactive icons are outlined and thin. Set the <code>isActive</code> 
input property to <code>true</code> or <code>false</code> to change the state of the icon. Icons will default 
to active if a value is not specified.</p>
<pre><code class="lang-html">&lt;!-- active --&gt;
&lt;ion-icon name=&quot;heart&quot;&gt;&lt;/ion-icon&gt;

&lt;!-- inactive --&gt;
&lt;ion-icon name=&quot;heart&quot; isActive=&quot;false&quot;&gt;&lt;/ion-icon&gt;
</code></pre>
<h3 id="dynamcially-changing-an-icon">Dynamcially Changing an Icon</h3>
<p>To set an icon using a variable, bind the <code>name</code> input property to a value on the component&#39;s model:</p>
<pre><code class="lang-html">&lt;ion-icon [name]=&quot;myIcon&quot;&gt;&lt;/ion-icon&gt;
</code></pre>
<pre><code class="lang-typescript">export class MyFirstPage {
  // use the home icon
  myIcon: string = &quot;home&quot;;
}
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
    
    <tr>
      <td>name</td>
      <td><code>string</code></td>
      <td><p> Icon to use. Will load the appropriate icon for each mode</p>
</td>
    </tr>
    
    <tr>
      <td>ios</td>
      <td><code>string</code></td>
      <td><p> Explicitly set the icon to use on iOS</p>
</td>
    </tr>
    
    <tr>
      <td>md</td>
      <td><code>string</code></td>
      <td><p> Explicitly set the icon to use on MD</p>
</td>
    </tr>
    
    <tr>
      <td>isActive</td>
      <td><code>bool</code></td>
      <td><p> Whether or not the icon has an &quot;active&quot; appearance. On iOS an active icon is filled in or full appearance, and an inactive icon on iOS will use an outlined version of the icon same icon. Material Design icons do not change appearance depending if they&#39;re active or not. The <code>isActive</code> property is largely used by the tabbar.</p>
</td>
    </tr>
    
  </tbody>
</table>




<!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='/docs/v2/components#icons'>Icon Component Docs</a>,
<a href='/docs/v2/ionicons'>Ionicon Docs</a><!-- end content block -->


<!-- end body block -->


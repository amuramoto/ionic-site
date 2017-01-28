---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "toast"
title: "Toast"
header_sub_title: "Ionic API Documentation"
doc: "Toast"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/src/toast/basic"
angular_controller: APIDemoCtrl 
---









<h1 class="api-title">
<a class="anchor" name="toast" href="#toast"></a>

Toast





</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/components/toast/toast.ts#L8">
Improve this doc
</a>






<p>A Toast is a subtle notification commonly used in modern applications.
It can be used to provide feedback about an operation or to
display a system message. The toast appears on top of the app&#39;s content,
and can be dismissed by the app to resume user interaction with
the app.</p>
<p>Instances of the Toast component are created by calling the <code>create()</code> function
of the <a href="../ToastController">ToastController class</a>. The Toast is displayed
to the user by calling <code>present()</code> on the Toast instance.</p>




<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<p>For a complete usage example, see the <a href="../ToastController">ToastController API docs</a>.</p>




<!-- @property tags -->



<!-- instance methods on the class -->

<h2><a class="anchor" name="instance-members" href="#instance-members"></a>Instance Members</h2>

<div id="setMessage"></div>

<h3>
<a class="anchor" name="setMessage" href="#setMessage"></a>
<code>setMessage(message)</code>
  

</h3>

Set the message for the instance of Toast



<table class="table param-table" style="margin:0;">
  <thead>
    <tr>
      <th>Param</th>
      <th>Type</th>
      <th>Details</th>
    </tr>
  </thead>
  <tbody>
    
    <tr>
      <td>
        message
        
        
      </td>
      <td>
        
  <code>string</code>
      </td>
      <td>
        <p>Toast message content</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="present"></div>

<h3>
<a class="anchor" name="present" href="#present"></a>
<code>present(opts)</code>
  

</h3>

Present the Toast instance.



<table class="table param-table" style="margin:0;">
  <thead>
    <tr>
      <th>Param</th>
      <th>Type</th>
      <th>Details</th>
    </tr>
  </thead>
  <tbody>
    
    <tr>
      <td>
        opts
        
        
      </td>
      <td>
        
  <code>NavOptions</code>
      </td>
      <td>
        <p>Nav options to go with this transition.<strong class="tag">Optional</strong></p>

        
      </td>
    </tr>
    
  </tbody>
</table>





<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Promise</code> <p>Returns a promise which is resolved when the transition has completed.</p>


</div>




<div id="dismissAll"></div>

<h3>
<a class="anchor" name="dismissAll" href="#dismissAll"></a>
<code>dismissAll()</code>
  

</h3>

Dismiss all Toast components which have been presented.












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
        <td><code>$toast-width</code></td>
        
          <td><code>100%</code></td>
        
        <td><p>Width of the toast</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-max-width</code></td>
        
          <td><code>700px</code></td>
        
        <td><p>Max width of the toast</p>
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
        <td><code>$toast-ios-background</code></td>
        
          <td><code>rgba(0, 0, 0, .9)</code></td>
        
        <td><p>Background of the toast wrapper</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-ios-border-radius</code></td>
        
          <td><code>.65rem</code></td>
        
        <td><p>Border radius of the toast wrapper</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-ios-title-color</code></td>
        
          <td><code>#fff</code></td>
        
        <td><p>Color of the toast title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-ios-title-font-size</code></td>
        
          <td><code>1.4rem</code></td>
        
        <td><p>Font size of the toast title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-ios-title-padding</code></td>
        
          <td><code>1.5rem</code></td>
        
        <td><p>Padding of the toast title</p>
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
        <td><code>$toast-md-background</code></td>
        
          <td><code>#333</code></td>
        
        <td><p>Background of the toast wrapper</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-md-title-color</code></td>
        
          <td><code>#fff</code></td>
        
        <td><p>Color of the toast title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-md-title-font-size</code></td>
        
          <td><code>1.5rem</code></td>
        
        <td><p>Font size of the toast title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-md-title-padding</code></td>
        
          <td><code>19px 16px 17px</code></td>
        
        <td><p>Padding of the toast title</p>
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
        <td><code>$toast-wp-background</code></td>
        
          <td><code>rgba(0, 0, 0, 1)</code></td>
        
        <td><p>Background of the toast wrapper</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-wp-border-radius</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Border radius of the toast wrapper</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-wp-button-color</code></td>
        
          <td><code>#fff</code></td>
        
        <td><p>Color of the toast button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-wp-title-color</code></td>
        
          <td><code>#fff</code></td>
        
        <td><p>Color of the toast title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-wp-title-font-size</code></td>
        
          <td><code>1.4rem</code></td>
        
        <td><p>Font size of the toast title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$toast-wp-title-padding</code></td>
        
          <td><code>1.5rem</code></td>
        
        <td><p>Padding of the toast title</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
</div>



<!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='/docs/v2/components#toast'>Toast Component Docs</a>,
<a href='../ToastController/'>ToastController API Docs</a><!-- end content block -->


<!-- end body block -->


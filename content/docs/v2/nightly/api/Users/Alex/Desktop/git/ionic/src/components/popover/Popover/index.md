---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "popover"
title: "Popover"
header_sub_title: "Ionic API Documentation"
doc: "Popover"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/src/popover/basic"
angular_controller: APIDemoCtrl 
---









<h1 class="api-title">
<a class="anchor" name="popover" href="#popover"></a>

Popover





</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/components/popover/popover.ts#L7">
Improve this doc
</a>






<p>A Popover is a dialog that appears on top of the current page.
It can be used for anything, but generally it is used for overflow
actions that don&#39;t fit in the navigation bar.</p>
<p>Instances of the Popover component are created by calling the <code>create()</code> function
of the <a href="../PopoverController">PopoverController class</a>. The Popover is displayed
to the user by calling <code>present()</code> on the Popover instance.</p>




<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<p>For a complete usage example, see the <a href="../PopoverController">PopoverController API docs</a>.</p>




<!-- @property tags -->



<!-- instance methods on the class -->

<h2><a class="anchor" name="instance-members" href="#instance-members"></a>Instance Members</h2>

<div id="present"></div>

<h3>
<a class="anchor" name="present" href="#present"></a>
<code>present(opts)</code>
  

</h3>

Present the popover instance.



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
        <td><code>$popover-ios-width</code></td>
        
          <td><code>200px</code></td>
        
        <td><p>Width of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-ios-min-width</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Min width of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-ios-min-height</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Minimum height of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-ios-max-height</code></td>
        
          <td><code>90%</code></td>
        
        <td><p>Maximum height of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-ios-border-radius</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Border radius of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-ios-text-color</code></td>
        
          <td><code>$text-ios-color</code></td>
        
        <td><p>Text color of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-ios-background</code></td>
        
          <td><code>$background-ios-color</code></td>
        
        <td><p>Background of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-ios-arrow-background</code></td>
        
          <td><code>$popover-ios-background</code></td>
        
        <td><p>Background of the popover arrow</p>
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
        <td><code>$popover-md-width</code></td>
        
          <td><code>250px</code></td>
        
        <td><p>Width of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-md-min-width</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Min width of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-md-min-height</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Minimum height of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-md-max-height</code></td>
        
          <td><code>90%</code></td>
        
        <td><p>Maximum height of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-md-border-radius</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border radius of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-md-text-color</code></td>
        
          <td><code>$text-md-color</code></td>
        
        <td><p>Text color of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-md-background</code></td>
        
          <td><code>$background-md-color</code></td>
        
        <td><p>Background of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-md-box-shadow-color</code></td>
        
          <td><code>rgba(0, 0, 0, .3)</code></td>
        
        <td><p>Box shadow color of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-md-box-shadow</code></td>
        
          <td><code>0 3px 12px 2px $popover-md-box-shadow-color</code></td>
        
        <td><p>Box shadow of the popover content</p>
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
        <td><code>$popover-wp-width</code></td>
        
          <td><code>200px</code></td>
        
        <td><p>Width of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-wp-min-width</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Min width of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-wp-min-height</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Minimum height of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-wp-max-height</code></td>
        
          <td><code>90%</code></td>
        
        <td><p>Maximum height of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-wp-border</code></td>
        
          <td><code>2px solid #ccc</code></td>
        
        <td><p>Border of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-wp-border-radius</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Border radius of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-wp-text-color</code></td>
        
          <td><code>$text-wp-color</code></td>
        
        <td><p>Text color of the popover content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$popover-wp-background</code></td>
        
          <td><code>$background-wp-color</code></td>
        
        <td><p>Background of the popover content</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
</div>



<!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='/docs/v2/components#popovers'>Popover Component Docs</a>,
<a href='../PopoverController/'>PopoverController API Docs</a><!-- end content block -->


<!-- end body block -->


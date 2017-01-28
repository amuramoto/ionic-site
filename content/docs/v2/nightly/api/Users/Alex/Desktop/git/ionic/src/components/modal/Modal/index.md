---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "modal"
title: "Modal"
header_sub_title: "Ionic API Documentation"
doc: "Modal"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/src/modal/basic"
angular_controller: APIDemoCtrl 
---









<h1 class="api-title">
<a class="anchor" name="modal" href="#modal"></a>

Modal





</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/components/modal/modal.ts#L8">
Improve this doc
</a>






<p>A Modal is a content pane that goes over the user&#39;s current page.
Usually it is used for making a choice or editing an item. A modal uses the
<code>NavController</code> to
<a href='/docs/v2/api/components/nav/NavController/#present'>present</a>
itself in the root nav stack. It is added to the stack similar to how
<a href='/docs/v2/api/components/nav/NavController/#push'>NavController.push</a>
works.</p>
<p>When a modal (or any other overlay such as an alert or actionsheet) is
&quot;presented&quot; to a nav controller, the overlay is added to the app&#39;s root nav.
After the modal has been presented, from within the component instance The
modal can later be closed or &quot;dismissed&quot; by using the ViewController&#39;s
<code>dismiss</code> method. Additionally, you can dismiss any overlay by using <code>pop</code>
on the root nav controller. Modals are not reusable. When a modal is dismissed
it is destroyed.</p>
<p>An instance of the Modal class is created by calling the <code>create()</code> function of the 
<a href='../ModalController/'>Modal Controller class</a>. The
Modal instance is then displayed by calling <code>present()</code> on the instance</p>




<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<p>For a complete usage example, see the
<a href='../ModalController/'>Modal Controller API docs</a>.</p>




<!-- @property tags -->



<!-- instance methods on the class -->

<h2><a class="anchor" name="instance-members" href="#instance-members"></a>Instance Members</h2>

<div id="present"></div>

<h3>
<a class="anchor" name="present" href="#present"></a>
<code>present(opts)</code>
  

</h3>

Present the action sheet instance.



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
        <td><code>$modal-inset-min-width</code></td>
        
          <td><code>768px</code></td>
        
        <td><p>Min width of the modal inset</p>
</td>
      </tr>
      
      <tr>
        <td><code>$modal-inset-min-height-small</code></td>
        
          <td><code>600px</code></td>
        
        <td><p>Minimum height of the small modal inset</p>
</td>
      </tr>
      
      <tr>
        <td><code>$modal-inset-min-height-large</code></td>
        
          <td><code>768px</code></td>
        
        <td><p>Minimum height of the large modal inset</p>
</td>
      </tr>
      
      <tr>
        <td><code>$modal-inset-width</code></td>
        
          <td><code>600px</code></td>
        
        <td><p>Width of the large modal inset</p>
</td>
      </tr>
      
      <tr>
        <td><code>$modal-inset-height-small</code></td>
        
          <td><code>500px</code></td>
        
        <td><p>Height of the small modal inset</p>
</td>
      </tr>
      
      <tr>
        <td><code>$modal-inset-height-large</code></td>
        
          <td><code>600px</code></td>
        
        <td><p>Height of the large modal inset</p>
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
        <td><code>$modal-ios-background-color</code></td>
        
          <td><code>$background-ios-color</code></td>
        
        <td><p>Background color for the modal</p>
</td>
      </tr>
      
      <tr>
        <td><code>$modal-ios-border-radius</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Border radius for the modal</p>
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
        <td><code>$modal-md-background-color</code></td>
        
          <td><code>$background-md-color</code></td>
        
        <td><p>Background color for the modal</p>
</td>
      </tr>
      
      <tr>
        <td><code>$modal-inset-box-shadow-color</code></td>
        
          <td><code>rgba(0, 0, 0, .4)</code></td>
        
        <td><p>Box shadow color of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$modal-inset-box-shadow</code></td>
        
          <td><code>0 28px 48px $modal-inset-box-shadow-color</code></td>
        
        <td><p>Box shadow of the alert</p>
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
        <td><code>$modal-wp-background-color</code></td>
        
          <td><code>$background-wp-color</code></td>
        
        <td><p>Background color for the modal</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
</div>



<!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='/docs/v2/components#modals'>Modal Component Docs</a>,
<a href='../ModalController/'>ModalController API Docs</a><!-- end content block -->


<!-- end body block -->


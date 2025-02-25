---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "modalcontroller"
title: "ModalController"
header_sub_title: "Ionic API Documentation"
doc: "ModalController"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/src/modal/basic"
angular_controller: APIDemoCtrl 
---









<h1 class="api-title">
<a class="anchor" name="modal-controller" href="#modal-controller"></a>

ModalController





</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/components/modal/modal.ts#L93">
Improve this doc
</a>






<p>The Modal Controller is used to create instances of the
<a href='../Modal/'>Modal Component</a>.</p>
<p>Data can be passed to a new modal through <code>Modal.create()</code> as the second
argument. The data can then be accessed from the opened page by injecting
<code>NavParams</code>. Note that the page, which opened as a modal, has no special
&quot;modal&quot; logic within it, but uses <code>NavParams</code> no differently than a
standard page.</p>




<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<pre><code class="lang-ts">import { ModalController, NavParams } from &#39;ionic-angular&#39;;

@Component(...)
class HomePage {

 constructor(public modalCtrl: ModalController) {

 }

 presentProfileModal() {
   let profileModal = this.modalCtrl.create(Profile, { userId: 8675309 });
   profileModal.present();
 }

}

@Component(...)
class Profile {

 constructor(params: NavParams) {
   console.log(&#39;UserId&#39;, params.get(&#39;userId&#39;));
 }

}
</code></pre>
<h2 id="modal-options">Modal Options</h2>
<table>
<thead>
<tr>
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>showBackdrop</td>
<td><code>boolean</code></td>
<td>Whether to show the backdrop. Default true.</td>
</tr>
<tr>
<td>enableBackdropDismiss</td>
<td><code>boolean</code></td>
<td>Whether the popover should be dismissed by tapping the backdrop. Default true.</td>
</tr>
</tbody>
</table>




<!-- @property tags -->



<!-- instance methods on the class -->

<h2><a class="anchor" name="instance-members" href="#instance-members"></a>Instance Members</h2>

<div id="create"></div>

<h3>
<a class="anchor" name="create" href="#create"></a>
<code>create(component,&nbsp;data,&nbsp;opts)</code>
  

</h3>

Creates a modal to display.



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
        component
        
        
      </td>
      <td>
        
  <code>object</code>
      </td>
      <td>
        <p>The Modal view</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        data
        
        
      </td>
      <td>
        
  <code>object</code>
      </td>
      <td>
        <p>Any data to pass to the Modal view</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        opts
        
        
      </td>
      <td>
        
  <code>object</code>
      </td>
      <td>
        <p>See <a href="#modal-options">Modal Options</a> above</p>

        
      </td>
    </tr>
    
  </tbody>
</table>






<h2><a class="anchor" name="advanced" href="#advanced"></a>Advanced</h2>
<p>A modal can also emit data, which is useful when it is used to add or edit
data. For example, a profile page could slide up in a modal, and on submit,
the submit button could pass the updated profile data, then dismiss the
modal.</p>
<pre><code class="lang-ts">import { Component } from &#39;@angular/core&#39;;
import { ModalController, ViewController } from &#39;ionic-angular&#39;;

@Component(...)
class HomePage {

 constructor(public modalCtrl: ModalController) {

 }

 presentContactModal() {
   let contactModal = this.modalCtrl.create(ContactUs);
   contactModal.present();
 }

 presentProfileModal() {
   let profileModal = this.modalCtrl.create(Profile, { userId: 8675309 });
   profileModal.onDidDismiss(data =&gt; {
     console.log(data);
   });
   profileModal.present();
 }

}

@Component(...)
class Profile {

 constructor(public viewCtrl: ViewController) {

 }

 dismiss() {
   let data = { &#39;foo&#39;: &#39;bar&#39; };
   this.viewCtrl.dismiss(data);
 }

}
</code></pre>



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
<a href='../Modal/'>Modal API Docs</a><!-- end content block -->


<!-- end body block -->


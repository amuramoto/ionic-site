---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "actionsheet"
title: "ActionSheet"
header_sub_title: "Ionic API Documentation"
doc: "ActionSheet"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/src/action-sheet/basic"
angular_controller: APIDemoCtrl 
---









<h1 class="api-title">
<a class="anchor" name="action-sheet" href="#action-sheet"></a>

ActionSheet





</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/components/action-sheet/action-sheet.ts#L7">
Improve this doc
</a>






<p>An Action Sheet opens a dialog on top of the app&#39;s content that contains buttons, and is.
usually used to present the user with a set of actions to choose from. Each button can be 
customized, and assigned a handler function that is called when the button is tapped.</p>
<h3 id="creating-an-action-sheet">Creating an Action Sheet</h3>
<p>An Action Sheet is defined by importing and creating an instance of ActionSheetController
then calling <code>create(options)</code> on the instance. Action Sheet options can also
be specified at a later time with <a href="#instance-members">instance methods</a>. For a complete
list of options see <a href="#action-sheet-options">Action Sheet Options</a> below.</p>
<p>To display an Action Sheet call <code>present()</code> on a defined Action Sheet.</p>
<h3 id="dismissing-an-action-sheet">Dismissing an Action Sheet</h3>
<p>A user must manually dismiss an Action Sheet, before they can resume interaction 
with the app. This is done by tapping one of the Action Sheet&#39;s buttons, 
tapping the back button (Android), or tapping the background outside the 
Action Sheet. To prevent tapping a button from dismissing the Action Sheet,
set the handler function for that button to return <code>false</code>.</p>




<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<pre><code class="lang-ts">import { ActionSheetController } from &#39;ionic-angular&#39;;

export class MyClass{

 //create instance of ActionSheetController
 constructor(public actionSheetCtrl: ActionSheetController) {}

 presentActionSheet() {
   let options = {
     title: &#39;Modify your album&#39;,
     buttons: [
       {
         text: &#39;Destructive&#39;,
         role: &#39;destructive&#39;,
         handler: () =&gt; {
           console.log(&#39;Destructive clicked&#39;);
         }
       },
       {
         text: &#39;Archive&#39;,
         handler: () =&gt; {
           console.log(&#39;Archive clicked&#39;);
         }
       },
       {
         text: &#39;Cancel&#39;,
         role: &#39;cancel&#39;,
         handler: () =&gt; {
           console.log(&#39;Cancel clicked&#39;);
         }
       }
     ]
   }

   // create the Action Sheet
   let actionSheet = this.actionSheetCtrl.create(options);

   // update the subtitle
   actionSheet.setSubTitle(&#39;Or Archive Your Album&#39;)

   // show the Action Sheet 
   actionSheet.present();
 }
}
</code></pre>
<h3 id="action-sheet-options">Action Sheet Options</h3>
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
<td>title</td>
<td><code>string</code></td>
<td>The title for the Action Sheet.</td>
</tr>
<tr>
<td>subTitle</td>
<td><code>string</code></td>
<td>The sub-title for the Action Sheet.</td>
</tr>
<tr>
<td>cssClass</td>
<td><code>string</code></td>
<td>Additional classes for custom styles, separated by spaces.</td>
</tr>
<tr>
<td>enableBackdropDismiss</td>
<td><code>boolean</code></td>
<td>If the Action Sheet should close when the user taps the backdrop. Defaults to true.</td>
</tr>
<tr>
<td>buttons</td>
<td><code>Array&lt;any&gt;</code></td>
<td>An array of <a href="#button-options">button options</a>. Buttons are displayed in the order they are included in the array, except buttons with <code>role: cancel</code>, which appear at the button of the Action Sheet.</td>
</tr>
</tbody>
</table>
<h3 id="button-options">Button Options</h3>
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
<td>text</td>
<td><code>string</code></td>
<td>The button text.</td>
</tr>
<tr>
<td>icon</td>
<td><code>icon</code></td>
<td>The button icon.</td>
</tr>
<tr>
<td>handler</td>
<td><code>any</code></td>
<td>A callback function to execute when the button is tapped. If the user dismisses the Action Sheet by tapping the background, the handler for the button with <code>role: cancel</code> will be executed</td>
</tr>
<tr>
<td>cssClass</td>
<td><code>string</code></td>
<td>Additional classes for custom styles, separated by spaces.</td>
</tr>
<tr>
<td>role</td>
<td><code>string</code></td>
<td><code>destructive</code> or <code>cancel</code>. <code>destructive</code> styles the button in iOS mode only. It is recommended that <code>destructive</code> buttons be included at the start of the <code>buttons</code> array. <code>cancel</code> styles the button across all platform modes, and places the button at the bottom of the Action Sheet.</td>
</tr>
</tbody>
</table>




<!-- @property tags -->



<!-- instance methods on the class -->

<h2><a class="anchor" name="instance-members" href="#instance-members"></a>Instance Members</h2>

<div id="setTitle"></div>

<h3>
<a class="anchor" name="setTitle" href="#setTitle"></a>
<code>setTitle(title)</code>
  

</h3>

Sets the title of the Action Sheet.


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
        title
        
        
      </td>
      <td>
        
  <code>string</code>
      </td>
      <td>
        <p>Action sheet title</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="setSubTitle"></div>

<h3>
<a class="anchor" name="setSubTitle" href="#setSubTitle"></a>
<code>setSubTitle(subTitle)</code>
  

</h3>

Sets the subtitle of the Action Sheet.


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
        subTitle
        
        
      </td>
      <td>
        
  <code>string</code>
      </td>
      <td>
        <p>Action sheet subtitle</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="addButton"></div>

<h3>
<a class="anchor" name="addButton" href="#addButton"></a>
<code>addButton(button)</code>
  

</h3>

Adds a button to the Action Sheet. See [Action Sheet Button Options](#action-sheet-button-options).


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
        button
        
        
      </td>
      <td>
        
  <code>object</code>
      </td>
      <td>
        <p>Action sheet button</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="present"></div>

<h3>
<a class="anchor" name="present" href="#present"></a>
<code>present(opts)</code>
  

</h3>

Show the Action Sheet instance to the user.



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


<h2><a class="anchor" name="advanced" href="#advanced"></a>Advanced</h2>
<h3 id="starting-page-transitions-in-handler-functions">Starting Page Transitions in Handler Functions</h3>
<p>If you want to start a page transition in your app from an Action Sheet button&#39;s handler
function, it is important to keep in mind that the Action Sheet dismissal and the 
page transition occur asynchronously. This may cause unexpected results, such as a 
janky page transition, since the page transition animation could start before the 
Action Sheet has been fully dismissed from the view.</p>
<p>To prevent this, you should programmatically dismiss the Action Sheet in the button&#39;s 
handler function using <code>dismiss()</code>, which returns a promise. You can then call the page
transition when the promise resolves to ensure everything happens in the expected order.</p>
<p>Also, the handler function must return <code>false</code>. This prevents Ionic from automatically
dismissing the Action Sheet once the handler function has finished, which allows us to 
manually control the order of events.</p>
<p>For example, the following creates an Action Sheet with a &#39;Transition Me!&#39; button whose 
handler function dismisses the Action Sheet, then transitions to the previous page
in the app.</p>
<pre><code class="lang-ts">let actionSheet = this.actionSheetCtrl.create({
  title: &#39;Hello&#39;,
  buttons: [{
    text: &#39;Transition Me!&#39;,
    handler: () =&gt; {
      // begin the Action Sheet&#39;s dimiss transition
      let navTransition = actionSheet.dismiss();

      // start the page transition when dismissal of
      // the Action Sheet is complete
      navTransition.then(() =&gt; {
        this.nav.pop();
      });

      // prevent Action Sheet from being dismissed automatically
      return false;
    }
  }]
});

actionSheet.present();
</code></pre>



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
        <td><code>$action-sheet-ios-text-align</code></td>
        
          <td><code>center</code></td>
        
        <td><p>Text align of the action sheet</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-padding</code></td>
        
          <td><code>0 10px</code></td>
        
        <td><p>Padding of the action sheet</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-group-margin-bottom</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Bottom margin of the action sheet button group</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-background</code></td>
        
          <td><code>#f9f9f9</code></td>
        
        <td><p>Background color of the action sheet</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-border-color</code></td>
        
          <td><code>#d6d6da</code></td>
        
        <td><p>Border color of the action sheet</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-border-radius</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Border radius of the action sheet</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-title-padding</code></td>
        
          <td><code>1.5rem</code></td>
        
        <td><p>Padding of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-title-color</code></td>
        
          <td><code>#8f8f8f</code></td>
        
        <td><p>Color of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-title-font-size</code></td>
        
          <td><code>1.3rem</code></td>
        
        <td><p>Font size of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-title-font-weight</code></td>
        
          <td><code>400</code></td>
        
        <td><p>Font weight of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-title-border-radius</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Border radius of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-min-height</code></td>
        
          <td><code>5.6rem</code></td>
        
        <td><p>Minimum height of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-padding</code></td>
        
          <td><code>18px</code></td>
        
        <td><p>Padding of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-text-color</code></td>
        
          <td><code>#007aff</code></td>
        
        <td><p>Text color of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-font-size</code></td>
        
          <td><code>2rem</code></td>
        
        <td><p>Font size of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-border-width</code></td>
        
          <td><code>$hairlines-width</code></td>
        
        <td><p>Border width of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-border-color</code></td>
        
          <td><code>#d1d3d6</code></td>
        
        <td><p>Border color of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-background</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-background-activated</code></td>
        
          <td><code>#ebebeb</code></td>
        
        <td><p>Background color of the activated action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-destructive-text-color</code></td>
        
          <td><code>#f53d3d</code></td>
        
        <td><p>Destructive text color of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-cancel-background</code></td>
        
          <td><code>#fff</code></td>
        
        <td><p>Background color of the action sheet cancel button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-ios-button-cancel-font-weight</code></td>
        
          <td><code>600</code></td>
        
        <td><p>Font weight of the action sheet cancel button</p>
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
        <td><code>$action-sheet-md-text-align</code></td>
        
          <td><code>left</code></td>
        
        <td><p>Text align of the action sheet</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-background</code></td>
        
          <td><code>#fafafa</code></td>
        
        <td><p>Background color of the action sheet</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-group-margin-bottom</code></td>
        
          <td><code>8px</code></td>
        
        <td><p>Bottom margin of the action sheet button group</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-title-color</code></td>
        
          <td><code>#757575</code></td>
        
        <td><p>Color of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-title-font-size</code></td>
        
          <td><code>1.6rem</code></td>
        
        <td><p>Font size of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-title-padding</code></td>
        
          <td><code>11px 16px 17px</code></td>
        
        <td><p>Padding of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-button-min-height</code></td>
        
          <td><code>4.8rem</code></td>
        
        <td><p>Minimum height of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-button-text-color</code></td>
        
          <td><code>#222</code></td>
        
        <td><p>Text color of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-button-font-size</code></td>
        
          <td><code>1.6rem</code></td>
        
        <td><p>Font size of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-button-padding</code></td>
        
          <td><code>0 16px</code></td>
        
        <td><p>Padding of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-button-background</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-button-background-activated</code></td>
        
          <td><code>#f1f1f1</code></td>
        
        <td><p>Background color of the action sheet activated button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-icon-font-size</code></td>
        
          <td><code>2.4rem</code></td>
        
        <td><p>Font size of the icon in the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-icon-width</code></td>
        
          <td><code>2.3rem</code></td>
        
        <td><p>Width of the icon in the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-icon-text-align</code></td>
        
          <td><code>center</code></td>
        
        <td><p>Text align of the icon in the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-icon-vertical-align</code></td>
        
          <td><code>middle</code></td>
        
        <td><p>Vertical align of the icon in the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-md-icon-margin</code></td>
        
          <td><code>0 32px 0 0</code></td>
        
        <td><p>Margin of the icon in the action sheet button</p>
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
        <td><code>$action-sheet-wp-text-align</code></td>
        
          <td><code>left</code></td>
        
        <td><p>Text align of the action sheet</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-background</code></td>
        
          <td><code>#fff</code></td>
        
        <td><p>Background color of the action sheet</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-box-shadow-color</code></td>
        
          <td><code>rgba(0, 0, 0, .2)</code></td>
        
        <td><p>Box shadow color of the action sheet</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-box-shadow</code></td>
        
          <td><code>0 -1px 0 $action-sheet-wp-box-shadow-color</code></td>
        
        <td><p>Box shadow of the action sheet</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-title-padding</code></td>
        
          <td><code>11px 16px 17px</code></td>
        
        <td><p>Padding of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-title-font-size</code></td>
        
          <td><code>2rem</code></td>
        
        <td><p>Font size of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-title-color</code></td>
        
          <td><code>#4d4d4d</code></td>
        
        <td><p>Color of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-title-text-align</code></td>
        
          <td><code>$action-sheet-wp-text-align</code></td>
        
        <td><p>Text align of the action sheet title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-button-height</code></td>
        
          <td><code>4.8rem</code></td>
        
        <td><p>Height of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-button-text-color</code></td>
        
          <td><code>#4d4d4d</code></td>
        
        <td><p>Text color of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-button-font-size</code></td>
        
          <td><code>1.5rem</code></td>
        
        <td><p>Font size of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-button-padding</code></td>
        
          <td><code>0 16px</code></td>
        
        <td><p>Padding of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-button-text-align</code></td>
        
          <td><code>$action-sheet-wp-text-align</code></td>
        
        <td><p>Text align of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-button-background</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-button-background-activated</code></td>
        
          <td><code>$list-wp-activated-background-color</code></td>
        
        <td><p>Background color of the action sheet activated button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-icon-font-size</code></td>
        
          <td><code>2.4rem</code></td>
        
        <td><p>Font size of the icon in the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-icon-width</code></td>
        
          <td><code>2.3rem</code></td>
        
        <td><p>Width of the icon in the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-icon-text-align</code></td>
        
          <td><code>center</code></td>
        
        <td><p>Text align of the icon in the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-icon-vertical-align</code></td>
        
          <td><code>middle</code></td>
        
        <td><p>Vertical align of the icon in the action sheet button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$action-sheet-wp-icon-margin</code></td>
        
          <td><code>0 20px 0 0</code></td>
        
        <td><p>Margin of the icon in the action sheet button</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
</div>



<!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='../ActionSheetController'>ActionSheetController API Docs</a><!-- end content block -->


<!-- end body block -->


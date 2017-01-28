---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "alert"
title: "Alert"
header_sub_title: "Ionic API Documentation"
doc: "Alert"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/src/alert/basic"
angular_controller: APIDemoCtrl 
additional_preview_device_urls:
  - alert-with-text-input: /docs/v2/demos/src/alert/prompt/
  - alert-with-checkboxes: /docs/v2/demos/src/alert/checkbox/
  - alert-with-radio-buttons: /docs/v2/demos/src/alert/radio/
  - confirmation-alerts: /docs/v2/demos/src/alert/confirm/
---









<h1 class="api-title">
<a class="anchor" name="alert" href="#alert"></a>

Alert





</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/components/alert/alert.ts#L7">
Improve this doc
</a>






<p>An Alert is a dialog that  opens a dialog on top of the app&#39;s content that may
contain buttons, inputs, and text. Alerts are commonly used to present the user 
with information or to prompt the user to provide information or make a selection.</p>
<h3 id="creating-an-alert">Creating an Alert</h3>
<p>An Alert is defined by importing and creating an instance of AlertController
then calling <code>create(options)</code> on the instance. Alert options can also
be specified at a later time with <a href="#instance-members">instance methods</a>.
For a complete list of options see <a href="#alert-options">Alert Options</a> below.</p>
<p>To display an Alert call <code>present()</code> on a defined Alert. </p>
<h3 id="dismissing-an-alert">Dismissing an Alert</h3>
<p>A user must manually dismiss an Alert before they can resume interaction 
with the app. This is done by tapping one of the Alert&#39;s buttons, 
tapping the back button (Android), or tapping the background outside the 
Alert. To prevent tapping a button from dismissing the Alert,
set the handler function for that button to return <code>false</code>.</p>
<h3 id="handling-user-input">Handling User Input</h3>
<p>Alerts can include several different types of inputs, including text, radio
buttons, and checkboxes, whose data can be passed back to the app. Only one
type of Input is allowed per Alert; however, different types of text inputs 
can be mixed, such as <code>url</code>, <code>email</code>, <code>text</code>, etc. </p>
<p>If you require a complex form UI which doesn&#39;t fit within the guidelines of
an alert, it is recommended that you create a form inside a Modal instead.</p>
<p>The user&#39;s input will be passed as an argument to the handler function that&#39;s 
called when the Alert is dismissed. For example, the following handler function
will set <code>userInput</code> on the model of our component:</p>
<pre><code>handler: inputResult =&gt; {
  this.userInput = inputResult;
}
</code></pre>




<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<pre><code class="lang-ts">constructor(private alertCtrl: AlertController) {

}

presentAlert() {
  let options = {
    title: &#39;Low battery&#39;,
    subTitle: &#39;10% of battery remaining&#39;,
    buttons: [{
      text: &#39;Cancel&#39;,
      role: &#39;cancel&#39;,
      handler: () =&gt; {
        console.log(&#39;Cancel clicked&#39;);
      }
    },
    {
      text: &#39;OK&#39;,
      handler: () =&gt; {
        console.log(&#39;Buy clicked&#39;);
      }
    }]
  }
  let alert = this.alertCtrl.create(options);
  alert.present();
}
</code></pre>
<h3 id="alert-options">Alert options</h3>
<table>
<thead>
<tr>
<th>Property</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>title</td>
<td><code>string</code></td>
<td>The title for the alert.</td>
</tr>
<tr>
<td>subTitle</td>
<td><code>string</code></td>
<td>The subtitle for the alert.</td>
</tr>
<tr>
<td>message</td>
<td><code>string</code></td>
<td>The message for the alert.</td>
</tr>
<tr>
<td>cssClass</td>
<td><code>string</code></td>
<td>Additional classes for custom styles, separated by spaces.</td>
</tr>
<tr>
<td>inputs</td>
<td><code>Array</code></td>
<td>An array of inputs for the alert. See <a href="#input-options">Input Options</a>.</td>
</tr>
<tr>
<td>buttons</td>
<td><code>Array</code></td>
<td>An array of buttons for the alert. See <a href="#button-options">Button Options</a>.</td>
</tr>
<tr>
<td>enableBackdropDismiss</td>
<td><code>boolean</code></td>
<td>Whether the alert will be dismissed when the background is tapped.</td>
</tr>
</tbody>
</table>
<h3 id="input-options">Input options</h3>
<table>
<thead>
<tr>
<th>Property</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>type</td>
<td><code>string</code></td>
<td>The type of input - text, radio, checkbox, tel, number, etc.</td>
</tr>
<tr>
<td>name</td>
<td><code>string</code></td>
<td>The name for the input.</td>
</tr>
<tr>
<td>placeholder</td>
<td><code>string</code></td>
<td>The input&#39;s placeholder (for textual/numeric inputs)</td>
</tr>
<tr>
<td>value</td>
<td><code>string</code></td>
<td>The input&#39;s value. This will be passed to the handler when the Alert is dismissed.</td>
</tr>
<tr>
<td>label</td>
<td><code>string</code></td>
<td>The input&#39;s label (only for radio/checkbox inputs)</td>
</tr>
<tr>
<td>checked</td>
<td><code>boolean</code></td>
<td>Whether or not the input is checked by default.</td>
</tr>
<tr>
<td>id</td>
<td><code>string</code></td>
<td>The input&#39;s id.</td>
</tr>
</tbody>
</table>
<h3 id="button-options">Button options</h3>
<table>
<thead>
<tr>
<th>Property</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>text</td>
<td><code>string</code></td>
<td>The buttons displayed text.</td>
</tr>
<tr>
<td>handler</td>
<td><code>any</code></td>
<td>A callback function that is executed when the button is pressed.</td>
</tr>
<tr>
<td>cssClass</td>
<td><code>string</code></td>
<td>An additional CSS class for the button.</td>
</tr>
<tr>
<td>role</td>
<td><code>string</code></td>
<td>The buttons role - <code>null</code> or <code>cancel</code>.</td>
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

Sets the title of the Alert


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
        <p>Alert title</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="setSubTitle"></div>

<h3>
<a class="anchor" name="setSubTitle" href="#setSubTitle"></a>
<code>setSubTitle(subTitle)</code>
  

</h3>

Sets the subtitle of the Alert


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
        <p>Alert subtitle</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="setMessage"></div>

<h3>
<a class="anchor" name="setMessage" href="#setMessage"></a>
<code>setMessage(message)</code>
  

</h3>

Sets the body text of the Alert


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
        <p>Alert message content</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="addInput"></div>

<h3>
<a class="anchor" name="addInput" href="#addInput"></a>
<code>addInput(input)</code>
  

</h3>

Adds a new input to the Alert


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
        input
        
        
      </td>
      <td>
        
  <code>object</code>
      </td>
      <td>
        <p>Alert input</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="addButton"></div>

<h3>
<a class="anchor" name="addButton" href="#addButton"></a>
<code>addButton(button)</code>
  

</h3>

Adds a new button to the Alert


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
        
  <code>any</code>
      </td>
      <td>
        <p>Alert button</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="setCssClass"></div>

<h3>
<a class="anchor" name="setCssClass" href="#setCssClass"></a>
<code>setCssClass(cssClass)</code>
  

</h3>

Adds one or more new CSS classes to the Alert


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
        cssClass
        
        
      </td>
      <td>
        
  <code>string</code>
      </td>
      <td>
        <p>Set the CSS class names on the alert&#39;s outer wrapper.</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="present"></div>

<h3>
<a class="anchor" name="present" href="#present"></a>
<code>present(opts)</code>
  

</h3>

Shows the Alert instance to the user.



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
<p>If you want to start a page transition in your app from an Alert button&#39;s handler
function, it is important to keep in mind that the Alert dismissal and the 
page transition occur asynchronously. This may cause unexpected results, such as a 
janky page transition, since the page transition animation could start before the 
Alert has been fully dismissed from the view.</p>
<p>To prevent this, you should programmatically dismiss the Alert in the button&#39;s 
handler function using <code>dismiss()</code>, which returns a promise. You can then call the page
transition when the promise resolves to ensure everything happens in the expected order.</p>
<p>Also, the handler function must return <code>false</code>. This prevents Ionic from automatically
dismissing the Alert once the handler function has finished, which allows us to 
manually control the order of events.</p>
<p>For example, the following creates an Alert with a &#39;Transition Me!&#39; button whose 
handler function dismisses the Alert, then transitions to the previous page
in the app.</p>
<pre><code class="lang-ts">let alert = this.alertCtrl.create({
  title: &#39;Hello&#39;,
  buttons: [{
    text: &#39;Transition Me!&#39;,
    handler: () =&gt; {
      // begin the Alert&#39;s dimiss transition
      let navTransition = alert.dismiss();

      // start the page transition when dismissal of
      // the Alert is complete
      navTransition.then(() =&gt; {
        this.nav.pop();
      });

      // prevent Alert from being dismissed automatically
      return false;
    }
  }]
});

let alert = this.alertCtrl.create(options);

alert.present();
</code></pre>
<h2 id="common-usage-patterns">Common Usage Patterns</h2>
<h3 id="alert-with-text-input">Alert with Text Input</h3>
<p>Prompts offer a way to input data or information.  Often times  Prompts will be used to ask 
the user for a password before moving forward in an application’s flow.</p>
<pre><code>let options = {
  title: &#39;Login&#39;,
  message: &quot;Enter a name for this new album you&#39;re so keen on adding&quot;,
  inputs: [
    {
      name: &#39;title&#39;,
      placeholder: &#39;Title&#39;
    },
  ],
  buttons: [
    {
      text: &#39;Cancel&#39;,
      handler: data =&gt; {
        console.log(&#39;Cancel clicked&#39;);
      }
    },
    {
      text: &#39;Save&#39;,
      handler: data =&gt; {
        console.log(&#39;Saved clicked&#39;);
      }
    }
  ]
}
</code></pre>
<h3 id="confirmation-alerts">Confirmation Alerts</h3>
<p>Confirmation Alerts are used when the user is required to explicitly confirm a choice before 
progressing forward in the app. A common example of the Confirmation Alert is checking to make 
sure a user wants to delete or remove a contact from their address book.</p>
<pre><code>let options = {
  title: &#39;Use this lightsaber?&#39;,
  message: &#39;Do you agree to use this lightsaber to do good across the intergalactic galaxy?&#39;,
  buttons: [
    {
      text: &#39;Disagree&#39;,
      handler: () =&gt; {
        console.log(&#39;Disagree clicked&#39;);
      }
    },
    {
      text: &#39;Agree&#39;,
      handler: () =&gt; {
        console.log(&#39;Agree clicked&#39;);
      }
    }
  ]
}
</code></pre>
<h3 id="alert-with-radio-buttons">Alert with Radio Buttons</h3>
<p>Alerts can use the <a href="/docs/v2/components/#radio">Radio Button component</a> to 
offer the user several choices. Only one option can be chosen.</p>
<pre><code>let alert = this.alertCtrl.create();
alert.setTitle(&#39;Lightsaber color&#39;);

alert.addInput({
  type: &#39;radio&#39;,
  label: &#39;Blue&#39;,
  value: &#39;blue&#39;,
  checked: true
});

alert.addButton(&#39;Cancel&#39;);
alert.addButton({
  text: &#39;OK&#39;,
  handler: data =&gt; {
    this.testRadioResult = data;
  }
});
</code></pre>
<h3 id="alert-with-checkboxes">Alert with Checkboxes</h3>
<p>Alerts can use the <a href="/docs/v2/components/#checkbox">Checkbox component</a> to offer several choices. 
Multiple options can be chosen.</p>
<pre><code>let alert = this.alertCtrl.create();
alert.setTitle(&#39;Which planets have you visited?&#39;);

alert.addInput({
  type: &#39;checkbox&#39;,
  label: &#39;Alderaan&#39;,
  value: &#39;value1&#39;,
  checked: true
});

alert.addInput({
  type: &#39;checkbox&#39;,
  label: &#39;Bespin&#39;,
  value: &#39;value2&#39;
});

alert.addButton(&#39;Cancel&#39;);
alert.addButton({
  text: &#39;Okay&#39;,
  handler: data =&gt; {
    console.log(&#39;Checkbox data:&#39;, data);
  }
});
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
        <td><code>$alert-ios-max-width</code></td>
        
          <td><code>270px</code></td>
        
        <td><p>Max width of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-border-radius</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Border radius of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-background</code></td>
        
          <td><code>#f8f8f8</code></td>
        
        <td><p>Background color of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-box-shadow</code></td>
        
          <td><code>none</code></td>
        
        <td><p>Box shadow of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-head-padding</code></td>
        
          <td><code>12px 16px 7px</code></td>
        
        <td><p>Padding of the alert head</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-head-text-align</code></td>
        
          <td><code>center</code></td>
        
        <td><p>Text align of the alert head</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-title-margin-top</code></td>
        
          <td><code>8px</code></td>
        
        <td><p>Margin top of the alert title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-title-font-size</code></td>
        
          <td><code>17px</code></td>
        
        <td><p>Font size of the alert title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-title-font-weight</code></td>
        
          <td><code>600</code></td>
        
        <td><p>Font weight of the alert title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-sub-title-font-size</code></td>
        
          <td><code>14px</code></td>
        
        <td><p>Font size of the alert sub title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-sub-title-text-color</code></td>
        
          <td><code>#666</code></td>
        
        <td><p>Text color of the alert sub title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-message-padding</code></td>
        
          <td><code>0 16px 21px</code></td>
        
        <td><p>Padding of the alert message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-message-font-size</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Font size of the alert message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-message-text-align</code></td>
        
          <td><code>center</code></td>
        
        <td><p>Text align of the alert message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-message-text-color</code></td>
        
          <td><code>inherit</code></td>
        
        <td><p>Text color of the alert message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-message-padding-empty</code></td>
        
          <td><code>0 0 12px 0</code></td>
        
        <td><p>Padding of the alert empty message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-content-max-height</code></td>
        
          <td><code>240px</code></td>
        
        <td><p>Maximum height of the alert content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-input-margin-top</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Margin top of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-input-padding</code></td>
        
          <td><code>6px</code></td>
        
        <td><p>Padding on the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-input-border-color</code></td>
        
          <td><code>#ccc</code></td>
        
        <td><p>Border color of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-input-border</code></td>
        
          <td><code>$hairlines-width solid $alert-ios-input-border-color</code></td>
        
        <td><p>Border of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-input-border-radius</code></td>
        
          <td><code>4px</code></td>
        
        <td><p>Border radius of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-input-background-color</code></td>
        
          <td><code>#fff</code></td>
        
        <td><p>Background color of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-group-flex-wrap</code></td>
        
          <td><code>wrap</code></td>
        
        <td><p>Flex wrap of the alert button group</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-flex</code></td>
        
          <td><code>1 1 auto</code></td>
        
        <td><p>Flex of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-margin</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Margin of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-min-width</code></td>
        
          <td><code>50%</code></td>
        
        <td><p>Min width of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-min-height</code></td>
        
          <td><code>44px</code></td>
        
        <td><p>Minimum height of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-font-size</code></td>
        
          <td><code>17px</code></td>
        
        <td><p>Font size of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-text-color</code></td>
        
          <td><code>color($colors-ios, primary)</code></td>
        
        <td><p>Color of the text in the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-background-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-background-color-activated</code></td>
        
          <td><code>#e9e9e9</code></td>
        
        <td><p>Background color of the alert activated button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-border-width</code></td>
        
          <td><code>$hairlines-width</code></td>
        
        <td><p>Border width of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-border-color</code></td>
        
          <td><code>#dbdbdf</code></td>
        
        <td><p>Border color of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-border-radius</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Border radius of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-button-main-font-weight</code></td>
        
          <td><code>bold</code></td>
        
        <td><p>Font weight of the main text on the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-list-border-top</code></td>
        
          <td><code>$alert-ios-button-border-width $alert-ios-button-border-style $alert-ios-button-border-color</code></td>
        
        <td><p>Border top of the alert list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-radio-label-padding</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Padding on the label for the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-radio-label-text-color-checked</code></td>
        
          <td><code>$alert-ios-button-text-color</code></td>
        
        <td><p>Text color of the label for the checked radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-radio-min-width</code></td>
        
          <td><code>30px</code></td>
        
        <td><p>Min width of the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-radio-icon-top</code></td>
        
          <td><code>-7px</code></td>
        
        <td><p>Top of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-radio-icon-left</code></td>
        
          <td><code>7px</code></td>
        
        <td><p>Left of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-radio-icon-width</code></td>
        
          <td><code>6px</code></td>
        
        <td><p>Width of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-radio-icon-height</code></td>
        
          <td><code>12px</code></td>
        
        <td><p>Height of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-radio-icon-border-width</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border width of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-radio-icon-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-radio-icon-border-color</code></td>
        
          <td><code>$alert-ios-button-text-color</code></td>
        
        <td><p>Border color of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-radio-icon-transform</code></td>
        
          <td><code>rotate(45deg)</code></td>
        
        <td><p>Transform of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-label-padding</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Padding of the label for the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-label-text-color-checked</code></td>
        
          <td><code>initial</code></td>
        
        <td><p>Text color of the label for the checked checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-margin</code></td>
        
          <td><code>10px 6px 10px 16px</code></td>
        
        <td><p>Margin of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-size</code></td>
        
          <td><code>21px</code></td>
        
        <td><p>Size of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-border-width</code></td>
        
          <td><code>$hairlines-width</code></td>
        
        <td><p>Border width of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-border-radius</code></td>
        
          <td><code>50%</code></td>
        
        <td><p>Border radius of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-border-color-off</code></td>
        
          <td><code>$list-ios-border-color</code></td>
        
        <td><p>Border color of the checkbox in the alert when off</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-border-color-on</code></td>
        
          <td><code>color($colors-ios, primary)</code></td>
        
        <td><p>Border color of the checkbox in the alert when on</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-background-color-off</code></td>
        
          <td><code>$list-ios-background-color</code></td>
        
        <td><p>Background color of the checkbox in the alert when off</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-background-color-on</code></td>
        
          <td><code>color($colors-ios, primary)</code></td>
        
        <td><p>Background color of the checkbox in the alert when on</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-icon-top</code></td>
        
          <td><code>4px</code></td>
        
        <td><p>Top of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-icon-left</code></td>
        
          <td><code>7px</code></td>
        
        <td><p>Left of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-icon-width</code></td>
        
          <td><code>4px</code></td>
        
        <td><p>Width of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-icon-height</code></td>
        
          <td><code>9px</code></td>
        
        <td><p>Height of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-icon-border-width</code></td>
        
          <td><code>$alert-ios-checkbox-border-width</code></td>
        
        <td><p>Border width of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-icon-border-style</code></td>
        
          <td><code>$alert-ios-checkbox-border-style</code></td>
        
        <td><p>Border style of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-icon-border-color</code></td>
        
          <td><code>$background-ios-color</code></td>
        
        <td><p>Border color of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-ios-checkbox-icon-transform</code></td>
        
          <td><code>rotate(45deg)</code></td>
        
        <td><p>Transform of the icon in the checkbox alert</p>
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
        <td><code>$alert-md-max-width</code></td>
        
          <td><code>280px</code></td>
        
        <td><p>Max width of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-border-radius</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border radius of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-background-color</code></td>
        
          <td><code>#fafafa</code></td>
        
        <td><p>Background color of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-box-shadow-color</code></td>
        
          <td><code>rgba(0, 0, 0, .4)</code></td>
        
        <td><p>Box shadow color of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-box-shadow</code></td>
        
          <td><code>0 16px 20px $alert-md-box-shadow-color</code></td>
        
        <td><p>Box shadow of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-head-padding</code></td>
        
          <td><code>24px 24px 20px 24px</code></td>
        
        <td><p>Padding of the alert head</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-head-text-align</code></td>
        
          <td><code>left</code></td>
        
        <td><p>Text align of the alert head</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-title-font-size</code></td>
        
          <td><code>22px</code></td>
        
        <td><p>Font size of the alert title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-sub-title-font-size</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Font size of the alert sub title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-message-padding</code></td>
        
          <td><code>0 24px 24px 24px</code></td>
        
        <td><p>Padding of the alert message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-message-font-size</code></td>
        
          <td><code>15px</code></td>
        
        <td><p>Font size of the alert message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-message-text-color</code></td>
        
          <td><code>rgba(0, 0, 0, .5)</code></td>
        
        <td><p>Text color of the alert message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-message-padding-empty</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Padding of the alert empty message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-content-max-height</code></td>
        
          <td><code>240px</code></td>
        
        <td><p>Maximum height of the alert content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-input-border-width</code></td>
        
          <td><code>1px</code></td>
        
        <td><p>Border width of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-input-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-input-border-color</code></td>
        
          <td><code>#dedede</code></td>
        
        <td><p>Border color of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-input-text-color</code></td>
        
          <td><code>#000</code></td>
        
        <td><p>Text color of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-input-border-width-focused</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border width of the alert input when focused</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-input-border-style-focused</code></td>
        
          <td><code>$alert-md-input-border-style</code></td>
        
        <td><p>Border style of the alert input when focused</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-input-border-color-focused</code></td>
        
          <td><code>color($colors-md, primary)</code></td>
        
        <td><p>Border color of the alert input when focused</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-input-margin-top</code></td>
        
          <td><code>5px</code></td>
        
        <td><p>Margin top of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-input-margin-right</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Margin right of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-input-margin-bottom</code></td>
        
          <td><code>5px</code></td>
        
        <td><p>Margin bottom of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-input-margin-left</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Margin left of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-group-flex-wrap</code></td>
        
          <td><code>wrap-reverse</code></td>
        
        <td><p>Flex wrap of the alert button group</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-group-padding</code></td>
        
          <td><code>8px 8px 8px 24px</code></td>
        
        <td><p>Padding of the alert button group</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-group-justify-content</code></td>
        
          <td><code>flex-end</code></td>
        
        <td><p>Justify content of the alert button group</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-padding</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Padding of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-margin</code></td>
        
          <td><code>0 8px 0 0</code></td>
        
        <td><p>Margin of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-font-weight</code></td>
        
          <td><code>500</code></td>
        
        <td><p>Font weight of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-text-color</code></td>
        
          <td><code>color($colors-md, primary)</code></td>
        
        <td><p>Text color of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-background-color</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-background-color-activated</code></td>
        
          <td><code>rgba(158, 158, 158, .2)</code></td>
        
        <td><p>Background color of the alert activated button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-border-radius</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border radius of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-text-transform</code></td>
        
          <td><code>uppercase</code></td>
        
        <td><p>Text transform of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-button-text-align</code></td>
        
          <td><code>right</code></td>
        
        <td><p>Text align of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-list-border-top</code></td>
        
          <td><code>1px solid $alert-md-input-border-color</code></td>
        
        <td><p>Border top of the alert list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-list-border-bottom</code></td>
        
          <td><code>$alert-md-list-border-top</code></td>
        
        <td><p>Border bottom of the alert list</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-label-padding</code></td>
        
          <td><code>13px 26px</code></td>
        
        <td><p>Padding on the label for the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-label-text-color-checked</code></td>
        
          <td><code>$alert-md-button-text-color</code></td>
        
        <td><p>Text color of the label for the checked radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-top</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Top of the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-left</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Left of the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-width</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Width of the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-height</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Height of the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-border-width</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border width of the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-border-radius</code></td>
        
          <td><code>50%</code></td>
        
        <td><p>Border radius of the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-border-color-off</code></td>
        
          <td><code>darken($list-md-border-color, 40%)</code></td>
        
        <td><p>Border color of the alert radio when off</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-border-color-on</code></td>
        
          <td><code>$alert-md-button-text-color</code></td>
        
        <td><p>Border color of the alert radio when on</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-icon-top</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Top of the icon in the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-icon-left</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Left of the icon in the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-icon-width</code></td>
        
          <td><code>8px</code></td>
        
        <td><p>Width of the icon in the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-icon-height</code></td>
        
          <td><code>8px</code></td>
        
        <td><p>Height of the icon in the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-icon-border-radius</code></td>
        
          <td><code>$alert-md-radio-border-radius</code></td>
        
        <td><p>Border radius of the icon in the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-icon-transform-off</code></td>
        
          <td><code>scale3d(0, 0, 0)</code></td>
        
        <td><p>Transform of the icon in the alert radio when off</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-icon-transform-on</code></td>
        
          <td><code>scale3d(1, 1, 1)</code></td>
        
        <td><p>Transform of the icon in the alert radio when on</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-radio-icon-transition</code></td>
        
          <td><code>transform 280ms cubic-bezier(.4, 0, .2, 1)</code></td>
        
        <td><p>Transition of the icon in the alert radio</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-label-padding</code></td>
        
          <td><code>13px 26px</code></td>
        
        <td><p>Padding of the label for the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-label-text-color-checked</code></td>
        
          <td><code>initial</code></td>
        
        <td><p>Text color of the label for the checked checkbox in the  alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-top</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Top of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-left</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Left of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-width</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Width of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-height</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Height of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-border-width</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border width of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-border-radius</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border radius of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-border-color-off</code></td>
        
          <td><code>darken($list-md-border-color, 40%)</code></td>
        
        <td><p>Border color of the checkbox in the alert when off</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-border-color-on</code></td>
        
          <td><code>$alert-md-button-text-color</code></td>
        
        <td><p>Border color of the checkbox in the alert when on</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-icon-top</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Top of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-icon-left</code></td>
        
          <td><code>3px</code></td>
        
        <td><p>Left of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-icon-width</code></td>
        
          <td><code>6px</code></td>
        
        <td><p>Width of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-icon-height</code></td>
        
          <td><code>10px</code></td>
        
        <td><p>Height of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-icon-border-width</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border width of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-icon-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-icon-border-color</code></td>
        
          <td><code>color-contrast($colors-md, $alert-md-checkbox-border-color-on)</code></td>
        
        <td><p>Border color of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-md-checkbox-icon-transform</code></td>
        
          <td><code>rotate(45deg)</code></td>
        
        <td><p>Transform of the icon in the checkbox alert</p>
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
        <td><code>$alert-wp-backdrop-background</code></td>
        
          <td><code>#fff</code></td>
        
        <td><p>Background of the alert backdrop</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-width</code></td>
        
          <td><code>100%</code></td>
        
        <td><p>Width of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-max-width</code></td>
        
          <td><code>520px</code></td>
        
        <td><p>Max width of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-border-width</code></td>
        
          <td><code>1px</code></td>
        
        <td><p>Border width of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-border-color</code></td>
        
          <td><code>color($colors-wp, primary)</code></td>
        
        <td><p>Border color of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-border-radius</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Border radius of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-background</code></td>
        
          <td><code>#e6e6e6</code></td>
        
        <td><p>Background color of the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-head-padding</code></td>
        
          <td><code>20px 22px 5px 22px</code></td>
        
        <td><p>Padding of the alert head</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-head-text-align</code></td>
        
          <td><code>left</code></td>
        
        <td><p>Text align of the alert head</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-title-font-size</code></td>
        
          <td><code>20px</code></td>
        
        <td><p>Font size of the alert title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-title-font-weight</code></td>
        
          <td><code>400</code></td>
        
        <td><p>Font weight of the alert title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-sub-title-font-size</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Font size of the alert sub title</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-message-padding</code></td>
        
          <td><code>0 22px 8px 22px</code></td>
        
        <td><p>Padding of the alert message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-message-padding-empty</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Padding of the alert empty message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-message-text-color</code></td>
        
          <td><code>#000</code></td>
        
        <td><p>Text color of the alert message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-message-font-size</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Font size of the alert message</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-content-max-height</code></td>
        
          <td><code>240px</code></td>
        
        <td><p>Maximum height of the alert content</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-input-margin</code></td>
        
          <td><code>5px 0 5px 0</code></td>
        
        <td><p>Margin of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-input-padding</code></td>
        
          <td><code>0 8px</code></td>
        
        <td><p>Padding on the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-input-border-width</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border width of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-input-border-style</code></td>
        
          <td><code>$alert-wp-border-style</code></td>
        
        <td><p>Border style of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-input-border-color</code></td>
        
          <td><code>$input-wp-border-color</code></td>
        
        <td><p>Border color of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-input-border-color-focused</code></td>
        
          <td><code>color($colors-wp, primary)</code></td>
        
        <td><p>Border color of the alert input when focused</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-input-line-height</code></td>
        
          <td><code>3rem</code></td>
        
        <td><p>Line height of the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-input-text-color</code></td>
        
          <td><code>#000</code></td>
        
        <td><p>Color of the text in the alert input</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-padding</code></td>
        
          <td><code>5px</code></td>
        
        <td><p>Padding of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-width</code></td>
        
          <td><code>49.5%</code></td>
        
        <td><p>Width of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-border-radius</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Border radius of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-font-weight</code></td>
        
          <td><code>400</code></td>
        
        <td><p>Font weight of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-text-color</code></td>
        
          <td><code>#000</code></td>
        
        <td><p>Color of the text in the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-background</code></td>
        
          <td><code>#b8b8b8</code></td>
        
        <td><p>Background color of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-background-activated</code></td>
        
          <td><code>color-shade($alert-wp-button-background)</code></td>
        
        <td><p>Background color of the activated alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-margin-right</code></td>
        
          <td><code>1%</code></td>
        
        <td><p>Margin right of the alert button</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-group-padding</code></td>
        
          <td><code>20px 22px 20px 22px</code></td>
        
        <td><p>Padding of the alert button group</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-group-justify-content</code></td>
        
          <td><code>flex-end</code></td>
        
        <td><p>Justify content of the alert button group</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-group-flex-wrap</code></td>
        
          <td><code>wrap-reverse</code></td>
        
        <td><p>Flex wrap of the alert button group</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-group-vertical-width</code></td>
        
          <td><code>100%</code></td>
        
        <td><p>Vertical width of the vertical alert button group</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-button-group-vertical-margin-top</code></td>
        
          <td><code>5px</code></td>
        
        <td><p>Margin top of the vertical alert button group</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-background</code></td>
        
          <td><code>color($colors-wp, primary)</code></td>
        
        <td><p>Background color of the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-border-color</code></td>
        
          <td><code>$input-wp-border-color</code></td>
        
        <td><p>Border color of the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-label-padding</code></td>
        
          <td><code>13px 26px</code></td>
        
        <td><p>Padding of the label for the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-label-text-color-checked</code></td>
        
          <td><code>$alert-wp-button-text-color</code></td>
        
        <td><p>Text color of the label for the checked radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-top</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Top of the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-left</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Left of the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-width</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Width of the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-height</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Height of the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-border-width</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border width of the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-border-radius</code></td>
        
          <td><code>50%</code></td>
        
        <td><p>Border radius of the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-border-color</code></td>
        
          <td><code>$input-wp-border-color</code></td>
        
        <td><p>Border color of the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-icon-top</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Top of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-icon-left</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Left of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-icon-width</code></td>
        
          <td><code>8px</code></td>
        
        <td><p>Width of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-icon-height</code></td>
        
          <td><code>8px</code></td>
        
        <td><p>Height of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-radio-icon-border-radius</code></td>
        
          <td><code>$alert-wp-radio-border-radius</code></td>
        
        <td><p>Border radius of the icon in the radio alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-label-padding</code></td>
        
          <td><code>13px 26px</code></td>
        
        <td><p>Padding of the label for the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-label-text-color-checked</code></td>
        
          <td><code>initial</code></td>
        
        <td><p>Text color of the label for the checked checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-top</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Top of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-left</code></td>
        
          <td><code>13px</code></td>
        
        <td><p>Left of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-width</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Width of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-height</code></td>
        
          <td><code>16px</code></td>
        
        <td><p>Height of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-border-width</code></td>
        
          <td><code>2px</code></td>
        
        <td><p>Border width of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-border-radius</code></td>
        
          <td><code>0</code></td>
        
        <td><p>Border radius of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-border-color</code></td>
        
          <td><code>$input-wp-border-color</code></td>
        
        <td><p>Border color of the checkbox in the alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-background-off</code></td>
        
          <td><code>transparent</code></td>
        
        <td><p>Background color of the checkbox in the alert when off</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-background-on</code></td>
        
          <td><code>color($colors-wp, primary)</code></td>
        
        <td><p>Background color of the checkbox in the alert when on</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-icon-top</code></td>
        
          <td><code>-2px</code></td>
        
        <td><p>Top of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-icon-left</code></td>
        
          <td><code>3px</code></td>
        
        <td><p>Left of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-icon-width</code></td>
        
          <td><code>6px</code></td>
        
        <td><p>Width of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-icon-height</code></td>
        
          <td><code>12px</code></td>
        
        <td><p>Height of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-icon-border-width</code></td>
        
          <td><code>1px</code></td>
        
        <td><p>Border width of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-icon-border-style</code></td>
        
          <td><code>solid</code></td>
        
        <td><p>Border style of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-icon-border-color</code></td>
        
          <td><code>color-contrast($colors-wp, $alert-wp-checkbox-background-on)</code></td>
        
        <td><p>Border color of the icon in the checkbox alert</p>
</td>
      </tr>
      
      <tr>
        <td><code>$alert-wp-checkbox-icon-transform</code></td>
        
          <td><code>rotate(45deg)</code></td>
        
        <td><p>Transform of the icon in the checkbox alert</p>
</td>
      </tr>
      
    </tbody>
  </table>
  
</div>



<!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='../AlertController'>Alert Controller API Docs</a><!-- end content block -->


<!-- end body block -->


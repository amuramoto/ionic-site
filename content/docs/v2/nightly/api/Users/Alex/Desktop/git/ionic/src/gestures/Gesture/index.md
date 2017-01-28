---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "gesture"
title: "Gesture"
header_sub_title: "Ionic API Documentation"
doc: "Gesture"
docType: "class"

---









<h1 class="api-title">
<a class="anchor" name="gesture" href="#gesture"></a>

Gesture





</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/gestures/gesture.ts#L1">
Improve this doc
</a>






<p>Ionic supports a variety of touch events and gestures. Basic gestures can 
be accessed from HTML by binding to <code>tap</code>, <code>press</code>, <code>pan</code>, <code>swipe</code>, <code>rotate</code>, 
and <code>pinch</code> events. You can also add the <code>tappable</code> attribute to any element to
remove the browser&#39;s 300ms tap delay that some elements, such as divs, experience.</p>




<!-- @usage tag -->

<h2><a class="anchor" name="usage" href="#usage"></a>Usage</h2>

<pre><code class="lang-html">&lt;ion-card (tap)=&quot;tapEvent($event)&quot;&gt;
  &lt;ion-item&gt;
    Tapped: {{tap}} times
  &lt;/ion-item&gt;
&lt;/ion-card&gt;
</code></pre>
<h3 id="using-rotate-and-pinch">Using Rotate and Pinch</h3>
<p>The <code>rotate</code> and <code>pinch</code> gestures are disabled by default because they are blocking. 
To enable, import and create an instance of <code>Gesture</code>, then assign an event listener 
to the desired DOM element.</p>
<p>Event listeners can be added for any event supported by hammer.js, e.g. <code>pinchstart</code>, 
<code>pinchend</code>, <code>rotatestart</code>, <code>rotateend</code>, etc. For a full list, see the 
<a href="http://hammerjs.github.io/recognizer-pinch/">hammer.js recognizers docs</a>. </p>
<pre><code class="lang-ts">import { Gesture } from &#39;ionic-angular&#39;;

...

export class HomePage {

  //get elementRef for DOM element we want to assign to
  @ViewChild(&#39;myTouchElement&#39;) element;
  gesture: Gesture

...

  ionViewDidLoad() {
    //create gesture obj w/ ref to DOM element
    this.gesture = new Gesture(this.element.nativeElement);    

    //listen for the gesture
    this.gesture.listen();

    //turn on listening for pinch or rotate events
    this.gesture.on(&#39;pinch&#39;, e =&gt; console.log(e));

    //add event listener
    this.gesture.on(&#39;pinch&#39;, () =&gt; console.log(&#39;pinch end event&#39;));
  }

}
</code></pre>




<!-- @property tags -->



<!-- instance methods on the class -->

<h2><a class="anchor" name="instance-members" href="#instance-members"></a>Instance Members</h2>

<div id="options"></div>

<h3>
<a class="anchor" name="options" href="#options"></a>
<code>options(opts)</code>
  

</h3>

Sets the options for an instance of `Gesture`. 


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
        
  <code>object</code>
      </td>
      <td>
        <p>The options object. For a complete list of options, see the <a href="http://hammerjs.github.io/api/#hammerdefaults">Hammer.js Docs</a></p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="on"></div>

<h3>
<a class="anchor" name="on" href="#on"></a>
<code>on(type,&nbsp;callback)</code>
  

</h3>

Attaches an event handler to an instance of `Gesture`.


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
        type
        
        
      </td>
      <td>
        
  <code>string</code>
      </td>
      <td>
        <p>The gesture type to listen for</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        callback
        
        
      </td>
      <td>
        
  <code>function</code>
      </td>
      <td>
        <p>A callback function to execute when the gesture occurs</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="off"></div>

<h3>
<a class="anchor" name="off" href="#off"></a>
<code>off(type,&nbsp;callback)</code>
  

</h3>

Detaches an event handler from an instance of `Gesture`.


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
        type
        
        
      </td>
      <td>
        
  <code>string</code>
      </td>
      <td>
        <p>The gesture type to detach</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        callback
        
        
      </td>
      <td>
        
  <code>function</code>
      </td>
      <td>
        <p>A callback function to execute when the gesture is detached</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="listen"></div>

<h3>
<a class="anchor" name="listen" href="#listen"></a>
<code>listen()</code>
  

</h3>

Sets an instance of `Gesture` to listen for events.











<div id="unlisten"></div>

<h3>
<a class="anchor" name="unlisten" href="#unlisten"></a>
<code>unlisten()</code>
  

</h3>

Stops an instance of `Gesture` from listening for events.











<div id="destroy"></div>

<h3>
<a class="anchor" name="destroy" href="#destroy"></a>
<code>destroy()</code>
  

</h3>

Destroys an instance of `Gesture`.














<!-- related link --><!-- end content block -->


<!-- end body block -->


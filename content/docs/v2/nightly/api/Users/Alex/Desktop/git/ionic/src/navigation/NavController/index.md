---
layout: "v2_fluid/docs_base"
version: "nightly"
versionHref: "/docs/v2/nightly"
path: ""
category: api
id: "navcontroller"
title: "NavController"
header_sub_title: "Ionic API Documentation"
doc: "NavController"
docType: "class"

---









<h1 class="api-title">
<a class="anchor" name="nav-controller" href="#nav-controller"></a>

NavController





</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic/edit/master//Users/Alex/Desktop/git/ionic/src/navigation/nav-controller.ts#L4">
Improve this doc
</a>






<p>NavController is the base class for navigation controller components like
<a href="../Nav/"><code>Nav</code></a> and <a href="../../tabs/Tab/"><code>Tab</code></a>. You use navigation controllers
to navigate to <a href="#view-creation">pages</a> in your app.</p>
<p>For more information, see the <a href="/docs/v2/navigation/navigation-controller">Navigation Controller doc</a>.</p>




<!-- @usage tag -->


<!-- @property tags -->



<!-- instance methods on the class -->

<h2><a class="anchor" name="instance-members" href="#instance-members"></a>Instance Members</h2>

<div id="viewDidLoad"></div>

<h3>
<a class="anchor" name="viewDidLoad" href="#viewDidLoad"></a>
<code>viewDidLoad</code>
  

</h3>

Observable to be subscribed to when a component is loaded.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Observable</code> <p>Returns an observable</p>


</div>




<div id="viewWillEnter"></div>

<h3>
<a class="anchor" name="viewWillEnter" href="#viewWillEnter"></a>
<code>viewWillEnter</code>
  

</h3>

Observable to be subscribed to when a component is about to be loaded.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Observable</code> <p>Returns an observable</p>


</div>




<div id="viewDidEnter"></div>

<h3>
<a class="anchor" name="viewDidEnter" href="#viewDidEnter"></a>
<code>viewDidEnter</code>
  

</h3>

Observable to be subscribed to when a component has fully become the active component.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Observable</code> <p>Returns an observable</p>


</div>




<div id="viewWillLeave"></div>

<h3>
<a class="anchor" name="viewWillLeave" href="#viewWillLeave"></a>
<code>viewWillLeave</code>
  

</h3>

Observable to be subscribed to when a component is about to leave, and no longer active.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Observable</code> <p>Returns an observable</p>


</div>




<div id="viewDidLeave"></div>

<h3>
<a class="anchor" name="viewDidLeave" href="#viewDidLeave"></a>
<code>viewDidLeave</code>
  

</h3>

Observable to be subscribed to when a component has fully left and is no longer active.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Observable</code> <p>Returns an observable</p>


</div>




<div id="viewWillUnload"></div>

<h3>
<a class="anchor" name="viewWillUnload" href="#viewWillUnload"></a>
<code>viewWillUnload</code>
  

</h3>

Observable to be subscribed to when a component is about to be unloaded and destroyed.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Observable</code> <p>Returns an observable</p>


</div>




<div id="parent"></div>

<h3>
<a class="anchor" name="parent" href="#parent"></a>
<code>parent</code>
  

</h3>

The parent navigation instance. If this is the root nav, then
it'll be `null`. A `Tab` instance's parent is `Tabs`, otherwise
the parent would be another nav, if it's not already the root nav.











<div id="push"></div>

<h3>
<a class="anchor" name="push" href="#push"></a>
<code>push(page,&nbsp;params,&nbsp;opts)</code>
  

</h3>

Push a new component onto the current navigation stack. Pass any aditional information
along as an object. This additional information is accessible through NavParams



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
        page
        
        
      </td>
      <td>
        
  <code>Page</code>
      </td>
      <td>
        <p>The page component class you want to push on to the navigation stack</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        params
        
        
      </td>
      <td>
        
  <code>object</code>
      </td>
      <td>
        <p>Any nav-params you want to pass along to the next view<strong class="tag">Optional</strong></p>

        
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




<div id="insert"></div>

<h3>
<a class="anchor" name="insert" href="#insert"></a>
<code>insert(insertIndex,&nbsp;page,&nbsp;params,&nbsp;opts)</code>
  

</h3>

Inserts a component into the nav stack at the specified index. This is useful if
you need to add a component at any point in your navigation stack.




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
        insertIndex
        
        
      </td>
      <td>
        
  <code>number</code>
      </td>
      <td>
        <p>The index where to insert the page.</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        page
        
        
      </td>
      <td>
        
  <code>Page</code>
      </td>
      <td>
        <p>The component you want to insert into the nav stack.</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        params
        
        
      </td>
      <td>
        
  <code>object</code>
      </td>
      <td>
        <p>Any nav-params you want to pass along to the next page.<strong class="tag">Optional</strong></p>

        
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




<div id="insertPages"></div>

<h3>
<a class="anchor" name="insertPages" href="#insertPages"></a>
<code>insertPages(insertIndex,&nbsp;insertPages,&nbsp;opts)</code>
  

</h3>

Inserts an array of components into the nav stack at the specified index.
The last component in the array will become instantiated as a view,
and animate in to become the active view.



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
        insertIndex
        
        
      </td>
      <td>
        
  <code>number</code>
      </td>
      <td>
        <p>The index where you want to insert the page.</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        insertPages
        
        
      </td>
      <td>
        
  <code>array</code>
      </td>
      <td>
        <p>An array of objects, each with a <code>page</code> and optionally <code>params</code> property.</p>

        
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




<div id="pop"></div>

<h3>
<a class="anchor" name="pop" href="#pop"></a>
<code>pop(opts)</code>
  

</h3>

Call to navigate back from a current component. Similar to `push()`, you
can also pass navigation options.



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




<div id="popToRoot"></div>

<h3>
<a class="anchor" name="popToRoot" href="#popToRoot"></a>
<code>popToRoot(opts)</code>
  

</h3>

Navigate back to the root of the stack, no matter how far back that is.



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




<div id="remove"></div>

<h3>
<a class="anchor" name="remove" href="#remove"></a>
<code>remove(startIndex,&nbsp;removeCount,&nbsp;opts)</code>
  

</h3>

Removes a page from the nav stack at the specified index.



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
        startIndex
        
        
      </td>
      <td>
        
  <code>number</code>
      </td>
      <td>
        <p>The starting index to remove pages from the stack. Default is the index of the last page.<strong class="tag">Optional</strong></p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        removeCount
        
        
      </td>
      <td>
        
  <code>number</code>
      </td>
      <td>
        <p>The number of pages to remove, defaults to remove <code>1</code>.<strong class="tag">Optional</strong></p>

        
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
        <p>Any options you want to use pass to transtion.<strong class="tag">Optional</strong></p>

        
      </td>
    </tr>
    
  </tbody>
</table>





<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Promise</code> <p>Returns a promise which is resolved when the transition has completed.</p>


</div>




<div id="removeView"></div>

<h3>
<a class="anchor" name="removeView" href="#removeView"></a>
<code>removeView(viewController,&nbsp;opts)</code>
  

</h3>

Removes the specified view controller from the nav stack.



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
        viewController
        
        
      </td>
      <td>
        
  <code>ViewController</code>
      </td>
      <td>
        <p>The viewcontroller to remove.<strong class="tag">Optional</strong></p>

        
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
        <p>Any options you want to use pass to transtion.<strong class="tag">Optional</strong></p>

        
      </td>
    </tr>
    
  </tbody>
</table>





<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Promise</code> <p>Returns a promise which is resolved when the transition has completed.</p>


</div>




<div id="setRoot"></div>

<h3>
<a class="anchor" name="setRoot" href="#setRoot"></a>
<code>setRoot(pageOrViewCtrl,&nbsp;params,&nbsp;opts)</code>
  

</h3>

Set the root for the current navigation stack.


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
        pageOrViewCtrl
        
        
      </td>
      <td>
        
  <code>string</code>|<code>ViewController</code>
      </td>
      <td>
        <p>The name of the component you want to push on the navigation stack.</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        params
        
        
      </td>
      <td>
        
  <code>object</code>
      </td>
      <td>
        <p>Any nav-params you want to pass along to the next view.<strong class="tag">Optional</strong></p>

        
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
        <p>Any options you want to use pass to transtion.<strong class="tag">Optional</strong></p>

        
      </td>
    </tr>
    
  </tbody>
</table>





<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Promise</code> <p>Returns a promise which is resolved when the transition has completed.</p>


</div>




<div id="setPages"></div>

<h3>
<a class="anchor" name="setPages" href="#setPages"></a>
<code>setPages(pages,&nbsp;opts)</code>
  

</h3>

Set the views of the current navigation stack and navigate to the
last view. By default animations are disabled, but they can be enabled
by passing options to the navigation controller.You can also pass any
navigation params to the individual pages in the array.



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
        pages
        
        
      </td>
      <td>
        
  <code>array</code>
      </td>
      <td>
        <p>An array of objects, each with a <code>page</code> and optionally <code>params</code> property to load in the stack.</p>

        
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




<div id="getByIndex"></div>

<h3>
<a class="anchor" name="getByIndex" href="#getByIndex"></a>
<code>getByIndex(index)</code>
  

</h3>




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
        index
        
        
      </td>
      <td>
        
  <code>number</code>
      </td>
      <td>
        <p>The index of the page to get.</p>

        
      </td>
    </tr>
    
  </tbody>
</table>





<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>ViewController</code> <p>Returns the view controller that matches the given index.</p>


</div>




<div id="getActive"></div>

<h3>
<a class="anchor" name="getActive" href="#getActive"></a>
<code>getActive()</code>
  

</h3>








<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>ViewController</code> <p>Returns the active page&#39;s view controller.</p>


</div>




<div id="isActive"></div>

<h3>
<a class="anchor" name="isActive" href="#isActive"></a>
<code>isActive(view)</code>
  

</h3>

Returns if the given view is the active view or not.


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
        view
        
        
      </td>
      <td>
        
  <code>ViewController</code>
      </td>
      <td>
        
        
      </td>
    </tr>
    
  </tbody>
</table>





<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>boolean</code> 

</div>




<div id="getPrevious"></div>

<h3>
<a class="anchor" name="getPrevious" href="#getPrevious"></a>
<code>getPrevious(view)</code>
  

</h3>

Returns the view controller which is before the given view controller.
If no view controller is passed in, then it'll default to the active view.


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
        view
        
        
      </td>
      <td>
        
  <code>ViewController</code>
      </td>
      <td>
        
        
      </td>
    </tr>
    
  </tbody>
</table>





<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>viewController</code> 

</div>




<div id="first"></div>

<h3>
<a class="anchor" name="first" href="#first"></a>
<code>first()</code>
  

</h3>

Returns the first view controller in this nav controller's stack.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>ViewController</code> 

</div>




<div id="last"></div>

<h3>
<a class="anchor" name="last" href="#last"></a>
<code>last()</code>
  

</h3>

Returns the last page in this nav controller's stack.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>ViewController</code> 

</div>




<div id="indexOf"></div>

<h3>
<a class="anchor" name="indexOf" href="#indexOf"></a>
<code>indexOf(view)</code>
  

</h3>

Returns the index number of the given view controller.


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
        view
        
        
      </td>
      <td>
        
  <code>ViewController</code>
      </td>
      <td>
        
        
      </td>
    </tr>
    
  </tbody>
</table>





<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>number</code> 

</div>




<div id="length"></div>

<h3>
<a class="anchor" name="length" href="#length"></a>
<code>length()</code>
  

</h3>

Returns the number of views in this nav controller.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>number</code> <p>The number of views in this stack, including the current view.</p>


</div>




<div id="getViews"></div>

<h3>
<a class="anchor" name="getViews" href="#getViews"></a>
<code>getViews()</code>
  

</h3>

Returns the current stack of views in this nav controller.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Array&lt;ViewController&gt;</code> <p>the stack of view controllers in this nav controller.</p>


</div>




<div id="getActiveChildNav"></div>

<h3>
<a class="anchor" name="getActiveChildNav" href="#getActiveChildNav"></a>
<code>getActiveChildNav()</code>
  

</h3>

Returns the active child navigation.











<div id="isTransitioning"></div>

<h3>
<a class="anchor" name="isTransitioning" href="#isTransitioning"></a>
<code>isTransitioning()</code>
  

</h3>

Returns if the nav controller is actively transitioning or not.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>boolean</code> 

</div>




<div id="canSwipeBack"></div>

<h3>
<a class="anchor" name="canSwipeBack" href="#canSwipeBack"></a>
<code>canSwipeBack()</code>
  

</h3>

If it's possible to use swipe back or not. If it's not possible
to go back, or swipe back is not enabled, then this will return `false`.
If it is possible to go back, and swipe back is enabled, then this
will return `true`.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>boolean</code> 

</div>




<div id="canGoBack"></div>

<h3>
<a class="anchor" name="canGoBack" href="#canGoBack"></a>
<code>canGoBack()</code>
  

</h3>

Returns `true` if there's a valid previous page that we can pop
back to. Otherwise returns `false`.






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>boolean</code> 

</div>







<!-- related link -->

<h2><a class="anchor" name="related" href="#related"></a>Related</h2>

<a href='/docs/v2/navigation'>Navigation Docs</a>,
<a href='../../components/nav/Nav'>Nav API Docs</a><!-- end content block -->


<!-- end body block -->


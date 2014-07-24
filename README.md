Marketo SlideShare Tracking
========================

Capture the page change event from a SlideShare embed into Marketo.

Install
========================

Load the slidetrack.js file into the design studio.

Update the path to the sidetrack.js file in the code below.
Update the slideshareName value.  This will be used as part of the simulated click that will show up for tracking.  Don't include spaces.
Put the following lines into the page's custom head section. 

```HTML
<script src='https://app.marketo.com/js/public/jquery-latest.min.js' ></script>
<script src='** PATH TO THE slidetrack.js FILE' ></script>
<script type="text/javascript"> var slideshareName = "MySlideShareName";</script>
```

In the body of the page you will have a HTML area with the embed code from SlideShare.  The source (src) url for the iframe will look something like this.

http://www.slideshare.net/slideshow/embed_code/31683337

You will need to append the following value to the end of the source URL

?jsapi=true

So the final result will look like this.

http://www.slideshare.net/slideshow/embed_code/31683337?jsapi=true

Searching for the clicks
========================

The simulated link click is to /slideshare/**slideshareName**/page/**page number**

With the **slideshareName** being replaced with the value you specified above and **page number** being replaced with the page you are changing to.

Note that this is a change event so you won't get one for the load of the first page unless you navigate back to it from another page.

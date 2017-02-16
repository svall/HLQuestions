### HLQuestions

_1. HTTP vs. HTTPS:  _
HTTPS is secure, data sent is encrypted. HTTP does not guarantee secure communication of data.

**2. HTTP GET vs. POST:  **
GET method is used by clients to make server requests, it is for information that exists. 
POST method sends data (ex. signup forms where user information is sent to a database).

**3. Status code 2 vs. 4:  **
The codes signal the client-server interaction result. 2 successful interaction, 4 signals an error on the client side.

**4. Ajax:  **
It is asynchronous JavaScript XML used with jQuery. It is a technique to send and retrieve information in the background without refreshing the page (a way around JavaScript being a single-thread language). The data can be received in a JSON file format, which is cleaner and easier to use. It is useful with pages like Twitter, where you only need small sets of data to be modified, without needing to reload the entire page content.

**5. Responsive design:  **
All browsers have different setups. Responsive design for websites is ensuring all compatibility issues that can make the page look different across browsers is considered. Going further, different platforms, such as mobile, are the next step.

**6. CSS rules:  **
`div {background:#fff;}`  --> refers to all html div tags   
`#div {background:#fff;}`  --> refers to the div tag with the id “div”  
`.div {background:#fff;}`  --> refers to the div tags with the class “div”  

**7. Script tags:    **
`<script src=”http://example.com/whatever.js”> </script> 
<script>var whatever = true</script>`

  The first snippet is a linking an html file to a JS file, the second is defining a JS variable directly inside the html file.

**8. Code snippets:  **
`var x = function() { return 1+1; }();  
var y = function() { return 1+1; };`

  The first is a function expression with a self-invoking function (the function call at the end). The second is a regular function expression. 


##PRACTICAL 

**1. Write HTML/CSS to draw the following scene (inline css is fine if you want):  **

  1. One red box, 200x200 pixels
  2. One blue box, 200x200 pixels
  3. One green box, 100x100 pixels
  4. The green box should be centered inside the red box
  5. The red and blue boxes should not overlap

  Code in practical.html and style.css files.


**2. Tracking pixels:  **

 ** a. Why is caching a problem for the analytics company?:  **
  I believe caching can be a problem because the visitor has the data requested in memory, so when they visit the site, the request does not have to be sent to the server, the information will be pulled from local memory. It can create a problem for the tracker if the requests are not sent to the server every time. 

 ** b. How could you prevent browser caching? (use any technique(s) you want):  **
  I know meta tags are used to prevent caching, but I am not very familiar with techniques to prevent caching.

  **c. What will happen if the customer’s website is served over HTTPS? How could you modify the tracking pixel to fix that?:   **
  I have not used tracking pixels, but I would imagine it is possible to target both with one.

  **d. List some information the tracking company could collect (ex: IP address):  **
  I believe information, such as:
  * time on site or bouce rate
  * number of visits
  * event tracking

  **e. List some additional information (if any) that could be collected if a script tag is used instead of an img tag:     **
  If a script tag is used, I believe more of the users behavior can be looked into. Using a script tag, event listeners can be set up to capture more information. An image tag is more of a static element. I have not used pixel tracking, but I do know JavaScript has very useful functionality to understand how the user interacts with a website.

**3. Harder!
The following image tag appears somewhere on some webpage. The rest of the page is valid HTML, but otherwise unknown.
Every 2 seconds:
­ Check whether the image is viewable**
­ If yes, write “visible” to the console (that is, window.console)
­ If no, do nothing
the image is “viewable” if any part of it appears on the screen (so if the image is entirely above or below the viewport, then the user cannot see it, so it is not considered “viewable”)**

  Steps:
  -  The first step would be to get the window viewport and image location (top and left)
  - Second, set up a function that will be called every two seconds with a timer
  - Third, compare the img to the window location using an if statement with conditionals
  - Fourth, log result.

  ```<script>
    // assumming I can get the window viewport wiht window.height
    var windView = window.height;
    var imagView = document.getElementById('myimage');

    // checkTime() sets a timer to run every 2 seconds
    function checkTime() {
      // console.log("checking");
      if(imagView > viewportHeight || imagView < viewportHeight) {
        console.log("Visible");
      }
    }
    window.onload = setInterval(checkTime, 2000);
  </script>```



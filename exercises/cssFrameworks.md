# Exercise: CSS Frameworks

In this exercise we explore the use of Frameworks in web development. Frameworks make up a large section of the web development community, since they offer a quicker development option, as well as provide a similar design language.

Start by downloading the starter file located here: [Frameworks Starter Files]().

## Part One - Look over the Default Styles

1. Look over your starter files, **open the directory in VS Code** (right click the folder or inside of it, and -- if it's a choice -- choose Open with Code... if not, use the open folder command from within VS Code), and preview the “default-start.html”. We will be using the Live Server extension for the exercise, so at this point, launch the Live Server and observe how the default-start.html appears in your web browser.

2. Go back to VS Code and look at the code. Notice we have a style.css file in our **css** folder. There are some basic CSS directives applied to our **default-start.html** file, nothing too fancy.

3. The body of the **default-start.html** file is pretty basic. To simplify our development for the exercise, we are not using images, but rely on a third party site called **[placeholder.com](https://placeholder.com/)**, this is a handy utility site that just provides placeholder images to whatever size you want. The remainder of the content is relatively basic, we have an HTML Table in the Main, as well as a basic form (I know we’ve not covered forms, but they are a standard part of web development). 

## Part Two - Bootstrap

1. Open a new browser window or tab, and go to https://getbootstrap.com/, click the “**Getting Started**” button on the page. We will be doing the **Quick Start**, and using a *CDN (Content Delivery Network)* and not downloading the framework locally. 

2. Back in VS Code, make a copy of the **default-start.html** file and rename to **bootstrap.html**, and open this file. 

3. In the **HEAD** section of the **bootstrap.html** file paste the CSS code from the Bootstrap Quick Start into your file (Be sure this line goes BEFORE your style.css):

   `<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" integrity="sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z" crossorigin="anonymous">`

4. Next, below the CSS link, paste the following 3 lines of Javascript:
   `<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script><script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js" integrity="sha384-9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu735Sk7lN" crossorigin="anonymous"></script><script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js" integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOMMV+rV" crossorigin="anonymous"></script>`

5. Now go to your web browser and load the **bootstrap.html** file in a new window or tab. Notice the differences between base styles and the bootstrap applied styles.

6. Base CSS changes are fine, but let's talk about some of the more interesting aspects of having a framework. Let's look at a NavBar and Carousel.

7. In VS Code, copy the bootstrap.html and name the new file bootstrap-navbar.html, and in the new file empty out the body content.

8. Let's first start with the NavBar, go to https://getbootstrap.com/docs/4.5/components/navbar/ and we will copy the first example code into our newly empties body:

   ```
   <nav class="navbar navbar-expand-lg navbar-light bg-light">
     <a class="navbar-brand" href="#">Navbar</a>
     <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
       <span class="navbar-toggler-icon"></span>
     </button>
   
     <div class="collapse navbar-collapse" id="navbarSupportedContent">
       <ul class="navbar-nav mr-auto">
         <li class="nav-item active">
           <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
         </li>
         <li class="nav-item">
           <a class="nav-link" href="#">Link</a>
         </li>
         <li class="nav-item dropdown">
           <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
             Dropdown
           </a>
           <div class="dropdown-menu" aria-labelledby="navbarDropdown">
             <a class="dropdown-item" href="#">Action</a>
             <a class="dropdown-item" href="#">Another action</a>
             <div class="dropdown-divider"></div>
             <a class="dropdown-item" href="#">Something else here</a>
           </div>
         </li>
         <li class="nav-item">
           <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
         </li>
       </ul>
       <form class="form-inline my-2 my-lg-0">
         <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
         <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
       </form>
     </div>
   </nav>
   ```

9. Now save and reload this page and see the results. Resize the browser window, notice what happens to the navigation? Go back into VS Code and look closely at the code, do you see the large number of CSS classes that each element has? All those classes are what makes the navbar function, there are also a number of data and aria attributes used as well. Feel free to experiment with the navbar, add some links, or even try to add another pulldown.

10. Lastly, let's look at a Slideshow Carousel. In VS Code, let's copy the current bootstrap-navbar.html and rename the new file to bootstrap-carousel.html. In the new file, clear out the body tag.

11. Now we will add in our **styles.css** into this document.

12. In your Bootstrap window, go to this url: https://getbootstrap.com/docs/4.5/components/carousel/. You can refer to this page for more information about the Carousel, but we'll be putting in some of our own code. The code below is based off the first sample, but I replaced the images with 5 slides from placeholder.com.

    ```
    <div id="container">
    	<div id="slideshow">
    		<div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel">
    			<div class="carousel-inner">
    				<div class="carousel-item active">
    					<img src="https://via.placeholder.com/500x300/0000FF/808080?text=Slide1" class="d-block w-100"
    						alt="...">
    				</div>
    				<div class="carousel-item">
    					<img src="https://via.placeholder.com/500x300/00AAFF/808080?text=Slide2" class="d-block w-100"
    						alt="...">
    				</div>
    				<div class="carousel-item">
    					<img src="https://via.placeholder.com/500x300/00FFAA/000000?text=Slide3" class="d-block w-100"
    						alt="...">
    				</div>
    				<div class="carousel-item">
    					<img src="https://via.placeholder.com/500x300/AADD00/000000?text=Slide4" class="d-block w-100"
    						alt="...">
    				</div>
    				<div class="carousel-item">
    					<img src="https://via.placeholder.com/500x300/22FADA/000000?text=Slide5" class="d-block w-100"
    						alt="...">
    				</div>
    			</div>            
    		</div>            
    	</div>
    </div>
    
    ```

13. Save and load this file in your browser, observer the glory of a fully functional carousel slideshow!

14. Now, can you alter this slideshow and change into a slideshow with controls? The code is on the Bootstrap page, see if you can make that work.



## Part Three - Materialize

1. Open a new browser window or tab, and go to https://materializecss.com/, click the “**Get Started**” button on the page. We will also be using the CDN version of Materialize. 

2. Back in VS Code, make a copy of the **default-start.html** file and rename to materialize.html, and open this file. 

3. In the **HEAD** section of the materialize.html file paste the CSS and Javascript code from the CDN section into your file *(Be sure the CSS goes BEFORE your style.css, and JavaScript after)*:
   `<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">`
   `<script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>`

4. Now go to your web browser and load the **materialize.html** file in a new window or tab. Notice the differences between three files.

5. Notice how just by including the frameworks, the differences can be quite dramatic. What do you notice?

6. 

   

   
   

## Part Four - Font Awesome

1. For our last part of the lab, we'll take a look at Font Awesome. Font Awesome isn't an extensive style library like the others, but it does provide an important function, which is to provide easy to use iconography for your web site.

2. In VS Code, open the **navbar-starter.html** file. To keep things simple, I have an embedded CSS style that formats our header, nav and main elements on our simple page. 

3. Open this page in a browser window or tab. Observe how it's just a simple page with a header, some text and 2 buttons. It's rather plain, so we'll add some imagery to make our links and options look much better.

4. Back in VS Code, copy the **navbar-starter.html** file to **fontawesome.html**.

5. In a web browser window or tab, go to https://fontawesome.com/. We will refer back to this site for finding icons. They don't provide a easy to get to CDN link, so we'll use another resource to get a CDN, open a new tab or window and go to https://cdnjs.com/libraries/font-awesome.

6. From cdnjs, copy the first css link, and paste into the HEAD section of your fontawesome.html file, once again, be sure this is before your style.css link.
   `https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.14.0/css/all.min.css`

7. Let's enhance one of our links in the nav bar. First, go back to the window you opened to https://fontawesome.com, and in the search box in the header, type in "instagram" and click the search button. In the search results, click the first matching result.

8. From the result, you will see that various styles the icon has, now click the "Start Using This Icon". A dialog appears with a snippet of code for this icon, copy the code:

   `<i class="fab fa-instagram"></i>`

9. Go back to VS Code and your fontawesome.html file. Locate the link for Instagram, and add this code in front of the "Instagram" text for the link, it should now look like the following:

   `<a href="#"><i class="fab fa-instagram"></i> Instagram</a>`

10. Save and load the page in a web browser. Notice how the link looks now?

11. Let's add another icon to our **Help** button, go back to the fontawesome site, and now search for "**help**", a large number of results comes back for this simple search term, but we'll pick the "question-circle". Once again, click on the icon and get the code from the "Start Using This Icon" button. 

12. Back in VS Code, find our help button and add the code to the front of our text:

    `<button><i class="fas fa-question-circle"></i> Help</button>`

13. Now reload the page and you should see the button now show the icon before the text.

14. Now it's time for you to complete the rest. Go forth and search for icons to use for the rest of the links in the navbar and the last email button. Feel free to add any additional buttons or icons to your file.









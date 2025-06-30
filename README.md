CSS selector syntax:


selector{
property1: value1;
property2: value2;
}


CSS can be provided in 3 ways: inline, internal, external

Inline CSS : We give CSS to HTML elements with style in HTML tag itself. Example:-

 <h1 style="color: blue; font-size: 34px">
      HTML & CSS Sandbox - Implementing CSS
    </h1>

 <h3 style="color: aqua; text-decoration: underline">This is heading</h3>




Internal CSS - Using internal and external CSS will separating CSS from HTML. Internal CSS is placed in <style> tag enclosed in <head> tag. Example:-

<head>
      <style>
      h4 {
        color: brown;
        font-size: 75px;
      }
      p {
        color: chartreuse;
      }
    </style>
  </head>




Full example:-

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <style>
      h4 {
        color: brown;
        font-size: 75px;
      }
      p {
        color: chartreuse;
      }
    </style>
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h5 style="color: blue; font-size: 34px">
      HTML & CSS Sandbox - Implementing CSS
    </h5>
    <h3 style="color: aqua; text-decoration: underline">This is heading</h3>

    <h4>Hello World</h4>
    <p>
      Construction of the mausoleum was completed in 1648, but work continued on
      other phases of the project for another five years. The first ceremony
     </p>
    <p>
      The Qutb Minar, also spelled Qutub Minar and Qutab Minar, is a minaret and
      victory tower comprising the Qutb complex, which lies at the site of
    </p>
  </body>
</html>


External CSS - creating a file (filename of your choice but the file extension should be css) and adding css selectors to it.




Selectors

Selectors are of 6 types: - Type Selectors, Class Selectors, ID Selectors, Descendants, html,body & Selector, Multiple Selectors.

selector{
property1: value1;
property2: value2;
}


Type selector example:- 

h2{
color: red;
font-size: 50px;
}

p{
color: brown;
font-size: 45px;
}




Class and ID selectors example:-

HTML document:-


 <!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Basic Selectors</h1>
    <div id="container">
      <div>
        <h2 class="sporty">Keeping it Sporty</h2>
        <p>Clothing to keep you active and healthy</p>
        <a href="#">View Collections</a>
      </div>
      <div>
        <h2 class="casual">Keeping it Casual</h2>
        <p>Clothing to keep you comfortable</p>
        <a href="#">View Collections</a>
      </div>
      <div>
        <h2 class="formal">Keeping it Formal</h2>
        <p>Clothing to keep you sharp</p>
        <a href="#">View Collections</a>
      </div>
    </div>
<p>Paragraph outside container id div</p>
  </body>
</html>




style.css file: -

/* Global selector*/
body{
    font-family: 'Arial', sans-serif;
}

/* Class selectors*/
.sporty{
    color: coral;
}
.casual{
    color: aqua;
}
.formal{
    color: blue;
}

/* ID selectors*/

#container{
    max-width: 600px;
    margin: 100px auto;
    padding: 20px;
}

/* Multiple Selector*/

.sporty, .casual,.formal{
    font-size: 35px;
    font-family: 'Times New Roman', Times, serif;
    font-weight: bold;
}

/*Descendant*/

#container p{
background-color: aquamarine;
}

Multiple selector are used when we want 1 or more classes or ids with common styles.
ID selector style starts with # and followed by he id name given in HTML.
Class selector style starts with . and followed by he class name given in HTML.
Descendant selector is the main id and class followed by tags shown above.

Specificity ( in the example below 'div' with 'id' as container p tag has more specificity than just the p tag. Hence, p tags under container div is having backgroundcolor  aquamarine and paragraph outside div of id as container will have background color darkcyan. So, '#container p ' overrides 'p' css.

#container p{
background-color: aquamarine;
}

p{
    background-color: darkcyan;
}



Global Selectors

Global selectors include body and html tag. Example below:-

body{
    font-family: 'Arial', sans-serif;
}

The entire children in the body tag will be have font family of Arial. If Arial doesn't exist uses 'sans-serif'.






Fonts

Some system safe fonts include Arial (sans-serif) , Verdana (sans-serif), Tahoma (sans-serif), Trebuchet (sans-serif), Times New Roman (serif), Georgia (serif)
, Garamond (serif), Courier New (monospace), Brush Script (cursive).
New Fonts can be imported to the HTML file using <link> or the CSS file using @import. Go to the website ' https://fonts.google.com/ '. Search for 'Poppins'. Click on 'Poppins' and click on 'Get Font' button. Click on 'Get Embed Code' button. Click on 'Change styles ' button. and toggle the button for fonts those are  required.
Place the link tags in the ' https://fonts.google.com ' in <head> tag in HTML. Example this piece of code in head tag.

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">




Full example

index.html file code:-

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="container">
      <div>
        <h2 class="sporty">Keep It Sporty</h2>
        <p>Clothing to keep you active and healthy</p>
        <a href="#">View Collection</a>
      </div>
      <div>
        <h2 class="casual">Keep It Casual</h2>
        <p>Clothing to keep you comfortable</p>
        <a href="#">View Collection</a>
      </div>
      <div>
        <h2 class="formal">Keep It Formal</h2>
        <p>Clothing to keep you looking sharp</p>
        <a href="#">View Collection</a>
      </div>
    </div>
  </body>
</html>





style.css file code :- 

body{
    font-family: 'Poppins', sans-serif;
}

p{
    font-weight: 600;
}









Font/Text properties

Font properties include font-family, font-size, font-weight, font-style, font-variant, line-height, letter-spacing, word-spacing, text-align, text-decoration, text-transform, text-indent. In the below example: -

body{
    font-family: 'Poppins', 'Arial', 'Times New Roman' sans-serif;
}

body elements will have font family of Poppins, if Poppins no there then Arial font family will be selected, if Arial doesn't exist then font family of Times New Roman
will be selected, if font family Times New Roman doesn't exist then it will have font family of sans-serif. 

font-size given to html element ( h2 in the below example ) can have different values like small, medium, x-large etc.  font-weight determines how bold and lighter should be the text or content given with font weight. font weight can have 300, 500, 600, bold, bolder etc  ( h2 in the below example ).  font-style determines whether the content should be normal or italic etc. font-variant is of small-caps (which puts all the text in uppercase and the first letter of each word will be little bit bigger than the rest). font-variant can have different values like normal, small-caps etc. in the below example for h2. 

 
 
h2{
    font-size: medium;
    font-weight: 900;
    font-style: normal;
    font-variant: small-caps;
}



We can provide font-style , font-variant, font-weight, font-size, font-family in single 'font' property (in this format) . example:-

h2{
font: italic small-caps 700 26px Arial;
}


text-decoration is having different values dashed, dotted, underline etc. text-transform can have value of uppercase, lowercase etc. Example below:-

h2{
    font-size: medium;
    font-weight: 900;
    font-style: normal;
    font-variant: small-caps;

    text-decoration: underline;
    text-transform: uppercase;
}






Full example:-

html file:-


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="container">
      <div>
        <h2 class="sporty">Keep It Sporty</h2>
        <p>Clothing to keep you active and healthy</p>
        <a href="#">View Collection</a>
      </div>
      <div>
        <h2 class="casual">Keep It Casual</h2>
        <p>Clothing to keep you comfortable</p>
        <a href="#">View Collection</a>
      </div>
      <div>
        <h2 class="formal">Keep It Formal</h2>
        <p>Clothing to keep you looking sharp</p>
        <a href="#">View Collection</a>
      </div>
    </div>
  </body>
</html>



style.css

body{
    font-family: 'Poppins', 'Arial', 'Times New Roman' sans-serif;
   line-height: 40px;
}

p{
    font-weight: 600;
}

h2{
    font-size: medium;
    font-weight: 900;
    font-style: normal;
    font-variant: small-caps;

    /* font: italic small-caps 700 26px Arial; */
    text-decoration: underline;
    text-transform: uppercase;
    text-indent: 50px;
    letter-spacing: 2px;
    word-spacing: 5px;
    text-align: center;
}

a{
  text-decoration: none;  
}



letter-spacing puts space between letters and word spacing between words.  text-align aligns text to center, left, right (In the above example aligns text to center).  line-height puts space between lines ( line-height: 40px; in the above example means space between lines 40px).







Colors

colors can be used to text colors (example:- color:red ), give background colors (example:- background-color:red ), give border colors (example:- border:red ), give outline colors (example:- outline:red ), give box drop shadows (example:- box-shadow:red ), give text drop shadows (example:- text-shadow:red ), fill used to svg fill colors (example:- fill:red )

(  https://htmlcolorcodes.com/color-names/  ) this site provides 147 color names used.
Hexadecimal values used instead of color name. Hexadecimal is a combination of 6 numbers and alphabets. Hexadecimal is made up of 6 digits organized in pairs of RGB. Hexadecimal range from 00 to FF where 00 means no intensity and FF means maximum internsity( Hexadecimal is of this format #AA3939 , where #AA3939 AA denotes red, first 39 denotes green and second 39 denotes blue.) Each colors are a combination red green blue combination with range of res green and blue values in the hexadecimal we can have wide range of colors). letters in hexadecimal represents intensity greater than 9. A represents 10, B represents 11 and so on until F which represents 15.
RGB values are made of 3 pairs of 3 digits from 0 to 255. O means no intensity and 255 means maximum intensity. rgba exists where a denotes alpha (transparency) example:- rgba(0,0,0,0.5) .
Black RGB value is 0,0,0. White RGB value is 255,255,255. Red RGB value is 255,255,0. Green RGB value is 0,255,0. Sky Blue value is 0,255,255. Purple value is 255,0,255. Dark blue value is 0,0,255.
opacity ranges from 0 to 1. Example:=

style.css file:- 


body {
  font-family: Arial, sans-serif;
  background-color: rgb(255, 255, 255);
}

/* Color names*/
.sporty{
  color:red
}

/* Color names*/
.casual{
  color: #0000FF;
}
.card{
  color: rgba(0,0,0,0.5);
}
.card-2{
  background-color: #000;
  color: #fff;
  opacity: 0.5;
}


index.html file


 <!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="container">
      <div class="card">
        <h2 class="sporty">Keep It Sporty</h2>
        <p>Clothing to keep you active and healthy.</p>
        <a href="#">View Collection</a>
      </div>

      <div class="card">
        <h2 class="casual">Keep It Casual</h2>
        <p>Clothing to keep you comfortable and stylish.</p>
        <a href="#">View Collection</a>
      </div>

      <div class="card">
        <h2 class="formal">Keep It Formal</h2>
        <p>Clothing to keep you looking sharp.</p>
        <a href="#">View Collection</a>
      </div>
      <div class="card-2">
        <p>
          Taj Mahal - Construction of the mausoleum was completed in 1648, but
          work continued on other phases of the project for another five years.
          The first ceremony held at the mausoleum was an observance by Shah
          Jahan, on 6 February 1643, of the 12th anniversary of the death of
          Mumtaz Mahal. The Taj Mahal complex is believed to have been completed
          in its entirety in 1653 at a cost estimated at the time to be around
          ₹5 million, which in 2023 would be approximately ₹35 billion (US$77.8
          million).
        </p>
      </div>
    </div>
  </body>
</html>






rgba is used when background color is added to div where rgba doesn't effect text only the background is effected.





Specificity

Specificity is an algorithm that calculates the weight that is applied to a given CSS declaration. If more than one css is provided to elements which css will apply depends on the specificity. Specificity is in the following order
1. Inline CSS ( style attribute)
2. ID (#)
3. Class (.)
4. Element


If more than one same css property to element is given then the resent one works. Example:-

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="container">
      <h1>HTML & CSS Sandbox - Inheritance & Specificity</h1>
    </div>
  </body>
</html>


style.css

body {
  font-family: Arial, sans-serif;
}
h1{
  color: red;
}
h1{
  color: blue;
}

here h1 element is given color red and blue. Since blue is the recent css color hence h1 element will have blue color.


Example:-

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="container">
      <h1>HTML & CSS Sandbox - Inheritance & Specificity</h1>
    </div>
  </body>
</html>


style.css

body {
  font-family: Arial, sans-serif;
}
.container h1{
  color: red;
}
h1{
  color: blue;
}

In the above example class(container) is having high priority than h1 element even though color blue is recent , So, the heading h1 element has color red.
In the below example:-

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="container">
      <h1 id="heading" class="heading">
        HTML & CSS Sandbox - Inheritance & Specificity
      </h1>
    </div>
  </body>
</html>


style.css

body {
  font-family: Arial, sans-serif;
}
/* .container h1{
  color: red;
} */
 
#heading{
  color: purple;
}
.heading{
  color: aquamarine;
}
h1{
  color: blue;
}



Since ID has higher specificity than class and element color purple comes for h1 heading.
In the below example we have given inline element so, inline has more specificity than ID, class and element. Hence heading will have yellow color. Example:-

 

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="container">
      <h1 style="color: yellow" id="heading" class="heading">
        HTML & CSS Sandbox - Inheritance & Specificity
      </h1>
    </div>
  </body>
</html>



style.css

body {
  font-family: Arial, sans-serif;
}
/* .container h1{
  color: red;
} */
 
#heading{
  color: purple;
}
.heading{
  color: aquamarine;
}
h1{
  color: blue;
}



But if we give !important to the css then that will have more specificity. In the below example heading will have blue color . Hence the heading element specified with important and given blue color has more specificity.  Example:-


index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="container">
      <h1 style="color: yellow" id="heading" class="heading">
        HTML & CSS Sandbox - Inheritance & Specificity
      </h1>
    </div>
  </body>
</html>




style.css


body {
  font-family: Arial, sans-serif;
}
/* .container h1{
  color: red;
} */
 
#heading{
  color: purple;
}
.heading{
  color: aquamarine;
}
h1{
  color: blue !important;
}







Background
Adding background image. (background-image: url('./hero.jpg');) adds the background image by giving the path of image in url. background-repeat set as no-repeat so image will not be repeated   ( background-repeat: no-repeat ) , since by defaultis background-repeat is repeat. (  background-size: cover )  background-size given cover will cover the image on the entire page in web browser.  ( background-position: center ) will put the images center part. ( background-position: 200px 500px ) if we give background-position 200px and 500px . Since the first pixel is 200px it moves the image 200px from the x axis and second pixel shift 500px from y axis.
Instead of giving these (  background-image: url('./hero.jpg'), background-repeat: no-repeat, background-position: center, background-size: cover  ) we can specify in one property ( background: url('./hero.jpg') no-repeat center/cover ). ( background-attachment: scroll ) when text is there to scroll then we add background-attachment as scroll so the full text is visible.



index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="hero">
      <h1>Welcome</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus molestias
        dicta excepturi, odit accusamus facere necessitatibus ab.
      </p>
    </div>
  </body>
</html>




style.css

body {
  font-family: Arial, sans-serif;
  margin: 0;
}

.hero {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0 20px;
  /* background-image: url('./hero.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center; */
  background: url('./hero.jpg') no-repeat center/cover;
  background-attachment: scroll;
}

.hero h1 {
  font-size: 40px;
  margin-bottom: 20px;
}

.hero p {
  text-align: center;
  font-size: 2rem;
}





Linear Gradient

 ( background: linear-gradient(to bottom, lightblue, darkblue) ) gives shades of 2 colors here light blue and dark blue . to bottom signifies the linear gradient should show to bottom.  We can change the direction of gradient (  background: linear-gradient(to left, lightgreen, darkblue))




index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="hero">
      <h1>Welcome</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus molestias
        dicta excepturi, odit accusamus facere necessitatibus ab.
      </p>
    </div>
  </body>
</html>




style.css


body {
  font-family: Arial, sans-serif;
  margin: 0;
}

.hero {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0 20px;

  /*Linear gradient*/
  background: linear-gradient(to bottom, lightblue, darkblue);
}

.hero h1 {
  font-size: 40px;
  margin-bottom: 20px;
}

.hero p {
  text-align: center;
  font-size: 2rem;
}






Styling Links

states
a:link      Normal unvisited link
a:hover     Link when hovered
a:active    Moment link is clicked
a:focus     Moment link receives focus
a:visited   Link user has visited


a {
  text-decoration: none;
  color:green
}

here  the default anchor tag text in webpage will have no underline (since text-decoration: none ) and color of text initially is assigned to green in the above example.

a:hover {
  color: red;
}

a:hover when we hover over the text in anchor tag in webpage the color becomes red


a:active {
  color: purple;
}

a:active when clicking the text in anchor tag in the web page color becomes purple for  quite short time



a:focus{
  color: yellow;
}

when we click on the link the link text in anchor is highlighted with yellow color as per the above example. But when we click outside the anchor tag text the color initial which is green is retained.


a:visited{
  color: aqua;
}

when we have clicked the link before then the a tag text will turn aqua because the link is visited.






Font awesome

Go to this website https://cdnjs.com/  and search for font and click on font-awesome.
Copy the link tag. From this link https://fontawesome.com/start  copy the icon which you want and copy the icon class name.


index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css"
      integrity="sha512-Evv84Mr4kqVGRNSgIGL/F/aIDqQb7xQ2vcrdIwxfjThSH8CSR7PBEakCr51Ck+w+/U6swU2Im1vVX0SVk9ABhg=="
      crossorigin="anonymous"
      referrerpolicy="no-referrer"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Font Awesome</h1>
    <h3>Icon Example</h3>
    <i class="fas fa-home"></i>
    <i class="fas fa-check"></i>
    <i class="fas fa-times"></i>
    <i class="fas fa-exclamation"></i>
    <i class="fas fa-exclamation-triangle"></i>
    <i class="fas fa-info"></i>
    <i class="fas fa-info-circle"></i>
    <i class="fas fa-question-circle"></i>
    <i class="fas fa-question"></i>

    <h3>Social media icons</h3>
    <i class="fab fa-facebook"></i>
    <i class="fab fa-twitter"></i>
    <i class="fab fa-linkedin"></i>
    <i class="fab fa-instagram"></i>
    <i class="fab fa-youtube"></i>

    <h3>Font awesome different size</h3>
    <i class="fas fa-check fa-2x"></i>
    <i class="fas fa-check fa-4x"></i>
    <i class="fas fa-check fa-5x"></i>
    <i class="fas fa-check fa-10x"></i>
  </body>
</html>




style.css


body {
  font-family: Arial, sans-serif;
}

.fa-facebook{
  color: blue;
  font-size: 50px;
}







Basic Challenge



index.html


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Lato:wght@100;300;400;700;900&family=Poppins:wght@300;400;500;600;700;800;900&display=swap"
      rel="stylesheet"
    />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <header class="header">
      <h1>Sneaker Hut</h1>
    </header>

    <nav>
      <ul class="main-menu">
        <li><a href="#">Jordans</a></li>
        <li><a href="#">Nike Air Max</a></li>
        <li><a href="#">Nike Air Force</a></li>
        <li><a href="#">Adidas Top Tens</a></li>
        <li><a href="#">Adidas Shell Toe</a></li>
        <li><a href="#">Reebok Classics</a></li>
      </ul>
    </nav>

    <section>
      <p class="lead">
        We have the best selection for old school and new era sneakers
      </p>

      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam
        accusamus, vel delectus consectetur, hic inventore fuga numquam quaerat
        aperiam reiciendis expedita pariatur quia ratione tempora illo ea
        labore, nesciunt perspiciatis dolor harum? Saepe enim, porro eaque ut
        quisquam laboriosam ducimus.
      </p>
    </section>
  </body>
</html>





style.css


body{
    font-family: 'Lato', sans-serif;
    font-size: 18px;
    line-height: 1.6;
}

.header {
background-color: #5e175b;
color: #fff;
}

.header h1{
    text-align: center;
    font-size: 40px;
    text-indent: 20px;
}
a{
    text-decoration: none; /*To remove underline from a tag*/
    color: #333;
}
a:hover{
color: rebeccapurple;
}
a:active{
    color: red;
}
ul{
    list-style: none; /*To remove bullets from li tag*/
    padding: 0;
}

ul.main-menu{
background-color: #f4f4f4;
text-indent: 10px;
text-transform: uppercase;
}

p.lead{
    font-size: 20px;
    color:rebeccapurple;
    font-weight: bold;
}






Box Model

padding - space between content and border.
border - separates the padding and margin.
Margin - space outside of border.

A web page can be considered as a rectangle box. blue color in the box is the content ( which can be any form of content like text and images ).
padding is the inner spacing between element and border. Border need not have to be visible,  but the border layer is actually there. The outer space outside border is the margin.

Box model properties

width -  (is from left to right the size) , if we give width:50%; the width is of strict 50%
max-width - (if max-width: 600px; ) then width can have till 600px and less.
min-width - (if min-width: 200px; ) then width can have till 200px and more.
height -  (is from top to bottom the size) , if we give height:50%; the height is of strict 50%
max-height - (if max-height: 600px; ) then height can have till height and less.
min-height - (if min-height: 200px; ) then height can have till 200px and more.

padding - is the space between border and content. padding can be padding-top, padding-right, padding-bottom,  padding-left.
margin - is the space between border and main window size. margin can be margin-top, margin-right, margin-bottom,  margin-left.

border - if you want you can set border. Border has the following properties border, border-style (border-style can have value dotted , dashed), border-color (border-color can have different colors) , border-width (border-width is the thickness of border).





Sizing


index.html


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Sizing & Overflow</h1>
    <div class="box box-1">
      <h3>Box 1</h3>
      <p>
        Following the Bangladesh Liberation war in 1972, a structure consisting
        of a black marble plinth with a reversed rifle, capped by a war helmet
        and bounded by four eternal flames, was built beneath the archway.
      </p>
    </div>
    <div class="box box-2">
      <h3>Box 2</h3>
      <p>
        Following the Bangladesh Liberation war in 1972, a structure consisting
        of a black marble plinth with a reversed rifle, capped by a war helmet
        and bounded by four eternal flames, was built beneath the archway.
      </p>
    </div>
    <div class="box box-3">
      <h3>Box 3</h3>
      <p>
        Following the Bangladesh Liberation war in 1972, a structure consisting
        of a black marble plinth with a reversed rifle, capped by a war helmet
        and bounded by four eternal flames, was built beneath the archway.
      </p>
    </div>
  </body>
</html>


style.css

body {
  font-family: 'Poppins', sans-serif;
}

.box{
  background-color: darkblue;
  color: white;
  padding: 20px 20px 20px 20px;
  border: 5px solid green;
  margin: 30px 30px 30px 30px;
}




Overflow

overflow css used when the content is more and cannot afford in the html page.
  ( overflow: scroll ) here the scroll bar appears. If overflow:hidden provided then the text outside the html element will be cut and only that space will be shown.
overflow-x : scroll (scrolls over x axis) and overflow-y: scroll  (scrolls over y axis) exists

style.css


body {
  font-family: 'Poppins', sans-serif;
}

.box{
  background-color: darkblue;
  color: white;
  padding: 20px 20px 20px 20px;
  border: 5px solid green;
  margin: 30px 30px 30px 30px;
}
.box-1{
  width: 200px;
  height: 200px;
   /* overflow: scroll; */
  overflow: hidden;
}

.box-2{
width: 50%;
}

.box-2 p{
  width: 50%;
}

.box-3{
  max-width: 800px;
  min-width: 500px;
}



width:50% given to div box-2 will have 50% of the width size. 

In the below css given to p (paragraph) of div with class box-2.

.box-2 p{
  width: 50%;
}


max-width: 800px; provides width to maximum 800px and less
mi-width:500x provides width to minimum of 500px where width is 500px and more.






Padding

index.html


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Padding</h1>
    <div class="box">
      <h2>Box One</h2>
      <p>
        Construction of the Burj Khalifa began in 2004, with the exterior
        completed five years later in 2009. The primary structure is reinforced      </p>
    </div>
  </body>
</html>



style.css


body {
  font-family: 'Poppins', sans-serif;
}

.box{
background-color: darkblue;
  color: white;
  /* padding: 20px; */
  width: 300px;
  padding-top: 20px;
  padding-right: 40px;
  padding-bottom: 70px;
  padding-left: 80px;
}


 padding: 20px; for div with class 'box' will have padding-top, padding-right, padding-left, padding-bottom each with 20px.

  For padding-top: 20px; from the border to the content top will have 20px
 For padding-right: 40px; from the border to the content right will have 40px
 For padding-bottom: 70px; from the border to the content bottom will have 70px
 For padding-left: 80px; from the border to the content left will have 80px


Instead of specifying padding-top, padding-right, padding-bottom, padding-left , we can specify in just padding property.

.box{
  background-color: darkblue;
  color: white;
  /* padding: 20px; */
  width: 300px;
  /* padding-top: 20px;
  padding-right: 40px;
  padding-bottom: 70px;
  padding-left: 80px; */
  padding: 20px 40px 70px 80px;
}



padding: 20px 40px;   means top as well as bottom will be 20px and right as well as left will be 40px.






Margin


index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Margin</h1>
    <div class="box box1">
      <h2>Box-1</h2>
      <p>
        The Taj Mahal 'Crown of the Palace' is an ivory-white marble mausoleum
        on the right bank of the river Yamuna in Agra, Uttar Pradesh, India. It
        was commissioned in 1631 by the fifth Mughal emperor, Shah Jahan
      </p>
    </div>
    <div class="box box2">
      <h2>Box-2</h2>
      <p>
        The Burj Khalifa is a skyscraper in Dubai, United Arab Emirates. It is
        the world's tallest structure. With a total height of 829.8 m (2,722 ft,
        or just over half a mile) and a roof height
      </p>
    </div>
    <div class="box box3">
      <h2>Box-3</h2>
      <p>
        The Statue of Liberty (Liberty Enlightening the World; French: La
        Liberté éclairant le monde) is a colossal neoclassical sculpture on
        Liberty Island in New York Harbor, within New York City.
      </p>
    </div>
  </body>
</html>


style.css

body {
  font-family: 'Poppins', sans-serif;
}
h2,p{
  margin: 0;
}
.box{
   background-color: coral;
  max-width: 400px;
  margin: 20px;
  padding: 20px;
}
.box h2{
  margin-bottom: 20px;
}
.box-2{
  margin-top: 20px;
  margin-right: 40px;
  margin-bottom: 60px;
  margin-left: 80px;
}

.box-3{
  margin-left: -30px;
}
.box-1{
  margin: 100px auto;
}

In the below code, the default margin of h2 and p (since by default h2 and p has margin) will reset and will have no margin.

 h2,p{
  margin: 0;
}


In the below code margin 20px is set because each box will have margin top, margin right, margin bottom, margin left is set 20px (space around each box on top, right bottom and left set as 20px).   padding: 20px; is given to put space between the content and border set 20px on top, right, bottom and left.


.box{
  background-color: coral;
  max-width: 400px;
  margin: 20px;
  padding: 20px;
}

In the below code each div with box ( each box  have a space between heading and content of 20px.

.box h2{
  margin-bottom: 20px;
}


In the below code box-2 div will have different margin ( margin-top, margin-right, margin-bottom, margin-left) specified as below.

.box-2{
  margin-top: 20px;
  margin-right: 40px;
  margin-bottom: 60px;
  margin-left: 80px;
}


we can combine each margin top, right, bottom and left as one.

.box-2{
  /* margin-top: 20px;
  margin-right: 40px;
  margin-bottom: 60px;
  margin-left: 80px; */

  margin: 20px 40px 60px 80px;
}


In the code below box with div box-3 will shift the box-3 to opposite since margin-left given -30px.

.box-3{
  margin-left: -30px;
}

In the below code 'auto' is given for left and right (horizontal). Hence, aligned at the middle. top and left of margin is 100px.

.box-1{
  margin: 100px auto;
}






Universal selector


Universal selector are given using asterik ( * ). example:-


index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Universal Selector & Reset</h1>
    <div class="box box-1">
      <h3>Box 1</h3>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora,
        architecto!
      </p>
    </div>
    <div class="box box-2">
      <h3>Box 2</h3>
      <p>
        Similique vero aliquid animi corrupti, itaque doloremque iusto eligendi
        voluptatum.
      </p>
    </div>
    <div class="box box-3">
      <h3>Box 3</h3>
      <p>
        Iste recusandae cum reprehenderit maxime laborum obcaecati quisquam
        dolorem minima.
      </p>

      <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
      </ul>
    </div>
  </body>
</html>


style.css

*{
  border: 3px solid red;
}
body {
  font-family: 'Poppins', sans-serif;
}

body {
  font-family: 'Poppins', sans-serif;
}

.box {
  background: coral;
  max-width: 400px;
  margin: 20px;
  padding: 20px;
}


In the below code is universal selector example ( since given * ) and hence all the elements in the html file will have border: 3px solid red;

*{
  border: 3px solid red;
}







Border
border: 4px solid coral; here 4px denotes thickness of border solid denotes what type of border line it should have , coral denotes the color of border. ( combination of these 3 css properties  border-width: 5px; border-style: dashed; border-color: blue; ). Shown below full example:-


style.css


* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
}
.box {
  background: coral;
  max-width: 400px;
  margin: 20px;
  padding: 20px;
  border-width: 5px;
  border-style: dashed;
  border-color: blue;
}
.box-1{
  border: 0;
  border-top: 5px solid red;
  border-bottom: 5px solid green;
}
.box-2{
  border-radius: 10px;
/* border-radius: 50%; */
}
.box-3{
  border-top-left-radius: 10px;
}


index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
     <h1>HTML & CSS Sandbox - Border</h1>
   <div class="box box-1">
        <h3>Box 1</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora,
          architecto!
        </p>
      </div>
      <div class="box box-2">
        <h3>Box 2</h3>
        <p>
          Similique vero aliquid animi corrupti, itaque doloremque iusto eligendi
          voluptatum.
        </p>
      </div>
      <div class="box box-3">
        <h3>Box 3</h3>
        <p>
          Iste recusandae cum reprehenderit maxime laborum obcaecati quisquam
          dolorem minima.
        </p>
      </div>
  </body>
</html>




( border-top: 5px solid red;) In the below code in style.css provide top border only red with 5px and style of border as solid to box-1 only. In ( border-bottom: 5px solid green;) provide bottom border only green with 5px and style of border as solid to box-1 only.

.box-1{
  border: 0;
  border-top: 5px solid red;
  border-bottom: 5px solid green;
}


In the below code the edge of border for box with div class box-2 is curved with radius 10px. We can give border-radius with percentage here its 50%.

.box-2{
  border-radius: 10px;
/* border-radius: 50%; */
}


In the below code we need curved side on top left for box-3, for that to happen we given the below css

.box-3{
  border-top-left-radius: 10px;
}












Display

display has the following values none, block, inline, inline-block, flex, grid, table, table-row, table-cell, list-item, inherit, initial.
p and div are block by default, we can set to inline using display property. ( display:inline; ). anchor tag are inline by default, we can set to block using display property ( display:block; ). If display none ( display:none; ) is given will remove from the layout.


index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h2>Set me to display: none</h2>
    <h2>Set me to visibility: hidden</h2>
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptates id
      adipisci laboriosam qui blanditiis
      <span>modi similique</span> vel, dicta incidunt magni architecto quidem
      sapiente esse labore! Quia sed quaerat iste doloremque!
    </p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptates id
      adipisci laboriosam qui blanditiis
    <a href="#">Link1</a>
    <a href="#">Link2</a>
    <p>Lorem, ipsum dolor.</p>
    <p>Lorem, ipsum dolor.</p>
  </body>
</html>



style.css

body {
  font-family: Arial, sans-serif;
}
.none-el{
display: none;
}
.hidden-el{
  visibility: hidden;
}
/* p{
  display: inline;
}
a{
  display: block;
} */
a{
  background-color: lightblue;
  border: 3px dashed red;
  padding: 10px;
  margin: 20px 10px;
 }



The below code will only removes and takes the space out of which was used to allocate to put the h2 with class none-el. 

.none-el{
display: none;
}



The below code will not only hides and but the space out of which was used to allocate to put the h2 with class hidden-el will be there as it is there. 

.hidden-el{
  visibility: hidden;
}


p paragraph tag is block by default, we can make p tag inline by the following

p{
  display: inline;
}


a anchor tag is inline by default, we can make a tag block by the following


a{
  display: block;
} 

The inline tag cannot have margin top or margin bottom or width because anchor tag is inline. In the below css margin top and bottom or width will not work for inline and for margin top as well as margin bottom as well as width to work we need to add display block or inline-block. If we add block ( display: block; ) the Link1 and Link2 will appear in different line , to have both Link1 and Link2 to appear in same line we add display inline-block (  display: inline-block; )

a{
  display: inline-block;
  background-color: lightblue;
  border: 3px dashed red;
  padding: 10px;
  margin: 20px 10px;
 }








Position
Specifies how to position elements on the page relative to the rest of the layout. position have values like static (position has default value as static if no other position value has not been given, position having static value means the elements given static to position will have the normal flow of layout as how the HTML document is written. static position elements cannot have css properties like top (to add pixels from top ), bottom (to add pixels from bottom ), left (to add pixels from left ) and right (to add pixels from right ) ) , relative (similar to static where position will have the normal flow of layout as how the HTML document is written but unless static we can use top, bottom, left and right properties ), absolute (we can have element inside a relative parent and position anywhere the element within the parent  ( marked position absolute) ), fixed (fixes the element there in the page even if we scroll) , sticky (similar to fixed position fixes the element there in the page at the spot even if we scroll but when the element reaches on the top the position of the element will be at top even if we scroll ).
Full example:-


index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <header>
      <h1>Positioning</h1>
    </header>
    <section class="container">
      <div class="box box1">Static</div>
      <div class="box box2">Relative</div>
      <div class="box box3">Fixed</div>
      <div class="box box4">Sticky</div>
      <div class="box box5">
        Box 5
        <div class="box box6">Absolute</div>
      </div>
      <div class="box box7">7</div>
      <div class="box box8">8</div>
      <div class="box box9">9</div>
    </section>
  </body>
</html>




style.css

body {
  font-family: Arial, sans-serif;
}
.box{
  width: 200px;
  height: 200px;
  background-color: lightblue;
  display: flex;
  justify-content: center;
  align-items:center;
  border: 3px solid red;
  margin: 10px;
}
.box1{
  position: static;
}
.box2{
  position: relative;
  left:40px;
  top: 20px;
}
.box3{
  position: fixed;
  top: 0;
  right: 0;
}
.box4{
  position: sticky;
  top: 200px;
}
.box5{
  position: relative;
  width: 600px;
  height: 600px;
  background-color: coral;
}
.box6{
  position: absolute;
  bottom: 20px;
  right: 30px;
}




In the below code position static for div with class box1 will have the box1 with normal flow. Since, position is static we cannot add left, right, bottom and top properties. 

.box1{
  position: static;
}


In the below code position relative for div with class box2 will have the box2 with normal flow. Since, position is relative we can add left, right, bottom and top properties.

.box2{
  position: relative;
  left:40px;
  top: 20px;
}

In the below code we have set position as fixed so, when scrolling the box3 will be fixed in the spot where its placed even if we scroll and visible even if we scroll. We can set a position here in the below code top is 0 and right is 0.

.box3{
  position: fixed;
  top: 0;
  right: 0;
}

In the below code position is sticky, sticky is a combination of relative and fixed. When box4 position is set sticky and top here its set 200px . So, when we scroll the box4 div when we reach top 200px the box4 remains sticky and when the scroll passes sticky box4 it remains there from top 200px.

.box4{
  position: sticky;
  top: 200px;
}



In the box6 is position absolute the parent class (box5) position is relative. When we add the following css box5 class will be a box of width and height 600px and background color coral. So box6 will be placed absolute to box5 where the box6 will be placed bottom 20px and right 30px relative to the parent class box5

.box5{
  position: relative;
  width: 600px;
  height: 600px;
  background-color: coral;
}
.box6{
  position: absolute;
  bottom: 20px;
  right: 30px;
}

box4 () will be under box5 , so to box4 to appear on the top of box5 we can z-index css property. Higher the z-index value more closer will be the element to you. Here box5 has z-index have greater value than box4 hence box5 overlaps box4 on scrolling. In the below example box4 given z-index value 2 hence box-4 overlaps box-5. ( z-index value starts from 0 and static position css elements cannot have z-index, z-index can have also negative values . If box5 is given a z-index greater than 2 then box5 will overlap box4 )

.box4{
  position: sticky;
  top: 200px;
  z-index: 2;
}









Box-shadow

box-shadow: 5px 6px 8px 7px #000;

5px denotes horizontal offset, 6px denotes vertical offset, 8px denotes blur radius, 7px denotes spread radius and #000 denotes color.
 
Horizontal and Vertical Offset denotes how far the element each both are horizontally and vertically.
blur radius denotes how blurry the color should be , if we dont give blur radius then the color provided will be maximum.
spread radius how much the shadow should grow and shrink.

Full example:-

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Box Shadows</h1>
    <div class="container">
      <div class="box box-1">Box 1</div>
      <div class="box box-2">Box 2</div>
      <div class="box box-3">Box 3</div>
    </div>
  </body>
</html>



style.css

body {
  font-family: Arial, sans-serif;
}

.container {
  display: flex;
  justify-content: space-around;
  gap: 10px;
  margin-top: 50px;
}
.box {
  width: 200px;
  height: 200px;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid #ccc;
  border-radius: 10px;
}
.box-1{
  box-shadow: 10px 10px 10px #000;
}
.box-2{
  box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.5);
}
.box-3{
  box-shadow: 5px 4px 10px 2px rgba(0, 0, 0, 0.5), 0 10px 5px red;
}













Flexbox

Flexbox is a layout model in CSS that provides an efficient way to arrange, align and distribute elements. Can be used with dynamic content and unknown sizes. One dimensional layout model. 
ROW is the horizontal and COLUMN is the vertical. flex-container can be div ul etc.
Items inside the flex-container can be flex-item, where flex-item can be div ul, span any of the HTML elements. When we use display: flex, then flex-container will be automatically set and flex items will be set as row wise by default. When flex is set as row then main axis will be horizontal and cross axis will be vertical (refer diagram FLEXBOX ROW).

If flex-direction s set to column, then flex will make vertical (refer diagram FLEXBOX COLUMN). main axis will be vertical and cross axis will be horizontal. (refer https://www.hulu.com/welcome ) for both flexbox row and flexbox column.

If you take an example of div for flex. In flex main div will be flex container and divs inside the flex-container will be flex-item. In the below example we have set flex-container of display flex hance by default the flex is row.

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="flex-container">
      <div class="flex-item">Item 1</div>
      <div class="flex-item">Item 2</div>
      <div class="flex-item">Item 3</div>
    </div>
  </body>
</html>



style.css

.flex-container {
  display: flex;
  background-color: #ccc;
  flex-direction: row;
   /* flex-direction: column; */
}
.flex-item {
  width: 200px;
  height: 200px;
  background-color: coral;
  border: 1px solid black;
}




In the below css the flex-container holding flex-item will be set to flex and hence flex-items will be arranged row wise by default and the background color set to #ccc.
If we give flex-direction: column; then the flex-items will be placed vertically, if flex-direction isn't provided or given flex-direction: row; then the flex-items will be arranged horizontally. If we give flex-direction row-reverse then item 3 will be placed be placed first then item2 and then item1 and starts from the end of row. If we give flex-direction column-reverse then item 3 will be placed be placed first then item2 and then item1.


.flex-container {
  display: flex;
  background-color: #ccc;
  flex-direction: row;
  /* flex-direction: column;*/
}

In the below code each flex-item is having a width and height of 200px and has background color coral and set a border solid and black. flex-item can be image , div, paragraph etc.

.flex-item {
  width: 200px;
  height: 200px;
  background-color: coral;
  border: 1px solid black;
}


In the below full example:-

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="flex-container">
      <div class="flex-item">Item 1</div>
      <div class="flex-item">Item 2</div>
      <div class="flex-item">Item 3</div>
      <div class="flex-item">Item 4</div>
      <div class="flex-item">Item 5</div>
      <div class="flex-item">Item 6</div>
      <div class="flex-item">Item 7</div>
      <div class="flex-item">Item 8</div>
      <div class="flex-item">Item 9</div>
      <div class="flex-item">Item 10</div>
    </div>
  </body>
</html>



style,css

body {
  font-family: Arial, sans-serif;
}
.flex-container {
  display: flex;
  background-color: #ccc;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 10px;
  /* row-gap: 10px;
  column-gap: 10px; */
}
.flex-item {
  width: 200px;
  height: 200px;
  background-color: coral;
  border: 1px solid black;
}


will put only flex-item with height and width 200px and the flex-item less than the 200px in width and height will be placed in next line horizontally. (flex-wrap: wrap;
). Also flex-wrap wrap-reverse is there which will reverse the items (  flex-wrap: wrap-reverse;). If we give (gap: 10px;) gap in flex-container then space between both horizontally and vertically between flex-items will be taken place, here in the below example gap is 10px. If we give row-gap then space around the horizontal. If we give column-gap space around vertical.

.flex-container {
  display: flex;
  background-color: #ccc;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 10px;
  /* row-gap: 10px;
  column-gap: 10px; */
}




justify-content

justify content to be given to flex-container when flex  direction is row are used to arrange flex-item's along the main axis which in a row is horizontal, by default justify-content is flex-start when display flex is row ((refer the diagram with file name 'flexbox row justify content and align items'). But when justify content to be given to flex-container when flex direction is column are used to arrange flex-item's along the main axis which in a column is vertical, so when flex direction is column then justify content arranges items vertically (refer the diagram with file name 'flexbox column justify content and align item'). 


align-item

In align-item if direction is row are used to arrange flex-item's along the cross axis which in a row is vertical (refer the diagram with file name 'flexbox row justify content and align items'). But when justify content to be given to flex-container when flex direction is column are used to arrange flex-item's along the cross axis which in a column is horizontal, so when flex direction is column then align-item arranges items horizontally. (for more information check this website https://css-tricks.com/snippets/css/a-guide-to-flexbox/ ). align-items default value is stretch which will be stretched from top to bottom when flex is row (refer the diagram with file name 'flexbox column justify content and align item'). 


Full example:-


index.html


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="flex-container">
      <div class="flex-item item-1">Item 1</div>
      <div class="flex-item item-2">Item 2</div>
      <div class="flex-item item-3">Item 3</div>
      <div class="flex-item item-4">Item 4</div>
    </div>
  </body>
</html>


style.css


body {
  font-family: Arial, sans-serif;
}
.flex-container {
  display: flex;
  background-color: lightblue;
  width: 100%;
  height: 400px;
  justify-content: center;
  align-items: center;
  /* align-items: flex-end; */
  /* justify-content: flex-end; */
  /* justify-content: center; */
  /* justify-content: space-around; */
  /* justify-content: space-evenly; */
  /* justify-content: space-between; */
/* align-items: stretch;*/
}
.flex-item {
  background-color: coral;
  /* height: 200px;*/

  width: 200px;
  border: 2px solid black;
}
 /* 
.item-2 {
  align-self: flex-end;
}
.item-3{
  align-self: flex-start;
}
*/

When flex-container is given (justify-content: flex-end), then the flex-items placed at the end horizontally. When flex-container is given (justify-content: center), then the flex-items placed at the center. When flex-container is given (justify-content:  space-between;), then the flex-items have space between the flex-items and no space at the ends of the webpage. When flex-container is given (justify-content:  space-around;), then the flex-items have space around the flex-items. When flex-container is given (justify-content:  space-evenly;), then the flex-items have space around the flex-items evenly at the sides and between the flex-items.



When flex-container is given ( align-items: flex-end;), then the flex-items placed at the end vertically. When flex-container is given (align-items: center), then the flex-items placed at the center. When flex-container is given (align-items: stretch;), then the flex-items will be stretched from top to bottom. 


In the below example if we give flex-direction column then justify-content will arrange items vertically. In the below example justify-content is center hence will be placed vertically center.

.flex-container {
  display: flex;
  background-color: lightblue;
  width: 100%;
  height: 400px;
  justify-content: center;
  flex-direction: column;
  align-items: stretch;
  }

.flex-item {
  background-color: coral;
  height: 200px;
  width: 200px;
  border: 2px solid black;
}


When flex-container is given (align-items: flex-end;), then the flex-items will be placed .at the end horizontally since flex-direction is set to column.

.flex-container {
  display: flex;
  background-color: lightblue;
  width: 100%;
  height: 400px;
  justify-content: center;
  flex-direction: column;
  align-items: flex-end;
}

.flex-item {
  background-color: coral;
  height: 200px;
  width: 200px;
  border: 2px solid black;
}

.item-2 {
  align-self: flex-end;
}
.item-3{
  align-self: flex-start;
}


align-self property given in the top code will align only item-2 box to end of the column because flex-direction is given column. item-3 box will be aligned start of the column because flex-direction is given column.


flex properties

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Flex Properties</h1>
    <div class="flex-container">
      <div class="flex-item item-1">Item-1</div>
      <div class="flex-item item-2">Item-2</div>
      <div class="flex-item item-3">Item-3</div>
      <div class="flex-item item-4">Item-4</div>
      <div class="flex-item item-5">Item-5</div>
      <div class="flex-item item-6">Item-6</div>
    </div>
  </body>
</html>


style.css


body {
  font-family: Arial, sans-serif;
}
.flex-container {
  background: lightblue;
  width: 100%;
  display: flex;
}
.flex-item {
  background-color: coral;
  padding: 20px;
  border: 2px solid black;
  width: 200px;
}
.item-1{
flex-shrink: 0;
}


flex-shrink will tell how much flex-item ( respective to which flex-item flex-shrink is given ) will shrink with respect to other flex-items in the container. All flex-item will have default value of flex-shrink property value of 1. If we given flex-shrink given value 0 to item-1 (as shown below, since flex-shrink is 0 then item-1 will not shrink ) then when the browser is dragged in and out by resizing the browser  then item-1 will not shrink it will have a width 200px (given in flex-item css property in style.css) everytime.

.item-1{
flex-shrink: 0;
}


If we given flex-shrink given value 2 to item-1 (as shown below, since flex-shrink is 2 then the item-1) then when the browser is dragged in and out by resizing the browser then item-1 will shrink twice as faster than the other flex-items in the container.

.item-1{
flex-shrink: 2;
}


flex-grow is how much the flex-item will grow with respect to other flex-items in the flex-container. If flex-grow is 0 then the flex-item will not grow. To flex-grow the flex-item we should give flex-grow a positive value. If we give the following css

body {
  font-family: Arial, sans-serif;
}
.flex-container {
  background: lightblue;
  width: 100%;
  display: flex;
}
.flex-item {
  background-color: coral;
  padding: 20px;
  border: 2px solid black;
  /* width: 200px; */
}
.item-1 {
  /* flex-shrink: 0; */
  flex-grow: 1;
}

here we give flex-grow: 1 then the rest of the space of flex-container after allocating 5 of the flex-items will be allocated with the flex item - 1 . (resize the browser). Rest of the flex-items have flex-grow 0 hence, will not grow. Default value of flex-grow is 0. (in the above example).

body {
  font-family: Arial, sans-serif;
}
.flex-container {
  background: lightblue;
  width: 100%;
  display: flex;
}
.flex-item {
  background-color: coral;
  padding: 20px;
  border: 2px solid black;
  /* width: 200px; */
}
.item-1 {
  /* flex-shrink: 0; */
  flex-grow: 1;
}
.item-3 {
  flex-grow: 2;
}


In the above exampleitem-3 is given flex-grow value 2. Here item3 will grow at the rate of 2 than item-1 which will grow in the rate of item-3 and rest of the flex-items will be of approximately same width.

Flex basis specifies the initial size of the item before any available space is distributed. In the below example item-3 is given flex-basis value of 200px, hence the size of item-3 will have size of 200px initially. But the item grows and shrinks when the browser window is resized.

body {
  font-family: Arial, sans-serif;
}
.flex-container {
  background: lightblue;
  width: 100%;
  display: flex;
}
.flex-item {
  background-color: coral;
  padding: 20px;
  border: 2px solid black;
  /* width: 200px; */
}
.item-1 {
  /* flex-shrink: 0; */
  /* flex-grow: 1; */
}
.item-3 {
  /* flex-grow: 2; */
  flex-basis: 200px;
}

If we give the following css, since flex-shrink is 0 and flex-basis is given 200px . Thus, item-3 will not shrink and will have a minimum size of 200px.
body {
  font-family: Arial, sans-serif;
}
.flex-container {
  background: lightblue;
  width: 100%;
  display: flex;
}
.flex-item {
  background-color: coral;
  padding: 20px;
  border: 2px solid black;
  /* width: 200px; */
}

.item-3 {
  /* flex-grow: 2; */
  flex-shrink: 0;
  flex-basis: 200px;
}

This flex-grow , flex-shrink and flex-basis can be given in single css flex property. The syntax is flex : flex-grow flex shrink flex-basis. In the below example the flex will be given each flex-items same space allocated in the flex container. Example shown below:

body {
  font-family: Arial, sans-serif;
}
.flex-container {
  background: lightblue;
  width: 100%;
  display: flex;
}
.flex-item {
  background-color: coral;
  padding: 20px;
  border: 2px solid black;
  flex: 1 0 200px;
}

If we give flex-basis in flex value 0, then the flex-items will be allocated space depending upon the content size inside the flex-item. example: flex 1 0 0 ;


body {
  font-family: Arial, sans-serif;
}
.flex-container {
  background: lightblue;
  width: 100%;
  display: flex;
}
.flex-item {
  background-color: coral;
  padding: 20px;
  border: 2px solid black;
  flex: 1 0 0;
  }


In the below example there are 3 flex-items in a flex-container. All the 3 of the flex-item should occupy the same space then the flex-container should be given display: flex and flex-item of each items should have flex:0, then all the three flex items will occupy the same space.


index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Flex Properties</h1>
    <div class="flex-container">
      <div class="flex-item item-1">Item-1</div>
      <div class="flex-item item-2">Item-2</div>
      <div class="flex-item item-3">Item-3</div>
    </div>
  </body>
</html>



style.css

body {
  font-family: Arial, sans-serif;
}
.flex-container {
  background: lightblue;
  width: 100%;
  display: flex;
}
.flex-item {
  background-color: coral;
  padding: 20px;
  border: 2px solid black;
  flex: 1;
}

In the below example there are 3 flex-items in a flex-container. If item-3 is to be have double the size of item-1 and item-2. Then the flex-container should be given display: flex and flex-item of item-1 and item-2 should have flex:0. Additionally item-3 will give flex:2. Then item-1 and item-2 will occupy the same space and item-3 will occupy double the space of item-1 or item-2.


style.css

body {
  font-family: Arial, sans-serif;
}
.flex-container {
  background: lightblue;
  width: 100%;
  display: flex;
}
.flex-item {
  background-color: coral;
  padding: 20px;
  border: 2px solid black;
  flex: 1;
}
.item-3 {
  flex: 2;
}


index.html


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Flex Properties</h1>
    <div class="flex-container">
      <div class="flex-item item-1">Item-1</div>
      <div class="flex-item item-2">Item-2</div>
      <div class="flex-item item-3">Item-3</div>
    </div>
  </body>
</html>



flex-order

item 2 can be arranged first even though its the second flex-item. Similarly, item-2 can be arranged first, item-3 arranged third,  item-4 arranged sixth,  item-5 arranged five,  item-6 arranged four by using order. (shown below)


style.css


body {
  font-family: Arial, sans-serif;
}

.flex-container {
  display: flex;
}

.flex-item {
  background-color: coral;
  border: 1px solid black;
  padding: 30px;
  flex: 1;
}
.item-2 {
  order: 1;
}
.item-1 {
  order: 2;
}
.item-3 {
  order: 3;
}
.item-4 {
  order: 6;
}
.item-5 {
  order: 5;
}
.item-6 {
  order: 4;
}




index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="flex-container">
      <div class="flex-item item-1">Item 1</div>
      <div class="flex-item item-2">Item 2</div>
      <div class="flex-item item-3">Item 3</div>
      <div class="flex-item item-4">Item 4</div>
      <div class="flex-item item-5">Item 5</div>
      <div class="flex-item item-6">Item 6</div>
    </div>
  </body>
</html>







Flexbox-layout-challenge

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <header class="header">
      <h1>Flexbox Layout Challenge</h1>
    </header>
    <nav>
      <ul class="main-menu">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
    <main class="main">
      <section>
        <h2>Lorem, ipsum dolor.</h2>
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ea veniam
          illum suscipit iste, vel corrupti veritatis libero nam eius tempora ad
          neque voluptatem voluptatibus reiciendis voluptatum necessitatibus
          provident distinctio saepe quasi laborum laudantium. Inventore error
          aperiam excepturi esse perferendis commodi!
        </p>

        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Tenetur
          assumenda facere nam, excepturi voluptates sint vero quis illum labore
          omnis. Ullam sequi quidem laborum doloribus facere. Natus facere
          doloremque eos? Dolore et obcaecati nobis atque explicabo facilis
          voluptatibus porro consequatur quia corporis, labore aspernatur qui
          quod cumque enim modi id tempora earum! Quasi reprehenderit, quas
          repellat magni modi ut facere.
        </p>
      </section>

      <aside>
        <h3>Recent Posts</h3>
        <ul>
          <li><a href="#">Post 1</a></li>
          <li><a href="#">Post 2</a></li>
          <li><a href="#">Post 3</a></li>
          <li><a href="#">Post 4</a></li>
          <li><a href="#">Post 5</a></li>
        </ul>
      </aside>
    </main>
  </body>
</html>




style.css


* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Poppins", sans-serif;
  line-height: 1.6;
}

ul {
  list-style-type: none;
}

a {
  text-decoration: none;
  color: #333;
}

a:hover {
  color: coral;
}

h2 {
  margin-bottom: 20px;
}
p {
  padding: 20px 0;
}
.header {
  background-color: coral;
  padding: 40px;
}
.main-menu {
  display: flex;
  gap: 20px;
  padding: 20px;
  background-color: #f4f4f4;
}
.main-menu a {
  font-size: 20px;
}
.main {
  display: flex;
  gap: 70px;
  padding: 40px;
}
.main section {
  flex: 1;
}
.main aside {
  width: 300px;
}
.main aside h3 {
  background-color: coral;
  padding: 10px;
  color: #fff;
}
.main aside li {
  padding: 10px;
  background-color: #f4f4f4;
  border-bottom: 1px solid #ccc;
}




Pricing Grid Project

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap"
      rel="stylesheet"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
      integrity="sha512-SnH5WK+bZxgPHs44uWIX+LLJAJ9/2PkPKZ5QiAj6Ta86w+fsb2TkcmfRyVX3pBnMFcV7oQPJkl9QevSCWr3W6A=="
      crossorigin="anonymous"
      referrerpolicy="no-referrer"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>Pricing</title>
  </head>
  <body>
    <!-- https://www.uidesigndaily.com/posts/sketch-pricing-cards-ui-design-card-day-1352 -->
    <div class="container">
      <div class="pricing">
        <div class="card card-free">
          <h2>Free</h2>
          <p class="price"><sup>$</sup>0</p>
          <p class="price-info"><strong>Great For Starters</strong></p>
          <p class="main-text">Discover how to create your first projects.</p>
          <a href="#" class="btn">Get Started</a>
          <ul>
            <li>1 User</li>
            <li>5 Projects</li>
            <li>10GB Storage</li>
            <li>Priority Support</li>
          </ul>
        </div>
        <div class="card card-pro">
          <h2>Pro</h2>
          <p class="price">
            <sup>$</sup>7<span>/mo</span>
          </p>
          <p class="price-info"><strong>For Planned Projects</strong></p>
          <p class="main-text">
            Bring your designs to the next level and export them.
          </p>
          <a href="#" class="btn btn-primary">Get Started</a>
          <ul>
            <li>5 Users</li>
            <li>50 Projects</li>
            <li>100GB Storage</li>
            <li>Priority Support</li>
          </ul>
        </div>
        <div class="card card-enterprise">
          <h2>Enterprise</h2>
          <p class="price">
            <sup>$</sup>12<span>/mo</span>
          </p>
          <p class="price-info"><strong>For Professional Use</strong></p>
          <p class="main-text">
            Enjoy limitless use with interactive export options.
          </p>
          <a href="#" class="btn">Get Started</a>
          <ul>
            <li>Unlimited Users</li>
            <li>Unlimited Projects</li>
            <li>Unlimited Storage</li>
            <li>Priority Support</li>
          </ul>
        </div>
      </div>
    </div>
  </body>
</html>




style.css

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  line-height: 1.6;
  background-color: #27264b;
  color: #433f63;
}
a {
  text-decoration: none;
  color: #007bff;
}
ul {
  list-style-type: none;
}
li {
  margin-bottom: 10px;
}
.container {
  background-color: #f8fafe;
  max-width: 1100px;
  border-radius: 10px;
  margin: 0 auto;
  margin-top: 150px;
  padding: 70px 60px;
}
.pricing {
  display: flex;
  justify-content: space-around;
  gap: 30px;
  flex-wrap: wrap;
}
.card {
  flex: 1;
  background-color: #fff;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
  margin-bottom: 20px;
}
.card h2 {
  font-size: 18px;
  background: #f8fafe;
  text-transform: capitalize;
  margin-bottom: 10px;
  padding: 15px;
  color: #333;
}
.card-pro h2 {
  background: linear-gradient(
    90deg,
    rgba(194, 227, 255, 1) 13%,
    rgba(180, 118, 254, 1) 100%
  );
  color: #fff;
}
.card-enterprise h2 {
  background: linear-gradient(
    90deg,
    rgba(255, 177, 194, 1) 13%,
    rgba(255, 203, 114, 1) 100%
  );
  color: #fff;
}

/* price */
.card .price {
  font-size: 45px;
  font-weight: 700;
  margin-bottom: 20px;
}

.card .price sup {
  font-size: 18px;
  position: relative;
  left: -5px;
}
.card .price span {
  font-size: 18px;
  margin-left: 5px;
}
.card .main-text {
  font-size: 14px;
  margin-bottom: 50px;
}
.btn {
  display: block;
  background-color: #fff;
  color: #27264b;
  border: 1px solid #27264b;
  border-radius: 5px;
  padding: 15px;
  width: 100%;
  cursor: pointer;
  font-size: 16px;
}
.btn-primary,
.btn:hover {
  background-color: #27264b;
  color: #fff;
}

.btn-primary:hover {
  background-color: #fff;
  color: #27264b;
}
.card ul li i {
  color: #98ca9e;
  margin-right: 10px;
}










Responsiveness

Responsive design - When web pages and layouts respond and render well on a varity of screen sizes from smartphones to large monitors. Some of the benefits of Responsive design is Improved user experience, better accessibility , enhanced SEO performance , simplified Maintenance.
Common components of Responsive design are flexible layouts ( max-width, percentages etc), correct viewport tag, flexible images, fluid typography , media queries and container queries.
Example of Responsive design is  https://www.traversymedia.com/

https://www.netflix.com



Percentage Responsiveness

html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="container">
      <h1>Lorem, ipsum dolor.</h1>
      <img src="https://picsum.photos/1100/300" alt="" /
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Explicabo,
        dolorum. Qui accusamus omnis perspiciatis voluptas praesentium fugit
        iure at ea nam animi nulla, aliquid ratione porro quae eveniet.
        Consequatur, nesciunt!
      </p>
    </div>
  </body>
</html>


style.css

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Poppins", sans-serif;
}
.container {
  /* width: 1100px; */
  max-width: 1100px;
  margin: 50px auto;
  padding: 20px;
}




In the above style.css when we give container width :1100px then when we resize the browser to small some contents will not be displayed as the width is given 1100px , instead of giving width we can give max-width :1100px, like below 

.container {
  /* width: 1100px; */
  max-width: 1100px;
  margin: 50px auto;
  padding: 20px;
}

Another solution is giving width in percentage instead of pixel (this percentage also make site responsive). Additionally give max-width will maintain the contents as 1100px width maximum like below even through size of browser is increased. Like below

.container {
  /* width: 1100px; */
  width: 80%;
  max-width: 1100px;
  margin: 15% auto;
  padding: 20px;
}


In html for image ( <img src="https://picsum.photos/1100/300" alt="" /> , here 1100 is width and 300 is height) when the browser size increased the image can be seen fully since the width is 1100, but when the browser size is reduced the image is not fully shown in the browser.

img{
  max-width: 100%;
}

.container {
  width: 80%;
  max-width: 1100px;
  margin: 15% auto;
  padding: 20px;
}

the image is set max-width 100% of the container since, image is enclosed in container (where container with width set as 80% of the browser).

When not to use percentages :- fixed sized elements (if you want elements of fixed size regardless of its environments then we should use pixels), font sizes ( font sizes not recommended to use percentages rather use relative units like rem and em (this will scale proportionally based on user settings on or parent element font size)), precise positioning (while using layouts where you need pixel perfect HTML and CSS version of psd)





Media Queries


example:-
@media screen and (max-width:600px){
//css rules
}

@media rule defines different style rules
Media features - min/max-height, min/max-width, orientation
Media types - screen, print, speech readers etc

576px -smartphones
768px -tablets
992px - desktp
1024px -landscape
1200px-desktop/widescreen


index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <div class="widescreen"><h1>Widescreen</h1></div>
    <div class="normal"><h1>Normal</h1></div>
    <div class="tablet"><h1>Tablet</h1></div>
    <div class="smartphone"><h1>Smartphone</h1></div>
    <div class="landscape"><h1>Landscape</h1></div>
    <div class="height"><h1>Height</h1></div>
  </body>
</html>


styles.css

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
}
@media screen and (max-width: 1200px) {
  .widescreen {
    background-color: coral;
  }
}
@media (max-width: 992px) {
  .normal {
    background-color: lightblue;
  }
}
@media (max-width: 768px) {
  .tablet {
    background: lightgreen;
  }
}
@media (max-width: 576px) {
  .tablet {
    background: purple;
  }
}
@media (orientation: landscape) {
  .landscape {
    background: chartreuse;
  }
}
@media (max-height: 500px) {
  .height {
    background: olive;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  body {
    background: #333;
  }
}





Grid


Grid is a 2D hence it has control over row and columns (using grid template rows and grid template columns - which specifies how much rows and columns you want and how wide should be the rows and columns).
CSS Grid is a layout system that provides properties to create rows, columns and two dimensional grid layouts.
Uses 'display: grid' to create a grid container with items, grid is 2D layout model and is  supported in all browsers.
Any grid direct child elements are grid items
Grid can be used in page where as shown in this image GRID used layout.png in attached files.
 Note: Flexbox is best suited for laying out single rows and columns, while CSS Grid is best for grid layouts with multiple rows and columns. Usually main page can be designed using grid and inner elements can be styled using flexbox.

CSS grid properties

display: grid should be given initially to use grid.
grid-template-rows (which defines the number and size of rows in the grid )
grid-template-columns (which defines the number and size of columns in the grid )
grid-gap ( used to put space around each grid items.)
grid-column (will put particular grid item in a column range)
grid-row (will put particular grid item in a row range)
grid-area (which means in a specific area grid is placed)
justify-items
align-items
justify-content
align-content

(grid-template-columns: 100px 100px 100px;) this creates 3 columns each of width 100px. Since 100px is repeated 3 times there will be 3 columns.
(grid-row-gap: 20px ) will add gap between rows of width 20px
(grid-column-gap: 20px ) will add gap between columns of width 20px

grid-row-gap: 20px; grid-column-gap: 20px; - these 2 combined using 'grid-gap:20px' or 'gap:20px'

Example

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Grid Columns</h1>
    <div class="container item-grid">
      <div class="item item-1">Item 1</div>
      <div class="item item-2">Item 2</div>
      <div class="item item-3">Item 3</div>
      <div class="item item-4">Item 4</div>
      <div class="item item-5">Item 5</div>
      <div class="item item-6">Item 6</div>
    </div>
  </body>
</html>


styles.css

body {
  font-family: Arial, sans-serif;
}
.container {
  max-width: 1100px;
  margin: 30px auto;
  background: #f4f4f4;
}
.item {
  background-color: coral;
  padding: 1rem;
  border: 1px solid #333;
  text-align: center;
}
.item-grid {
  display: grid;
  grid-template-columns: 100px 100px 100px;
  /* grid-row-gap: 20px;
  grid-column-gap: 20px; 
  grid-gap: 20px;*/
  gap: 20px;
}



 here instead of repeating 100px 3 times (like this  grid-template-columns: 100px 100px 100px; ) we can do like this grid-template-columns: repeat(3, 100px); here 3 means 3 columns and 100px means 100px width for each grid column.

grid-template-columns: repeat(3, minmax(200px, 300px)); in this minmax has 2 values 200px and 300px here the columns will have minimum in 200px width and maximum 300px in width.

Example:

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - repeat() & minmax()</h1>
    <div class="container item-grid">
      <div class="item item-1">Item 1</div>
      <div class="item item-2">Item 2</div>
      <div class="item item-3">Item 3</div>
      <div class="item item-4">Item 4</div>
      <div class="item item-5">Item 5</div>
      <div class="item item-6">Item 6</div>
      <div class="item item-7">Item 7</div>
      <div class="item item-8">Item 8</div>
      <div class="item item-9">Item 9</div>
    </div>
  </body>
</html>


styles.css

body {
  font-family: Arial, sans-serif;
}

.container {
  max-width: 1100px;
  margin: 30px auto;
  background: #f4f4f4;
}

.item {
  background-color: coral;
  padding: 1rem;
  border: 1px solid #333;
  text-align: center;
}

.item-grid {
  display: grid;
  /* grid-template-columns: repeat(3, 100px); */
  grid-template-columns: repeat(3, minmax(200px, 300px));
}



grid-template-rows

 grid-template-rows: 100px 200px 300px; here 3 rows , in which first row will be of width 100px, second row will be of width 200px, third row will be of width 300px, rest of the rows will accommodate space allocating the content since only 3 rows mentioned in grid-template-rows. Since in the html there is total 6 rows. To overcome this problem we can use 'grid-auto-rows: 100px' where the rest of the rows thats row4, row 5, row 6 will have width of 100px.
We can give both  grid-template-rows and  grid-template-columns together.

Example

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Grid Rows</h1>
    <div class="container item-grid">
      <div class="item item-1">Item-1</div>
      <div class="item item-2">Item-2</div>
      <div class="item item-3">Item-3</div>
      <div class="item item-4">Item-4</div>
      <div class="item item-5">Item-5</div>
      <div class="item item-6">Item-6</div>
    </div>
  </body>
</html>


styles.css

body {
  font-family: Arial, sans-serif;
}
.container {
  max-width: 1100px;
  margin: 30px auto;
}
.item-grid {
  display: grid;
  /* grid-template-rows: 100px 200px 300px; */
  grid-template-rows: 1fr 2fr 3fr;
  grid-template-columns: 1fr 2fr 3fr;
  grid-auto-rows: 100px;
  background: #f4f4f4;
}
.item {
  background-color: coral;
  padding: 1rem;
  border: 1px solid #333;
  text-align: center;
}

Example 2: -

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Grid Challenge 1</h1>
    <div class="container item-grid">
      <div class="item item-1">Item-1</div>
      <div class="item item-2">Item-2</div>
      <div class="item item-3">Item-3</div>
      <div class="item item-4">Item-4</div>
      <div class="item item-5">Item-5</div>
      <div class="item item-6">Item-6</div>
      <div class="item item-7">Item-7</div>
      <div class="item item-8">Item-8</div>
      <div class="item item-9">Item-9</div>
      <div class="item item-10">Item-10</div>
      <div class="item item-11">Item-11</div>
      <div class="item item-12">Item-12</div>
    </div>
  </body>
</html>


styles.css

body {
  font-family: Arial, sans-serif;
}

.container {
  max-width: 1100px;
  margin: 30px auto;
  background: #f4f4f4;
}

.item {
  background-color: coral;
  padding: 1rem;
  border: 1px solid #333;
  text-align: center;
}

.item-grid {
  display: grid;
  grid-template-rows: 1fr 2fr 3fr;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 4fr;
  gap: 1rem;
}



Align and justify

justify-items: Align the items inside the grid along the row axis
align-items: Align the items inside the grid along the column axis
justify-content: Align the grid along the row axis
align-items: Align the grid along the column axis
place-items: A shorthand for align-items and justify-items
place-content: A shorthand for align-content and justify-content

When we give justify-content: start it will place grid in the start.
When we give justify-content: end it will place grid in the end.
When we give justify-content: space-between it will place space between the items in the grid.
When we give justify-content: space-around it will place space between the items in the grid and the edge at start and end of grid too.
When we give justify-content: space-evenly it will place space evenly between the items in the grid and the edge at start and end of grid too.

When we give justify-items: start it will place items in the start.
When we give justify-items: end it will place items in the end.
When we give justify-items: stretch it will stretch the items in the grid.


To put 'justify-content' and 'align-content' together as 'space-around' value we can put the CSS property 'place-content' value as 'space-around'
To put 'justify-items' and 'align-items' together as 'space-around' value we can put the CSS property 'place-items' value as 'space-around'






repeat() with autofill and autofit

When we want to create a dynamic grid where we are not aware of the number of rows, columns used or the number of items are not aware beforehand then we use these repeat() with autofit and autofill.
Instead of allocating 6 columns like this  'grid-template-columns: repeat(6, 100px);' we can give like this '  grid-template-columns: repeat(auto-fit, 100px);' which will fit 6 columns with width 100px each. But there will space after row if 100px is not there to allocate the item and the other items come in another line when we reduce the browser width. To overcome this issue we can give minmax(100px, 1fr) like this 'grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));'. Instead of auto-fit we can give auto-fill too like this '  grid-template-columns: repeat(auto-fill, 100px);' but when we give auto-fill there will be some space after column if could allocate in 1 row. So, to overcome that solution we can use auto-fit.

Full example:-

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - autofill & autofit</h1>
    <div class="container item-grid">
      <div class="item item-1">Item 1</div>
      <div class="item item-2">Item 2</div>
      <div class="item item-3">Item 3</div>
      <div class="item item-4">Item 4</div>
      <div class="item item-5">Item 5</div>
      <div class="item item-6">Item 6</div>
      <div class="item item-7">Item 7</div>
      <div class="item item-8">Item 8</div>
      <div class="item item-9">Item 9</div>
    </div>
  </body>
</html>


styles.css

body {
  font-family: Arial, sans-serif;
}
.container {
  max-width: 600px;
  margin: 30px auto;
  background: #f4f4f4;
}
.item {
  background-color: coral;
  border: 1px solid #333;
  padding: 1rem;
  text-align: center;
}
.item-grid {
  display: grid;
  /* grid-template-columns: repeat(auto-fit, 100px); */
  /* grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); */
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
}


grid-template

grid-template isa combination of both grid-template-rows and grid-template-columns like this grid-template: repeat(3, 1fr) / repeat(3, 1fr);
first repeat(3, 1fr) refers to grid-template-rows and the other repeat(3, 1fr) is grid-template-columns

Example:-

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - autofill & autofit</h1>
    <div class="container item-grid">
      <div class="item item-1">Item 1</div>
      <div class="item item-2">Item 2</div>
      <div class="item item-3">Item 3</div>
      <div class="item item-4">Item 4</div>
      <div class="item item-5">Item 5</div>
      <div class="item item-6">Item 6</div>
      <div class="item item-7">Item 7</div>
      <div class="item item-8">Item 8</div>
      <div class="item item-9">Item 9</div>
    </div>
  </body>
</html>


styles.css

body {
  font-family: Arial, sans-serif;
}
.container {
  max-width: 600px;
  margin: 30px auto;
  background: #f4f4f4;
}
.item {
  background-color: coral;
  border: 1px solid #333;
  padding: 1rem;
  text-align: center;
}
.item-grid {
  display: grid;
  /* grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr); */
  grid-template: repeat(3, 1fr) / repeat(3, 1fr);
}


POISTIONING AND SPANNING ITEMS

grid-column

if one item need to be extended from column 1 to column 3 then we can use the following css properties 'grid-column-start: 1;' and 'grid-column-end: 3;'. Meanwhile we can combine both grid-column-start and grid-column-end together by using 'grid-column: 1 / 3;'

example 

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Positioning Grid Items</h1>
    <div class="container item-grid">
      <div class="item item-1">Item 1</div>
      <div class="item item-2">Item 2</div>
      <div class="item item-3">Item 3</div>
      <div class="item item-4">Item 4</div>
      <div class="item item-5">Item 5</div>
      <div class="item item-6">Item 6</div>
      <div class="item item-7">Item 7</div>
      <div class="item item-8">Item 8</div>
      <div class="item item-9">Item 9</div>
    </div>
  </body>
</html>


styles.css

body {
  font-family: Arial, sans-serif;
}

.container {
  max-width: 1100px;
  margin: 30px auto;
  background: #f4f4f4;
  height: 600px;
}

.item {
  background-color: coral;
  padding: 1rem;
  border: 1px solid #333;
  text-align: center;
}

.item-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
}
.item-1 {
  /* grid-column-start: 1;
  grid-column-end: 3; */
  grid-column: 1 / 3;
}



grid-row

if one item need to be extended from row 2 to row 4 then we can use the following css properties 'grid-row-start: 2;' and 'grid-row-end: 4;'. Meanwhile we can combine both grid-row-start and grid-row-end together by using 'grid-row: 2 / 4;'

Example

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Positioning Grid Items</h1>
    <div class="container item-grid">
      <div class="item item-1">Item 1</div>
      <div class="item item-2">Item 2</div>
      <div class="item item-3">Item 3</div>
      <div class="item item-4">Item 4</div>
      <div class="item item-5">Item 5</div>
      <div class="item item-6">Item 6</div>
      <div class="item item-7">Item 7</div>
      <div class="item item-8">Item 8</div>
      <div class="item item-9">Item 9</div>
    </div>
  </body>
</html>


styles.css

body {
  font-family: Arial, sans-serif;
}

.container {
  max-width: 1100px;
  margin: 30px auto;
  background: #f4f4f4;
  height: 600px;
}

.item {
  background-color: coral;
  padding: 1rem;
  border: 1px solid #333;
  text-align: center;
}

.item-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
}
.item-1 {
  /* grid-column-start: 1;
  grid-column-end: 3; */
  grid-column: 1 / 3;
}
.item-3 {
  /* grid-row-start: 2;
  grid-row-end: 4; */
  grid-row: 2 / 4;
}


span

when we want to span of item-1 in grid column from 1 till 2 columns then we can use ' grid-column: 1 / span 2;'
when we want to span of item-3 in grid column from 1 till 2 rows then we can use ' grid-row: 1 / span 2;'

example

index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body>
    <h1>HTML & CSS Sandbox - Positioning Grid Items</h1>
    <div class="container item-grid">
      <div class="item item-1">Item 1</div>
      <div class="item item-2">Item 2</div>
      <div class="item item-3">Item 3</div>
      <div class="item item-4">Item 4</div>
      <div class="item item-5">Item 5</div>
      <div class="item item-6">Item 6</div>
      <div class="item item-7">Item 7</div>
      <div class="item item-8">Item 8</div>
      <div class="item item-9">Item 9</div>
    </div>
  </body>
</html>


styles.css

body {
  font-family: Arial, sans-serif;
}

.container {
  max-width: 1100px;
  margin: 30px auto;
  background: #f4f4f4;
  height: 600px;
}

.item {
  background-color: coral;
  padding: 1rem;
  border: 1px solid #333;
  text-align: center;
}

.item-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
}
.item-1 {
  /* grid-column-start: 1;
  grid-column-end: 3; */
  /* grid-column: 1 / 3; */
  grid-column: 1 / span 2;
}
.item-3 {
  /* grid-row-start: 2;
  grid-row-end: 4; */
  grid-row: 2 / span 2;
}
.item-9 {
  grid-column: 2 / span 2;
}


# FrontEndWebDev-ClassProject - Louie's Pizza

Louie has the best pizza in town, but his small pizza shop is only known to some die-hard local fans.  Louie wants to expand his business and attract new customers so that more people can enjoy his amazing pizza.  Louie has contracted you to build a website for "Louie's Pizza" and he has provided you with a PDF with what he wants the final product to look like.  You will build a site that matches Louie's design in phases, with the final product being a marketing site that will help Louie grow his business.

## Challenge 1 - Starting From Scratch

In this challenge, we will scaffold our web project by creating a bare-bones html, css, and js file.  Then we'll add some content and add some simple styling.  We're building this site mobile-first, so our styling should target mobile devices first, and then later we will adjust our styles for larger screens via *media queries*.  

### Part A - Scaffolding a Site

1. Create an index.html file and copy this html into your newly created file:
```
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Louie's Pizza</title>

    <!-- Insert Style Sheet Here-->
    
    <!-- Insert Google Fonts Here -->

</head>

<body>

    <!-- Header -->

    <!-- /Header -->

    <!-- Welcome -->

    <!-- /Welcome -->

    <!-- Mail List -->

    <!-- /Mail List -->

    <!-- History -->

    <!-- /History -->

    <!-- Food Menu -->

    <!-- /Food Menu -->

    <!-- Map -->

    <!-- /Map -->

    <!-- Footer -->

    <!-- /Footer -->


    <!-- Insert JavaScript Here -->

</body>
</html>
```
2. Inside the css directory create a new file and name it `site.css`.
3. In your index.html file, add the appropriate `link tag` in the `<head>` element to link your `site.css` style sheet.

Now you have a basic html/css site to work with!

### Part B - Adding Content

Now we will add a little bit of content to our website, and add a little bit of layout.  Let's get started with the top section of the site.

In index.html, find the section labeled `Header` and paste in the following html:
```
<section class="header">
        <img src="img/louies-logo.svg">
        <nav id="main-nav" role="navigation">
            <ul>
                <li><a href="#">Welcome</a></li>
                <li><a href="#">History</a></li>
                <li><a href="#">Menu</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    <div class="hero-block">
        <h1>World's Favorite Pizza!</h1>
        <p>Located on Clay Street, in NuLu, Louie’s Pizza is part of one of Louisville’s most lively neighborhoods. In close proximity to Downtown and near Washington Park, our NuLu pizzeria has a cool atmosphere suited for anyone looking to find a spot to hang out.</p>
        <a href="#" class="hero-button">View Menu</a>
    </div>
</section>
```

Here we have added a section to our website.  This section contains a logo, navigation, and a "Hero Block" with informaiton about our website.  If you open Index.html in a web browser, it won't look like much now since we haven't added any CSS to our site.  Let's style this section to make it match the mobile version of the site as shown in the mobile.pdf file.  

### Part C - Styling the Header

#### Fonts
This site uses the Google fonts `Roboto` and `Roboto Slab`.  To use these fonts on our site, let's add the font stylesheet from Google to the head element inside index.html.

```
<link href="https://fonts.googleapis.com/css?family=Roboto+Slab:700|Roboto:300,300i,700,700i" rel="stylesheet">
```

#### Body

For the body element, set the margin and padding to 0, and the font-family to 'Roboto', sans-serif.

#### Box-Sizing

We'll be using the border-box box-sizing model globally.  To set this, add the following to your css file:

```
* {
    box-sizing: border-box;
}
```

#### Headings

H1 headings should:
* Be upper case 
* Have a font-size that is 2.5x larger than the base font size (1.2rem)
* Have a margin of 2rem for the top and bottom
* Have a font family of 'Roboto Slab' with a fallback to serif.  

#### Paragraphs

Paragraphs should:
* Have a font size that is 1.2x larger than the base font size (1.2rem)
* Have a bottom margin of 2rem.
* Have a font-weight of 300.

#### Anchors (Links)

Anchors should be white, with no text decoration;

#### Wrapper

The wrap class should have a 2rem padding all around.

#### Header Section

Now we're getting into specifics for the header section.  This section should set its background to the `hero-bg-pizza.jpg` image, have a background color of #333333, a font color of #FFFFFF, and have its text center-aligned.  The css for the header section should look like the following when you're done:

```
.header {
  background-color: #333333;
  background-image: url('../img/hero-bg-pizza.jpg');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  color: #FFFFFF;
  text-align: center;
}
```

#### Navigation
* The font inside the navigation should have a font family of `Roboto Slab` with a fallback to `serif`.  The font should be bold, uppercate, and the text should be center aligned.  
* The `ul` element should be unstyled and have no padding.
* The li element should be set to display as block.
* The a element should have a padding of .5rem and should also be displated as block.
* When the user hovers over an anchor tag, the background color should be set to #871719.

Here is an example of how the nav styling should look:

```
nav {
    font-family: 'Roboto Slab', serif;
    font-weight: bold;
    text-transform: uppercase;
    text-align: center;
}
nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
   display: block;
}

nav a {
  padding: .5rem;
  display: block;
}

nav a:hover {
  background-color: #871719;
}
```

#### Hero Button
Finaly let's make a pretty button.  Target the hero-button class and apply the following:

* The font size should be 1.4x the base font size (1.4rem).
* The font family should be `Roboto Slab` with a fallback to `serif`.  The text should be uppercase and font should be bold.  
* There should be a 2px solid border that is white.  
* It should have a top/bottom padding of 6px with a left/right padding of 12px.  
* Then a user hovers over the button, the border color and background color should change to #871719.

Here is an example of what the css should look like:

```
.hero-button {
  font-size: 1.4rem;
  font-family: 'Roboto Slab', serif;
  text-transform: uppercase;
  font-weight: bold;
  border: 2px solid #FFFFFF;
  padding: 6px 12px;
}

.hero-button:hover {
  border-color: #871719;
  background-color: #871719;
}
```

Now we have a styled header section for our site!

## Challenge 2

Let's build out the Welcome and Mail List sections of our page.

### Welcome Section

This one is pretty simple.  Similar to the Header section, you will need a section element with a wrapper inside of it.  Inside the wrapper you should add a h2 with the words "Welcome to Louie's", but "Louie's" should be red (#871719). 

Now add a paragraph below the h2 with the following text:

```
Enjoy the old-school ambiance, original wooden booths sentimentally etched by our loyal customers, the black and white art deco floors worn by time, turn of the century tin ceilings and faded murals tell tale of a bygone era. Sit back, relax, enjoy the smell of simmering tomatoes and hot pizza, feel the warmth and camaraderie, hear the laughter and conversation of happy diners and you feel like you are home again, somewhere familliar, comfortable, affordable, family centered and “ORIGINAL”.
```

Make sure that the h2 uses the 'Roboto Slab' font-family with a fallback to serif.  The font size for h2 should be 175% of the base font-size (1.75rem).

### Mail List Section

Similar to the Welcome section, you will need a section element with a wrapper inside of it.  Inside the wrapper you should add a h2 with the words "Join Louie's List today, and get a free slice!". 

Create a new form element with a label of "Email", an input with placeholder text like "jsmith@gmail.com", and a submit button with the text "Sign Up."  Lastly, add a paragraph with the text "We promise not to SPAM you, unless you want it on your pie! Data charges may apply if your still using dial-up or AOL." and make it 80% of the base font size (.8rem).

The lable, input, and button should be block level elements that take 100% of the width of their containing element.  Create classes for the newsletter label, input and button.  Be sure that these classes contain the following CSS properties in addition to being displayed as block level elements, and having 100% width.

#### Label

```
    margin: 0 0 16px 0;
```

#### Input

```
    border: 1px solid #c0af8e;
    border-radius: 3px;
    height: 40px;
    padding: 8px;
    margin: 0 0 10px 0;
    font-size: 1rem;
``` 

#### Button

```
    background-color: #871719;
    border-radius: 3px;
    color: #FFFFFF;
    font-family: 'Roboto Slab', serif;
    font-size: .8rem;
    text-transform: uppercase;
    font-weight: bold;
    height: 40px;
```

Finally, let's make the "Sign Up" button change to purple (#800080) when the user hovers over it.  We should now have a completed Mail List section that looks great on mobile devices.  


# sass-website

### about this website

It is a simple responsive site with beautiful design and created with sass.

### What is SASS?

SASS (Syntactically Awesome Stylesheets) is a CSS pre-processor that lets you use variables, mathematical operations, mixins, loops, functions, imports, and other interesting functionalities that make writing CSS much more powerful. In some ways, you may think of SASS as a style sheet extension language because it extends the standard CSS characteristics by introducing the benefits of a basic programming language. So SASS will compile your code and generate the CSS output a browser can understand.

![alt text](<SCSS to CSS-1.jpg>)

Yes, you just read "programming language" but it really is basic stuff. If you are a programmer, it will only take you 15 minutes to get SASS. But if you have no experience coding, then your learning curve will be a little higher. Once you learn CSS with SASS, you won't write CSS from scratch anymore.

Here are seven benefits of using SASS:

### It's CSS syntax friendly

If you know CSS, you know SASS. SASS comes with two different syntaxes: SASS itself and SCSS, the most used one. SCSS syntax is CSS compatible, so you just have to rename your .css file to .scss et voilà! Your first SCSS file has been created, just like that.

Of course, by doing this you are not using any of the superpowers and abilities SASS provides, but at least you realize you don't need to spend hours and hours to start using SASS. From this starting point, you would be able to learn the SASS syntax as you go.

Here's where you can learn about the SASS basics.

### It offers variables for whatever you want

One of the great benefits of using a CSS pre-processor like SASS is the ability to use variables. A variable allows you to store a value or a set of values, and to reuse these variables throughout your SASS files as many times you want and wherever you want. Easy, powerful, and useful.

Imagine a scenario in which you're building a site with a fantastic blue colour everywhere; buttons, menus, icons, containers, etc. You're also using a couple of great fonts: Ubuntu and Nunito. Using traditional CSS, you would need to repeat the same code over and over, but with SASS you can store these values as variables:

```$blue: #004BB4;
$ubuntu-font: 'Ubuntu', 'Arial', 'Helvetica', sans-serif;
$nunito-font: 'Nunito', 'Arial', 'Helvetica', sans-serif;
```

Once you have created the variables, you can use them wherever you need to, like this:

```
h1 {
  font: $ubuntu-font;
  color: $blue;
}
a {
  font: $nunito-font;
  background-color: $blue;
  padding: 6px;
}
```

When you compile your SCSS files, SASS will take care of the variables you used, replacing the variable name with its stored value. Powerful, right? And, of course, changing the value of the colour is as quick as updating the variable content and re-compiling. The days of using "Find and Replace" in your text editor to update colours in your CSS file are gone!

This benefit alone makes it worthwhile to become a SASS ninja, but there is more.

### It uses nested syntax

Another fantastic benefit of CSS pre-processors is their improved syntax. SASS allows you to use a nested syntax, which is code contained within another piece of code that performs a wider function. In SASS, nesting allows a cleaner way of targeting elements. In other words, you can nest your HTML elements by using CSS selectors.

Benefits of nesting:

    .More natural syntax and easy to read in most cases

    .Prevents the need to rewrite selectors multiple times

    .Better code organization and structure thanks to its visual hierarchy, which bring us to...

    .More maintainable code.

Example of nested SASS (SCSS syntax) code:

```
.navbar {
  font: $ubuntu-font;
  color: $blue;
  li {
    margin-left: 1rem;
    a {
      padding: 5px;
      font-size: 1.5rem;
      span {
        font-weight: 600;
      }
    }
  }
}
```

However, be aware that nesting too deeply is not good practice. The deeper you nest, the more verbose the SASS file becomes and the larger the compiled CSS will potentially be, since the nesting is flattened when compiled. So, overuse of nesting can create:

    .Overly specific CSS rules that are hard to maintain

    .Selectors that cannot be reused

    .Performance issues. Nested selectors will create a long CSS selector string that will end up generating a bigger CSS file.

### It includes mixins

Using variables is great but what if you have blocks of code repeating in your style sheet more than once? That is when mixins come into play. Mixins are like functions in other programming languages. They return a value or set of values and can take parameters including default values. Note that SASS also has functions, so do not confuse a mixin with a function.

Let's look at an example. Imagine you have this mixin:

```
@mixin set-font( $family: 'Ubuntu' , $weight: 400 , $style: normal ) {
  font-family: $family , 'Arial', 'Helvetica', sans-serif;
  font-style: $style;
  font-weight: $weight;
}
```

Now that you have your mixin defined, you can include it wherever you want. Note that because you have declared default values there is no need to pass any parameter:

```
h1 {
  @include set-font;
  color: $blue;
}
```

This will be compiled into:

```
h1 {
  font-family: 'Ubuntu', 'Arial', 'Helvetica', sans-serif;
  font-style: normal;
  font-weight: 400;
  color: #004BB4;
}
```

If you want to update the default mixin values, you just need to pass the parameters within the @include call.

```
h1.callout {
  @include set-font('Nunito',600);
  color: $blue;
}
```

### You can divide and conquer

As your project grows and becomes more complex, so will your stylesheets. You can add comments into your 3,000-line style sheet and then search for a specific pattern in your text editor, but that's not a great solution. Or you could split your CSS file into 20 smaller parts, but then you will have an HTTP request for each .css file you import. You don't want that either.

Fortunately SASS has the @import rule. @import allows you to modularize your code making it easier to maintain by importing smaller SASS files. The difference between this and the CSS @import rule is that all imported SCSS files will be merged together into a single CSS file, so in the end, only a single HTTP call will be requested because you will be serving a unique CSS file to the web server.

Importing SCSS/SASS files is really easy:

```
@import "source/font-awesome";
@import "source/slick";
@import "framework/bootstrap";
@import "my-custom-theme";
```

As you can see, you don't have to provide the file extension name, and the import path could contain directories as well, which means you can give your SASS working directory the desired structure.

### It has a large community and is well documented

Another advantage of using SASS is the huge amount of documentation available online. From tutorials to books, SASS has all you need to become an expert. One of the best starting points is the official SASS Documentation page, where you will find great documentation full of practical examples.

You can also find a lot of great resources on the SASS community page, including interesting blog posts, guides, tutorials, projects, etc. You won't feel like you're on your own when it comes to learning SASS.

### If you know SASS, you can customize Bootstrap 4

The fact is, SASS is all around. Along with LESS, one of the other solid alternatives, SASS has become the most used CSS pre-processor in the front-end universe. Some of the best front-end frameworks like Bootstrap and Foundation have been developed with SASS.

If you are familiar with Bootstrap, knowing SASS will give you the ability to change this web framework by simply customizing its SASS code. Sounds amazing, right? And the good thing is that it's super easy to do and you only have to change the value of some variables.

For example, let's say you are unhappy with the default breakpoints Bootstrap provides, and you would like to add one more. All you have to do is update the $grid-breakpoints mapping variable you will find within the \_variables.scss file, to add the new breakpoints you want to support. In the following example we added an extra 1440px breakpoint:

```
$grid-breakpoints: (
  xs: 0,
  sm: 576px,
  md: 768px,
  lg: 992px,
  xl: 1200px,
  xxl: 1440px
) !default;
```

After compiling your Bootstrap's source Sass files, the new breakpoint will be created including the new identifier, xxl in this case, to all responsive classes Bootstrap generates. For example, if by default Bootstrap provides responsive classes like "d-xl-none" or "col-sm-7", now you'll be able to do "col-xxl-6" or "mx-xxl-3".

And of course, you would be able to customize default aspects of Bootstrap like colours, fonts, margins, padding, etc.

### Recap and final thoughts

CSS pre-processors are here to stay. They extend the basic CSS features by providing you with a set of powerful functionalities that will raise your productivity right away. We mentioned a few benefits but there are many more, like inheritance, functions, control directives, and expressions like if(),for() or while(), data types, interpolation, etc.

Becoming a SASS guru may take a bit of time; all you need to do is look into the Bootstrap SASS files to see how SASS could turn into a complex thing. But learning the basics and setting it up for your project won't take you long.

# I hope I have given you good information ✌️

# CSS Basics Continued

### CSS Variables

A CSS variable is just a value on a CSS property that we save in a central place. This value can we then reuse throughout the application. A very common case for a CSS variable is when using colors. Usually you have a bunch of those in different settings and most of the time you are using the same color in several places. It would be nice if you want to change this color to just change it in on place.

To create a CSS variable, you need to attache it to a specific element. This element should be at the top of you DOM tree, and that element is usually the `html` tag. You can also use the `:root` tag, this is essentially the same thing as the `html` tag. 

The variable is created with two dashes and a variable name, and then the value after a colon, and the end the css rule with a semi-colon

```css
html {
    --main_color: #04aa6d;
    --background_color: #c8c8c8;
}
```
To access the variable you just substitute your value with the CSS variable inside parentheses and the `var` keyword

``` css
p {
    color: var(--main_color);
}

body {
    background-color: var(--background_color);
}
```
A CSS variable doesn't only have to be colors, it can be anything really that you want to reuse in your project.

```css
html {
--main_color: #04aa6d;
--background_color: #c8c8c8;

--border_styling: 2px solid #9763f6;
}
```

In this case we create a standard border styling that we can use in multiple places in our css.

A CSS variable doens't have to be defined in the `html` tag, we can also create them locally by defining them on specific elements. In that case the variables will only apply on those elements and every child element to that specific element.
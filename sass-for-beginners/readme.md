
<img src="https://sass-lang.com/assets/img/logos/logo.svg" width="200" height="200">
Author : Jp Lazaro  


# Learn SASS
In this article, you will learn SASS and its basic features such as variables, inheritance and mixins.
This article is for beginners who doesnt have an idea on SASS / SCSS
<br><br>



## How to install?
To get started with SASS you have to install it.

Via NPM

```
npm install -g sass
```
<br><br>


## Generating CSS from SASS via SASS CLI
To generate open cmd / cli then follow the command below
```
sass source/stylesheets/index.scss build/stylesheets/index.css
```
<br><br>

## Variables
Creating your first variable in SASS. 
Variable is basically a holder of value that you can assign to different attribute everytime you needed the value of it.
In the table below we have intiated a variable $primary-color and assigned #333 value to it . Where #333 is a hexadecimal value representing color.
Then we have used the variable $primary-color in the body to represent the background to #333.
<br><br>
> [!TIP]
> Please think a more descriptive variable name as possible

### SASS 
```
 $primary-color: #333
 body 
   background-color: $primary-color
```
 
### SCSS 
```
 $primary-color: #333;
 body {
   background-color: $primary-color
}
```

### CSS 
```
 body {
   background-color:  #333;
}
```


<br><br>


 ## Style multiple html tags using one variable
In this section, we will create a variable that we will use to multiple tags.
For example, you want to create a website that will have a common padding to all the containers like cards,  alerts and panel.
This way you can standardize the breathing space (padding) in your app. Also, if  want to change the padding
size of the padding just change the value of padding and that's it. No need to change the padding for each container.


### HTML 
```html
<div class="panel">I'm panel</div>

<div class="card">I'm card</div>

<div class="alert">I'm alert<div>

```
 
### SASS
```css
$global-padding: 14px

.panel
 padding: $global-padding
	
.card
 padding: $global-padding
	
.alert 
 padding: $global-padding 

```


### SCSS
```css
$global-padding: 14px;

.panel {
 padding: $global-padding;
}	
.card {
 padding: $global-padding;
}	
.alert {
 padding: $global-padding;
}
```

### CSS
```css
.panel {
 padding: 14px;
}	
.card {
 padding: 14px;
}	
.alert {
 padding: 14px;
}
```

<br><br>

## Nesting
In CSS, in order for you to style nested html elements you have to follow the CSS nesting syntax which has many curly braces.
When your styles is getting bigger and larger nesting styles quite hard to maintain as there is no way to group related styles in CSS.
In SASS / SCSS nesting styles is pretty easy. It allows you to group your nested styles into more readable and maintainable way.
In the below example you will see how to organize your nested styles properly in SASS/SCSS.

### CSS
For example, you have a card which has card title , card description and card thumbnail image. 
In CSS here is the code to style nested html elements.
```css
.card {
 width:100%;
 height:auto;
}	
.card .title {
  font-size:24px;
}	
.card .description {
  font-size:15px;
}
.card .thumbnail {
 background-image:url('');
 width:100%;
 height:150px;
}
```


### SASS
Below is the code in SASS, as you can see below. As SASS does not have curly braces, tbis is how it looks when we do nesting in SASS.
A very neat and clean implementation. Please take note that you need to indent the child for SASS to read it properly.

```css
.card 
 width:100%
 height:auto
 	
  .title  
  font-size:24px
	
 .description 
  font-size:15px

 .thumbnail 
  background-image:url('')
  width:100%
  height:150px

```

### SCSS
In SCSS, it is quite the same with CSS with curly braces. Some people wants this kind of implementation as they still want to you curly brances. 
SCSS will group your nested styles using curcly brace. As parent style, you need to enclosed the child styles inside your curcly braces.
Below is the implementation of Nesting using SCSS

```css
.card  {
 width:100%
 height:auto
 	
  .title {
  font-size:24px }
	
 .description  {
  font-size:15px }

 .thumbnail {
  background-image:url('')
  width:100%
  height:150px }
}
```
You’ll notice that the .title, description, and thumbnail selectors are nested inside the .card selector. This is a great way to organize your styles and make it more readable and easy to find.






<br><br>

## Partial / Modularize	 
When your app is getting bigger the stylesheet is also getting bigger. Due to this, maintaining your CSS is quite challenging and time consuming.
For example, if you want to update the style of card you have to go through your long styles.css
and find the card related codes that you have to change. In SASS / SCSS, you can create a partial sass. 
You can create _card.sass where you can put all the card related styles and attached it to your main sass file.
To import it to your main class just simply follow 
<br>

File name :  `_card.sass`
```css
.card 
 width:100%
 height:auto
 	
  .title  
  font-size:24px
	
 .description 
  font-size:15px

 .thumbnail 
  background-image:url('')
  width:100%
  height:150px

```
In `main.sass`  /  `styles.sass` just use the below command to use card partial class `_card.sass` .
<br>
File name :  styles.sass or main.sass
```css
 @use 'card'
```
Keep in mind that for you to create a partial class you have to use underscore ( _filename.sass / _filename.scss ) at the beginning of your partial class name. In the example above "_card.sass" is being imported to "main.sass".

<br>
Partial sass is basically a sass file that allows you to modularize your styles and keep things separated and easier to maintain. 

Having a partial sass allows you to share style funtionality across your application. Using partial class "_card.sass" it is very easy to maintain, if you need to change the card styles you can just simply go to card.sass and do your changes without affecting the other styles.

<br>You can also create folder to organize and group your partial classes according to their purpose.
<br>
All partial class will be merged to main.css as one file after compiling the sass/ scss file. 
<br><br>



<br><br>

## Mixins
SASS allows you to reuse block of code to create customizable and dynamic styling. Using mixins, you are able to have a function to customize your styles. You can have paramters and control your styles accordingly.
<br>
Let's use mixins and create a style for tags.Tags could have many variations of sizes it could be small, medium, large. Also tags, sometimes could have close button. All of these you can achieve through mixins.
<br>
## sass 
```css
  .alert {
}
```
## scss 
```css
  .alert {
}
```

## css  
```css
  .alert {
} 
```










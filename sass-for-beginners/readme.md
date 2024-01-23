
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
 	
 .card .title  
  font-size:24px
	
 .card .description 
  font-size:15px

 .card .thumbnail 
  background-image:url('')
  width:100%
  height:150px

```






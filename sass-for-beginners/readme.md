
<img src="https://sass-lang.com/assets/img/logos/logo.svg" width="200" height="200">

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
In the demo below we have intiate a variable $primary-color and assigned #333 value to it . Which #333 is a hexadecimal value representing color.
Then we have used the variable $primary-color in the body to represent the background to #333.
<br><br>
 
<table>
<tr>
<th> SASS </th>
<th> SCSS </th>
</tr>
<tr>
<td>
 
```css
$primary-color: #333
body 
  background-color: $primary-color
```
 
</td>
<td>
 
```css 
$primary-color: #333;

body { 
  background-color: $primary-color;
}
```

</td>
</tr>
</table>

 
> [!TIP]
> Please think a more descriptive variable name as possible





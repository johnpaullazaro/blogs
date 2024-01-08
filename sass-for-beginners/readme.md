
<img src="https://sass-lang.com/assets/img/logos/logo.svg" width="200" height="200">

# Learn SASS
In this article, you will learn SASS and its basic features such as variables, inheritance and mixins.
This article is for beginners who doesnt have an idea on SASS / SCSS




## How to install?
To get started with SASS you have to install it.

Via NPM

```
npm install -g sass
```



## Generating CSS from SASS via SASS CLI
To generate open cmd / cli then follow the command below
```
sass source/stylesheets/index.scss build/stylesheets/index.css
```


## Variables
Creating your first variable in SASS. 
Variable is basically a holder of value that you can assign to different attribute everytime you needed the value of it.
<br>
styles.sass
```sass
$primary-color: #333

body 
  background-color: $primary-color
```

 
> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.









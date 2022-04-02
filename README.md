# 3D Cube Utility Library
This is an experimental but fully usable 3D cube utility library. It is 100% pure CSS. No pre-processor, No JavaScript.

You can create cubes easily without the need to create endless lines of code to size each cube. The utility CSS file does all 
the work for you. 

Check it out here https://designkojo.com/3D-cube-utility-library/

## The cube
The cube is designed differently than what is typically used. It use 3 inner divs that consist of 2 faces each. This was done so that there was no need to use a Z dimension. Why no Z dimension I hear you ask? That is because Z requires a unit such as px, you can't use % on the Z dimension as it is technically infinite. 

## How does it work?
Instructions to come but have a look at the style.css and the HTML and copy a cube and adjust the CSS. The utility CSS then works out all the dimension for you. 

```
/* lala or should I say dada!*/
/* Set a outer size for the cube */
.lala-cube {
  --width: 100px;
  transform: translateX(-150px) translateY(0) translateZ(0) rotateX(0) rotateY(0);
}
/* Adjust the height and depth as a percent on the width */
[class$="lala"] {
  --height: 50%;
  --depth: 130;
}
[class$="lala"] .inner {
  /* Larger borders px and em doesn't work*/
  border: .25em inset blue;
}
```

Change the classes `lala-cube` `depth-lala` to match the CSS
```
  <!-- Cube w/ Height & Depth -->
  <div class="cube lala-cube depth-lala">
    <div class="face-wrapper cube-height f1">
      <div class="inner inner--face-1 face-1"></div>
      <div class="inner inner--face-3 face-3"></div>
    </div>
    <div class="face-wrapper cube-height f2">
      <div class="inner inner--face-2 face-2"></div>
      <div class="inner inner--face-4 face-4"></div>
    </div>
    <div class="face-wrapper top-bottom">
      <div class="inner top cube-height-top"></div>
      <div class="inner bottom cube-height-bottom"></div>
    </div>
  </div>
```
Everything inside the `<div class="cube lala-cube depth-lala"> </div>` doesn't change so could use JavaScript to add it dynamically. JavaScript isn't needed for the utility library to work, it is 100% pure CSS. 


## Boiler Plate 
This project uses my base boiler plate. This is available from https://github.com/siramsay/bare-bones-boiler-plate

## HTML
### Elements Included
1. We have included a header and a main element. 
2. The main element has 2 elements an article and aside. 

**Main**

The main element has `display: flex;` set on it and the flex items as centred with `justify-content: center;` and 
`align-items: center;`.
That is all that is included since the main purpose of this boiler plate is CSS experimentation and drawing.

## CSS
### Reset CSS
I don't use a reset as such and prefer the idea of making base CSS style consistent. For that reason the boiler
plate uses normalize.css. It's included in the header and delivered via a CDN. If you prefer to download it, you can
visit https://github.com/necolas/normalize.css/

### Root and body color
I have added one custom property to override the body color this is for demonstration purposes and please change to 
a color. 

### Font 
There is no font set in the initial commit, so the font is default serif font.

### Box-sizing
We have set box-sizing to border-box using the most accept method that supports both content-box and padding-box
when needed.

## JavaScript
I have included a blank action.js file. 



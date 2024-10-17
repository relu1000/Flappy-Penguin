# Flappy-Penguin
Flappy Penguin
step1
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Your Page Title</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Your content goes here -->
</body>
</html>

step2
Target the body element to set the background to a linear gradient angled 45 degrees clockwise, starting at rgb(118, 201, 255) and ending at rgb(247, 255, 222).

body {
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
}

step3

Normalise your page's sizing, by removing the body element's margin and padding. 
body {
  margin: 0;
  padding: 0;
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
}

Step4

 body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100vh;
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
}
Step 5Passed
Remove both the horizontal and vertical scrollbars, using only one property.
body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100vh;
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
  overflow: hidden;
} 
step 6
<body>
  <div class="ground"></div>
</body>

Step 7Passed
Target the .ground element, and set its width to take up the full width of the viewport. Then, set the height to 400px.
.ground {
  width: 100vw;
  height: 400px;
}
Step 8Passed
Give the .ground element a background with a linear gradient angled 90 degrees clockwise, starting at rgb(88, 175, 236) and ending at rgb(182, 255, 255).
.ground {
  width: 100%;
  height: 400px;
  background: linear-gradient(90deg, rgb(88, 175, 236), rgb(182, 255, 255));
}
Step 9Passed
As the .ground element will be third in the stacking context of the page layout, set its z-index to 3, and position to absolute.
.ground {
  width: 100%;
  height: 400px;
  background: linear-gradient(90deg, rgb(88, 175, 236), rgb(182, 255, 255));
  position: absolute;
  z-index: 3;
}
Above the .ground element, add a div with a class of penguin. This div will contain Flappy Penguin.
<body>
  <div class="penguin">
    <!-- Flappy Penguin content will go here -->
  </div>
  <div class="ground"></div>
</body>
Target the .penguin element, and set its width and height to 300px.
.penguin {
  width: 300px;
  height: 300px;
}
Step 12
Use the margin property to horizontally center the .penguin element, and set the margin-top to 75px.
.penguin {
  width: 300px;
  height: 300px;
  margin: 75px auto 0;
}
Step 13
To create some scenery in the background, you will add two mountains.

Above the .penguin element, add a div with a class of left-mountain.
<body>
  <div class="left-mountain"></div>
  <div class="penguin">
    <!-- Flappy Penguin content will go here -->
  </div>
  <div class="ground"></div>
</body>
14 Target the .left-mountain element, and set its width and height to 300px. Then, set the background to a linear gradient starting at rgb(203, 241, 228) and ending at rgb(80, 183, 255).

.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
}
To prevent the mountain from pushing the .ground element, adjust its position to prevent it from taking up space in the page layout.

.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
}

To make the mountain look more like a mountain, you can use the skew transform function, which takes two arguments. The first being an angle to shear the x-axis by, and the second being an angle to shear the y-axis by.

Use the transform property to skew the mountain by 0deg in the x-axis and 44deg in the y-axis.

.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
  transform: skew(0deg, 44deg);
}
Step 17
Set the stack level of the mountain element such that it remains directly behind the .ground element.
.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
  transform: skew(0deg, 44deg);
  z-index: 2;
}
Step 18
To overlap the mountain and .ground elements better, give the mountain a margin-top of 100px, and the .ground element a margin-top of -58px.
.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
  transform: skew(0deg, 44deg);
  z-index: 2;
  margin-top: 100px;
}

.ground {
  width: 100%;
  height: 400px;
  background: linear-gradient(90deg, rgb(88, 175, 236), rgb(182, 255, 255));
  position: absolute;
  z-index: 3;
  margin-top: -58px;
}
Step 19
To give the effect of a mountain range, add another mountain, by creating a new div immediately after .left-mountain, and give the new div the class of back-mountain.
<body>
  <div class="left-mountain"></div>
  <div class="back-mountain"></div>
  <div class="penguin">
    <!-- Flappy Penguin content will go here -->
  </div>
  <div class="ground"></div>
</body>
Step 20
Target the .back-mountain element, and set its width and height to 300px. Then, set the background to a linear gradient starting at rgb(203, 241, 228) and ending at rgb(47, 170, 255).
.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
}
Step 21
Set the position property of the .back-mountain to prevent it from taking up space in the page layout.
.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
  position: absolute;
}
Step 22
Change the stack level of the .back-mountain element such that it is directly behind the .left-mountain element.
.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
  position: absolute;
  z-index: 1;
}
Step 23
Rotate the .back-mountain element by 45deg clockwise. Then, give it a left property of 110px, and a top property of 225px.
.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
  position: absolute;
  z-index: 1;
  transform: rotate(45deg);
  left: 110px;
  top: 225px;
}
Step 24
To finish the background, add a sun, by creating a new div element immediately after the .back-mountain element, and give it the class of sun.
<body>
  <div class="left-mountain"></div>
  <div class="back-mountain"></div>
  <div class="sun"></div>
  <div class="penguin">
    <!-- Flappy Penguin content will go here -->
  </div>
  <div class="ground"></div>
</body>
Step 25
Give the .sun element a width and height of 200px, and a background-color of yellow
.sun {
  width: 200px;
  height: 200px;
  background-color: yellow;
}
Step 26
Set the position property of the sun to prevent it from taking up space in the page layout, and set the border-radius such that the sun's shape is a circle.
.sun {
  width: 200px;
  height: 200px;
  background-color: yellow;
  position: absolute;
  border-radius: 50%;
}
Step 27
Position the sun in the top right corner of the screen such that 75px of its top and right edges are off screen.
.sun {
  width: 200px;
  height: 200px;
  background-color: yellow;
  position: absolute;
  border-radius: 50%;
  top: -75px;
  right: -75px;
}
Step 28
Your penguin will consist of two main sections: the head, and the body.

Within .penguin, add two new div elements. The first with a class of penguin-head, and the second with a class of penguin-body.
<body>
  <div class="left-mountain"></div>
  <div class="back-mountain"></div>
  <div class="sun"></div>
  <div class="penguin">
    <div class="penguin-head"></div>
    <div class="penguin-body"></div>
  </div>
  <div class="ground"></div>
</body>
Step 29
Change the stack level of the .penguin element such that it appears in front of the .ground element, and give it a position of relative.
.penguin {
  width: 300px;
  height: 300px;
  margin: 75px auto 0;
  position: relative;
  z-index: 4;
}
Step 30
Target the .penguin-head element, and give it a width half of its parent's, and a height of 45%. Then, set the background to a linear gradient at 45deg starting at gray, and ending at rgb(239, 240, 228).
.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(45deg, gray, rgb(239, 240, 228));
}
Step 31
Most penguins do not have a square head.

Give the penguin a slightly oval head by setting the radius of the top corners to 70% and the radius of the bottom corners to 65%.
.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(45deg, gray, rgb(239, 240, 228));
  border-top-left-radius: 70%;
  border-top-right-radius: 70%;
  border-bottom-left-radius: 65%;
  border-bottom-right-radius: 65%;
}
Step 32
Target the .penguin-body element, and give it a width of 53%, and a height of 45%. Then, set the background to a linear gradient at 45deg, rgb(134, 133, 133) from 0%, rgb(234, 231, 231) from 25%, and white from 67%.
.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(45deg, rgb(134, 133, 133) 0%, rgb(234, 231, 231) 25%, white 67%);
}
Step 33
Another interesting fact about penguins is that they do not have square bodies.

Use the border-radius property with a value of 80% 80% 100% 100%, to give the penguin a slightly rounded body.
.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(45deg, rgb(134, 133, 133) 0%, rgb(234, 231, 231) 25%, white 67%);
  border-radius: 80% 80% 100% 100%;
}
Step 34
Target all descendent elements of the .penguin element, and give them a position of absolute.
.penguin * {
  position: absolute;
}
Step 35
Position the .penguin-head element 10% from the top, and 25% from the left of its parent.
.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(45deg, gray, rgb(239, 240, 228));
  border-top-left-radius: 70%;
  border-top-right-radius: 70%;
  border-bottom-left-radius: 65%;
  border-bottom-right-radius: 65%;
  top: 10%;
  left: 25%;
}
Step 36
Position the .penguin-body element 40% from the top, and 23.5% from the left of its parent.
.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(45deg, rgb(134, 133, 133) 0%, rgb(234, 231, 231) 25%, white 67%);
  border-radius: 80% 80% 100% 100%;
  top: 40%;
  left: 23.5%;
}
Step 37
Change the stack level of the .penguin-head element such that it appears in front of the .penguin-body element.
.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(45deg, gray, rgb(239, 240, 228));
  border-top-left-radius: 70%;
  border-top-right-radius: 70%;
  border-bottom-left-radius: 65%;
  border-bottom-right-radius: 65%;
  top: 10%;
  left: 25%;
  z-index: 1;
}

.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(45deg, rgb(134, 133, 133) 0%, rgb(234, 231, 231) 25%, white 67%);
  border-radius: 80% 80% 100% 100

  Step 38
To give the penguin body a crest, create a pseudo-element that is the first child of the .penguin-body element. Set the content property of the pseudo-element to an empty string.
.penguin-body::before {
  content: '';
}
Step 39
Position the pseudo-element relative to its closest positioned ancestor.
.penguin-body::before {
  content: '';
  position: absolute;
}
Step 40
Give the pseudo-element a width half that of its parent, a height of 45%, and a background-color of gray.
.penguin-body::before {
  content: '';
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: gray;
}
Step 41
Position the pseudo-element 10% from the top and 25% from the left of its parent.
.penguin-body::before {
  content: '';
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: gray;
  top: 10%;
  left: 25%;
}
Step 42
Round off the crest, by giving the pseudo-element bottom corners a radius of 100%, leaving the top corners at 0%.
.penguin-body::before {
  content: '';
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: gray;
  top: 10%;
  left: 25%;
  border-bottom-left-radius: 100%;
  border-bottom-right-radius: 100%;
  border-top-left-radius: 0%;
  border-top-right-radius: 0%;
}
Step 43
Increase the pseudo-element's transparency by 30%.
.penguin-body::before {
  content: '';
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: gray;
  top: 10%;
  left: 25%;
  border-bottom-left-radius: 100%;
  border-bottom-right-radius: 100%;
  border-top-left-radius: 0%;
  border-top-right-radius: 0%;
  opacity: 0.7; /* 100% - 30% transparency */
}
Step 44
Start the penguin's face, by adding two div elements within .penguin-head, and giving them both a class of face.
<div class="penguin-head">
  <div class="face"></div>
  <div class="face"></div>
</div>
Step 45
Give the .face elements a width of 60%, a height of 70%, and a background-color of white.
.face {
  width: 60%;
  height: 70%;
  background-color: white;
}
Step 46
Make the top corners of the .face elements have a radius of 70%, and the bottom corners have a radius of 60%.
.face {
  width: 60%;
  height: 70%;
  background-color: white;
  border-top-left-radius: 70%;
  border-top-right-radius: 70%;
  border-bottom-left-radius: 60%;
  border-bottom-right-radius: 60%;
}

Step 47
Position the .face elements so that they are 15% from the top.
.face {
  width: 60%;
  height: 70%;
  background-color: white;
  border-top-left-radius: 70%;
  border-top-right-radius: 70%;
  border-bottom-left-radius: 60%;
  border-bottom-right-radius: 60%;
  top: 15%;
}
Step 48
Currently, the two .face elements are on top of each other.

Fix this, by adding a class of left to the first .face element, and a class of right to the second .face element.
<div class="penguin-head">
  <div class="face left"></div>
  <div class="face right"></div>
</div>
Step 49
Target the .face element with the left class, and position it 5% left of its parent.

.face.left {
  left: 5%;
}
Step 50
Target the .face element with the right class, and position it 5% right of its parent.
.face.right {
  right: 5%;
}
Step 51
Below the .face.right element, add a div element with a class of chin.
<div class="penguin-head">
  <div class="face left"></div>
  <div class="face right"></div>
  <div class="chin"></div>
</div>
Step 52
Target the .chin element, and give it a width of 90%, height of 70%, and background-color of white.
.chin {
  width: 90%;
  height: 70%;
  background-color: white;
}
Step 53
Position the .chin element such that it is 25% from the top, and 5% from the left of its parent. Then, give the top corners a radius of 70%, and the bottom corners a radius of 100%.
.chin {
  width: 90%;
  height: 70%;
  background-color: white;
  top: 25%;
  left: 5%;
  border-top-left-radius: 70%;
  border-top-right-radius: 70%;
  border-bottom-left-radius: 100%;
  border-bottom-right-radius: 100%;
}
Step 54
So far, the .face and .chin elements have the same background-color.

Create a custom CSS property called --penguin-face, and set it to white.
:root {
  --penguin-face: white;
}

.face {
  width: 60%;
  height: 70%;
  background-color: var(--penguin-face);
  border-top-left-radius: 70%;
  border-top-right-radius: 70%;
  border-bottom-left-radius: 60%;
  border-bottom-right-radius: 60%;
  top: 15%;
}

.chin {
  width: 90%;
  height: 70%;
  background-color: var(--penguin-face);
  top: 25%;
  left: 5%;
  border-top-left-radius: 70%;
  border-top-right-radius: 70%;
  border-bottom-left-radius: 100%;
  border-bottom-right-radius: 100%;
  
}

Step 55
Where relevant, replace property values with your --penguin-face variable.
:root {
  --penguin-face: white;
}

.face {
  width: 60%;
  height: 70%;
  background-color: var(--penguin-face);
  border-top-left-radius: 70%;
  border-top-right-radius: 70%;
  border-bottom-left-radius: 60%;
  border-bottom-right-radius: 60%;
  top: 15%;
}

.chin {
  width: 90%;
  height: 70%;
  background-color: var(--penguin-face);
  top: 25%;
  left: 5%;
  border-top-left-radius: 70%;
  border-top-right-radius: 70%;
  border-bottom-left-radius: 100%;
  border-bottom-right-radius: 100%;
}

.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(45deg, rgb(134, 133, 133) 0%, rgb(234, 231, 231) 25%, white 67%);
  border-radius: 80% 80% 100% 100%;
  top: 40%;
  left: 23.5%;
  z-index: 0;
}
Step 56
Below the .chin element, add two div elements each with a class of eye. Also, give the first .eye element a class of left, and the second .eye element a class of right.
<div class="penguin-head">
  <div class="face left"></div>
  <div class="face right"></div>
  <div class="chin"></div>
  <div class="eye left"></div>
  <div class="eye right"></div>
</div>
Step 57
Target the .eye elements, and give them a width of 15%, height of 17%, and background-color of black.
.eye {
  width: 15%;
  height: 17%;
  background-color: black;
}
Step 58
Position the .eye elements 45% from the top of their parent, and give all corners a radius of 50%.
.eye {
  width: 15%;
  height: 17%;
  background-color: black;
  top: 45%;
  border-radius: 50%;
}
Step 59
Target the .eye element with the left class, and position it 25% from the left of its parent. Then, target the .eye element with the right class, and position it 25% from the right of its parent.
.eye.left {
  left: 25%;
}

.eye.right {
  right: 25%;
}
Step 60
Within each .eye element, add a div with a class of eye-lid.
<div class="penguin-head">
  <div class="face left"></div>
  <div class="face right"></div>
  <div class="chin"></div>
  <div class="eye left">
    <div class="eye-lid"></div>
  </div>
  <div class="eye right">
    <div class="eye-lid"></div>
  </div>
</div>
Step 61
Target the .eye-lid elements, and give them a width of 150%, height of 100%, and background-color of --penguin-face.
.eye-lid {
  width: 150%;
  height: 100%;
  background-color: var(--penguin-face);
}
Step 62
Position the .eye-lid elements 25% from the top, and -23% from the left of their parents. Then, give all corners a radius of 50%.
.eye-lid {
  width: 150%;
  height: 100%;
  background-color: var(--penguin-face);
  top: 25%;
  left: -23%;
  border-radius: 50%;
}
Step 63
Below the .eye.right element, add two div elements each with a class of blush. Also, give the first .blush element a class of left, and the second .blush element a class of right.
<div class="blush left"></div>
  <div class="blush right"></div>
</div>
Step 64
Target the .blush elements, and give them a width of 15%, height of 10%, and background-color of pink.
.blush {
  width: 15%;
  height: 10%;
  background-color: pink;
}
Step 65
Position the .blush elements 65% from the top of their parent, and give all corners a radius of 50%.
.blush {
  width: 15%;
  height: 10%;
  background-color: pink;
  top: 65%;
  border-radius: 50%;
}
Step 66
Target the .blush element with a class of left, and position it 15% left of its parent. Then, target the .blush element with a class of right, and position it 15% right of its parent.
.blush.left {
  left: 15%;
}

.blush.right {
  right: 15%;
}

Step 67
Below the .blush.right element, add two div elements each with a class of beak. Also, give the first .beak element a class of top, and the second .beak element a class of bottom.
<div class="beak top"></div>
  <div class="beak bottom"></div>
</div>
Step 68
Target the .beak elements, and give them a height of 10%, background-color of orange, and give all corners a radius of 50%.
.beak {
  height: 10%;
  background-color: orange;
  border-radius: 50%;
}
Step 69
Target the .beak element with a class of top, give it a width of 20%, and position it 60% from the top, and 40% from the left of its parent.
.beak.top {
  width: 20%;
  height: 10%;
  background-color: orange;
  border-radius: 50%;
  top: 60%;
  left: 40%;
}
Step 70
Target the .beak element with a class of bottom, and give it a width 4% smaller than .beak.top, 5% further from the top, and 2% further from the left of its parent than .beak.top.
.beak.bottom {
  width: 16%; /* 4% smaller than 20% */
  height: 10%;
  background-color: orange;
  border-radius: 50%;
  top: 65%; /* 5% further from the top than 60% */
  left: 42%; /* 2% further from the left than 40% */
}
Step 71
The penguin's body looks a bit plain. Spruce him up by adding a div element with a class of shirt, immediately before the .penguin-body element.
<div class="shirt"></div>
Step 72
Within the .shirt element, add a div with the following emoji as content: 💜
<div class="penguin">
  <div class="shirt">
    <div>💜</div>
  </div>
  Step 73
Within .shirt, after the div element, add a p element with the following content: I CSS

    <p>I CSS</p>
  Step 74
Target the .shirt element, and set its font-size to 25px, font-family to Helvetica with a fallback of sans-serif, and font-weight to bold.
.shirt {
  font-size: 25px;
  font-family: Helvetica, sans-serif;
  font-weight: bold;
}
Step 75
In some browsers, the heart emoji may look slightly different from the previous step. This is because some of the character's properties were overridden by the font-weight style of bold.

Fix this, by targeting the div with the heart emoji, and setting its font-weight to its original value.
.shirt div {
  font-weight: normal;
}
Step 76
Position the div with the heart emoji 22.5px from the top, and 12px from the left of its parent.
.shirt div {
  font-weight: normal;
  position: absolute;
  top: 22.5px;
  left: 12px;
}
Step 77
Position the .shirt element 165px from the top, and 127.5px from the left of its parent. Then, increase its stacking order such that it appears above the .penguin-body element.
.shirt {
  font-size: 25px;
  font-family: Helvetica, sans-serif;
  font-weight: bold;
  position: absolute;
  top: 165px;
  left: 127.5px;
  z-index: 1; /* Ensure it appears above .penguin-body */
}

.shirt div {
  font-weight: normal;
  position: absolute;
  top: 22.5px;
  left: 12px;
}
Step 78
For the shirt's final touch, set the color to #6a6969.
.shirt {
  font-size: 25px;
  font-family: Helvetica, sans-serif;
  font-weight: bold;
  position: absolute;
  top: 165px;
  left: 127.5px;
  z-index: 1; /* Ensure it appears above .penguin-body */
  color: #6a6969;
}

.shirt div {
  font-weight: normal;
  position: absolute;
  top: 22.5px;
  left: 12px;
}
Step 79
Fun fact: Penguins cannot stand without at least two feet.

Within the .penguin-body element, add two div elements each with a class of foot. Give the first .foot a class of left, and the second .foot a class of right.
<div class="penguin-body">
    <div class="foot left"></div>
    <div class="foot right"></div>
     </div>
Step 80
Target the .foot elements, and give them a width of 15%, height of 30%, and background-color of orange.
.foot {
  width: 15%;
  height: 30%;
  background-color: orange;
}
Step 81
Position the .foot elements 85% from the top of their parent, and give all corners a radius of 50%.
.foot {
  width: 15%;
  height: 30%;
  background-color: orange;
  top: 85%;
  border-radius: 50%;
}
Step 82
The penguin's beak and feet share the same color.

Create a new custom CSS variable named --penguin-picorna, and replace all relevant property values with it.
:root {
  --penguin-picorna: orange;
}

.beak {
  height: 10%;
  background-color: var(--penguin-picorna);
  border-radius: 50%;
}

.beak.top {
  width: 20%;
  top: 60%;
  left: 40%;
}

.beak.bottom {
  width: 16%;
  top: 65%;
  left: 42%;
}

.foot {
  width: 15%;
  height: 30%;
  background-color: var(--penguin-picorna);
  top: 85%;
  border-radius: 50%;
}
Step 83
Target the .foot element with a class of left, and position it 25% left of its parent. Then, target the .foot element with a class of right, and position it 25% right of its parent.
.foot.left {
  left: 25%;
}

.foot.right {
  right: 25%;
}
Step 84
To make the penguin's feet look more penguiny, rotate the left foot by 80deg, and the right by -80deg.
.foot.left {
  left: 25%;
  transform: rotate(80deg);
}

.foot.right {
  right: 25%;
  transform: rotate(-80deg);
}
Step 85
Change the stacking order of the .foot elements such that they appear beneath the .penguin-body element.
.foot {
  width: 15%;
  height: 30%;
  background-color: var(--penguin-picorna);
  top: 85%;
  border-radius: 50%;
  z-index: -1; /* Ensuring it appears beneath .penguin-body */
  position: absolute;
}

.penguin-body {
  z-index: 1;
}
Step 86
Fun fact: Penguins cannot fly without wings.

Within .penguin-body, before the .foot elements, add two div elements each with a class of arm. Give the first .arm a class of left, and the second .arm a class of right.
<div class="penguin-body">
  <div class="arm left"></div>
  <div class="arm right"></div>
  <div class="foot left"></div>
  <div class="foot right"></div>
  
  </div>
</div>
Step 87
Target the .arm elements, and give them a width of 30%, a height of 60%, and a background of linear gradient at 90deg from clockwise, starting at gray, and ending at rgb(209, 210, 199).
.arm {
  width: 30%;
  height: 60%;
  background: linear-gradient(90deg, gray, rgb(209, 210, 199));
}
88 Create a custom CSS variable named --penguin-skin, and set it to gray. Then, replace all relevant property values with it.
:root {
  --penguin-face: white;
  --penguin-picorna: orange;
  --penguin-skin: gray; 
}

body {
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
  transform: skew(0deg, 44deg);
  z-index: 2;
  margin-top: 100px;
}

.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
  position: absolute;
  z-index: 1;
  transform: rotate(45deg);
  left: 110px;
  top: 225px;
}

.sun {
  width: 200px;
  height: 200px;
  background-color: yellow;
  position: absolute;
  border-radius: 50%;
  top: -75px;
  right: -75px;
}

.penguin {
  width: 300px;
  height: 300px;
  margin: auto;
  margin-top: 75px;
  z-index: 4;
  position: relative;
}

.penguin * {
  position: absolute;
}

.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(45deg, var(--penguin-skin), rgb(239, 240, 228));
  border-radius: 70% 70% 65% 65%;
  top: 10%;
  left: 25%;
  z-index: 1;

  
  border-radius: 70% 70% 65% 65%;
  top: 10%;
  left: 25%;
  z-index: 1;
}

.face {
  width: 60%;
  height: 70%;
  background-color: var(--penguin-face);
  border-radius: 70% 70% 60% 60%;
  top: 15%;
}

.face.left {
  left: 5%;
}

.face.right {
  right: 5%;
}

.chin {
  width: 90%;
  height: 70%;
  background-color: var(--penguin-face);
  top: 25%;
  left: 5%;
  border-radius: 70% 70% 100% 100%;
}

.eye {
  width: 15%;
  height: 17%;
  background-color: black;
  top: 45%;
  border-radius: 50%;
}

.eye.left {
  left: 25%;
}

.eye.right {
  right: 25%;
}

.eye-lid {
  width: 150%;
  height: 100%;
  background-color: var(--penguin-face);
  top: 25%;
  left: -23%;
  border-radius: 50%;
}

.blush {
  width: 15%;
  height: 10%;
  background-color: pink;
  top: 65%;
  border-radius: 50%;
}

.blush.left {
  left: 15%;
}

.blush.right {
  right: 15%;
}

.beak {
  height: 10%;
  background-color: var(--penguin-picorna);
  border-radius: 50%;
}

.beak.top {
  width: 20%;
  top: 60%;
  left: 40%;
}

.beak.bottom {
  width: 16%;
  top: 65%;
  left: 42%;
}

.shirt {
  font: bold 25px Helvetica, sans-serif;
  top: 165px;
  left: 127.5px;
  z-index: 1;
  color: #6a6969;
}

.shirt div {
  font-weight:  initial;
  top: 22.5px;
  left: 12px;
}

.penguin-body::before {
  content: "";
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: var(--penguin-skin);
  top: 10%;
  left: 25%;
  border-radius: 0% 0% 100% 100%;
  opacity: 70%;
}

  border-radius: 80% 80% 100% 100%;
  top: 40%;
  left: 23.5%;
}

.penguin-body::before {
  content: "";
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: gray;
  top: 10%;
  left: 25%;
  border-radius: 0% 0% 100% 100%;
  opacity: 70%;
}

.arm {
  width: 30%;
  height: 60%;
  background: linear-gradient(90deg, var(--penguin-skin), rgb(209, 210, 199));
}

}

Step 89
Target the .arm element with a class of left, and position it 35% from the top, and 5% from the left of its parent. Then, target the .arm element with a class of right, and position it 0% from the top, and -5% from the right of its parent.
.arm.left {
  top: 35%;
  left: 5%;
}

.arm.right {
  top: 0%;
  right: -5%;
}
Step 90
Within the .arm.left selector, alter the origin of the transform function to be the top left corner of its parent.
.arm.left {
  top: 35%;
  left: 5%;
  transform-origin: top left;
}


.arm.right {
  top: 0%;
  right: -5%;
}
Step 91
To keep the linear gradient on the correct side of the penguin's left arm, first rotate it by 130deg, then invert the x-axis.
.arm.left {
  top: 35%;
  left: 5%;
  transform-origin: top left;
  transform: rotate(130deg) scaleX(-1);
}

92 Rotate the right arm by 45deg counterclockwise.
.arm.right {
  top: 0%;
  right: -5%;
  transform: rotate(-45deg);
}
Step 93
Fun fact: Most, if not all, flippers are not naturally rectangles.

Give the .arm elements' top-left, top-right, and bottom-right corners a radius of 30%, and the bottom-left corner a radius of 120%
.arm {
  width: 30%;
  height: 60%;
  background: linear-gradient(90deg, var(--penguin-skin), rgb(209, 210, 199));
  border-top-left-radius: 30%;
  border-top-right-radius: 30%;
  border-bottom-right-radius: 30%;
  border-bottom-left-radius: 120%;
  position: absolute;
}

.arm.left {
  top: 35%;
  left: 5%;
  transform-origin: top left;
  transform: rotate(130deg) scaleX(-1);
}

.arm.right {
  top: 0%;
  right: -5%;
  transform: rotate(-45deg);
}
Step 94
Change the .arm elements' stacking order such that they appear behind the .penguin-body element.
.arm {
  width: 30%;
  height: 60%;
  background: linear-gradient(90deg, var(--penguin-skin), rgb(209, 210, 199));
  border-radius: 30% 30% 30% 120%;
  position: absolute;
  z-index: -1; /* Ensuring it appears behind .penguin-body */
}

.penguin-body {
  z-index: 1;
}
Step 95
Now, you are going to use CSS animations to make the penguin wave.

Define a new @keyframes named wave.
@keyframes wave {
  /* Animation keyframes will go here */
}
@keyframes wave {
  10% { /* Add your transformations here */ }
  20% { /* Add your transformations here */ }
  30% { /* Add your transformations here */ }
  40% { /* Add your transformations here */ }
}
Step 97
Within the first waypoint, rotate to 110deg, and retain the scaling of the left arm.
@keyframes wave {
  10% {
    transform: rotate(110deg) scaleX(-1);
  }
  20% {
    /* Add your transformations here */
  }
  30% {
    /* Add your transformations here */
  }
  40% {
    /* Add your transformations here */
  }
}
Step 98
Within the second waypoint, rotate to 130deg, and retain the scaling of the left arm.
@keyframes wave {
  10% {
    transform: rotate(110deg) scaleX(-1);
  }
  20% {
    transform: rotate(130deg) scaleX(-1);
  }
  30% {
    /* Add your transformations here */
  }
  40% {
    /* Add your transformations here */
  }
}
Step 99
For the third and fourth waypoints, repeat the transform pattern once more.
@keyframes wave {
  10% {
    transform: rotate(110deg) scaleX(-1);
  }
  20% {
    transform: rotate(130deg) scaleX(-1);
  }
  30% {
    transform: rotate(110deg) scaleX(-1);
  }
  40% {
    transform: rotate(130deg) scaleX(-1);
  }
}
Step 100
Use the wave animation on the left arm. Have the animation last 3s, infinitely iterate, and have a linear timing function.
.arm.left {
  top: 35%;
  left: 5%;
  transform-origin: top left;
  transform: rotate(130deg) scaleX(-1);
  animation: wave 3s linear infinite;
}
Step 101
Target the .penguin element when it is active, and increase its size by 50% in both dimensions.
.penguin:active {
  transform: scale(1.5);
}
Step 102
When you activate the .penguin element, it might look as though you can drag it around. This is not true.

Indicate this to users, by giving the active element a cursor property of not-allowed.
.penguin:active {
  transform: scale(1.5);
  cursor: not-allowed;
}
Step 103
Change the .penguin element's transition behavior during transformation to have a duration of 1s, a timing function of ease-in-out, and a delay of 0ms.
.penguin {
  transition: transform 1s ease-in-out 0ms;
}

.penguin:active {
  transform: scale(1.5);
  cursor: not-allowed;
}
Step 104
Finally, calculate the height of the .ground element to be the height of the viewport minus the height of the .penguin element.

Congratulations! You have completed the Responsive Web Design certification.
.ground {
  width: 100vw;
  height: calc(100vh - 300px); /* Subtracting the height of the .penguin */
  background: linear-gradient(90deg, rgb(88, 175, 236), rgb(182, 255, 255));
  z-index: 3;
  position: absolute;
  margin-top: -58px;
}




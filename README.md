# MountainKing1.github.io

https://github.com/MountainKing1/MountainKing1.github.io/

<!DOCTYPE html>
<html> 
  <head>
    <title>Processing.JS inside Webpages: Template</title> 
  </head>
  <body>
	<!--This draws the canvas on the webpage -->
    <canvas id="mycanvas"></canvas> 
  </body>
 
  <!-- Include the processing.js library -->
  <!-- See https://khanacademy.zendesk.com/hc/en-us/articles/202260404-What-parts-of-ProcessingJS-does-Khan-Academy-support- for differences -->
  <script src="https://cdn.jsdelivr.net/processing.js/1.4.8/processing.min.js"></script> 
  <script>
  var programCode = function(processingInstance) {
    with (processingInstance) {
      size(400, 400); 
      frameRate(30);
        
      // Paste code from Khan Academy here:
      
draw = function() {
    
background(255, 255, 255);

noStroke();

var fiF;
fiF = 50;

//Eyes Left Right
var center2Axis;
center2Axis = 200;

//Head Left / Right 
var center1Axis;
center1Axis = mouseX;

//Head Up / Down
var y1Axis;
y1Axis = mouseY;

//Eyes Up / Down
var y0Axis;
y0Axis = (76);
    
//Outer Ears
    //Left Ear A, B, C
    fill(117, 147, 78);
    triangle(
        center1Axis-124 , y1Axis+16,
        center1Axis+82 , y1Axis-29,
        center1Axis-194 , y1Axis-117
        );
    
    //Right Ear A, B, C
    fill(117, 147, 78);
    triangle(
        center1Axis+124 , y1Axis+16,
        center1Axis-82 , y1Axis-29,
        center1Axis+194 , y1Axis-117
        );
    
//Inner Ears
    var innerScale;
    innerScale = 1.2;
    
    //Left Ear A, B, C
    fill(17, 147, 78);
    triangle(
        (-80*innerScale) + (center1Axis-79) , (-51*innerScale) + (y1Axis-43),
        (-32*innerScale) + (center1Axis-79) , (41*innerScale) + (y1Axis-43),
        (112*innerScale) + (center1Axis-79) , (10*innerScale) + (y1Axis-43)
    );
    
    //Right Ear A, B, C
    fill(17, 147, 78);
    triangle(
        (80*innerScale) + (center1Axis+79) , (-51*innerScale) + (y1Axis-43),
        (32*innerScale) + (center1Axis+79) , (41*innerScale) + (y1Axis-43),
        (-112*innerScale) + (center1Axis+79) , (10*innerScale) + (y1Axis-43)
    );
    
//Pupil Movement
    //Left Eye
    noStroke();
    fill(255, 255, 255);
    ellipse( (center1Axis-52) , (y1Axis-45) , 60 , 60 );
    
    //Right Eye
    noStroke();
    fill(255, 255, 255);
    ellipse( (center1Axis+52) , (y1Axis-45) , 60 , 60 );
    
//Eyes Big
    //Left Pupil
    noStroke();
    fill(40, 40, 40);
    ellipse( center2Axis-52 , y0Axis-45 , 35 , 35 );
    
    //Right Pupil
    noStroke();
    fill(40, 40, 40);
    ellipse( center2Axis+52 , y0Axis-45 , 35 , 35 );

    //Left Iris
    noStroke();
    fill(255, 255, 255);
    ellipse( center2Axis-44 , y0Axis-50 , 12 , 12 );
    
    //Right Iris
    noStroke();
    fill(255, 255, 255);
    ellipse( center2Axis+60 , y0Axis-50 , 12 , 12 );
    
//Eyes Small
    //Left Small
    noStroke();
    fill(40, 40, 40);
    ellipse( center2Axis-52 , y0Axis , 7 , 7 );
    
    //Right Small
    noStroke();
    fill(40, 40, 40);
    ellipse( center2Axis+52 , y0Axis , 7 , 7 );
    
//Hearts
    //Left Heart - Left Side
    noStroke();
    fill(255, 0, 0);
    beginShape();
    curveVertex( center2Axis+127 , y0Axis+180 );
    curveVertex( center2Axis-52 , y0Axis+29 );
    curveVertex( center2Axis-52 , y0Axis+50 );
    curveVertex( center2Axis+12 , y0Axis+25 );
    endShape();
    
    //Left Heart - Right Side
    beginShape();
    curveVertex( center2Axis-222 , y0Axis+180 );
    curveVertex( center2Axis-52 , y0Axis+29 );
    curveVertex( center2Axis-52 , y0Axis+50 );
    curveVertex( center2Axis-112 , y0Axis+25 );
    endShape();
    
    //Right Heart - Left Side
    noStroke();
    fill(255, 0, 0);
    beginShape();
    curveVertex( center2Axis+222 , y0Axis+180 );
    curveVertex( center2Axis+52 , y0Axis+29 );
    curveVertex( center2Axis+52 , y0Axis+50 );
    curveVertex( center2Axis+112 , y0Axis+25 );
    endShape();
    
    //Right Heart - Right Side
    beginShape();
    curveVertex( center2Axis-127 , y0Axis+180 );
    curveVertex( center2Axis+52 , y0Axis+29 );
    curveVertex( center2Axis+52 , y0Axis+50 );
    curveVertex( center2Axis-12 , y0Axis+25 );
    endShape();
    
//Crazy Eyes
    //Crazy Left
    stroke(40, 40, 40);
    strokeWeight(3);
    noFill();
    bezier(
        center2Axis-48 , y0Axis+84 , center2Axis-101 , y0Axis+89,
        center2Axis-11 , y0Axis+40 , center2Axis-60 , y0Axis+79
    );
    bezier(
        center2Axis-44 , y0Axis+82 , center2Axis-72 , y0Axis+82,
        center2Axis-61 , y0Axis+46 , center2Axis-44 , y0Axis+74
    );
    
    //Crazy Right
    stroke(40, 40, 40);
    strokeWeight(3);
    noFill();
    bezier(
        center2Axis+48 , y0Axis+84 , center2Axis+101 , y0Axis+89,
        center2Axis+11 , y0Axis+40 , center2Axis+60 , y0Axis+79
    );
    bezier(
        center2Axis+44 , y0Axis+82 , center2Axis+72 , y0Axis+82,
        center2Axis+61 , y0Axis+46 , center2Axis+44 , y0Axis+74
    );
    
//Rainbows
var r2Width;
r2Width = 191;

    //Red
    noStroke();
    fill(255, 0, 0);
    rect( center2Axis-(r2Width/2), y0Axis+18+(fiF*2), r2Width, 60 );
    
    //Orange
    noStroke();
    fill(255, 125, 0);
    rect(center2Axis-(r2Width/2),y0Axis+0+(fiF*3), r2Width, 60);

    //Yellow
    noStroke();
    fill(255, 255, 0);
    rect(center2Axis-(r2Width/2),y0Axis-18+(fiF*4), r2Width, 60);    
    
    //Green
    noStroke();
    fill(26, 255, 0);
    rect(center2Axis-(r2Width/2),y0Axis-36+(fiF*5), r2Width, 60);  
    
    //Blue
    noStroke();
    fill(0, 0, 255);
    rect(center2Axis-(r2Width/2),y0Axis-54+(fiF*6), r2Width, 60);  
    
    //Purple
    noStroke();
    fill(255, 0, 255);
    rect(center2Axis-(r2Width/2),y0Axis-72+(fiF*7), r2Width, 60);
    
//Face 2
    //Left "Eyelid"
    noFill();
    strokeWeight(38);
    stroke(117, 147, 78);
    arc( center1Axis-52 , y1Axis-45 , 85 , 85 , 0 , 360 );
    
    //Right "Eyelid"
    noFill();
    strokeWeight(38);
    stroke(117, 147, 78);
    arc( center1Axis+52 , y1Axis-45 , 85 ,85 , 0 , 360 );
    
    //Head Outline
    noFill();
    strokeWeight(39);
    stroke(117, 147, 78);
    arc( center1Axis , y1Axis , 221 , 221, 0 , 360 );
    
    //Rectangle 1
var r1Width;
r1Width = 55;
    fill(117, 147, 78);
    noStroke();
    rect( center1Axis-(r1Width/2) , y1Axis-100 , r1Width , 200 );
    
    //Rectangle 2
var r2Width;
r2Width = 191;
    fill(117, 147, 78);
    noStroke();
    rect( center1Axis-(r2Width/2) , y1Axis-8 , r2Width , 94 );
    
    //Nose
    noFill();
    strokeWeight(10);
    stroke(38, 71, 48);
    arc( center1Axis , y1Axis+15 , 34 , 19 , 190 , 350 );

    //Mouth
    noFill();
    strokeWeight(10);
    stroke(38, 71, 48);
    arc( center1Axis , y1Axis , 180 , 200 , 20 , 160 );
    
    //Text
    fill(30, 30, 30);
    textFont("monospace", 89);
    text("", 100, 304, 236, 411);
    
};


  // Get the canvas that ProcessingJS will use
  var canvas = document.getElementById("mycanvas"); 
  // Pass the function to ProcessingJS constructor
  var processingInstance = new Processing(canvas, programCode); 
  </script>
</html>

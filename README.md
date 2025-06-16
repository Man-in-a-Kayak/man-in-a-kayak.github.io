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
      
//Color backgroung white
background(255, 255, 255);
//1st Panel
    //Blue Shadow
        strokeWeight(0.25);
        fill(84, 84, 84);
        ellipse(120, 180, 68, 10);
    //Blue Circle
        strokeWeight(0.25);
        fill(0, 0, 255);
        ellipse(120, 140, 80, 80);
    //Red Shadow
        strokeWeight(0.25);
        fill(82, 82, 82);
        ellipse(48, 190, 85, 13.75);
    //Red 
        strokeWeight(0.75);
        fill(255, 0, 0);
        ellipse(48, 135, 100, 110);
    //Red Speech Bubble
        fill(255, 0, 0);
        textFont("monospace", 22);
        text("Okay honey, I'm off to work", 0, 2, 200, 400);
    //Blue Speech Bubble
        fill(0, 0, 255);
        textFont("monospace", 22);
        text("Okay, bye", 80, 62, 200, 400);
//2nd Panel
    //Red Text
        fill(255, 0, 0);
        textFont("monospace", 22);
        text("*                   Red Circle", 217, 62, 195, 400);
    //Black Text
        fill(0, 0, 0);
        textFont("monospace", 22);
        text("*Later, while                      is at work*", 217, 62, 195, 400);
//3rd Panel
    //Blue Shadow
        strokeWeight(0.25);
        fill(84, 84, 84);
        ellipse(120, 387, 68, 10);
    //Blue Circle
        strokeWeight(0.25);
        fill(0, 0, 255);
        ellipse(120, 347, 80, 80);
    //Heart
            rotate(6);
            strokeWeight(1);
            fill(255, 0, 0);
            beginShape();
        //Right Hump
            curveVertex(-221,  716);
        //Right Boot
            curveVertex(150,  284);
        //Dip
            curveVertex(150,  247);
        //Left Hump
            curveVertex(130,  237);
        //Left Boot
            curveVertex(150, 285);
        //Left Panel
            curveVertex(220, 321);
            endShape();
    //Green rectangle shadow
        fill(87, 87, 87);
        rotate(-6);
        rect(-5, 380, 96, 16);
    //Green rectangle
        strokeWeight(1.46);
        fill(37, 176, 60);
        rotate(6);
        rect(40, 247, 90, 135);
//4th Panel
    rotate(-6);
    //Blue Shadow
        strokeWeight(0.25);
        fill(84, 84, 84);
        ellipse(330, 385, 68, 10);
    //Blue Circle
        strokeWeight(0.25);
        fill(0, 0, 255);
        ellipse(330, 345, 80, 80);
    //Fetus
        strokeWeight(0.25);
        fill(39, 231, 189);
        ellipse(330, 357, 29, 32);
    //Red Shadow
        strokeWeight(0.25);
        fill(82, 82, 82);
        ellipse(258, 395, 85, 13.75);
    //Red 
        strokeWeight(0.75);
        fill(255, 0, 0);
        ellipse(258, 340, 100, 110);
    //Red Speech Bubble
        fill(255, 0, 0);
        textFont("monospace", 22);
        text("You're pregnant?!", 210, 207, 200, 400);
    //Blue Speech Bubble
        fill(0, 0, 255);
        textFont("monospace", 22);
        text("It was a mistake,          I swear!", 299, 231, 147, 400);
//Panel Frames
    rotate(0);
    strokeWeight(10);
    line(200, 0, 200, 400);
    line(0, 200, 400, 200);


  // Get the canvas that ProcessingJS will use
  var canvas = document.getElementById("mycanvas"); 
  // Pass the function to ProcessingJS constructor
  var processingInstance = new Processing(canvas, programCode); 
  </script>
</html>

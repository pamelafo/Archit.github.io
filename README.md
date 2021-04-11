
 -->
<html> 
 <head>
    <title>Processing.JS inside Webpages: Template</title> 
</head>
 <body>
    <p align="center"> 
	<!--This draws the Canvas on the webpage -->
      <canvas id="mycanvas"></canvas> 
    </p>
 </body>
 
 <!-- Run all the JavaScript stuff -->
 <!-- Include the processing.js library -->
 <!-- See https://khanacademy.zendesk.com/hc/en-us/articles/202260404-What-parts-of-ProcessingJS-does-Khan-Academy-support- for differences -->
 <script src="https://cdn.jsdelivr.net/processing.js/1.4.8/processing.min.js"></script> 
 
 <script>
    var sketchProc = function(processingInstance) {
     with (processingInstance) {
        size(400, 400); 
        frameRate(30);
        
        // ProgramCodeGoesHere
        fill(255, 255, 0);
        ellipse(200, 200, 200, 200);
        noFill();
        stroke(0, 0, 0);
        strokeWeight(2);
        arc(200, 200, 150, 100, 0, PI);
        fill(0, 0, 0);
        ellipse(250, 200, 10, 10);
        ellipse(153, 200, 10, 10);
    }};

    // Get the canvas that Processing-js will use
    var canvas = document.getElementById("mycanvas"); 
    // Pass the function sketchProc (defined in myCode.js) to Processing's constructor.
    var processingInstance = new Processing(canvas, sketchProc); 
 </script>

</html>

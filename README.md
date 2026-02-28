# hello!


function setup() {
  createCanvas(400, 400);
  noStroke();
}

function draw() {
  background(20);
  
  // Use HSB color mode for easy rainbow cycling
  colorMode(HSB, 360, 100, 100);
  
  // Change color based on time (framecount)
  let hue = frameCount % 360;
  catColor = color(hue, 80, 100);
  
  // Move the cat to the mouse position
  let x = mouseX;
  let y = mouseY;
  
  // Draw the Cat
  fill(catColor);
  
  // Ears
  triangle(x - 30, y - 40, x - 10, y - 20, x - 30, y - 10); // Left
  triangle(x + 30, y - 40, x + 10, y - 20, x + 30, y - 10); // Right
  
  // Head
  ellipse(x, y, 60, 50);
  
  // Eyes
  fill(0);
  ellipse(x - 15, y - 5, 10, 10);
  ellipse(x + 15, y - 5, 10, 10);
  
  // Nose
  fill(255, 100, 100); // Pinkish
  triangle(x, y + 5, x - 5, y, x + 5, y);
}

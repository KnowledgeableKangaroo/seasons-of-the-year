var scene;
var season = "";
var seasonTime = 20; // Number of seconds each season is shown
var m = month();
var d = day();
var interA = color(255, 127.5, 0);
var interB = color(255, 255, 255);
if ((m === 12 && d >= 21) || m === 1 || m === 2 || (m === 3 && d < 20)) {
    scene = 1;
} // If days are within the season of Winter
if ((m === 3 && d >= 20) || m === 4 || m === 5 || (m === 6 && d < 21)) {
    scene = 2;
} // If days are within the season of Spring
if ((m === 6 && d >= 21) || m === 7 || m === 8 || (m === 9 && d < 22)) {
    scene = 3;
} // If days are within the season of Summer
if ((m === 9 && d >= 22) || m === 10 || m === 11 || (m === 12 && d < 21)) {
    scene = 4;
} // If days are within the season of Fall
var timer = 0;
var Flakes = function(x, y) {
    fill(255, 255, 255);
    ellipse(x, y, 10, 10);
};
var drawWinter = function() {
    scene = 1;
    if(!drawWinter.init) {
    drawWinter.trans = 10;
    drawWinter.positions = [75, 280, 310, 200, 140, round(random(100, 350)), 380, 50, 100, 240, 180];
    drawWinter.speedB = [3.5, 3, 5, 4, 4.5, 2.5, 2, 3.2, 2.2, 4.2, 5.2, 4.7];
    drawWinter.sy = [-10, -10, -10, -10, -10, -10, -10, -10, -10, -10, -10, -10];
    drawWinter.init = true;
    }
    var trans = drawWinter.trans;
    var positions = drawWinter.positions;
    var speedB = drawWinter.speedB;
    var sy = drawWinter.sy;
    drawWinter.init = true;
    // The Outline
    background(0, 238, 255);
    noStroke();
    // The Ground
    fill(226, 233, 252);
    rect(0, 300, 400, 100);
    // The Snowman Body
    fill(255, 255, 255);
    ellipse(200, 300, 150, 150);
    ellipse(200, 200, 100, 100);
    ellipse(200, 120, 75, 75);
    // The Snowman Nose
    fill(255, 127, 0);
    triangle(266, 123, 184, 127, 184, 114);
    // The Snowman Eyes
    stroke(0, 0, 255);
    strokeWeight(7);
    point(181, 105);
    translate(40, 0);
    point(181, 105);
    // The Snowman Mouth
    stroke(0);
    strokeWeight(4);
    point(130, 120);
    translate(10, 10);
    point(130, 120);
    translate(trans, trans);
    point(130, 120);
    translate(trans, 0);
    point(130, 120);
    translate(10, 0);
    point(130, 120);
    translate(trans, -trans);
    point(130, 120);
    resetMatrix();
    for (var l = 0; l < positions.length; l++) {
        noStroke();
        Flakes(positions[l], sy[l]);
        sy[l] += speedB[l];
        if (sy[l] > 338) {
            sy[l] = -1;
        }
    } // Snowflakes
};
var Rainbow = function(x, y, radius) {
    this.x = x;
    this.y = y;
    this.radius = radius + -7;
};
var drawRainbow = function(rainbow) {
    noFill();
    strokeWeight(5);
    stroke(255, 0, 0);
    arc(rainbow.x, rainbow.y, rainbow.radius, rainbow.radius, 180, 360);
    stroke(250, 200, 0);
    arc(rainbow.x, rainbow.y, rainbow.radius - 10, rainbow.radius - 10, 180, 360);
    stroke(240, 255, 102);
    arc(rainbow.x, rainbow.y, rainbow.radius - 20, rainbow.radius - 20, 180, 360);
    stroke(29, 255, 13);
    arc(rainbow.x, rainbow.y, rainbow.radius - 30, rainbow.radius - 30, 180, 360);
    stroke(122, 155, 255);
    arc(rainbow.x, rainbow.y, rainbow.radius - 40, rainbow.radius - 40, 180, 360);
};
var smallestRainbow = new Rainbow(200, 200, 150);
var smallerRainbow = new Rainbow(200, 200, 200);
var smallRainbow = new Rainbow(200, 200, 250);
var bigRainbow = new Rainbow(200, 200, 300);
var biggerRainbow = new Rainbow(200, 200, 350);
var biggestRainbow = new Rainbow(200, 200, 400);
var drawSpring = function() {
    scene = 2;
    if(!drawSpring.init) {
    drawSpring.rainDrop = {
        xPositions: [109, 128, 90, 110, 360, 360, round(random(20, 380)), 262, 40, 75, 280, 310, 200, 140, round(random(100, 350)), 80, 50, 10, 211, 180],
        yPositions: [0, -110, -110, -85, -50, -75, 0, -10, -25, -10, -10, 79, -10, -10, -10, -10, -10, -10, -10, -10, -10],
        startyPositions: [0, -110, -110, -85, -50, -75, 0, -10, -25, -10, -10, -10, -10, -10, -10, -10, -10, -10, -10, -10, -10],
        startxPositions: [200, 270, 90, 25, 360, 360, round(random(20, 380)), 385, 40, 75, 280, 30, 200, 140, round(random(100, 350)), 80, 50, 10, 240, 180],
        speeds: [2, 1.5, 3, 2.5, 2.5, 2.5, 4, 4.5, 5, round(random(1.1, 5.6)), 3.5, 3, 5, 4, 4.5, 2.5, 2, 3.2, 2.2, 4.2, 5.2, 4.7],
        width: [10, 20, 10, 10, 5, 10, 10, 15, 10, 10, 15, 15, 20],
        height: [20, 30, 30, 40, 15, 15, 20, 20, 10, 10, 15, 10]
    };
    drawSpring.init = true;
}
    var rainDrop = drawSpring.rainDrop;
    background(0, 204, 255);
    drawRainbow(smallerRainbow);
    drawRainbow(bigRainbow);
    drawRainbow(biggerRainbow);
    drawRainbow(smallestRainbow);
    drawRainbow(biggestRainbow);
    drawRainbow(smallRainbow);
    noStroke();
    fill(200, 195, 200);
    ellipse(70, 200, 165, 50);
    ellipse(320, 200, 165, 50);
   for (var i = 0; i < rainDrop.xPositions.length; i++) {
        noStroke();
        fill(0, 0, 255);
        ellipse(rainDrop.xPositions[i], rainDrop.yPositions[i], rainDrop.width[i], rainDrop.height[i]);
        rainDrop.yPositions[i] += rainDrop.speeds[i];
        rainDrop.xPositions[i] += 0.5;
        if (rainDrop.yPositions[i] >= 405) {
            rainDrop.yPositions[i] = rainDrop.startyPositions[i];
        }
        if (rainDrop.xPositions[i] >= 425) {
            rainDrop.xPositions[i] = rainDrop.startxPositions[i];
        }
    } // Rain
};
var drawSummer = function() {
    scene = 3;
    var widt = 175;
    background(lerpColor(interA, interB, 0.5));
    noStroke();
    fill(255,255,255);
    ellipse(220, 165, widt, 65); // Vanilla Scoop
    fill(90, 60, 10);
    ellipse(220, 195, widt, 65); // Chocolate Scoop
    fill(255, 127, 255);
    ellipse(220, 235, widt, 65); // Straberry Scoop
    fill(235, 185, 60);
    ellipse(300, 50, 50, 50);
    stroke(235, 185, 60);
    line(300, 50, 225, 85);
    line(300, 50, 265, 110);
    pushMatrix();
    rotate(180);
    fill(255);
    triangle(-140, -260, -300, -260, -220, -400);
    popMatrix();
};
var drawLeaves = function(x, y, c) {
    stroke(0, 0, 0);
    strokeWeight(0.5);
    line(x - 15, y + 35, x - 15, y - 5);
    noStroke();
    fill(c);
    triangle(x, y, x - 30, y, x - 15, y - 35);
    triangle(x, y, x - 30, y, x - 40, y - 20);
    triangle(x, y, x - 30, y, x + 25, y - 20);
    rect(x - 30, y, 30, 15);
};
var drawFall = function() {
    scene = 4;
    var leafCount = [];
    background(lerpColor(interA, interB, 0.5));
    drawLeaves(160, 120, color(97, 65, 11));
    drawLeaves(300, 121, color(194, 147, 27));
    drawLeaves(100, 196, color(255, 127, 0));
    drawLeaves(350, 196, color(255, 0, 0));
};
var draw = function() {
    fill(255, 255, 255);
    rect(0, 0, 50, 50);
    fill(0, 0, 0);
    text(timer, 10, 30);
    if (scene === 1) {
        if(timer <= seasonTime) {
            drawWinter();
        }
        else {
            timer = 0;
            scene = 2;
        }
        season = "Winter";
    } // Winter
    if (scene === 2) {
        if(timer <= seasonTime) {
            drawSpring();
        }
        else {
            scene = 3;
            timer = 0;
        }
        season = "Spring";
    } // Spring
    if (scene === 3) {
        if(timer <= seasonTime) {
            drawSummer();
        }
        else {
            scene = 4;
            timer = 0;
        }
        season = "Summer";
    } // Summer
    if (scene === 4) {
        if(timer <= seasonTime) {
            drawFall();
        }
        else {
            scene = 1;
            timer = 0;
        }
        season = "Fall";
    } // Fall
    timer+=1/60; // 1/60 for one second
    text(round(timer), 10,30); // Rounded to the nearest whole to show each second, positioned in the top-left corner
    text(season, 340, 27); // Season
};

// this is for your game/web toy
var stageLayout = [
  [1, 1, 1, 1, 1, 1, 1, 1, 1, 1],
  [1, 0, 0, 1, 0, 0, 0, 0, 0, 1],
  [1, 0, 0, 1, 0, 0, 0, 0, 0, 1],
  [1, 0, 0, 1, 0, 0, 0, 0, 0, 1],
  [1, 0, 0, 0, 0, 0, 1, 0, 0, 1],
  [1, 0, 0, 0, 0, 0, 1, 0, 0, 1],
  [1, 1, 1, 1, 1, 1, 1, 1, 1, 1],
];
var fishImage;
var finish;

var bubbleImage;
var bubble;



var seaweedImage;
var seaweedGroup;

var fish;

var seaImage

function preload() {
  fishImage = loadImage('assets/fish.png');
  seaweedImage = loadImage('assets/seaweed.png');
  seaImage = loadImage('assets/sea.png');
  bubbleImage = loadImage('assets/bubble.png');

}

function setup() {
    createCanvas(1425, 1000);

    fish = new Sprite(300, 300);
    fish.scale = 0.2;
    fish.img = 'assets/fish.png';
    fish.w = 50;
    fish.h = 50;

    bubble = new Sprite(300, 300);
    bubble.img = 'assets/bubble.png';
    bubble.w = 75;
    bubble.h = 75;
    bubble.scale = 0.5;
    // if (bubble.collides(finish)) {
    //      bubble.visible = false;
    //      finish.visible = false;
    //      fish.visible = false;
    //      seaweed.visible = false;
    // }

    finish = new Sprite(1115, 750, 100, 100, 'static');
    finish.img = 'assets/finish.png';
    finish.layer = 1;
    finish.scale = 0.5;

    seaweedGroup = createGroup();
    for (var y = 0; y < stageLayout.length; y++) {
        for (var x = 0; x < stageLayout[y].length; x++) {
            if(stageLayout[y][x] == 1) {
                
            var seaweed = new Sprite(x * 140 + 70, y * 140 + 70, 'static');
            seaweed.addImage(seaweedImage);
            seaweedGroup.add(seaweed);
            seaweed.scale = 0.5;

            }
        }
    }
}

function draw() {
    fish.moveTowards(mouse);
    background(seaImage);
}
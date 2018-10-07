
# Scratch Dot Matrix

[Project on Scratch](https://scratch.mit.edu/projects/250079262/)

This repository contains the Python script used to generate strings of coordinates, which are interpreted by my Scratch program to draw letters. I used the [Vertical Fonts](https://github.com/BaronWilliams/Vertical-Fonts) library to get the coordinates for the fonts. The file for the font I used is in this repository. They are lists of columns in decimal form, which turn into pixels when converted to binary.

**Example:** The first column for the letter 'A' is `14336`. When converted to binary, it reads `0011 1000 0000 0000`. Turn this sideways and it shows:

(some zeroes omitted)

&#9675;

&#9675;

&#9675;

&#9675;

&#9675;

&#9675;

&#9679;

&#9679;

&#9679;

&#9675;

&#9675;

This makes sense because there's some space below for certain letters and the lower part of the 'A' is touching the side of the frame.

**Implementation:** I used some bit shifting operations to process these numbers and create strings in a format that I can process with Scratch. This format is `x1,y1;x2,y2;` etc.

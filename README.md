# CarND-Controls-PID
My implementation of PID Controller for Self-Driving Car Engineer Nanodegree Program is inclueded here.  This file is based on that provided by Udacity and extended with the reflection part at the end.

---

## Dependencies

* cmake >= 3.5
 * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools]((https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* [uWebSockets](https://github.com/uWebSockets/uWebSockets) == 0.13, but the master branch will probably work just fine
  * Follow the instructions in the [uWebSockets README](https://github.com/uWebSockets/uWebSockets/blob/master/README.md) to get setup for your platform. You can download the zip of the appropriate version from the [releases page](https://github.com/uWebSockets/uWebSockets/releases). Here's a link to the [v0.13 zip](https://github.com/uWebSockets/uWebSockets/archive/v0.13.0.zip).
  * If you run OSX and have homebrew installed you can just run the ./install-mac.sh script to install this
* Simulator. You can download these from the [project intro page](https://github.com/udacity/CarND-PID-Control-Project/releases) in the classroom.

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./pid`

## Reflection

The P component determines the effect of cte, the I component corrects the systematic bias, and the D component dampens the oscillation.  The smaller P, the less effect of cte; I is not important because the systematic bias is not significant; larger D reduces the oscillation.  The final hyperparameters are figured out through manual tuning: increase P until it starts oscillating a bit, then make D large to combat the oscillation and become stable, resulting in D > P > I.  After understanding the effect of the P, I, D, components, choosing P, I, D, coefficients by hand is a simple way for this project.  Tuning them manually can get a better intuition on the PID algorithm.

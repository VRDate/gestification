Flying Leap 3D
==============

Live Demo #1: http://jaanga.github.io/gestification/projects/flying-leap-3d/r1/flying-leap-3d.html  
- The landscape along with the placement of the trees is controlled by an algebraic function. Note the refresh of colors with each reload.

Live Demo #2: http://jaanga.github.io/gestification/projects/flying-leap-3d/castle/load-castle.html
- A test of loading an OBJ file into Thrree.js. Note the castle - which is the static OBJ file - also refreshes its colors with each reload. 

Live Demo #3: http://jaanga.github.io/gestification/projects/flying-leap-3d/barfolina-pavillion/r1/barfolina-pavillion.html
- Worth a visit
- The entire pavilion - except for the sculpture - is created by procedures. This is the modern way of designing - which we are calling 'archieCode'.

Built for Nicolás Berríos of Iquique, Chile

The proposal is to build an app for the Leap Motion device that allows you to 'fly' over [Iquique harbor](http://goo.gl/Tq4F59). 
But how to fly using just one hand? These demos are testing grounds for learning how to fly 
- and, more importantly, for us to learn good ways of tehing people how to fly. 

Aning other things we are working on an updated First Person camera controller for Three.js.

Leap.js + Three.js: a Leaped first person camera controller

###Demos: Status and Issues
See the readme in each demo's folder for more details and status of issues

###Leap Actions
Hand open over Leap device:
* Supports the following FirstPersonControls parameters: moveLeft, moveRight, moveUp, moveUp, moveForward, moveBackword 
* Supports pitch and yaw via Three.js lat and lon parameters
* Making fist restricts camera movement to lat and lon only
* Supports Freeze all interaction toggle via a swipe gesture.

###New First Person Control Mouse Actions
* The fork supports all the standard Three.js First Person Control functions
* The fork supports the following additions:
* Turning the scroll wheel controls the speed of movementSpeed and lookSpeed << This feature is wonderful. Try it!
* When a mouse button is not being pressed the scroll wheel updates lookSpeed.
* When a mouse button is being pressed, the scroll wheel updates movementSpeed
* Clicking the scroll wheel toggles Freeze on and off.

###New First Person Control  Keyboard Commands
	The following new keyboard commands are added to the fork:
	
	````
	switch ( event.keyCode ) {
	case 32: /*spacebar*/ this.freeze = !this.freeze; break;
	
	case 33: /*page up*/ this.moveUp = true; break;
	case 34: /*page down*/ this.moveDown = true; break;
	
	case 36: /*home*/ this.lookSpeed = 0; this.lat += 1.0; break;
	case 35: /*end*/ this.lookSpeed = 0; this.lat -= 1.0; break;	

	case 188: /*< or ,*/ this.lookSpeed = 0; this.lon -= 0.5; break;
	case 190: /*> or .*/ this.lookSpeed = 0; this.lon += 0.5; break;	
	
	
	````

###Copyright and License
Copyright &copy; 2013 Jaanga authors

MIT License

###Change Log

2013-09-02 ~ Theo
* Updated this readme.

2013-08-29 ~ Theo
* barofolina pavillion demo added

2013-08-26 ~ Theo
* Added castle demo

2013-08-24 ~ Theo
* Folders and files added
* Updates a forked Three.js FirstPersonControls
* Adds freeze and speed controls via mousewheel
* Adds more keyboard commands
* hand2Go2 HTML/JS file is a test bed.
* Adds Leap interaction with FPController
* Provides for XYZ movement plus pitch, yaw and freeze




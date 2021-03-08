# SCARA Electromagnetic Arm 

## Plan 
  
  ### Goal
  To build a robotic arm that will be able to electromagnetically move and sort metal pieces to precise locations.
      
  ### Specifics
 Will be a SCARA type robot arm and will utilise inverse kinematics in order to move in the x and y plane. Inverse kinematics refers to positioning and moving the arm based on calculated joint angles. The arm will be fixed in the y-direction and an electromagnet will be used to lift and sort pieces. The desired positioning values will be entered into the robot via a computer interface. 
      
      
 ### Code 
  
 #### Pseudocode 1
 
 ```C++

Void setup()

magnet.pin = n

Move.arm ()
	Servoangle.read (ፀx0, ፀy0)
	Position.read(x1,y1) 
	Angle.calc (ፀx1, ፀy1) 
	Angle.calc (ፀx1-ፀx0, ፀy1-ፀy0) = val 1
	Servo.move (val 1) 
	# redo with increasing numbers, save data of initial angle. Ex new ፀx0= old ፀx1


Magnet.on()
	magnet.pin (HIGH,)

Magnet.off()
	magnet.pin (LOW) 

Void loop() 

Move.arm  (x0,y0 to x1,y1)

Magnet.on 

move.arm (x1, y1 to x2, y2)

Magnet.off 


 ```
 #### Pseudocode 2
 
 ```C++

Void setup()

Servo_x.attach(n).

Servo_Y.attach(n)

Servo_3.attach(n) 


Move.arm ()
	Servo_x.angleread(ፀx0) 
	Servo_y.angleread(ፀy0)
	
	Position.read(x1,y1) 
	    potentiometerx.read= x1 
	    potentiometery.read= y1
	    LCD.write ('x1', 'y1') 
	    
	
	Angle.calc (ፀx1, ፀy1)
	# need a grid of some kind to locate positions. Then need a formula to calculate servo angles based on grid positions.  
	
	Angle.calc (ፀx1-ፀx0, ፀy1-ፀy0) = val 1x, val 1y
		val ፀx1-ፀx0 = val 1x
		val ፀy1-ፀy0 = val 1y
	Servo_x.move (val 1x)
	Servo_y.move (val 1y) 
	# redo with increasing numbers, save data of initial angle. Ex new ፀx0= old ፀx1


Magnet.on()
	Servo_3.write(90) 
	
Magnet.off()
	Servo_3.write(0)  

Void loop() 

Move.arm  #(x0,y0 to x1,y1)

Magnet.on 

move.arm #(x1, y1 to x2, y2)

Magnet.off 


 ```
          

 #### Formula 
 
 Formula for conversion of servo angle into graphing placement
  
  
### OnShape "Pseudocode"

[OnShape Model](https://cvilleschools.onshape.com/documents/f6d9cc65e05e26eae1d5c45a/w/8edde5e97c4994cb9e9d50f3/e/d1962944a79fd9c4dc7f6611) <br/>
[OnShape VERY Rough Prototype](https://cvilleschools.onshape.com/documents/0627f950d927ef87b77603c8/w/3575573e58b9fedf54dfd438/e/1fe431af62f1e4169310c066)

### Web Links
 - A place to put any potentially useful website links: 
      - [Aphex Twin Themed SCARA Robot Instructables](https://www.instructables.com/SCARA-Robot-Learning-About-Foward-and-Inverse-Kine/) 
      - [Ball Drop Joystick SCARA Robot](https://create.arduino.cc/projecthub/311549/scara-arm-controlled-by-joystick-486870) 
      - [Kinematics Formula Walkthrough Video](https://robotacademy.net.au/lesson/inverse-kinematics-for-a-2-joint-robot-arm-using-geometry/)


### Week 1
#### CAD (Alden):
<IMG SRC="Media/ServoBracket.PNG" width="250" height="202"> <br/>
[Servo Bracket](https://cvilleschools.onshape.com/documents/575ef6b5b2807b09a30dcc8b/w/4e40a84d3513593e765af328/e/250a50aca4f88581c475a6ac)
<br/>
This week I designed the bracket that will hold the servo and prevent the leverage of the arm from breaking the servo. It was fairly simple to do; I just had to look up where the use/project feature was. My goal for next week is to design the first arm.

#### Code (Georgia): 
 This week I created a second version of the pseudocode with further specifications (Pseudocode 2). While working on this, I realized that in order to progress further with creating the code I would have to find a working formula for the kinematics of the arm (converting x,y grid coordinates into servo angles) so that's my goal for week two. 
 
 ### Week 2 

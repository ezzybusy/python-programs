from Brickpi import *

BrickPi.SensorType[PORT_4] = TYPE_SENSOR_EV3_US_M0  

BrickPiSetup()  # setup the serial port for communication

sensor_port_number = PORT_1	# Define the port number here From whichever port has the sensor plugged in

BrickPi.SensorType[port_number] = TYPE_SENSOR_ULTRASONIC_CONT   #Set the type of sensor at PORT_1

BrickPiSetupSensors()  

as_close_as_we_want_to_get = 30 # max distance in cm we want to be

def robot_fwd():
	BrickPi.MotorSpeed[motor1] = speed  
	BrickPi.MotorSpeed[motor2] = speed  
#Move Left

def turn_robot_left():
	BrickPi.MotorSpeed[motor1] = speed  
	BrickPi.MotorSpeed[motor2] = -speed 
#Move Right

def turn_robot_right():
	BrickPi.MotorSpeed[motor1] = -speed  
	BrickPi.MotorSpeed[motor2] = speed
#Move backward

def robot_back():
	BrickPi.MotorSpeed[motor1] = -speed  
	BrickPi.MotorSpeed[motor2] = -speed
#Stop

def stop_robot():
	BrickPi.MotorSpeed[motor1] = 0  
	BrickPi.MotorSpeed[motor2] = 0

speed = 150

def get_distance: # is a function that returns our distance in cm 
		result = BrickPiUpdateValues() # Updates information from all sensors and motors
		if not result: 
			return BrickPi.Sensor[sensor_port_number]

def are_we_too_close(): # checks if robot is too close.  If it is too close stops robot and returns True. Return False  
	
	if get_distance() < as_close_as_we_want_to_get:
		stop_robot() 		
		return True	
	else:
		return False

def fourty_five_degrees(direction):
	if direction = 'right':
		turn_robot_right()
		time.sleep(some amount of time it takes to turn right)
		stop_robot()
	if direction = 'left':
		turn_robot_left()
		time.sleep(some amount of time it takes to turn right)
		stop()
	# put code here to turn 45 degrees right
	if direction = 'left':	 	
	


def check_right():
	while are_we_too_close(): 
		fourty_five_degrees("right")							

def simpleavoidance(): # function for avoiding with right angles
	while True:  # infinite loop for program
		fwd()	# turn on motors to move forward
		time.sleep(.5) # pause program for half a second.  Let robot move
		if are_we_too_close(): #if too close check_right() 
			check_right()
		

simpleavoidance()

# MobileRobot-Openloopcontrol
```Developed by : Aliya Sheema
Register nuumber : 23005529
Department : AIDS
```

## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:
Use from robomaster import robot
Step2:
Choose the x,y,z - axis movement distance(meters).
Step3:
Give ep_chassis.move to move straight.
Step4:
Give time.sleep() for a break.
Step5:
Give ep_chassis.drive_speed to have a circular movement.

## Program
```Developed by : Aliya Sheema
Register Number : 23005529 
```
python
from robomaster import robot
import time
from robomaster import camera

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.55, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=80, xy_speed=0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=153,b=225,effect="on")

    ep_chassis.move(x=0, y=-1.4, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=60, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=192,g=192,b=192,effect="on")

    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=225,g=225,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=45, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=225,g=225,b=0,effect="on")

    ep_chassis.move(x=1.45, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=225,b=225,effect="on")

    ep_chassis.move(x=0, y=0, z=3, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=153,b=225,effect="on")

    ep_chassis.move(x=0, y=-2.1, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=170, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=225,b=0,effect="on")

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=51,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")
    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here
![a54b92fd-010f-45b2-ad7f-258c1fb1de98](https://github.com/23005529/mobilerobot-openloopcontrol/assets/148604723/9c6cee80-3d5d-493e-b873-99949e682a13)

![02155bfb-a7ee-4944-8890-408c16f12cd8](https://github.com/23005529/mobilerobot-openloopcontrol/assets/148604723/90b0b2cf-d837-47e6-9bfc-fa77f08b40d4)

![40683948-a4e2-489f-a728-2936d9cbd80f](https://github.com/23005529/mobilerobot-openloopcontrol/assets/148604723/4d609af7-4c4d-49fd-a1d9-b2847fab9a18)

![97583cb9-3c09-483b-8986-d6bd745da38a](https://github.com/23005529/mobilerobot-openloopcontrol/assets/148604723/0e228cd5-fd43-411e-984c-9c80d796915e)


## MobileRobot Movement Video:

https://youtube.com/shorts/fH1QrrpZba4?feature=share

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```

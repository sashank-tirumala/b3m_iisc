
# B3M

1. [Main Page](https://kondo-robot.com/product/03092)
2. [Software](https://kondo-robot.com/faq/b3m-series-software-manualenglish) [[.pdf]](https://kondo-robot.com/w/wp-content/uploads/B3M_SoftwareManual1.2.0.2_en.pdf)



### To Control the Servo (Linux)


**Start Up**

```
sudo modprobe ftdi_sio
sudo su
echo "165C 0009" > /sys/bus/usb-serial/drivers/ftdi_sio/new_id
exit
```

**To Configure Build**
```
rm -r build/
mkdir build & cd build
cmake ../
```

**Then, To Build It**
```
cmake --build .
```
or
```
make
```

**Run The Programming**

```
cd build/src
./position /dev/ttyUSB0
./velocity /dev/ttyUSB0
```

****

Reference

1. **[sugar_sweet](https://github.com/sugarsweetrobotics/libb3m)**
2. **[ros-kondo-b3m-driver-beta](https://github.com/AriYu/ros-kondo-b3m-driver-beta)**
3. [mbed](https://os.mbed.com/users/sgrsn/code/B3MServo/)
4. [arm_linux](https://github.com/servo/servo/wiki/Building-on-ARM-desktop-Linux)
5. [KRS_adapter_linux](https://github.com/longjie/kondo_motor)

### RS485 USB / serial conversion adapter

1. [Main Page](https://kondo-robot.com/product/02133)

**Technical guide**

0. **[To use serial USB adapter with Linux](https://kondo-robot.com/faq/usb-adapter-for-linux)**
1. **[How to use our USB adapter with Linux (2019 version)](https://kondo-robot.com/faq/usb_adapter_for_linux_2019)**
2. [Procedure for installing KO_Driver_2013 on Windows 8 (provisional version)](https://kondo-robot.com/faq/ko_driver_2013-install-windows8)
3. [RS485 USB / serial conversion adapter product manual](https://kondo-robot.com/faq/rs485usbserial_adp_manual) [[.pdf]]()

**Data Sheet**

* [FT232RL: USB to serial UART interface](https://www.ftdichip.com/Support/Documents/DataSheets/ICs/DS_FT232R.pdf)

* [ADM3078E: Data transceiversfor full- and half-duplex communication on multipoint bus transmission lines. ](https://www.analog.com/media/en/technical-documentation/data-sheets/ADM3070E_3071E_3072E_3073E_3074E_3075E_3076E_3077E_3078E.pdf)



### To Control the Servo (Windows)

Do this to check if the sevvo, adapter and everything is fine and also to change the **servo ID**

**From their Software**

**Reference**
1. [Let's move B3M servomotor (Preparation (1))](https://kondo-robot.com/faq/b3m_settings1)
2. [Let's run B3M servomotor (Preparation (2))](https://kondo-robot.com/faq/b3m_settings2)

**Steps**

1. [Installation of driver](https://kondo-robot.com/w/wp-content/uploads/KO-Driver2015.zip)
2. [Download the B3M software](https://kondo-robot.com/w/wp-content/uploads/B3M_Manager_V1132.zip)
3. bps = 1500000 and ID = 0 and check the COM port
4. Then  click Read all
5. Go to **Options and Status**, Then select normal (run mode) and position (control) and then write
6. Check the servo by moving the scroll bar in **servo paprameters**



**From Microsoft Visual Studio**
1. [Let's run B3M servomotor (C # Preparation)](https://kondo-robot.com/faq/b3mwinprogram1)
  * [a](https://www.dotnetperls.com/form)
  * [b](https://www.freetutes.com/learn-vb6-advanced/lesson6/p2.html)
  * [c](https://www.winehq.org/)
2. [Let's move B3M servomotor (C # Position Control)](https://kondo-robot.com/faq/b3mwinprogram2)

### Power Supply

Power supply
B3M servo also requires as its power supply at **9-12 V battery** or AC power supply, etc

SC-1170-A: Ampacity of **Max 5.4A** required for each servo unit

# Impedance Control

* [MIT Guy](http://www.matthematic.com/projects/mit/2.740/jumper.html)
* [ppt](http://www.adrlab.org/archive/forcecontrol11.pdf)
* [Interaction Control for Contact Robotics](https://www.youtube.com/watch?v=GjKy3EFs3g8)

#Current authors:
sashank-tirumala
varunvp


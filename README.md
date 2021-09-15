# Seeed_Python_SI115X

Grove - Sunlight Sensor (si115x) is a multi-channel digital light sensor, which has the ability to detect UV-light, visible light and infrared light.

This device is based on SI1151, a new sensor from SiLabs. The Si1151 is a low-power, ambient light sensor with I2C digital interface and programmable-event interrupt output. This device offers excellent performance under a wide dynamic range and a variety of light sources including direct sunlight.

# Dependencies

This driver depends on:
- [***grove.py***](https://github.com/Seeed-Studio/grove.py)

This is easy to install with the following command.

```python
pip3 install Seeed-grove.py
```
 

## Usage Notes

First, Check the corresponding i2c number of the board:

```

pi@raspberrypi:~ $ sudo i2cdetect -y 1

```

Check if the i2c device works properly， 0x53 is the SI1151 i2c address.
```

pi@raspberrypi:~/Seeed_Python_SI114X $ i2cdetect -y -r 1
     0  1  2  3  4  5  6  7  8  9  a  b  c  d  e  f
00:          -- 08 -- -- -- -- -- -- -- -- -- -- -- 
10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
40: -- -- -- -- -- -- -- -- 53 -- -- -- -- -- -- -- 
50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
70: -- -- -- -- -- -- -- --   

```

## Usage

Step.1 

```
git clone https://github.com/0hotpotman0/python_SI1151_test.git
```
setp.2

```
python3 seeed_si115x.py
```

Then it will display the light value.
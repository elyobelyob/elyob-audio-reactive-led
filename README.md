# audio-reactive-led-strip
Real-time LED strip music visualization using the ESP8266 and Python

![block diagram](images/block-diagram.png)

![overview](images/description-cropped.gif)

# Demo (click gif for video)

[![visualizer demo](images/scroll-effect-demo.gif)](https://www.youtube.com/watch?v=HNtM7jH5GXgD)

# Overview
The repository includes everything needed to build an LED strip music visualizer (excluding hardware):

- Python real-time visualization code, which includes code for:
  - Recording audio with a microphone ([microphone.py](python/microphone.py))
  - Digital signal processing ([dsp.py](python/dsp.py))
  - Constructing 1D visualizations ([visualization.py](python/visualization.py))
  - Sending pixel information to the ESP8266 over WiFi ([led.py](python/led.py))
- Arduino firmware for the ESP8266 ([ws2812_controller.ino](arduino/ws2812_controller/ws2812_controller.ino))

# What do I need to make one?
The following hardware is needed to build an LED strip music visualizer:
- Computer with Python 2.7 or 3.5 ([Anaconda](https://www.continuum.io/downloads) is recommended on Windows)
- Any ESP8266 module with RX1 pin exposed. These modules are known to be compatible (but many others work too):
  - NodeMCU v3
  - Adafruit HUZZAH
  - Adafruit Feather HUZZAH
- Any ws2812b LED strip (such as Adafruit Neopixels)

# Installation
## Python Dependencies
Visualization code is compatible with Python 2.7 or 3.5. A few Python dependencies must also be installed:
- Numpy
- Scipy (for digital signal processing)
- PyQtGraph (for GUI visualization)
- PyAudio (for recording audio with microphone)

On Windows machines, the use of [Anaconda](https://www.continuum.io/downloads) is **highly recommended**. Anaconda simplifies the installation of Python dependencies, which is sometimes difficult on Windows.

### Installing dependencies with Anaconda
Create a [conda virtual environment](http://conda.pydata.org/docs/using/envs.html) (this step is optional but recommended)
```
conda create --name visualization-env python=3.5
activate visualization-env
```
Install dependencies using pip and the conda package manager
```
conda install numpy scipy pyqtgraph
pip install pyaudio
```

### Installing dependencies without Anaconda
The pip package manager can also be used to install the python dependencies.
```
pip install numpy
pip install scipy
pip install pyqtgraph
pip install pyaudio
```
If `pip` is not found try using `python -m pip install` instead.

## Arduino dependencies
The [ws2812b i2s library](https://github.com/JoDaNl/esp8266_ws2812_i2s) must be downloaded and installed in the Arduino libraries folder.

# Setup / Getting Started
Information coming soon. README is currently under active development.

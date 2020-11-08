# Hardware Lecture
An Overview of Hardware Development by TingliangZhang

Using [reveal.js](https://github.com/hakimel/reveal.js)

<p align="center">
  <a href="https://revealjs.com">
  <img src="https://hakim-static.s3.amazonaws.com/reveal-js/logo/v1/reveal-black-text.svg" alt="reveal.js" width="450">
  </a>
  <br><br>
  <a href="https://github.com/hakimel/reveal.js/actions"><img src="https://github.com/hakimel/reveal.js/workflows/tests/badge.svg"></a>
  <a href="https://slides.com/"><img src="https://s3.amazonaws.com/static.slid.es/images/slides-github-banner-320x40.png?1" alt="Slides" width="160" height="20"></a>
</p>

The full reveal.js documentation is available at [revealjs.com](https://revealjs.com/).



## Setup

1. Install [Node.js](https://nodejs.org/) (10.0.0 or later)

2. Clone the reveal.js repository

   ```shell
   $ git clone https://github.com/hakimel/reveal.js.git
   ```

3. Move to the reveal.js folder and install dependencies

   ```shell
   $ cd reveal.js && npm install
   ```

4. Serve the presentation and monitor source files for changes

   ```shell
   $ npm start
   ```

5. Open [http://localhost:8000](http://localhost:8000/) to view your presentation

## Outline

- What is Hardware Development, why it is so important
- How to develop any prototype
  - A brief IDEA about any non-pure-software stuff
  - Split the function into a few small function
  - Decide use which model to achieve each function
  - Buy lots of stuff from Taobao, JLC
  - Build the prototype
  - Test and Debug
  - Iteration
- A list of what we need to learn(incomplete)
- A brief introduction to: 
  1. Dev boards such as Arduino and STM32; 
  2. Communication protocol such as UART, SPI, I2C, and RS232; 
  3. Programming languages including C, Python, Java, C++, Verilog; 
  4. Debug tools such as oscilloscope, waveform generator, multimeter; 
  5. Peripherals(外设) like brushless motor, servo motor, stepper motor, microphone, IMU, display; 
  6. Circuits simulate and PCB design tools: Multisim, KiCAD, Altium Designer; 
  7. Soldering and SMT: QFNP, QFP, BGA, DIP......JLC
  8. Algorithms: FFT, PID
  9. HCI design
  10. Shape(shell) design
- A thorough introduction of Microcontrollers
- Discussion about the future of hardware engineering.



## Keys

Hardware of embedded system includes embedded processor, memory, peripherals and interfaces.



## Speech Notes

Microcontrollers are single chip computers that include a minimum of a microprocessor, memory, and input-output module. A microcontroller can be anything from a tiny single chip embedded controller to a large computer system having keyboard, monitor, hard disk, printer, and so on.



A microprocessor is different from a microcontroller in many different ways. The main difference is that a microprocessor requires several additional external support chips such as memory and input-output circuits before it can be used as a digital controller. A microcontroller on the other hand includes all these support chips on the same chip and that is why it is called a single chip computer. As a result, multiple chip microprocessor-based computer systems consume considerably more power than microcontroller-based systems. The costs of the single chip microcontroller systems are also much lower than the costs of the multiple chip-based microprocessor systems.

Microprocessors and microcontrollers operate by executing user programs. These programs are stored in the program memory of the device and consist of instructions that can be understood and obeyed by the device. The device fetches these instructions from its program memory one by one and then implements the required operations. Under the control of the user program data is received from external input devices (inputs), manipulated as requested, and then sent to external devices (outputs).



we shall see how a microcontroller can be used in a simple control system application. The Figure shows a liquid control system where the aim is to control the level of the liquid in the reservoir at a specified point. Water is pumped from the reservoir to the tank using a pump and pipes. The level of the liquid is controlled manually without using a microcontroller. Here, the person in charge observes the liquid level inside the tank and turns the pump off when the liquid level reaches the required prespecified level.



The system shown in [Fig. 1.1](https://www.sciencedirect.com/science/article/pii/B978008102969500001X#f0010) is manual and requires constant attention of a person. A simple microcontroller version of this system is shown in [Fig. 1.2](https://www.sciencedirect.com/science/article/pii/B978008102969500001X#f0015). Here, the liquid level is read by the microcontroller via a liquid level sensor device. The program running inside the microcontroller compares the actual liquid level with the desired level and then actuates the pump automatically in order to keep the liquid at the desired level. If the liquid inside the tank is low, the microcontroller operates the pump to draw more liquid from the reservoir.



The system shown in [Fig. 1.2](https://www.sciencedirect.com/science/article/pii/B978008102969500001X#f0015) is a very simplified liquid level control system with no user interaction. In a more sophisticated system we may include a keypad to set the desired liquid level and an LCD (liquid crystal display) to see the desired and/or the actual liquid levels in the tank. [Fig. 1.3](https://www.sciencedirect.com/science/article/pii/B978008102969500001X#f0020) shows the block diagram of our upgraded system. Notice that here we are using two inputs and two outputs from our microcontroller.



We can make our system even more sophisticated as shown in [Fig. 1.4](https://www.sciencedirect.com/science/article/pii/B978008102969500001X#f0025) by adding an audible alarm to indicate when the water level is above the desired point. Also, a PC can be interfaced to the microcontroller so that, for example, the actual liquid levels can be sent to the PC at regular intervals and graphs of liquid level variations can be plotted on the PC between the required intervals.



In [Fig. 1.5](https://www.sciencedirect.com/science/article/pii/B978008102969500001X#f0030), wireless interface is added to our system in the form of Bluetooth or Wi-Fi. With the help of the wireless interface we can, for example, send and save the liquid level readings on a Cloud. Additionally, we can monitor and/or control the liquid level remotely through the Cloud using, for example, a mobile phone. Because the microcontrollers are programmable and in general offer many input and output ports, we can make our system as simple or as complex as we like.

## Reference

[Microcontroller-Based Project Development Cycle](https://www.sciencedirect.com/science/article/pii/B9780081029695000021)

Dogan Ibrahim, in [ARM-Based microcontroller projects using MBED](https://www.sciencedirect.com/book/9780081029695), 2019



[ARM-Based microcontroller projects using MBED](https://www.sciencedirect.com/science/book/9780081029695)  2019, Pages 1-7

[Chapter 1 - Introduction](https://www.sciencedirect.com/science/article/pii/B978008102969500001X)



[oxit Hardware Development](https://oxit.com/hardware-development/)
<h1 style="font-family: courier;" align="center">satshakit multicore</h1>
<p align="center">
<img src="media/satshakit_multicore/satshakit_multicore_5.jpg" width="70%">
<div align="center"><i>An improved & fabbable 100% Arduino IDE/libraries compatible board.</i></div>
</p>  

What is satshakit?
--

satshakit is a **100% Arduino IDE  and libraries compatible**, fabbable and open source board, and also an improved version of [Fabkit](http://fabacademy.org/archives/2015/doc/projects/fabkit-0.4.html). 

Main **improvements and features** over Fabkit are:

- **16Mhz** instead of 8Mhz
- **crystal** instead of resonator
- **costs less** (7-9 euro vs 13 euro)
- 100% compatible with **default Arduino IDE** (satshakit is recognized as Arduino UNO)
- ADC6/7 connected instead of ADC6/7 not connected (satshakit laser and cnc)
- larger space to easy soldering (satshakit laser and cnc)

satshakit boards
--

There are different kinds of **satshakit boards** depending on the **fabrication technique** you will use to make them, or on the **size** of the board. 

<img src="media/readme/satshakit_versions.jpg" width="70%">

Here is a comparison table about different satshakit boards:

|name|mcu|pins|size(mm)|
| :---: | :---:|:---:|:---:|
|`satshakit laser`|ATmega328P|Arduino + ADC6/7|48 x 42|
|`satshakit cnc`|ATmega328P| Arduino + ADC6/7  |54 x 45|
|`satshakit multicore`|2 x ATmega328P| 2 x Arduino + ADC6/7|50 x 42|
|`satshakit micro`| ATmega328P|Arduino|40 x 24|
|`satshakit flight controller`| ATmega328P|MultiWii|48 x 48|

Here you can find all of the satshakit boards: **[satshakit organization](https://github.com/satshakit)**.

satshakit multicore
--

**satshakit multicore** boards born as a further experiment on **MCU multithreading and networking**. satshakit multicore boards have only the following modifications in confront of the standard satshakit: 4 extra pin headers (1 GND,1 VCC,1 A4, 1 A5). These pin headers serve also a structural pillars to build a modular satshakit tower. So modular satshakit share the same power source, and can direct communicate with **I2C**. 

Here is the **satshakit multicore board**:

<img src="media/satshakit_multicore/satshakit_multicore_board.jpeg" width="60%">

<img src="media/satshakit_multicore/satshakit_multicore.png" width="60%">

**downloads (right click, download as)**

- [satshakit multicore svg](https://raw.githubusercontent.com/satshakit/satshakit-multicore/master/media/satshakit_multicore/satshakit_multicore.svg)
- [satshakit multicore schematic](https://raw.githubusercontent.com/satshakit/satshakit-multicore/master/eagle_projects/satshakit_multicore/satshakit_multicore.sch)
- [satshakit multicore board](https://raw.githubusercontent.com/satshakit/satshakit-multicore/master/eagle_projects/satshakit_multicore/satshakit_multicore.brd)
- [satshakit multicore BOM Open Document](https://github.com/satshakit/satshakit-multicore/raw/master/docs/satshakit_BOM.ods)
- [satshakit multicore BOM Excel](https://github.com/satshakit/satshakit-multicore/raw/master/docs/satshakit_BOM.xlsx)

**media**

<img src="media/satshakit_multicore/satshakit_multicore_1.jpg" width="60%">

<img src="media/satshakit_multicore/satshakit_multicore_4.jpg" width="60%">

5-core satshakit system:

<img src="media/satshakit_multicore/satshakit_multicore_2.jpg" width="60%">

<img src="media/satshakit_multicore/satshakit_multicore_3.jpg" width="60%">

satshakit multicore assembly & test:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=nVHYBydPKpk
" target="_blank"><img src="http://img.youtube.com/vi/nVHYBydPKpk/0.jpg" 
alt="http://img.youtube.com/vi/nVHYBydPKpk/0.jpg" width="240" height="180" border="10" /></a>

satshakit multicore blink:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=bxnmX-B9Czo
" target="_blank"><img src="http://img.youtube.com/vi/bxnmX-B9Czo/0.jpg" 
alt="http://img.youtube.com/vi/bxnmX-B9Czo/0.jpg" width="240" height="180" border="10" /></a>

quad satshakit bluetooth triangulation:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=uuVuoD9TB4M
" target="_blank"><img src="http://img.youtube.com/vi/uuVuoD9TB4M/0.jpg" 
alt="http://img.youtube.com/vi/uuVuoD9TB4M/0.jpg" width="240" height="180" border="10" /></a>

Getting Started
--
A satshakit board is **totally like an Arduino board**, thus is possible to use the Arduino IDE without any modification. When you finish solder satshakit, you're ready to program it. If you want to use satshakit as an Arduino, you first need to **upload Arduino bootloader**. This will also set the ATmega328P fuses as the same of an Arduino UNO.
 To do this you need to use a **programmer**, for example another Arduino or FabISP. If you plan to program a satshakit with an Arduino, be sure to upload the **Arduino as ISP skecth** before connecting the satshakit to it.

Here are the connection schemas to program **satshakit laser**, **satshakit cnc** or a **satshakit multicore** with an Arduino as ISP or with a FabISP:

<img src="media/readme/satshakit_laser_arduino_programming.png" width="60%">

<img src="media/readme/satshakit_laser_fabisp_programming.png" width="60%">

Once everything is connected, follow these steps to upload Arduino bootloader:

1. open Arduino IDE 
2. select proper programmer (for example Arduino as ISP or USBtinyISP) 
3. select Arduino UNO as board
4. click on tools->Burn Bootloader

With satshakit multicore, you can use an **FTDI USB cable to upload and use you favourite sketch** without the need to use a programmer anymore.

Here is the connection schema to program a satshakit multicore using the FTDI cable:

<img src="media/readme/satshakit_laser_programming_FTDI.jpg" width="60%">

Remember that if you don't have an FTDI cable you always need a programmer, and to select **File->Upload using a programmer** to upload the code to satshakit.

To use a satshakit like an Arduino, here is the Arduino pinout on satshakit multicore:

<img src="media/readme/satshakit_laser_arduino_pin_mapping.png" width="60%">

What's in the repo
--
- **[docs](https://github.com/satshakit/satshakit-multicore/tree/master/docs)**: BOM files for Farnell
- **[egle projects](https://github.com/satshakit/satshakit-multicore/tree/master/eagle_projects)**: eagle projects of satshakit
- **[media](https://github.com/satshakit/satshakit-multicore/tree/master/media)**: svg of satshakits, connections schemas, images for cnc milling machine and fiber laser cutter, other images

Authors
--

- Daniele Ingrassia and [Engineering Ingegneria Informatica](http://www.eng.it)

Contact
--
- **ingrassiada@gmail.com**
- **[linkedin](http://it.linkedin.com/in/danieleingrassia)**


Thanks
--

[Fablab opendot](http://www.opendotlab.it/)<br />
info@opendotlab.it<br />
Via Tertulliano N70, 20137, Milan, Italy<br />
 +39.02.36519890<br />

License
--
This work is licensed under the terms of Attribution-NonCommercial-ShareAlike 4.0 International ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)).

Disclaimer  
--

<div class="align-justify">
This hardware/software is provided "as is", and you use the hardware/software at your own risk. Under no circumstances shall any author be liable for direct, indirect, special, incidental, or consequential damages resulting from the use, misuse, or inability to use this hardware/software, even if the authors have been advised of the possibility of such damages.</div>

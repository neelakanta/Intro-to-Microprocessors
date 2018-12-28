# Intro-to-Microprocessors
Documentation of material covered in the spring '19 class lectures on this topic

This is a core course that we teach at the Florida Atlantic University (FAU) for engineering undergraduates. Currently, students use both C and Assembly language in developing codes for use on a TI board. We use TI's CCStudio software, available both on the local server and for use on individual laptops. The board is connected through an USB port of the dumb terminal in our computer labs (to access the server version) or the laptop. 

In two of the three sections in Spring '19, we are pivoting towards a different microcontroller, from the PIC16 family. One of these two sections is a distance learning section and is supposed to be taught concurrent to the other live section. We had to evaluate alternatives to facilitate this and yet make sure students will get enough hands-on experience for the lab component. 

This Repository is focused on PIC16 and its C compiler, in an attempt to develop a distance learning friendly environment for teaching this course. PIC16 (our specific version is: PIC16F18855), marketed around 2015, is also a RISC (reduced instruction set computer) architecture that is C-friendly. The [technical reference manual](http://ww1.microchip.com/downloads/en/DeviceDoc/400001802D.pdf) from the microchip website is attached.  They also provide several [examples](https://mplabxpress.microchip.com/mplabcloud/example). There are 133 examples included for this specific microcontroller, as of Nov 2018. MPLab Express Evaluation Boards are listed [here](http://ww1.microchip.com/downloads/en/DeviceDoc/30010119B.pdf). The specific one for our purposes is: MPLAB Xpress PIC16F18877 Evaluation Board (DM164142). The board that we have has the product number of DM164140. DigiKey provides a [datasheet](https://www.digikey.com/product-detail/en/microchip-technology/DM164140/DM164140-ND/6044842?WT.srch=1&gclid=EAIaIQobChMItPHnhKD63gIVA1uGCh3HnwjgEAQYASABEgJeNfD_BwE). 

From a Microchip [site](http://ww1.microchip.com/downloads/en/DeviceDoc/30010119B.pdf): "MPLAB Code Configurator (MCC) is a free software plugin – available in both the MPLAB X IDE and MPLAB Xpress IDE – that bridges our MCUs, development hardware, and your code. With MCC, you can easily generate modifiable, production-ready application code for the MPLAB Xpress Evaluation Boards in just a few mouse clicks. Find out more at www.microchip.com/MCC ". It is my understanding that there is a cloud-based compiler that can also be used directly with the board (via an usb link to a local PC). 

The electrosome.com website has multiple [tutorials](https://electrosome.com/category/tutorials/pic-microcontroller/mplab-xc8/) that seem amenable for easy interconnections. Their first tutorial is also included, with appropriate acknowledgement here. 

Here is a good trade journal article: https://hackaday.com/2016/02/15/microchip-unveils-online-mplab-ide-and-10-board/

The off-line IDE is entitled MPLab X. Here is the linkk for details and download: http://microchipdeveloper.com/tls0101:start

I downloaded my CoolTerm Terminal software from [here](https://learn.sparkfun.com/tutorials/terminal-basics/coolterm-windows-mac-linux)

MPLab X IDE example with Curiosity Nano: http://microchipdeveloper.com/touch:lowpincount-curiosity
PIC 8-bit family comparison: http://microchipdeveloper.com/8bit:summary
Curiosity Nanoboard: https://www.digikey.com/en/product-highlight/m/microchip-technology/dm164144-curiosity-nano-board
libraries: https://www.microchip.com/mplab/microchip-libraries-for-applications . Microchip libraries for Windows has an .exe here that can be used to install.

This is a very useful link for relevant details for each of the key peripherals for a 8-bit PIC controller, and application examples for them on PIC 8 MCU boards: http://microchipdeveloper.com/8bit:peripherals. We plan to use MPLAB Xpress Evaluation Board which uses PIC16F188xx (specifically PIC16F18855 microcontroller - it is considered a Enhanced Mid-Range MCU). At present, we are evaluating the choice between the MPLAB Xpress Evaluation board which can be used with Microchip's cloud IDE and the Curiosity Evaluation board (perhaps their Nano version, which costs around the same as the Xpress Evaluation board). The former can be used with Microchip's cloud IDE and thus would not need one to learn the MPLAB X IDE that needs to be installed on one's PC. More recently, Curiosity Nano has also been integrated into cloud IDE. See this link: http://ww1.microchip.com/downloads/en/DeviceDoc/50002560A.pdf . However, checking through the app examples at this site:   http://microchipdeveloper.com/8bit:peripherals, It is not clear whether the Nano is close to the Xpress Eval board, in terms of maturity on the cloud IDE. For the latter, there is a good book as a lab supplement for this course: "In 10 Lines of Code" by  Lucio Di Jasio. Link: http://www.lulu.com/shop/lucio-di-jasio/in-10-lines-of-code/paperback/product-22653575.html . So the decision is probably to go with the MPLAB Xpress Evaluation board for the spring '19 semester. Architecture and register setting of various peripherals are well explained in the link about peripherals. That could provide the reading material for the students, in addition to the Reference manual for the specific MCU. Note that the examples at the link on peripherals are not for our specific MCU, but similar ones. So study the material and adapt to our needs (for e.g., the ADC module there is really the ADCC module in our PIC MCU. 

For launching the cloud IDE: Here is the link: https://mplabxpress.microchip.com/mplabcloud/ide/

Another way: Start from the examples site given above. Choose any example for this board. Click on the IDE icon under the "Open" column on the right hand side. It opens the IDE. Click on the myMicrochip login at the right bottom. You can create your login there, or use login if you already have an account. Click on MCC and open .jnlp file with Java web launcher.  

Win 7 installation: MCC download (a .jnp file) was somehow connected to wordpad. So, I had to do 'open with' and choose 'Java Launcher.' JRE was out-of-date. Installed it - with Oracle's recommended settings. Once it is installed, hope the Cloud IDE will work. Not sure of MCC launch. But the previously developed code compiled easily. Downloaded to the board and the board executed the code (for LED On Off) successfully. Still to go back and understand the MCC part. 

Linux installation: 

i remember my sister used to have a really small mp3 player and i got it when she got a a phone , thus not needing the mp3 player,
i remembering adding songs to it with the help of my older cousin brother and then listening to music everywhere i went - school ,tution , bus rides you name it i took it there 
but then i shortly after lost and i never found it again :(


i remember how good one purpose tech used to be in that era. 
i recently took a lil visit to that era when i got my hands on my ps2. 
tearing it down to clean it , respraying the case a better colour and restoring it. 
along the way i fell in love with old technology.
i got myself a few playstaion portable and restored them all and jailbroke them and wrote custom 
hombrew apps for them. 

i first wanted to build a custom homebrew app for my psp go and make it into a handy mp3 player
as it has bluetooth and a audio jack so that would be really cool. but then my psp go broke and i couldnt do that.

for the longest time i have been meaning to buy a old ipod classic and restoring it and jailbreaking and modding it 
but then i thought why not make my own mp3player? 
and so i began on the short journey of making the pcb for it.

i was in the same duration making a kindle and thus i had that "e ink display fever" 
i.e meaning i was in love with e ink displays and so i decided to use an e ink display

when i began i lowk just started designing without much of a design in my head. 

## The display 

okay so i will be using this e ink display - 

<img width="1154" height="246" alt="image" src="https://github.com/user-attachments/assets/d477c76d-3e15-4d1c-a2c2-b47230cb62e2" />

this is the Waveshare 2.13inch E-Ink Paper display HAT for Raspberry Pi, Three-Color
which is honesly so exciting to use.
this is made for the raspberry pi however there are pins given so i can use it with the esp32 aswell

<img width="523" height="293" alt="image" src="https://github.com/user-attachments/assets/18810f12-cd82-4f67-838d-e1da959fdb18" />



okay so here is more info on the e ink display -


# interface :- 
1) VCC	3.3V/5V
2) GND	Ground
3) DIN	SPI MOSI pin
4) CLK	SPI SCK pin
5) CS	SPI chip selection, low active
6) DC	Data/Command selection (high for data, low for command)
7) RST	External reset, low active
8) BUSY	Busy status output, high active

a total of 8 pins , 6 pins excluding the vcc and gnd 


# specifications :-

1) Model No. / Name:	Display HAT
2) Display Size (Inch):	2.13
3) Display Resolution (pixel)	212 × 104
4) Display Color	Red, Black and White
5) Operating Voltage (V):	3.3
6) Outline dimension (mm)	65 × 30.2
7) Dot Pitch	0.229 × 0.228
8) Grey level	2
9) Viewing Angle (Deg.)	&gt;170°
10) Interface:	3-wire SPI, 4-wire SPI
11) Full Refresh Time (s)	15
12) Refresh Power	26.4mW(typ.)
13) Standby Power (mW)	&lt;0.017
14) Dimensions (L x W x H) mm	65 x 31 x 8
15) Weight (g):	20


this info i got from robu.in 

# the microcontroller - 

Im using the ESP32-C3-WROOM-02

<img width="609" height="406" alt="image" src="https://github.com/user-attachments/assets/03acea6b-f310-494a-b81a-dd92b6a3c0a7" />

using this board ill be making my own board with required gpio pins and boot and reset button


# specifications:-

1) Frequency (GHz):	2.4
2) Data Transfer Rate	150Mbps
3) Sensitivity (dBm):	-105
4)
5) Supply Voltage	3 to 3.6Mounting Type:	Surface Mount
6) Operating Temperature (°C):	-40 to 85
7) Memory Capacity	384KB ROM, 400KB SRAM, 4MB Flash

also got the above info from robu.in 


# the audio dac

<img width="1119" height="482" alt="image" src="https://github.com/user-attachments/assets/d265515e-1428-4934-95c2-6128a77ca352" />



# Specifications :

1) Product Type : I2S DAC Audio Decoder Module
2) Model : GY-PCM5102
3) DAC Chip : PCM5102A
4) Audio Interface : I2S
5) Input Interface : 3-Pin I2S
6) Audio Output : 3.5mm Stereo Jack
7) Audio Resolution : 16-Bit / 24-Bit / 32-Bit
8) Output Channel : Stereo
9) Operating Voltage : 5V DC
10) Form Factor : PHAT Format
11) Compatibility : Raspberry Pi & I2S Compatible Devices
12) Signal Type : Digital Audio Input
13) Output Type : Analog Stereo Audio
14) Mounting Type : Board Mount
15) Communication Protocol : I2S
16) Power Supply : 5V DC
17) Dimensions : 32 x 18 mm

 # the sd card module 
 
 <img width="1028" height="325" alt="image" src="https://github.com/user-attachments/assets/a1c28fa6-4738-4a76-85d8-6981748d19ef" />
 which is honestly just a normal sd card module 

 
 its wired like this-



 <img width="463" height="264" alt="image" src="https://github.com/user-attachments/assets/15e633d3-472a-4fca-b798-23a1d6a88204" />


and then the switched, at first i was using the touch capacitive buttons but when i was designing the case for the kindle im making , which used them , i realised that it makes the entire case wayyyy tooo big and i would rather my mp3 player be slim


# the multifunctional buttons

<img width="873" height="584" alt="image" src="https://github.com/user-attachments/assets/08b14923-0158-45fb-988b-b053f33851b4" />

okay so im using these buttons because they are slim tiny and i really like the satisfying click they have. 

they are multifunctional because i will use them for everything i.e - play , pause , next , volume up , volume down. 

now lets get onto making the schematic

i actually made this earlier and documented it  but it was super super bad 

<img width="939" height="749" alt="image" src="https://github.com/user-attachments/assets/e78c9454-b2f8-472d-a8cd-e49efde8cc00" />

okay so i just made the microcontroller again 

<img width="481" height="641" alt="image" src="https://github.com/user-attachments/assets/4d2eb006-9886-4a3c-ba4f-4fac7fac3f34" />

okay so ive added the lithium battery charger aswell 

<img width="853" height="761" alt="image" src="https://github.com/user-attachments/assets/ae22f305-d19e-4d02-855b-57aa37e0bba8" />




finally added all the components im having a terrible migraine 

<img width="702" height="755" alt="image" src="https://github.com/user-attachments/assets/f9a5af5d-f427-411f-8d2f-98d124e15146" />

## august 10th 

yesterday i didnt complete the pcb fully but today i am. 

okay so apparently i didnt connect the pins to any of my modules so i just did that 

here is how i wired everything 

<img width="395" height="225" alt="Screenshot From 2026-08-10 11-16-31" src="https://github.com/user-attachments/assets/fab3bab7-efc8-4b55-9f9e-891d59a373d2" />

and then 

<img width="330" height="230" alt="Screenshot From 2026-08-10 11-15-11" src="https://github.com/user-attachments/assets/009be9f6-be31-4191-bbea-ab1571fc3411" />

and then 

<img width="415" height="259" alt="Screenshot From 2026-08-10 11-14-45" src="https://github.com/user-attachments/assets/4004d98a-6401-46a1-a38b-0f4b0caca4ba" />

and then finally - 

<img width="550" height="694" alt="Screenshot From 2026-08-10 11-15-28" src="https://github.com/user-attachments/assets/a09f311e-04cf-4363-8a6d-ca0622cb1631" />

okay so i removed the crystal because apparently the esp32 module already has a inbuilt crystal so i didnt really need that . so thats cool ig 


# the pcb - 
the pcb after all the routing looks like this. ( i dont want to redesign again )

<img width="962" height="600" alt="image" src="https://github.com/user-attachments/assets/fa77f83c-a240-4c00-9c6e-ddc7f15e118c" />


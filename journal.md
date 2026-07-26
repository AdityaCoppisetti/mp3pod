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

## **THE DISPLAY**
i was thinking of using this e ink display-

<img width="1333" height="346" alt="image" src="https://github.com/user-attachments/assets/7c7249ca-9e8d-4dc4-b91a-b72a7af0b259" />

which was lowkey good but then my pcb would be bigger and i didnt want it to be overlapping or anything so i decided on using this e ink display

<img width="1333" height="346" alt="image" src="https://github.com/user-attachments/assets/f37bd8fd-a75e-493c-a0b2-b569df10dfd4" />

this is bigger and the pcb could hide really easily behind the display

this is from the datasheet , this the measurement and the mechanical drawing of the e ink display -


<img width="801" height="556" alt="Screenshot From 2026-07-26 23-49-33" src="https://github.com/user-attachments/assets/48cf1800-b1f9-4f44-bbc6-30b143282cc4" />. 



im not using the raw display because the module is not that much expensive than the raw one
but if you want to make your pcb extremely flush then you can follow this schematic ( from the actual datasheet) and put this onto your pcb.


<img width="1116" height="777" alt="image" src="https://github.com/user-attachments/assets/08b3f165-4c46-4f3e-b325-57c1abb68ad1" />

but since im using the module here is how my module looks like actually from the behind- 

<img width="1115" height="795" alt="image" src="https://github.com/user-attachments/assets/f09a8519-54f4-4baa-b115-a274ea13787a" />

and then the actual picture of the module- 

<img width="658" height="546" alt="image" src="https://github.com/user-attachments/assets/52260321-bfc2-40b1-9f8a-34ff266258dd" />

here is the Typical Operating Sequence of the e ink display- 

<img width="551" height="713" alt="image" src="https://github.com/user-attachments/assets/fdf9ded2-6a57-4aae-91ea-fea195ea6d7a" />

and the display is really reliable aswell - 

<img width="602" height="762" alt="image" src="https://github.com/user-attachments/assets/fa0dc0e5-1e75-46d5-a21d-9146fa32240c" />




<img width="603" height="555" alt="image" src="https://github.com/user-attachments/assets/2a570388-0f7f-4c02-bead-a6805877e2a3" />


## THE MAIN MOTHERBOARD OF THE PCB - ESP32-C3-WROOM-02 

This is the module that i intend to use- 

<img width="1312" height="593" alt="image" src="https://github.com/user-attachments/assets/65f9687d-8989-495f-85b6-271d03548519" />


im using this because im really familiar with it since im using it in my kindle project aswell. 
for the kindle project i actully made my own esp32 devboard
so safe to say that im familiar with this module. 
but for this projcet i didnt want to make a whole diff esp32 devboard and then wire the tp4056 module and allat 
i wanted everything to be on the same pcb , atleast what i could make.

these are the specifications of the esp32 module on the robu.in website

<img width="975" height="403" alt="image" src="https://github.com/user-attachments/assets/19f68b9b-fe4a-4a62-8636-0ccadf909954" />

there are 2 kinds of modules- 

<img width="396" height="218" alt="image" src="https://github.com/user-attachments/assets/962b6743-754c-4c42-bf5c-404e4c8fad23" />


the ESP32-C3-WROOM-02U doesnt have a onboard antena yet has a slot to put it on.
still in a better description here is the comparision between the two modules

<img width="649" height="169" alt="image" src="https://github.com/user-attachments/assets/73b0cd64-437d-4dce-b41a-b1f772b92dcf" />



we want something that has bluetooth and wifi both and so i chose that.

i want to be able to connect my bluetooth headphone and custom wireless earplugs ill make in the future.

also i found a page from the datasheet that shows exactly why im using the module- 

<img width="676" height="806" alt="image" src="https://github.com/user-attachments/assets/c473793d-6d40-4d96-92aa-f5139525ceb9" />


here is a better way of how the module looks like -

<img width="675" height="580" alt="image" src="https://github.com/user-attachments/assets/24156314-f23e-4e70-9f3a-efaa5059ab3b" />



and then the module block diagram- 
<img width="628" height="745" alt="image" src="https://github.com/user-attachments/assets/bccafc20-cd80-49b7-80a7-401b31e90242" />




<img width="459" height="503" alt="image" src="https://github.com/user-attachments/assets/3881bda9-8e04-47e2-a8a1-bce1a832a5be" />



okay so i started working on the schematic and for the esp32 here is how it looks like , 
you may want to watch my lapse recording to trace backwards what i did if it isnt clear
https://lapse.hackclub.com/user/@adityacoppisetti

<img width="525" height="565" alt="image" src="https://github.com/user-attachments/assets/53d1cb58-1878-4ba4-b8b5-29c0df2d062b" /> 
also note that the crystal is wired within.

i know i know this is the prettiest and if you dont understand you can even look at my kindle project and you will see ive done the same wiring over there


<img width="589" height="475" alt="image" src="https://github.com/user-attachments/assets/0b0358ab-857c-4669-ab4c-c34ef964e7a6" />

this section of the schematic provides power to the board and enables usb communicatoin via the c type port between the esp32-c3 and the computer youre using. it handles the usb power input and even protekcs the usb data lines from fluctuation and wierd electrocstatic discharge.

why am i using that exact usb type c recepticle- i have a ton of c type wires lying around and no one has those old micro usb( idek what they were called) lying around.

whats with the pull down resistors? (R1 & R2) the usb c requires configuration channel (CC) resistors so that the host recognizes the device correctly ( i lowk really wanna give this board a really funky name bahahaha)

why they are needed- identify the borad as usb device (sink) allow the usb host to enable the 5v supply ensure the compatibility regardless of cable orientation. without these resistors i dont think the usb-c would provide power.

VBUS ( the 5v) the vbus line carries the incoming 5v from the usb connector. it supplies the oboard voltage regulator , supplies the usb 5v header pin. acts as the primary power source when connected to a computer.

i think that the D10ESD protection diode is very very very important because the usb connector is exposed to the outside world and is susceptible to electrostatic discharge. it 
protects the pcb from static electricity. diverts voltage spikes safely to ground helps prevent the damage to the esp32 and usb circuitry.


and then we have the LDO (3.3v)

<img width="439" height="445" alt="image" src="https://github.com/user-attachments/assets/e134f075-8ad3-4dce-965a-d940637a1c1e" />

once again if you dont understand everything is there in the kindle journal.md


and then this is the wiring for the boot and reset buttons 

<img width="308" height="475" alt="image" src="https://github.com/user-attachments/assets/d4a3da78-5113-4b20-842c-b490b275b687" />


and with that we have the esp32!


## **lets move onto the tp4056 module**

in the kindle project i actually made the tp4056 as a entirely different small pcb
but for this project i didnt want that so i make it all on the same pcb board

# the  MCP3831-2-OT BATTERY CHARGING CIRCUIT


<img width="356" height="260" alt="image" src="https://github.com/user-attachments/assets/8441f54a-d8ab-4480-a20e-71acd262d380" />

here is how wired it , make sure this is the 3.3v one not the 5 volt one

and then i want to charge the batteries and i only have like c type wires so im using a c type recepticle

<img width="369" height="317" alt="image" src="https://github.com/user-attachments/assets/edfb0095-8844-45e8-adc6-4c5a848bef62" />


and i want to connect batteries so thats battery connector and then i want to power the esp32 so thats system out


<img width="435" height="255" alt="image" src="https://github.com/user-attachments/assets/4fb25c96-99e8-4049-9044-6915096044cb" />

very simple honestly 











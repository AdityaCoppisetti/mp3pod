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










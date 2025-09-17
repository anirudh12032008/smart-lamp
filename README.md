# smart-lamp
this is a smart voice controlled lamp! it uses the AI thinker vc-02 module to recive the audio input and then processes it through the firmware installed in it and sends signal! I converted the signals from 5V to 12V using a step UP converter and then used it to power the LED cause my relay module didn't work :(, we can also expand this project by connecting it with a esp32 MCU and then use it wirelessly from anywhere

## DEMO VIDEO
https://github.com/user-attachments/assets/136a9e41-25e5-49ad-b2e5-8eb487ddbee8



## JOURNAL
### Started with getting all the items
I decided to start with a hall sensor and a espcam along with voice commands and LDR sensor
![IMG_20250913_223731](https://github.com/user-attachments/assets/213bbf31-1ce4-401c-9bc0-d0a01b361fab)

### Connecting the hall sensor with the espcam
it was quite easy and I even tested it before 
![IMG_20250913_225925](https://github.com/user-attachments/assets/9063a10e-f239-4104-aa22-3af4d4dd7cc0)

### Programming the espcam and AI thinker VC02
at this stage espcam was making me break and to lose hope :( first it takes wayyy too much time to compile and second it was really tuff with modifying stuff to hit a custom endpoint
![IMG_20250914_001449](https://github.com/user-attachments/assets/45b6cb51-91f3-4c38-9c9d-217fba061f79)

### Continued with VC02
created the configurations for the firmware of the thinker module! changed everything for better customization and future expansion! the firmware was taking a lot of time to process cause it was tuff to like configure every word in the module
![IMG_20250914_004315](https://github.com/user-attachments/assets/173640ae-9da0-40e6-971f-6305e5dc824b)

### Had to restart with the firmware
Due to some error in the previous configurations cause this was my first time I had to go look for better documentations but then ended up reverse engineering to setup the firmware and finally got the firmware working and I configured it for 2 commands Light Up and Light Off!! I added multiple variations for the same command like please turn up the light etc, initialization command as HELLO PUDDING, and boot msg to HELLO ANIRUDH SAHU, kaise ho aap ( hindi{hinglish} )
![IMG_20250914_104824](https://github.com/user-attachments/assets/2c17f576-4235-441e-9670-43b6864550ca)


### got it working with a small LED
tested it with a small led to check if it was working fine
https://github.com/user-attachments/assets/74a0974e-3f79-498e-bc2f-eb72f5bbd583

### Added relay module
to drive the 12V light strip I decided to use a relay module instead of using the stepped up signal from the module but this was a really frustrating thing cause idk why the relay decided not to work! it was from BIN so it was old but I did not expected it to stop working but Ig I had bad luck I spent too much time trying to fix it but ended up with nothing
![IMG_20250914_155212](https://github.com/user-attachments/assets/82c41dec-af62-4e6a-91ea-28bc7c177846)

The relay didn't even work with a small LED so I had to drop the plan of using a relay! Instead I decided to use a step up module to increase the signal from 5V to 12V it would make the led glow very dim but that was my only way to get it working!!
![IMG_20250914_161822](https://github.com/user-attachments/assets/8b25f7b1-70c2-4a72-a797-89c9788244c3)

### Soldering the connections
#### LED Strip
started by soldering the led strip though I had to be carefull as the plastic covering started to melt as I was trying to do it
![IMG_20250914_163541](https://github.com/user-attachments/assets/65526dbd-c026-4f44-bee2-708734966641)

#### Step Up module
the jumper pins were also melting when I was trying to solder them and also coming out but then I just bend the pins and it all worked fine!! ( hopefuly )
![IMG_20250914_163926](https://github.com/user-attachments/assets/16da926e-0520-4be8-8b2c-ef4f043d435e)
![IMG_20250914_163924](https://github.com/user-attachments/assets/11ec2d85-fdcd-4540-b66b-720e9d6b82c0)
![IMG_20250914_163935](https://github.com/user-attachments/assets/7d80aab2-8c23-4c8c-8f10-71d74c146f3a)

#### Battery
I added a TP4056 module and connected a 3.7V battery with it, idk why but this was not working but after desoldering and using another module it worked even when both the module were same and were working absolutely fine!!! 
![IMG_20250914_165539](https://github.com/user-attachments/assets/501eb48f-bafa-4b16-8cdc-fbc522e0493f)
![IMG_20250914_165809](https://github.com/user-attachments/assets/7677cd82-10d2-49cc-815e-c35eaba26bed)

### Added the switch and got it all set up 
I used a cardboard box to put everything inside carefully and a pen to fix the led strip on! though closing the box was a issue as the wire were thick and the connection was breaking when I was closing the box!!!! and also i had to position the mic outside as from inside it was not catching anything!! but the speakers were working fine from inside
https://github.com/user-attachments/assets/2ef69706-edb3-4099-8c6b-dee3e00616df


https://github.com/user-attachments/assets/fd4c2174-6007-49fe-b94a-87c98dd91414



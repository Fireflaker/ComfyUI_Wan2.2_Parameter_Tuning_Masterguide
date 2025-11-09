# ComfyUI_Wan2.2_Parameter_Tuning_Masterguide
Mostly 14B I2v, attempts all diffusers (UNET, no GGUF). Also t2v, ect

## Vantage Long 1 :

Clip:
gg mega12 (from checkpoint loader)
VAE:
gg mega12 (from checkpoint loader)
Model Init:
gg mega12 shift 5
1 step
Model High:
gg mega12 shift 5
3 step
Model Low:
i2v low fp16 shift 5, 4 step t2v lora
2 step


cfg all 1, eular_a, beta, mid size, 0.95 denoise, overlap 1

No 5 seconds connection at all, sputtering foam.
<img width="105" height="116" alt="image" src="https://github.com/user-attachments/assets/32b7581a-b453-4ee0-ac73-47582eab5ce5" />



## Vantage Long 2 :

### Clip:
gg mega12 (from checkpoint loader)
### VAE:
gg mega12 (from checkpoint loader)
### Model Init:
gg mega12 STRAIGHT NO SHIFT
1 step
### Model High:
gg mega12 shift 5
2 step
### Model Low:
i2v low fp16 shift 5, 4 step t2v lora
2 step


cfg all 1, eular_a, beta, mid size, 0.95 denoise, overlap 2

Immedietly color spots, no recovery
<img width="215" height="204" alt="image" src="https://github.com/user-attachments/assets/1873ef11-ee79-4a0b-a3a5-c223512b2f4a" />

Did 3 rounds, all 150s all fail colorblind noise in 100ms.

<img width="671" height="242" alt="image" src="https://github.com/user-attachments/assets/3094ca39-c230-4161-9b11-97c84cef19ed" />


 
## Vantage Long 3:

### Clip:
gg mega12 (from checkpoint loader)
### VAE:
gg mega12 (from checkpoint loader)
### Model Init:
gg mega12 Past the SAME SHIFT 5
1 step
### Model High:
gg mega12 shift 5
2 step
### Model Low:
i2v low fp16 shift 5 BYPASS LORA
11 step

500ms to colorblinde color spot noise. Same fail.

<img width="441" height="230" alt="image" src="https://github.com/user-attachments/assets/da43cdfb-258e-4861-bf78-4c04aa440cb9" />




 
## Vantage Long 4:

### Clip:
wan2.2 umt5 xxl fp16
### VAE:
wan2.1 vae
### Model Init:
gg v7 shift 5
1 step
### Model High:
gg v7 same shift 5
2 step
### Model Low:
VACE low fp16 shift 5 , 4 step i2v lora
11 step

Does not look like photo. Character human limbs wrong, bright colorful rgb oblong dots all over

 
## Vantage Long 5 OK:

<img width="883" height="582" alt="image" src="https://github.com/user-attachments/assets/43955043-6ab4-42e0-9084-1084a4cbe055" />
Good coherance and vidual quality, good body phyusics, bad action, where things show and connected move.
<img width="207" height="219" alt="image" src="https://github.com/user-attachments/assets/1f9c901d-3870-4ece-9a5e-8ad91fb451d9" />

## Vantage Long 6 OK:
<img width="976" height="650" alt="image" src="https://github.com/user-attachments/assets/21bb296f-4c4e-4847-8234-a6806b023e52" />
Just stand and do nothing - ish, but otherwise resonable
<img width="220" height="209" alt="image" src="https://github.com/user-attachments/assets/4702b673-1183-4fba-b1d6-4d9d6c0d41ef" />


## Vantage Long 7 ok worse:

Steps: 1,4,26. Same
Stands and do nothing at all bounce, slihgly dreamy




## Vantage Long 8 older but better:

<img width="848" height="589" alt="image" src="https://github.com/user-attachments/assets/89687e14-f262-42d3-81a4-b24f80b5d547" />



## Way worse on 7860
<img width="1589" height="780" alt="image" src="https://github.com/user-attachments/assets/9bee8bb1-2bec-43ba-9b0a-6fb115520695" />





Steps all 1,1,2
All i2v loras

All VACE: dark movie feel, from a different movie, not same person, no 5s coherance at all. No.
<img width="269" height="254" alt="image" src="https://github.com/user-attachments/assets/a25e3a78-f145-4d27-bdc8-c1b5cc43f6e7" />

All i2v: works, character does not follow well, low quality like seeing through water glass
<img width="296" height="292" alt="image" src="https://github.com/user-attachments/assets/f1b730b7-dff2-459b-9167-a52c7439a835" />

All t2v: no 5s coherance. White spotty blurry, looks ok. No.
<img width="239" height="250" alt="image" src="https://github.com/user-attachments/assets/cb14740c-7993-4360-bdbc-9b644373e631" />

All inpaint: Sharper slightly, but ruined face, sporatic short morph fast; has potencial
<img width="259" height="278" alt="image" src="https://github.com/user-attachments/assets/4fea1f3b-297a-4256-aca4-e6803ce41ec2" />

All Fun Control:
Vector size run fail
<img width="618" height="277" alt="image" src="https://github.com/user-attachments/assets/aa642701-039c-43c0-9bcd-3c088d166dc9" />

All Fun Camera: 
has some 5s coherance, but useless. Double face, no idea with text prompt
<img width="245" height="268" alt="image" src="https://github.com/user-attachments/assets/b85dced2-baad-4a82-932d-c5c05a6e4e7d" />




I2v all ,but 0.5 lora for both
Worse waterglass effect. Useless
<img width="593" height="748" alt="image" src="https://github.com/user-attachments/assets/ef4d9ecf-05a7-43ea-91b2-4a3f5b38339a" />


I2v all ,but 2.4 lora for both
Light fried, no detail, understand text better. 
<img width="241" height="263" alt="image" src="https://github.com/user-attachments/assets/0f685998-04ac-4022-8117-aa0036722f9e" />

I2v all, no lora, 1, 12, 12
Very bad. Immedietly melted. BAD
<img width="278" height="283" alt="image" src="https://github.com/user-attachments/assets/5a7f9b75-f3de-4b77-ba30-476e2c3864c9" />
<img width="280" height="289" alt="image" src="https://github.com/user-attachments/assets/8c2c6e21-51a4-4e1e-8b28-8575be34a016" />
same setting different seed, do nothing, random things, BAD.
<img width="285" height="316" alt="image" src="https://github.com/user-attachments/assets/e6c52b4b-8e8c-4cb6-b0d6-17cc5ce30484" />


I2v all, revert to yes lora 1:00, 1, 5, 5
lora 1.0
Pretty good, slowly develops more and more color noise comfetty max colorful
<img width="299" height="293" alt="image" src="https://github.com/user-attachments/assets/14bffc1a-5e0d-4a28-a03d-b89f10a8c99a" />

I2v all, revert to yes lora 1:00, 1, 5, 5
lora increased both to 1.8
First 5s very good, then at second clip over saturation shot red hot. Indeed no more colro noise dot at all!
<img width="290" height="298" alt="image" src="https://github.com/user-attachments/assets/35def9a1-68b5-4433-927d-84b6f633a2dd" />
<img width="271" height="284" alt="image" src="https://github.com/user-attachments/assets/786c1fcd-13dc-4337-9dc1-fd20abeba8cf" />

SAVE POINT t12 v7
Same as above, loras down to 1.5; steps down to 1, 3, 2
Promising, low ish motion. Dumb to understand follow text.
<img width="266" height="298" alt="image" src="https://github.com/user-attachments/assets/61ae1712-5084-45ae-a47b-46ca68ecd757" />
second chunk takeover ok
<img width="277" height="290" alt="image" src="https://github.com/user-attachments/assets/1fff588c-7b66-4b74-b31f-2168a4849708" />

Try in order to improve text following, exact same but now use gg12 clip and vae
Honestly, zero improvement.
COMCLUSION: IGNORE MEGA12 VAE AND CLIP; theyre the same. Need doucble varify.
<img width="601" height="466" alt="image" src="https://github.com/user-attachments/assets/4886ee00-c621-4bf2-a86b-e9c55655a72a" />
<img width="287" height="284" alt="image" src="https://github.com/user-attachments/assets/ae90a693-0cad-4f7b-a438-a1df20b03a74" />

Core issue (right): Not following text enough

Increse shift from 5 to 6; then to 8
RIGHT RUNNIGN q1 and Q2




left after the 211.25s 3 is
All 1,2,2 steps; eular_a, beta, 0.9 demoise
1.8 lora surprizingly quite good
<img width="569" height="635" alt="image" src="https://github.com/user-attachments/assets/0db1af99-e243-4add-802a-282cc1a1f73b" />

high, gg, low, same everything. gg v7. normal vae and clip
Better useful motion, silimar quality to lora 1.8
<img width="250" height="269" alt="image" src="https://github.com/user-attachments/assets/ba8b0eba-c624-42c2-8fc5-75e74d065abf" />


high, gg, low, same everything. !BAD gg v12 BAD!   normal vae and clip
Instant merge to text only mood, no image retention at all, wrong physics. Wrong body parts. BAD
<img width="233" height="266" alt="image" src="https://github.com/user-attachments/assets/4d845086-04f2-465e-a021-1bd0addfb1cd" />


high, gg v7, low. WITH ggv12's vae and clip using load checkpoint (super mix)
lora 1.8
Broken physics, weird body parts, but action amount ok. low-ish res, but visually ok ish. Good understanding of text prompt.
<img width="247" height="251" alt="image" src="https://github.com/user-attachments/assets/40e5dbd7-8852-4f2a-b763-48ab39be1d54" />


LEARNING: when see color spotty max blue yellow noise, increase lora strength from 1 to 1.8

Same as above but using only vae and clip from the mega 12 gg; otherwise normal high low i2v with lora
same 1,2,2
same lora 1.8
Good early on, morphed body, trashed physics likly due to early noise
Second 5s fail to take over
<img width="237" height="266" alt="image" src="https://github.com/user-attachments/assets/14f5bf41-6be5-4785-bd2f-2d746eb8981b" />
<img width="231" height="265" alt="image" src="https://github.com/user-attachments/assets/a2a8c54c-50ea-4659-842d-cc2f480536cc" />

Down loras to 1.4 Otherwise same Only original high low, only using clipa dn vae from gg12
no longer fried, but body morph likly due to way too mcuh noise
<img width="604" height="743" alt="image" src="https://github.com/user-attachments/assets/c4e19f57-f5ac-4338-b55e-5d05f3fb8c9e" />

Now issue: Noise too high

Down shift all from 5 to 3. Same all else
<img width="647" height="506" alt="image" src="https://github.com/user-attachments/assets/adb6b934-60d5-4f2f-8942-62f490bf1317" />
<img width="262" height="267" alt="image" src="https://github.com/user-attachments/assets/c6fb47f7-6e90-4bec-91ab-d54e23135cbc" />
Still body morphic. Maybe just low resolution not noise at this poitn currentis 784 x 976 so...shoudl not be an auissue. Denoise is still 0.9

Last attempt, just up 992 x 1680 huge. All else same. Still 1,2,2 (gpu ram pushing max)
Left quese first

Then up steps to 1, 3, 3
Left quese second


r12 end. Re approch, using 



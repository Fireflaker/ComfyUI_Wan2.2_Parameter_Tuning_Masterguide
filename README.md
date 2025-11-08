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

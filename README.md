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

### Clip:
xx
### VAE:
xx
### Model Init:
xx
1 step
### Model High:
xx
4 step
### Model Low:
VACE low fp16 shift 5, NO LORA
26 step

Good coherance and vidual quality, good body phyusics, bad action, where things show and connected move.
<img width="460" height="678" alt="image" src="https://github.com/user-attachments/assets/faa1be17-06f8-4bfc-8e38-0f6e6c04e27c" />
<img width="312" height="292" alt="image" src="https://github.com/user-attachments/assets/92c0c041-0667-459e-88b7-a5ce705c309f" />
<img width="207" height="219" alt="image" src="https://github.com/user-attachments/assets/1f9c901d-3870-4ece-9a5e-8ad91fb451d9" />

## Vantage Long 6 OK:
<img width="976" height="650" alt="image" src="https://github.com/user-attachments/assets/21bb296f-4c4e-4847-8234-a6806b023e52" />
Just stand and do nothing - ish, but otherwise resonable
<img width="220" height="209" alt="image" src="https://github.com/user-attachments/assets/4702b673-1183-4fba-b1d6-4d9d6c0d41ef" />

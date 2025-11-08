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


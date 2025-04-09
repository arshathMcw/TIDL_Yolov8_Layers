### 1. 
```
Input : 1x192x80x80
Output : 1x64x80x80
Kernel1 : 64x192x3x3
Stride1 : 1x1
Padding1 : 1x1x1x1
Kernel2 : 64x64x3x3
Stride2 : 1x1
Padding2 : 1x1x1x1
```
### In Netron
![alt text](image-10.png)
### In Model Artifact
![alt text](image-20.png)
### Running on ARM
![alt text](image-13.png)
### Running on TIDL
![alt text](image-12.png)
### Evaluation
![alt text](image-11.png)

## Descripción 
This [garden](https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg) contains more than it seems.
## Hints
1. What is a hex editor?
## Solución
```
unsigned char ucDataBlock[40] = {
	// Offset 0x0023056E to 0x00230595
	0x70, 0x69, 0x63, 0x6F, 0x43, 0x54, 0x46, 0x7B, 0x6D, 0x6F, 0x72, 0x65,
	0x5F, 0x74, 0x68, 0x61, 0x6E, 0x5F, 0x6D, 0x33, 0x33, 0x74, 0x73, 0x5F,
	0x74, 0x68, 0x65, 0x5F, 0x33, 0x79, 0x33, 0x36, 0x35, 0x37, 0x42, 0x61,
	0x42, 0x32, 0x43, 0x7D
};

```
![[Pasted image 20251001192328.png]]
## Notas

## Referencias
https://cyberchef.io/#recipe=From_Hex('Auto')&input=MHg3MCwgMHg2OSwgMHg2MywgMHg2RiwgMHg0MywgMHg1NCwgMHg0NiwgMHg3QiwgMHg2RCwgMHg2RiwgMHg3MiwgMHg2NSwweDVGLCAweDc0LCAweDY4LCAweDYxLCAweDZFLCAweDVGLCAweDZELCAweDMzLCAweDMzLCAweDc0LCAweDczLCAweDVGLCAweDc0LCAweDY4LCAweDY1LCAweDVGLCAweDMzLCAweDc5LCAweDMzLCAweDM2LCAweDM1LCAweDM3LCAweDQyLCAweDYxLCAweDQyLCAweDMyLCAweDQzLCAweDdE
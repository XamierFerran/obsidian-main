---
tags:
  - projects/work/guajira/geofencing
  - projects/work/guajira/gps
  - projects/work/guajira/
---
## Questions
- Is Runni's implementation for geofencing? GPS turns off power?
## Conversation References
![[Pasted image 20250304223244.png]]
![[Pasted image 20250304223315.png]]
## Hypothesis
1. "En el diagrama, no existe un diodo que evite ele retorno de corriente a traves del sistema"
	1. Flyback diode
	2. Back voltage/current
	3. TVS diode
2. "El empate en el cable de 600mm"
	1. $P=IR^2$
	2. Immediate change in temperature
	3. Added resistance from splice worsening system performance
3. "Condiciones de ventilacion"
4. "Picos de voltaje a la salida del rele"
	1. 
5. "Interferencias y ruidos ocasionados por el convertidor DC/DC"
## Arguments
- The relay is galvanically isolated and therefore cannot cause a voltage spike in the Guajira system
	- https://www.digikey.com/en/articles/how-to-implement-galvanic-isolation-for-power-and-signal-lines
## System Information
![[Pasted image 20250304223151.png]]
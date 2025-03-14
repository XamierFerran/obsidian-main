---
tags:
  - projects/work/guajira/geofencing
  - projects/work/guajira/gps
  - projects/work/guajira/
  - resources/electrical_components/relays
---
# Questions
- Is Runni's implementation for geofencing? GPS turns off power?
	- yes!
- 350W at 48V on website, 7amps? I thought like 22?
	- Battery can produce up to 19A at 48V constant and 52.1V peak
	- Runni bikes run a different controller than the ones in Bogota but still provided by Guajira 
	- Controller Runni is using runs at 22A and the Bogota ones at 17A
- Do you have a way to capture the voltage spike in the relay? Need oscilloscope rated for voltage and current?
# Hypothesis
1. **"En el diagrama, no existe un diodo que evite ele retorno de corriente a traves del sistema"**
2. **"El empate en el cable de 600mm"**
3. **"Condiciones de ventilacion"**
4. **"Picos de voltaje a la salida del rele"**
5. **"Interferencias y ruidos ocasionados por el convertidor DC/DC"**
# Failure Points
- **Spliced/Melted Wire Jacket** according to the picture is rated at 16AWG, which is about 13 amps. The system runs 6A-9A higher, which could explain why there is heat lost on the wire.
- **The spliced wire** can cause significant heat due to power loss according to this equation $$P_{loss}=I^2R$$ where any significant increase in resistance can cause drastic power loss the higher the current is.
- **The relay is galvanically isolated** but that does not mean that a voltage spike cannot happen. In the data sheet of a relay, there should be a voltage and amperage rating that would allow insight into at what voltage the galvanic isolation would break down. Relay failures are not uncommon: [source](https://automationcommunity.com/most-common-relay-failure-reasons/). 
	- Note - relay rated for 40 amps according to video
- **The relay can experience a voltage spike due to induction**. When an inductive load, such as a relay coil, is cut off from a circuit, the load generates a high voltage of hundreds to thousands of volts in the reverse direction to the source voltage. This voltage is referred to as "reverse voltage." A high reverse voltage causes a large current to flow through the circuit, which damages the contact that controls power supply to the inductive load, and the circuit itself as well. As a result, the service life of the circuit is reduced significantly. [source](https://ac-blog.panasonic.com/relay/protecting-a-relay-coil-from-a-surge)
- **The relay can also experience inrush current**. This is different from a voltage spike due to induction as that is caused by opening the contacts and deenergizing the coils and an inrush current is caused when the contacts close and connects the system to a capacitive load such as a battery. This initial rush of current is much higher than the steady state. [source][https://components.omron.com/us-en/solutions/relays/high-capacity-relays/inrush-prevention-circuits]![[Pasted image 20250307141754.png]]
- **Regardless of failure point, a TVS diode** would prevent any voltage spikes from occurring that could potentially harm the system. The diode on the GPS's PCB likely only protects its own side of the system as the relay is isolated. Another TVS diode on the Guajira side would protect it. [source](https://ac-blog.panasonic.com/relay/protecting-a-relay-coil-from-a-surge) [source](https://uk.rs-online.com/web/content/discovery/ideas-and-advice/tvs-diodes-guide)
# System Information
![[Pasted image 20250304223151.png]]
# How to Build a Syringe Pump

- [Mechanics](/Syringe-Pump/mechanics): See how to construct the Syringe Pump
- [Electrical Logic](/Syringe-Pump/electrical): See how to wire the Syringe Pump
- [Code](/Syringe-Pump/code): See the code to operate the Syringe Pump

## Performance
### Resolution
The Syringe Pump is made for a 20mL volume syringe. Resolution will depend on the microstepping implemented when wiring and programming the NEMA 17 stepper motor. The implementation presented on this webpage uses one sixteenth microstepping. Further, the pitch of the threaded rod used for linear actuation plays a key role in determining the resolution of syringe extrusion. For this design, a threaded rod with a 1.25mm pitch was used. 

_Thus, the resolution limit of our design is approximately **0.45uL**._

Our syringe has an internal diameter of 19mm. Each rotation of the motor moves the syringe pump 1.25mm. The resultant volume extruded in one complete rotation is 1.418mL. Since we are microstepping, however, we are moving the syringe 1.25mm/3200 steps per rotation. Thus, improving the resolution to the sub-microliter level. 

Further improvements can be made by using a threaded rod with a lower pitch.

### Max Flow Rate
The max flow rate of our designed syringe pump is limited by a few key factors. (1) The speed and step size of the NEMA 17 motor. Particularly, the max flow rate is inhibited by the occurrence of ringing (i.e., the internal oscillations of the magnets within motor due to momentum). Ringing occurs when the motor is wired to make full steps. While this would aid in achieving the highest max flow rate, it makes the motor inefficient and very noisy. (2) The pitch of the threaded rod. The greater the pitch, the further the syringe pump moves in one rotation of the motor, and the faster the solution is extruded. (3) The properties of the material in the syringe pump. For example, more viscious fluids would be more resistive to extrusion or non-Newtonian fluids would counter any rapid movements by the syringe plunger.  

### Happy building!!
![Syringe Pump Success](/Syringe-Pump/Assets/IMG_3467.jpg)

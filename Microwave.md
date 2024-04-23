Modulation is needed 
- No interference of signals. 
- Multiplexing is possible. 

Antennas with a length of (lambda/2) work as transducers - they convert electrical signals to EM waves. 
Guided transmission lines:
- Metallic wire 
- Optical fibre 
- Coaxial cables 
- wave guides 

*Skin Depth* - Characteristic distance at which the amplitude of an EM wave has attenuated to 1/e (36.8%) of its original strength. 
![[Pasted image 20240423070956.png]]

Range of microwave signals - 1Ghz to 1000Ghz. 
Agar conventional tx lines have dimensions comparable to lambda/2 then they will start behaving like antenna and emit EM waves and radiation loss will occur. 

WiFi and Bluetooth operate at 2.4/5/5.8Ghz since these are free and unlicensed. 
Mobile communication - 700, 800, 900, 1800 Mhz and 2.1, 2.5, 3.1, 3.2 Ghz
Microwave oven - 2.4Ghz 
free bands are used for ISM - industrial, scientific, medical. 
![[Pasted image 20240423071433.png]]
TE10 is dominant mode with lowest cutoff freq and then comes TM11 mode.
SWR - Standing wave ratio = Vmax/Vmin

Matched termination -> No standing wave -> SWR = 1
![[Pasted image 20240423072709.png]]
On considering direction it becomes
![[Pasted image 20240423072748.png]]
![[Pasted image 20240423072942.png]]

## Microwave sources
Gunn diode, Travelling Wave Tube, Magnetron, Reflex Klystron, PLL (Phase locked loop) Synthesizer, Solid State Device 

Klystron Sources - Two cavity klystron, Multicavity klystron, reflex klystron

Generates microwave signal at DC voltage.
Third new energy band.

TE and TM only exist bin waveguide and not in free space.
TE electric field is perpendicular to the direction of wave propagation and zero in the direction of the same. 
![[Pasted image 20240423074038.png]]

Boundary conditions:- 
- Et1 = Et2 
- En1a1 - En2a2 = sigmas (surface charge density at boundary)

- H1n1 = H2n2
- Ht1 - Ht2 = k (current density at boundary)
## For TE Mode 
![[Pasted image 20240423074610.png]]
![[Pasted image 20240423074632.png]]

## For TM Mode
![[Pasted image 20240423074702.png]]

## Properties of Scattering Matrix 
1. Zero property - Multiplication of a row with complex conjugate term-wise and adding all elements is equal to 0.
2. Unit property - Multiplication of row with its complex conjugate followed by addition of all is equal to 1. 
3. Symmetric property - When power applied through port N and remaining ports are match terminated then:- 
- Snn = 0
- Sij - Sji

## E-Plane Tee
Direction of electric field is parallel to E Arm (side arm).
If power is applied at port 3 then it is equally divided at port 1 and port 2. 

Single port device - antenna 
2-port device - isolator, variable attenuator, slotted line section, SS tuner 
3-ports device - E-Plane Tee, H-Plane Tee
4-ports devices - Magic Tee/Hybrid tee, directional coupler

- Symmetric around E arm. 
- Port 1 and port 2 are match terminated - S33 = 0.
- S23 = -S13

## H-Plane Tee
Side arm is parallel to the direction of H.
Power applied at port 3 is equally divided between port 1 and 2. 

- Symmetric about the H arm. 
- S13 = S23
- For matched termination of port 1 and 2, S33 = 0

## Magic Tee 
If power is fed at port 1 and 2, no power at 4. 
When power is fed at port 3, it is divided between 1 and 2 with a phase difference of 180 degree. 
Port 3 and 4 are isolated. 

- S34 = S43 = 0
- Symmetric 
- When power is applied at port 3 or 4 and ports 1 and 2 are match terminated, S33 = S44 = 0.
- When power is fed at one of the collinear ports, the power obtained at the other collinear port is 0. 
- It's a combination of E-Plane and H-Plane Tee -> S14 = -S24 and S13 = S23
- Ports 1 and 2 are also isolated from each other -> S12 = S21

FDD (Frequency division duplexing) is more used because TDD me there's time delay. 

(n + 3/4) modes are possible in a reflex klystron. 

## Symmetric directional coupler 
Used to transfer power form primary waveguide to secondary waveguide. 
- Symmetric device - Sij = Sji 
- Port 1 and 3 are isolated from each other -> S13 = S31 = 0 
- Port 2 and 4 are isolated from each other -> S24 = S42 = 0
- If all the ports are match terminated -> S11 = S22 = S33 = S44 = 0

_Coupling Factor_ - 10log(power in primary waveguide/Power in secondary waveguide) = 10log(P1/P4)

*Directivity* - 10log(P1/P3)
Should be infinite. 

## Circulator 
Circulates power from one port to another port in one direction. 

### Matched Termination 
Every waveguide has a characteristic impedance. This is the impedance at which the waveguide transmits power most efficiently with minimal reflection. 
Matched termination means that the port is connected with impedance that exactly match the characteristic impedance of the waveguide system. 
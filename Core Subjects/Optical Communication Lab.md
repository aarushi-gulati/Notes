## Introduction

#### Advantages of Optical Communication 
- High security 
- Low bit error rate 
- Good for long distance communication 
- Per bit cost of transmission is very low (although bohot costly hota hain optical communication, but because it is able to transmit large number of bits at once, per bit costing kaafi kam ho jaati hain)
- High speed 
- Electromagnetic compatibility 

Operating wavelengths - 850, 1310, 1550 nm (1550 latest hain)

Due to properties of Silica, losses are maximum at 1400 nm. 

#### Disadvantage
It cannot be used for broadcasting. 

#### Total Internal Reflection 
Light needs to travel from ==denser to rarer medium. ==
==Angle of incidence <= Critical Angle==

#### Relative Refractive index
![](../Meta/Pasted%20image%2020240423192604.png)
![](../Meta/Pasted%20image%2020240423192953.png)

#### Numerical Aperture 
Helps in determining how much amount of light can be coupled, inside an optical fibre from the source. 
![](../Meta/Pasted%20image%2020240423193035.png)

#### Types of Errors 
1. Longitudnal
2. Laterall 
3. Angular 

#### EMI of an optical fibre 
Optical fibres offer very low EMI but not zero due to the following reasons:- 
- Minimal level of energy coupling between the light signal and the atomic structures within the fibre. 
- Very strong external magnetic fields me minimal energy conversion and potential EMI ke chances rehte hain.
- Bending losses and mode mixing. 
- Faint mechanical vibrations. 
- Imperfect terminations. 

## Types of refractive index profiles 

### Step-Index fibre 
![](../Meta/Pasted%20image%2020240423194104.png)

### Graded Index fibre (GRIN)
![](../Meta/Pasted%20image%2020240423194131.png)
![](../Meta/Pasted%20image%2020240423194149.png)
Where alpha controls the shape of the profile within the core. 
Graded index is for core, nothing for cladding. 

For parabolic, alpha = 2. 

## Essential concepts

### V-Number
Aka normalised frequency. 
It's a dimensionless quantity. 
Essentially represents the ration between the core size and light confinement capability of the fibre. 

It's used to determine the number of modes that a fibre can support. 
![](../Meta/Pasted%20image%2020240423194619.png)

### Linear Polarisation
Jab ek light travel karti hain, usme electric and magnetic field constantly oscillate karte hain perpendicular to each other and perpendicular to the direction of propagation. 
Polarisation of light is mainly defined by the orientation of the electric field vector. 

In linear polarisation, ==electric field vector maintains a fixed orientation throughout its travel== and non linear mein electric field vector's orientation changes as the wave propagates. 

Advantages of the same are:- 
- Reduced polarisation mode dispersion - slight difference between the propagation speeds of various modes an cause signal distortion.
- Simpler system design - ek hi polarisation mode se deal krna hain toh simpler design.

### Normalised propagation constant 
Signal passes through different modes and each has its own propagation constant - toh apan in total bas ek normalised propagation constant define karte hain - normalised propagation constant. 
![](../Meta/Pasted%20image%2020240423201047.png)

To get exact number of modes, we draw a graph between b and v. 

Single mode fibre design criteria :- v <= 2.405

## Linearly Polarised Modes
They are nothing but a combination of TE, TM, HE etc modes. 
Linear polarisation is maintained to transfer data at very high speed.

LPum where   u = Number of nodes in the angular direction 
			m = Number of modes in the radial direction 

Cladding is made thicker at than the radius because:- 
- Intensity is not zero at core radius. 
- We need to reduce the effect of electric field. 

### Mode Field Diameter 
Can be measured only in single mode fibre. 
It characterises the effective area of light propagation within a single mode fibre. 
	It is the distance in the radial direction of the field where the field reduces to 1/e^2 of the maximum intensity of the field. 

## Single mode and multi mode fibres 
1. Single mode supports only one mode - LP01 while multimode supports more than one. 
2. Single mode fibre is thinner. 
3. Due to above, light launching is more difficult in single mode fibre. 
4. LASER can be used for light launching in single mode fibre while both LASER and LED could be used in multi mode fibre. 
5. Only intramodal dispersion exists in single mode while both intramodal and intermodel exists in multi mode fibres. 
6. Single mode is suitable for long distance communication while multi mode is suitable for LANs. 
7. Single mode fibre me there's step index type variation while in multimode there's both step index and GRIN fibre. 
8. Single mode fibres give higher transmission capacity because transmission capacity is inversely proportional to the amount of dispersion. 

## Dispersion 
The pulse of light in due course of propagation gets spreaded in the time domain, thereby resulting in the probability of intersymbol interference, due to the collision of two adjacent pulses -> This results in limiting the overall transmission capacity. 
![](../Meta/Pasted%20image%2020240423211412.png)
![](../Meta/Pasted%20image%2020240423211459.png)

In multimode fibre, there's more dispersion -> GRIN fibre is preferred as it reduces the amount of dispersion. 

### Material Dispersion
Arises from the inherent properties of the materials used in the fibre core. 
It affects how different wavelengths of light travel within the fibre, leading to signal distortion. 

Bulk property which occurs because the group velocity is a non linear function of frequency (lambda) through the non linear dependence of refractive index on the wavelength. 
It's uniform for a particular wavelength once the material composition is finalised. 

For a source of spectral width sigma, 
![](../Meta/Pasted%20image%2020240423212345.png)
As evident, kam spectral width pe kam dispersion hoga -> LASER me kam hoga as compared to LED. 
![](../Meta/Pasted%20image%2020240423212436.png)

### Waveguide Dispersion 
Arises due to the confinement of light within the fibre core and he way different wavelengths propagate at slightly different speeds. 

Offered because group velocity is a non-linear function of frequency through its dependence on the structure of the waveguide. 
![](../Meta/Pasted%20image%2020240423212737.png)
To control dispersion, we tailor the waveguide dispersion so that its shape cancels the material dispersion at one or more wavelengths.

## Types of single mode fibres 

### Conventional Single Mode Fibre (CSMF)
![](../Meta/Pasted%20image%2020240423213002.png)
1310nm par the waveguide dispersion cancels out the material dispersion. 
But it exhibits rather high dispersion at 1550 nm which is bad becausemodern light wave systems prefer operation near the 1550 nm window because of low attenuation and availability of commercial optical amplifiers. 

Also, transmission capacity is low because fibre is ready to transfer but the terminal devices cannot work with data at single wavelength. 
### Dispersion Shifted Fibre (DSF)
Exhibits 0 dispersion at 1550 nm. 
![](../Meta/Pasted%20image%2020240423213255.png)
Compatible with modern light wave systems BUT if we shift either way from 1550 nm wavelength -> It's suitable only for single wavelength operation and not for multi-wavelength operations. 

#### Four Wave Mixing 
Four-wave mixing (FWM) is a nonlinear phenomenon that occurs in optical fibers when intense light beams interact. It results in the generation of new light waves at different frequencies compared to the original input signals.

If lambda1 and lambda2 ki 2 waves transmit ho rahi thi toh iss effect ke kaaran 2 new generate ho jaengi -> 2lambda2 - lambda1 and 2lambda1 - lambda2 which may interfere with the originally transmitted wavelengths. 

To overcome this effect, we need dispersion to be small, but not zero. 

### Non-Zero Dispersion Shifted Fibre (NZDSF)
Modified form of DSF. 
![](../Meta/Pasted%20image%2020240423214231.png)

	The above three are capable of supporting at most 100 GBPS but not more than that -> order or Terabits per second ke nahi ho paenge. 

### Dispersion Flattened Fibre (DFF)
Capable of supporting very high transmission capacity of the order of terabits per second. 
![](../Meta/Pasted%20image%2020240423214444.png)
Exhibits 0 dispersion at more than one wavelengths. 
Capacity of DFF1 > DFF2 since it has a broader spectral range. 

This type can't be fabricated using step index fibre. 
#### W-Profile or doubly cladded 
![](../Meta/Pasted%20image%2020240423214728.png)
Variations are done is core as a step function. 
a -> core radius 
n3 -> cladding refractive index

#### Q-Profile or quadrupply cladded 
![](../Meta/Pasted%20image%2020240423214830.png)
This is used to get a DFF-1 type characterstic. 
a -> Core radius 
n5 -> cladding refractive index

### Dispersion Compensation Fibre (DCF)
Used to compensate the positive dispersion exhibited by the millions of kms of CSMF already installed in the country. 
Capable of generating large negative dispersion.

![](../Meta/Pasted%20image%2020240423220523.png)
Positive dispersion of CSMF needs to be compensated at regular intervals by inserting a drum of fibre consisting of DCF and mode converter. We want to compensate not at a single wavelength, but multiple. 

![](../Meta/Pasted%20image%2020240423220716.png)
![](../Meta/Pasted%20image%2020240423220727.png)
Pre-compensation -> DCF installed at transmitter end.
Post-compensation -> DCF installed at receiver end. 

Q Profile is suitable for generating large negative dispersion. 

## Wavelength Division Multiplexing (WDM)
Multiple data is transmitted over different wavelengths down the same optical fibre by multiplexing them in wavelength domain. 

![](../Meta/Pasted%20image%2020240423215522.png)
All the devices applied after optical transmitter and before detector need to be operated in optical domain otherwise there may occur bottlenecks, resulting in loss of data transmission. 

#### Channel Wavelength Division Multiplexing (CWDM)
1-1 nm ka gap hota hain between successive multiplexed wavelengths. 
![](../Meta/Pasted%20image%2020240423215301.png)

#### Dense Wavelength Division Multiplexing (DWDM)
0.17nm ka gap hota hain between successive wavelengths. yeh achieve karne ke lie advanced lasers are used. 

#### Distributed Feedback Laser (DFB)
![](../Meta/Pasted%20image%2020240423215744.png)
- Lasing medium which is covered with an outer thermal jacket in which the coolant is continuously circulated. 
- Optical filter at the output end of the device allows only those photons which exactly match the tuned of this filter. 
- Other photons are reflected back to the lasing medium. 
- These reflected photons again contribute to the lasing action, resulting in generation of additional photons. 

## Optical Sources 
![](../Meta/Pasted%20image%2020240423221728.png)

### Recombination
When P-N junction is forward biased, electrons and holes enter p and n junction s respectively and combine with the respective majority carriers, 
- Radiatively - release energy in the form of photon 
- Non-radiatively - release energy in the form of heat. 

Recombination process occurs between the minimum energy level of conduction band and maximum energy level of valence band. 
Above process must conserve both energy and momentum. 

![](../Meta/Pasted%20image%2020240423222038.png)
Indirect me momentum conserve karne ke lie heat dissipate hogi. 
Energy conservation ke lie light photon will be generated. 

### Quantum Efficiency of Optical Source
Ratio of injected electron-hole pairs that combine radiatively. 

![](../Meta/Pasted%20image%2020240423222505.png)

![](../Meta/Pasted%20image%2020240423222531.png)

The two recombination processes happen in parallel and so:

![](../Meta/Pasted%20image%2020240423222602.png)
![](../Meta/Pasted%20image%2020240423222619.png)


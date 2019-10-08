# GPS Tutorial: Scheme and spoofing

Jianqiu Cao

## GPS Introduction

GPS consists of three segments - the satellite segment (**satellite constellation**), the ground segment (**ground control network**), and the user segment (**user equipment**). See Figure 1 below.

![GPS Segments](Picture1.png)

Figure 1. GPS segment

The **satellite constellation** comprises satellites in low earth orbit that provide the ranging signals and navigation data messages to user equipment. 

The **ground control network** tracks and maintains the satellite constellation by monitoring satellite health and signal integrity and maintaining the satellite orbital configuration. Furthermore, the ground control network also updates the *satellite clock corrections* and *ephemerides* as well as numerous other parameters essential to determining user position,velocity, and time (PVT). 

The **user equipment** receives signals from the satellite constellation and computes user PVT.

## Positioning Principles: Triangulating

Editing...

## GPS Signals

Editing...

## Attacks

**GPS Simulator Attacks**[^1]

* Generate fake ephemeris data which includes spoofing location.

* Transmit signal using SDR(Software Defined Radio) platforms.

  ​


**C/A Code Spoofing Attack**[^2]

* Does not change the navigation message, but rather tampers with the pseudorange between the satellite and receiver. 
* The spoofer estimates the position and velocity of the victim thru radar and transmits an artificial seamless signal that conveys spoofing C/A code.




## Reference list

[^1]: Wang,K., etc., [Time and Position Spoofing with Open Source Projects. ](https://docs.google.com/a/hawaii.edu/viewer?a=v&pid=sites&srcid=aGF3YWlpLmVkdXx1aC11YXMtcHJvamVjdHN8Z3g6MjcxM2JkMjllYzA1NzM2)
[^2]: Shin,B., ..etc., [Spoofing Attack Results Determination in Code Domain Using a Spoofing Process Equation.](https://docs.google.com/a/hawaii.edu/viewer?a=v&pid=sites&srcid=aGF3YWlpLmVkdXx1aC11YXMtcHJvamVjdHN8Z3g6N2FjNzY5MzhmZDgxOWU3)
# GPS Tutorial: Scheme and spoofing

Jianqiu Cao

## GPS Introduction

GPS consists of three segments - the satellite segment (**satellite constellation**), the ground segment (**ground control network**), and the user segment (**user equipment**). See Figure 1 below.

![GPS Segments](Picture1.png)

Figure 1. GPS segment

The **satellite constellation** comprises satellites in low earth orbit that provide the ranging signals and navigation data messages to user equipment. 

The **ground control network** tracks and maintains the satellite constellation by monitoring satellite health and signal integrity and maintaining the satellite orbital configuration. Furthermore, the ground control network also updates the *satellite clock corrections* and *ephemerides* as well as numerous other parameters essential to determining user position,velocity, and time (*PVT*). 

The **user equipment** receives signals from the satellite constellation and computes user *PVT*. [^3]

## Positioning Principles: Triangulating

The GPS positioning principles can be shown in Figure 2 below. [^1]

![GPS Positioning Principle](Picture2.png)

Figure 2. GPS Positioning Principle

If we have three satellites (Satellite 1, 2 and 3) in the constellation broadcasting their coordinates (x1, y1, z1), (x2, y2, z2), (x3, y3, z3), and we measure the durations (τ1, τ2, τ3) between the broadcasting signals are sent and received by a user equipment, we can then solve the user's coordinate by the following equations: 

<a href="https://www.codecogs.com/eqnedit.php?latex=\sqrt{(x-x_{1})^{2}&plus;(y-y_{1})^{2}&plus;(z-z_{1})^{2}}=c\tau&space;_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\sqrt{(x-x_{1})^{2}&plus;(y-y_{1})^{2}&plus;(z-z_{1})^{2}}=c\tau&space;_{1}" title="\sqrt{(x-x_{1})^{2}+(y-y_{1})^{2}+(z-z_{1})^{2}}=c\tau _{1}" /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=\sqrt{(x-x_{2})^{2}&plus;(y-y_{2})^{2}&plus;(z-z_{2})^{2}}=c\tau_{2}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\sqrt{(x-x_{2})^{2}&plus;(y-y_{2})^{2}&plus;(z-z_{2})^{2}}=c\tau_{2}" title="\sqrt{(x-x_{2})^{2}+(y-y_{2})^{2}+(z-z_{2})^{2}}=c\tau_{2}" /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=\sqrt{(x-x_{3})^{2}&plus;(y-y_{3})^{2}&plus;(z-z_{3})^{2}}=c\tau_{3}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\sqrt{(x-x_{3})^{2}&plus;(y-y_{3})^{2}&plus;(z-z_{3})^{2}}=c\tau_{3}" title="\sqrt{(x-x_{3})^{2}+(y-y_{3})^{2}+(z-z_{3})^{2}}=c\tau_{3}" /></a>



## GPS Signals

Editing...

## Attacks

**GPS Simulator Attacks**[^1]

* Generate fake ephemeris data which includes spoofing location.

* Transmit signal using SDR (Software Defined Radio) platforms.

  ​


**C/A Code Spoofing Attack**[^2]

* Does not change the navigation message, but rather tampers with the pseudorange between the satellite and receiver. 
* The spoofer estimates the position and velocity of the victim thru radar and transmits an artificial seamless signal that conveys spoofing C/A code.




## Reference list

[^1]: Wang, K., Chen, S., Pan, A., [Time and Position Spoofing with Open Source Projects](https://docs.google.com/a/hawaii.edu/viewer?a=v&pid=sites&srcid=aGF3YWlpLmVkdXx1aC11YXMtcHJvamVjdHN8Z3g6MjcxM2JkMjllYzA1NzM2). 

[^2]: Shin, B., ..etc., [Spoofing Attack Results Determination in Code Domain Using a Spoofing Process Equation](https://docs.google.com/a/hawaii.edu/viewer?a=v&pid=sites&srcid=aGF3YWlpLmVkdXx1aC11YXMtcHJvamVjdHN8Z3g6N2FjNzY5MzhmZDgxOWU3). 

[^3]: FAA, [GNSS Frequently Asked Questions - GPS](https://www.faa.gov/about/office_org/headquarters_offices/ato/service_units/techops/navservices/gnss/faq/gps/#1). 
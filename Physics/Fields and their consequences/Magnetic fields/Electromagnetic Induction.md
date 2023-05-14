
When a conductive rod moves relative to a magnetic field, the electrons in the rod will experience a force, as they are [[Flux density and Moving charges|charged particles moving relative to a field]]. This force causes them to accumulate on one side of the rod, inducing an emf in the rod. This is known as electomagnetic induction.

Two laws govern the effects of electromagnetic induction:
>Faraday's Law: the magnitude of induced emf is equal to the rate of change of [[Magnetic Flux and Flux linkage|flux linkage]]
>Lenz's Law: the direction of induced current is such that it opposes the motion causing it


# Demonstration of Lenz's Law:

To demonstrate Lenz's Law, the speed of a magnet falling through a coil of wire can be compared to one falling without a coil.

As the magnet approaches the coil, there is a change of flux through the coil, so emf and current are induced in said coil. Due to Lenz's Law, the direction of this current opposes the movement of the magnet. The flow of this current causes the same pole to form on the top side of the coil as the pole of the magnet approaching it, causing repulsion between the two. This repulsion slows the magnet's fall. When the magnet passes through the centre of the coil, there is no change in flux so no emf or current is induced. As the magnet leaves the coil, there is a change in flux again. This causes current to flow in the direction opposing the magnet's motion. The current forms a pole on the bottom of the coil opposite to the pole that is moving away from it. This results in two opposite poles, causing attraction between the coil and magnet, slowing the magnets fall again:
![[Lenz's Law.png|450]]


# Faraday's Law:

Faraday's Law is expressed as:
$$\Huge \epsilon=N\frac{\Delta \phi}{\Delta t}=N\frac{d\phi}{dt}$$
This formula can be used to derive an equation that describes the emf induced in a straight conductor of length $l$ moving through a field of flux density $B$:
$$\huge s=v\Delta t,\,\,\,s\times l=lv\Delta t=A$$
$$\huge \Delta \phi=BA=B\left(lv\Delta t\right)=Blv\Delta t$$
$$\huge \epsilon=1\times\frac{\Delta \phi}{\Delta t}=\frac{Blv\Delta t}{\Delta  t}=Blv$$
If a coil is rotating at a constant frequency in a magnetic field, the emf induced can be calculated by finding the derivative of flux linkage with respect to time:
$$\huge \epsilon=N\frac{d}{dt}\left(\phi\right)=N\frac{d}{dt}\left(BA\,cos\,\theta\right)$$
$$\huge \epsilon=N\frac{d}{dt}\left(BA\,cos\,(\omega t)\right)=N\times-BA\omega\,sin(\omega t)$$
$$\Huge \epsilon=BAN\omega\,sin(\omega t)$$
Where $\omega$ is the angular velocity of the rotating coil, given by $2\pi f$.
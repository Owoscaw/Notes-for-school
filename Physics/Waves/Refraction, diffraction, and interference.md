Interference:

Path difference is the difference in distance travelled by two waves. See [[Progressive waves]] for information on phase difference. A coherent source has the same frequency and wavelength, as well as a fixed phase difference between the two. A laser is an example of a coherent source, the light emitted is monochromatic and only emits a single wavelength of light. Lasers are used as sources in diffraction experiments, as they tend to form clear interference patterns.

Young's double slit experiment demonstrates the interference patterns formed from two coherent light sources. This experiment can be done with two sources or a single source and a double slit. As the light passes through the slits, it diffracts and radiates out to form a series of maxima and minima, seen in the following image:
![[Double slit experiment.png|400]]
The formula associated with the above experiment is as follows:
$$\Huge W=\frac{\lambda D}{s}$$
Where $W$ is fringe spacing, $\lambda$ is wavelength, $D$ is the distance between S2 and F, and $s$ is the slit separation.

The series of maxima form when the path difference from the two sources (slits) is an integer multiple of the wavelength. This is because the two waves are in phase when they superimpose, so their displacements sum to create a more positive wave that appears as a bright spot. This is explored further in [[Principle of superposition and stationary waves]]. Formula for constructive interference:
$$\Huge |P_{1}\,-P_{2}|=n\lambda$$
$$\Huge n\in\mathbb{Z}$$
The series of minima form when the path difference from the two sources is a half integer multiple of the wavelength. This is because the two waves are completely out of phase when they superimpose, so their displacements completely cancel each other out. This is explored further in [[Principle of superposition and stationary waves]]. Formula for destructive interference:
$$\Huge |P_{1}\,-P_{2}|=\frac{n\lambda}{2}$$
$$\Huge n\in\mathbb{Z}$$


The same phenomenon can be observed with sound waves by placing two coherent speakers a distance away from each other and observing spots where they sound quieter and louder. These correspond to constructive and destructive interference of sound waves.

Young's slit experiment was initally evidence to support that light has wave-like properties and was used to deduce that EM waves exhibit wave-like properties.

Diffraction:

Diffraction is the spreading out of waves when they pass through or around a gap. The greatest diffraction occurs when the gap is the same length as the wavelength. As the gap gets increasingly small, the amount of the wave reflected instead of diffracted becomes increasingly greater. There is noticably less diffraction when the gap is larger than the wavelength.

Diffraction also occurs when a wave collides with an object, as it diffracts over the edge of the object. Less diffraction occurs when the object is wider in comparison to the wavelength.

Monochromatic (single wavelength) light can be diffracted through a single slit onto a screen to form an interference pattern of light and dark fringes. This pattern has a bright central fringe, which other maxima becoming increasingly less bright due to the inverse square law of EM radiation. This can be seen through the follwing graph:
![[Single slit interference.png|300]]

White light can be used instead of monochromatic light to produce a diffraction pattern of all different wavelengths of light. As each wavelength is diffracted by varying amounts, each different wavelength forms a maxima at different points. This forms a spectrum of all the colours of light on the screen. The interference pattern can be seen in comparison to monochromatic light in the following image:
![[Diffraction spectrum.jpg|500]]

A diffraction grating is a slide containing many equally spaced slits. When monochromatic light is passed through it, the resultant diffraction pattern is significantly sharper and more defined than double slits. This is because there are more waves constructively interfering at maxima, as there are more sources (slits).

The central maxima are also called the zero order maxima, as it is the "0th" maxima. The maxima immediatly next to the central maxima are first order, and so on and so forth. 

The formula associated with the diffraction grating experiments is:
$$\Huge d\,sin\theta=n\lambda$$
Where $d$ is the distance between the slits, $\theta$ is the angle to the normal made by the maximum, $n$ is the order of the maxima, and $\lambda$ is the wavelength of light. As wavelength increases, the distance between orders will increase as $\theta$ grows larger due to the increase in diffraction as slit spacing becomes closer to the wavelength.

The formula can be derived throught the following steps:
\> Consider central maxima, path difference is a single wavelength and $\theta$ is made between the normal to the grating, and a ray of light
\> A right angle triangle forms with the hypotenuse as the distance between slits, base as $\lambda$ (path difference), and the angle between the hypotenuse and height of the triangle being $\theta$.
\> Trigonometric equations therefore dictate that $sin\,\theta =\frac{\lambda}{d}$, which rearranges to $d\,sin\,\theta =\lambda$ for the first order maxima.
\> Path difference only increases by $n\lambda$ as the order of the maxima increases, so the equation can be generalised to $d\,sin\,\theta =n\lambda$.
![[Diffraction grating proof.png|200]]


Refraction:

Refractive index is a property of a material that is a measure of how much it slows light down when passing through it. It is calculated by dividing the speed of light in a vacuum by the speed of light in the substance:
$$\Huge n=\frac{c}{c_{s}}$$
Where $c_{s}$ is the speed of light in the substance and $n$ is the refractive index of the substance.

A material with higher refractive index can be characterised as being more optically dense. The refractive index of air is approximately 1, as light does not slow down to a significant degree when passing through air.

Refraction occurs when a wave enters a different medium, causing a change in direction either towards or away from a normal, depending of the materials refractive index. Snell's law is used for calculations involving refraction:
$$\Huge n_{1}\,sin\,\theta_{1}=n_{2}\,sin\,\theta_{2}$$
Where:
\> $n_{1}$ is the refractive index of material 1
\> $\theta_{1}$ is the angle of incidence of the ray in material 1
\> $n_{2}$ is the refractive index of material 2
\> $\theta_{2}$ is the angle of refraction of the ray in material 2

![[Refraction.png|220]]
As the ray of light meets the interface between materials of different refractive indexes, the ray of light that hits the interface first slows down first. As the rest of the ray crosses the interface, it will meet up with the parts that hit the interface first and bend towards the normal. This is true for a ray of light entering a more optically dense material. The opposite is true when a ray of light is travelling to a less optically dense material.

When the angle of refraction is exactly 90 degrees, the ray will travel along the boundary. The angle of refraction that causes this is known as the boundary's critical angle, $\theta_{c}$. This can be found by subsituting in 90 degrees for the angle of refraction in snell's law:
$$\Huge n_{1}\,sin\,\theta_{c}=n_{2}\,sin(90)$$
$$\Huge n_{1}\,sin\,\theta_{c}=n_{2}$$
$$\Huge sin\,\theta_{c}=\frac{n_{2}}{n_{1}}$$
$$\Huge n_{1}>n_{2}$$

Total internal reflection occurs when the angle of incidence is greater than the critical angle and the incident refractive index ($n_{1}$) is greater than the refractive index of the material at the boundary ($n_{2}$).
![[Total internal reflection.png|500]]

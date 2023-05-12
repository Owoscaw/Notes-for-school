
# Charge:

A capacitor can be charged by applying a potential difference across it. Once this happens, current starts to flow and a negative charge builds up on the plate connected to the negative terminal. This is because in conventional current, electrons flow from negative to positive. When the electrons reach the negative plate, they cannot jump across to the positive plate, so charge accumulates.

On the opposing plate, electrons are replelled by the like charge from the negative plate and move towards the positive terminal. The lack of electrons here causes an equal but opposite charge on the plate opposing the negative plate. This creates a potential difference across the plates.

As the charge across the plates increases, the potential difference between them will also increase. However, the rate of electron flow will decrease due to the force of electrostatric repulsion on the negative plate. As electron flow is decreasing, current will decrease and eventually reach zero when the charge across the plates is at a maximum. This is seen in the equation for current when charging:
$$\Huge I=I_0e^{-\frac{t}{RC}}$$
The other three quantities can be described by the equations:
$$\huge V=V_0\left(1-e^{-\frac{t}{RC}}\right),Q=Q_0\left(1-e^{-\frac{t}{RC}}\right)$$
Where $_0$ denotes the initial value of the quantity, $t$ represents time since charging began, and $RC$ is the time constant, equivalnent to the product of the capacitance of the capacitor and the resistance of the charging circuit.


# Discharge:

A capacitor can be discharged through a circuit if it is closed. When a capacitor is discharging, current will flow in the opposite direction used to charge it. Current, charge, and potential difference across the capacitor all fall exponentially.

This is because initially, there is a high force of electrostatic repulsion at the negative plate. This means that electrons will flow faster during the start of the discharge. The rate at which the electrons flow depends on the electrostatic force of repulsion; so as the amount of electrons on the negative plate decreases, current will decrease. The following three equations describe this:
$$\huge I=I_0e^{-\frac{t}{RC}},V=V_0e^{-\frac{t}{RC}},Q=Q_0e^{-\frac{t}{RC}}$$
Where $_0$ denotes the initial value of the quantitiy, $t$ represents time since the circuit closing, and $RC$ is the time constant, equivalent to the product of the capacitance of the capacitor and the resistance of the circuit.


# Time constant:

The time constant for a capacitor is equal to the product of it's [[Parallel plates and dielectrics|capacitance]] and the resistance of the circuit it is being used in:
$$\Huge \tau = RC$$
The time taken for current, charge, or potential difference to half can be found using this. Take current, for example:
$$\huge \frac{1}{2}I_0=I_0\,e^{-\frac{T_{\frac{1}{2}}}{\tau}},\,\,\,\frac{1}{2}=e^{-\frac{T_{\frac{1}{2}}}{\tau}}$$
$$\Large ln\left(\frac{1}{2}\right)=-\frac{T_{\frac{1}{2}}}{\tau},\,\,\,T_{\frac{1}{2}}=-\tau\left(ln1-ln2\right)=\tau\,ln(2)$$
$$\Huge T_{\frac{1}{2}}=RC\times ln(2)$$


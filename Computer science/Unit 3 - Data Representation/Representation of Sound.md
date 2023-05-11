
Real world data is analouge - it is a continuous signal. Digital signals are discrete, so digital signals can only approximate real world analouge data. A device that converts an analouge signal into a digital signal is called an ADC (Analouge to Digital Converter), whereas a device that does the opposite is called a DAC (Digital to Analouge Converter).

## ADC / DAC:

Analouge sound samples are recorded through an amplifer before reaching an ADC. At the ADC, sound samples of a wave are recorded and quantised to measure its wave height (amplitude) and translate this into an integer value that can be recorded.

Digital sound samples are converted into analouge data (sound) through a speaker. The digital signal causes the speaker diaphgramn to move in order to move air particles in a way that they represent the original analouge data.

## Sampling:

To convert from Analouge to Digital, the analouge source has to be sampled at regular periods. The amplitude of the source is measured at regular intervals, which can then take many values. The amount of times a signal is sampled per second is called the sampling rate, and the amount of values it can take is called the bit depth or resolution.

Higher bit depth and higher sampling rate both determine the quality of the conversion. This results in a more faithful recreation of the analouge source, however takes up more space in memory.
$$\Large File\,Size=Sample\,rate\times Resolution\times Length\,\,of\,recording$$

There is a limit on the lowest sampling rate that can be used or an accurate recording, as sound is made of many components at many different frequencies and amplitudes. Therefore, Nyquists Theorem dictates that the lowest sampling rate, $f_s$, must be at least twice that of the highest frequency present in the recording:
$$\Huge f_s\gt2f_{max}$$
This is so even at the highest frequency, the full amplitude of a wave can be captured at sampling:
![[Nyquist's theorem.png]]

## Midi:

Midi, Musical Instrument Digital Interface, creates sound as requested using software. Using the Midi system, only "events" need to be transmitted, not entire sound bites. It is up to the Midi software to synthesise the sound once it recieves an event. As the sounds are synthesised, the sound may be less realistic - however can have much higher quality as no data about musical notes is lost.
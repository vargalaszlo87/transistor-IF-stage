# 🚀 transistor-IF-stage

These are two versions of IF-stage for a transistor radio (in my **FLEX-radio project :)**). The two circuits contain TOKO band IF transformers. (Why TOKO? This is a well-know brand in the world of radio, many radio receivers worldwide contain TOKO coils. I also found it in an old pocket radio! ❤️)

So, the IF (intermediate frequency) transformer provides the selectivity of this stage in this case. This is a proven solution in radio world, therefore we examine it. I make two versions of this method (only the input side is different), let's see!

## First "traditional" circuit

Why did i say "that is a traditional circuit"? Easy, many radio receiver contains very similar circuit.

- The input side of this circuit is the output of the transformer of previous stage (therefore we not need use a coupling capacitor).
- The output side is a galvanically isolated output for next stage.

If we take a closer look, this is a common-emitter amplifier circuit with a [swamping resistor](https://eng.libretexts.org/Bookshelves/Electrical_Engineering/Electronics/Semiconductor_Devices_-_Theory_and_Application_(Fiore)/07%3A_BJT_Small_Signal_Amplifiers/7.3%3A_Common_Emitter_Amplifier) for emitter and an active work resistance (LC).

The gain of this amlpifier can be adjusted between ~4 and ~13dB using an 2.2k potentiometer (The R4 provides the lower range of the amplifier and the R3 is the swamping resistor). The bypass capacitor in the emitter network helps stabilize DC Q-point and increase the AC-gain.  The network of R1 and R2 is the voltage divider for biasing. C3 capacitor provides negative feedback to the circuit. 

<img width="818" height="768" alt="image" src="https://github.com/user-attachments/assets/6dae7ce2-436a-4560-aa33-7ac8c9d8228a" />

## Second version

In this case, the signal reaches the base of the transistor through the coupling capacitor C4. This is a general type of an amplifiers input. Warning! Each capacitor (coupler, decoupler, bypass, feedback etc.) can be modified the frequency response of amplifier, therefore our goal is to use fewer capacitor if possible. 

The other parts are same as the previous version.

<img width="1219" height="889" alt="image" src="https://github.com/user-attachments/assets/22e32c0f-736a-4567-95d9-85379dfc822a" />

# 🖖 Let's see it in practice!

**Important!** Usually several IF stage must be used in succession. Why? High gain and good selectivity are not a simple mission in RF world. If you've ever seen a pocket radio from the inside, you know the PCB containst more IF transformer. Amplification and filtering of all stages are smaller and less efficient, but together is well! (two amplifiers in series are **gain 1** x **gain**)

Some of the components in the breadboard example are different than in my LTSpice files. 

So what are the differents?

- The parameters of the yellow TOKO coil: tow primers are 257u and 101u and the secunder is 1u
- The pair in voltage divider are 47k and 4,7k
- In emitter network: 1k potentiometer, 9.1ohm swamping resistor and 180ohm emitter resistor.

![transistor-IF-stage-capacitor-coupling-breadboard-01](https://github.com/user-attachments/assets/38157f20-46ee-4593-923a-6987cd377d34)


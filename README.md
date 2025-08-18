# 🚀 transistor-IF-stage

These are two versions of IF-stage for a transistor radio (in my **FLEX-radio project :)**). The two circuits contain TOKO band IF transformers. (Why TOKO? This is a well-know brand in the world of radio, many radio receivers worldwide contain TOKO coils. I also found it in an old pocket radio! ❤️)

So, the IF (intermediate frequency) transformer provides the selectivity of this stage in this case. This is a proven solution in radio world, therefore we examine it. I make two versions of this method (only the input side is different), let's see!

## First "traditional" circuit

Why did i say "that is a traditional circuit"? Easy, many radio receiver contains very similar circuit.

- The input side of this circuit is the output of the transformer of previous stage (therefore we not need use a coupling capacitor).
- The output side is a galvanically isolated output for next stage.

If we take a closer look, this is a common-emitter circuit with a [swamping resistor](https://eng.libretexts.org/Bookshelves/Electrical_Engineering/Electronics/Semiconductor_Devices_-_Theory_and_Application_(Fiore)/07%3A_BJT_Small_Signal_Amplifiers/7.3%3A_Common_Emitter_Amplifier) for emitter and an active work resistance (LC).

The gain of this amlpifier can be adjusted between ~4 and ~13dB using an 2.2k potentiometer.


<img width="818" height="768" alt="image" src="https://github.com/user-attachments/assets/6dae7ce2-436a-4560-aa33-7ac8c9d8228a" />


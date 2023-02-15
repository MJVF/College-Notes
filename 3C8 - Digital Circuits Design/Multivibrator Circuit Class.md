---
tags: 
- Astable
---

### Glossary:
- [[#Multivibrator Description]]
- [[#Astable]]
- [[#Monostable]]
- [[#Bistable]]
---
# Multivibrator Description

> #Astable : in which the circuit is not stable in either state - it continually switches from one state to the other. e.g: _clock circuit._
>
> #Monostable : in which one of the states is stable, but the other state is unstable (transient). A _trigger pulse_ causes the circuit to enter the _unstable state_. After entering the _unstable state_, the circuit will return to the stable state after a set time. Such a circuit is useful for creating a _timing period of fixed duration_ in response to some external event.
>
> #Bistable : in which the circuit is stable in either state. It can be flipped from one state to the other by an _external trigger pulse_. This circuit is also known as a #Flip_Flop . It can store one bit of information, and is widely used in _digital logic and memory_.

---

# Astable 

> - Electronic equivelant of a _pendulum/metronome_
> - Typically used to _implement clock circuits.__
> - Want _all latches/flip-flops_ in a circuit to update or change at the _same time_.
>
>![[Pasted image 20230213225406.png|300]]
>
> - (a) never really used in industry, latches are bad. Career ending?!?!?!
> 	- most commonly falling/rising (positive/negative) edge triggered multivibrators.
> - Edge triggered flip flop only activates at one specific instance.

__Discrete time__ relies on _sampling at the same time_, therefore using a _latch_ you _do not know_ what you are _sampling_. 

&nbsp;

# Monostable

 > #CD4538 is a dual, precision monostable multivibrator with independant trigger and reset controls.
 > Generates a pulse whos duration can be set in response to an external pulse.
 > $\,$
 > ![[Pasted image 20230213225856.png|550]]
 >
> - B input is usually inverted.
> - T2 = toggle signal within the chip, two reference voltages inside, set by resistor and capacitor.
> - Cd achieves pulse shortening.

&nbsp;


- Output pulse width is a function of the profuct of R & C
> insert image 3/3




---

# Bistable

jk flip flop 1 and 2

- feeding output of first JK flip flop into the second, and it generates a counter

d type flip flop 1 and 2

- We will present simplified d-type flip flop functionality as it has been derived & covered in greater detail in 3C7


 - __Timing Constraints to ensure correct operation:__
	 - <u> _Setup time:_</u>
			 - Minimum time for which D input must be maintained at constant value prior to transition of the clock.
	- <u>_Hold time:_</u>
		- Minimum time for which the D input must not change after the clock transition.
	- <u>_Clock-to-q delay:_</u>
		- time to propogate calue of D at rising/falling edge of clock.
		- it is not anticipated these will cause you any challenges in the project.




> insert image bistable multivibrator d-type flip flop 3/3




note, check if chip is asyncronous or syncronous reset.
- asyncronous goes to known state on reset
- syncronous goes to known state on next clock cycle
- 
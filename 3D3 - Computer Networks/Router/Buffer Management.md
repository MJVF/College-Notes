
```ad-note
- Average buffering equal to "typical" #RTT (say 250ms) times link capacity C
	- e.g. C = 10Gbps link: 2.5 Gbit buffer
- More recently $\frac{RTT \times C}{\sqrt{ N } }$
```
- Too much __buffering increases delays__ : long RTTs: poor performance for realtime apps, sluggish TCP response.

- Recall #Delay-Based_Congestion_Control: " Keep bottleneck link just full enough (busy) but no fuller"

- Drop: #Tail_Drop, #Priority_Drop

- Marking: #ECN, #RED

```ad-note
- __Transfer packet__ form input link to appropriate output link.
- __Switching rate__: rate at which pckets can be transfred from the inputs to outputs.
```


- _Memory, Bus, Interconnection network_.
- Multistage switch, exploiting #Parallellism (fragment into cells, multiple parallel switching planes)
$\,$
- __Input port queueing__ - Head of line blocking
- __Output port queueing__ - Buffering (Datagrams arrive from fabric faster than link transmission rate). _Drop Policy_? _Scheduling discipline_.
$\,$
- Datagrams lost due to congestion, lack of capacity, buffers; --prioirity scheduling - who gets best performance, net neutrality.
# DataJoint Element for BEADL
At this point, this repo simply designs a DataJoint schema for BEADL data -- disconnected from a complete pipeline. 
It reproduces the [NWB Extension Demo](https://github.com/rly/ndx-beadl).

[BEADL](https://beadl.org/) is a behavior task description language developed in the [Kepecs Lab](https://sites.wustl.edu/kepecslab/).
It specifies event-based behavior experiments in the form of state machines. 
It comes with a neat [online design and visualization tool](https://www.beta.beadl.org) -- currently in a closed beta.

## Definitions

A behavior experiment session comprises a sequence of *trials* with a sequence of *states*. 
Transitions between states are triggered by *actions* (what the hardware does) or *events* (what the animal does). 
Note: this naming is formed from the perspective of the state machine driving the experiment and may seem reversed from the animal's perspective.

These states and their transitions are specified by the state machine and are interpreted by the experiment hardware such as [BPod](https://www.sanworks.io/shop/products.php?productFamily=bpod).

The acquisition system records the trials including their states, actions, and events with their timestamps. 

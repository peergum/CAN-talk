# CAN-talk
A library for microcontrollers that allows decent comms over a CAN bus

## PURPOSE

This library (work-in-progress) should allow you to implement some communications between microcontrollers over a CAN bus. It will tentatively implement two different roles, that should be selected at compilation time:
- Master: a main controller over the bus, that communicates with slaves
- Slave: a device that is controlled by the Master over the bus

The point is NOT to allow communications with existing CAN bus devices, although it might be possible if they implement ISO-TP themselves (no guarantees at this point), but rather to set your own system that will use the CAN bus without negative interferences with other devices present on the bus.

## WARNING/DISCLAIMER

There's no guarantee that heavy communications between your devices couldn't cause issues to the whole CAN bus ecosystem, so just be wise in your implementation. Ideally, your project would use its own dedicated CAN bus if requiring heavy exchanges between your devices, like firmware updates or data transfers in general (we're talking about hundreds of KB here, possibly less at slow speeds, or more generally communications that would span over seconds rather than milliseconds). Think of it this way: you don't want your devices to add seconds to the response of a break pedal push.

## AUTHOR

CAN-talk by [Phil "PeerGum" Hilger](mailto:phil@peergum.com)

[Isotp-C original library](https://github.com/Zosoworld/isotp-c) by Shen Li, Simon Cahill & others

## LICENSE

This library is distributed under [GPLv3 License](/LICENSE).

Copyright (c) 2023, PeerGum.
Some parts Copyright (c) 2019 Shen Li, Simon Cahill & Co-Operators

Please be aware __you can't distribute any work using this library without publishing the whole source code of your work__. If you plan to patent some device using this code, you'll have to share its source code to be able to do that, otherwise your patent can not be invalidated. That's how free developers get some recognition, and get payback for their hard work. There's no free lunch.
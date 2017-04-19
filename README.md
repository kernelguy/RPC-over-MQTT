# RPC-over-MQTT
Generic description of a way to implement RPC over MQTT.

This document is a suggestion on one method to implement an RPC interface, using MQTT as the transport layer.

Why MQTT?
For many years I have been developing various Json-RPC implementations in different languages, mostly using HTTP(S) as transport, but also Websockets. This works fine, but the HTTP has some overhead on short lived requests, and since many of my projects are for embedded systems on low end hardware using GPRS modems, I always try to optimize/reduce my communication overhead.
It is often a tradeoff between functionality and maintainability.

MQTT has a much lower overhead, but is designed as a publish/subscribe protocol, without any specifications regarding Remote Procedure Calls.



Servers are like systems. This naming is due to its need to handle different clients, such as nodes that need rendering, audio playing, etc. 

One of the design pattern which we will use for these servers is the singleton. This is necessary to allow the [[Scene Tree]] to interact with the systems.

The main goal of using servers is to decouple the libraries we are using from the engine's code. This is essential to increase the engine's overall friendliness to designers and developers.
## What servers do we need?
- Rendering
- Audio
- Input
- Assets
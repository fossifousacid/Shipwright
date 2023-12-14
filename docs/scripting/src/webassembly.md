#WebAssembly
One of the potential approaches to the scripting engine is to embed a webassembly runtime in Ship of Harkinian.

##Interface

###WebAssembly Interface Types (WIT)

One of the benefits of using web assembly is that it allows for the use of WebAssembly Interface Types. This is an interface description language that is designed to model APIs and ABIs across the VM. It operates under the expectation that the modules are all running on the same machine.

The WIT language has associated tools to allow for automatic generation of APIs in supported languages. Unfortunately, the target languages are somewhat limited at the moment.

##Security

##Performance

##WebAssembly Micro Runtime (WAMR)

One of the potential issues with using webassembly is that it cannot modify the host's memory structures. This means that we will need to provide an API for modifying complex data structures if serialization across the API boundary is too expensive.

With all that said, pointers in the other direction can work. The host can access data structures held by the guest. This means that it could be possible for mods to send pointers to their internal memory for large data structures. Probably not worth dealing with this, but it's food for thought.




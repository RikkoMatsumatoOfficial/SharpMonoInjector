# SharpMonoInjector by RikkoMatsumatoOfficial(FORK)

**I'm Updated this version of SharpMonoInjector for mono-2.0-bdwgc library(THIS LIBRARY IS FULLY FREE WITH OPEN SOURCE CODE)!!! So Enjoy to use this!!!**

SharpMonoInjector is a tool for injecting assemblies into Mono embedded applications, commonly Unity Engine based games. The target process *usually* does not have to be restarted in order to inject an updated version of the assembly. Your unload method must to destroy all of its resources (such as game objects).

SharpMonoInjector works by dynamically generating machine code, writing it to the target process and executing it using CreateRemoteThread. The code calls functions in the mono embedded API. The return value is obtained with ReadProcessMemory.

Both x86 and x64 processes are supported.

In order for the injector to work, the load/unload methods need to match the following method signature:

    ``` csharp
    namespace Example
    {
        public class ClassPub
        {
            public void Load(){
                // Create You're MonoBehaviour Class Cheat with Functions!!!
            }
            public void Unload(){
                // Unload or Release You're Cheat!!!
            }
        }
    }
    ```
    _**P.S: Before Use, You Need Remember Names of Namespace, class and void function!!!**_

[Examples](https://github.com/RikkoMatsumatoOfficial/SharpMonoInjectorExamples)

[Join To My Discord Server](https://discord.gg/U2P5Hrcq9C)

## Donations

[DonationAlerts](https://donationalerts.com/r/rikkomatsumato)

> **_Monero Wallet:_** 
> monero:49SVX8xZ3TCAqKDqW4Ybt1FPTZuMF4SVf2XQWamHZVYddk6pViYJbgrY911RJ6CgFm14vQUuH8Zv5Qouxb6U3YMG1jHQsRq?recipient_name=RikkoMatsumato

[Ko-Fi](https://ko-fi.com/rikkomatsumato)

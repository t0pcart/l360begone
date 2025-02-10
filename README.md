## l360killer

Bypass that disables Life360's background location refresh on iOS;prevents location from being updated 

Circle Members will not get any location updates/notifications when this bypass is used.

This bypass manipulates executable flags, _set and used by the kernel and AMFI to vaildate binaries' permissions_, allowing us to mark the Life360 app binary as non-executable

Binaries marked with a non-executable flag will be rejected by AMFI and the kernel will refuse to run those binaries. By preventing the execution of any Life360 binary/library, background location updates are defeated

# Bypass Types

The automatic bypass method requires a proper bootstrap/terminal to be executed. Installing those can be done via a jailbreak [(Dopamine)](https://github.com/opa334/Dopamine), or using an app installed via a CoreTrust bypass [(Bootstrap)](https://github.com/RootHide/Bootstrap).

The manual bypass method works using any kernel r/w exploit that allows you to manipulate userspace's processes' page flags

**Automatic Bypass**

- Download the "enable" and "disable" executables
- Use chmod +x as root to give the executables proper permissions
- Run disable to disable background location updating
- Run enable to re-enable background location updating
- _The automatic bypass persists after reboots_

**Manual Bypass**
- Use a kernel r/w exploit to obtain userspace memory page read/write privileges
- Manipulate Life360's binary's executable flag(in memory) to mark it non-executable(disabling)
- Manipulate Life360's binary's executable flag(in memory) to mark it executable(enabling)
-  _The manual bypass can persist after reboots_


  


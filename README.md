## l360killer

Bypass that disables Life360's background location refresh on iOS;prevents location from being updated 

Circle Members will not get any location updates/notifications when this bypass is used.

This bypass manipulates executable flags, _set and used by the kernel and AMFI to vaildate binaries' permissions_, allowing us to mark the Life360 binary as non-executable

Binaries marked with a non-executable flag will be rejected by AMFI and the kernel will refuse to run those binaries. By preventing the execution of any Life360 binary/library, background location updates are defeated

# Bypass Types

The automatic bypass method requires a proper bootstrap/terminal to be executed. Installing those can be done via a jailbreak [(Dopamine)](https://github.com/opa334/Dopamine), or using an app installed via a CoreTrust bypass [(Bootstrap)](https://github.com/RootHide/Bootstrap).

The semi-automatic bypass method requires Filza to be installed on the iPhone with root privileges

**Automatic Bypass Method**

- Download the "enable" and "disable" executables
- Use chmod +x as root to give the executables proper permissions
- Run disable to disable background location updating
- Run enable to re-enable background location updating
- _The automatic bypass persists after reboots_


**Semi-Automatic Bypass Method**

- Open Filza
- Go to /var/containers/Bundle/Application/"YourLife360AppFolder"/Life360.app
- Find the Life360 executable(has gear icon) and click the i Button
- Go to Access Permissions and remove the executable flag from the owner, group, and others id's(disables life360)
- Add the executable permissions back(re-enables life360)
- **Note:** This does not kill the actively running Life360 binary you must kill it.
- _The semi-automatic bypass method persists after reboots_

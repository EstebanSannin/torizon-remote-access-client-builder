# torizon-remote-access-client-builder
Helper repo that should allow you to test the new Remote Access Feature provided by Torizon.


# Configuration
Attention, to push the new package containing the remote access client on the Torizon platform you need the credentials file (credentials.zip)
Before to build the project, you must configure your machine. There are available 2 basic tcbuild file one for 32 bit machines and one for the 64bit machines.
So based on your machine, open the right file anche change the machine field with the right one.
The default machine provided in the TCB configuration file are, verdin-imx8mp for 64bit machine and colibri-imx6 for 32bit.

# How to build

```
torizoncore-builder build --file tcbuild-64bit.yaml
```

# Push to the platform

```
torizoncore-builder images unpack rac-binary

torizoncore-builder platform push --credentials credentials.zip --package-name rac64-binary base
```
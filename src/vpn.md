# Connecting to the VPN

NCSSM uses the GlobalProtect VPN to allow you to connect to services on the NCSSM network
from non-eduroam networks.

Additionally, some things, like the NCSSM Github server, are only accessible this way.

You will need to use [this client](https://github.com/yuezk/GlobalProtect-openconnect) to connect to the VPN.
Scroll down to the "Installation" section for instructions for your distro.

However, the GUI is paid proprietary software, so we will need to use the command line interface.

Once you have installed the client, simply run **`sudo gpclient connect fw.ncssm.edu`** (`fw.ncssm.edu` is the portal address).
You should be prompted to login with your NCSSM Google account, and then you must leave the program running to use the VPN.

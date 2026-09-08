# Printing

The daunting task of printing at NCSSM on Linux is finally documented!

First you will of course need to install [CUPS](https://wiki.archlinux.org/title/CUPS) on your distro.

The rest of this guide will use the CUPS GUI which can be accessed from your browser at
[http://localhost:631/](http://localhost:631/).

Go to the Administration tab and click "Add Printer". Choose "Internet Printing Protocol (ipps)".

For the connection URI, enter:

`ipps://papercut.ncssm.edu:9164/printers/Copier_Queue`

*(This was the hard part to discover. It's not documented and I had to find it with a bit of brute force.)*

Fill in the human-readable details as you like, hit Continue, and select **Generic** > **IPP Everywhere ™** as the driver. Now you can add the printer!

To print something, select the `Copier_Queue` printer (or whatever you named it).
The first time you do it, you should be prompted to log in.
You might need to use the system dialog the first time or the job will hang and not prompt you.
Log in with your NCSSM credentials and you should be able to submit a print job!

Then just go to the physical printer, tab your fob, and release the job to print your document.

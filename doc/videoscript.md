RISC OS Community - WakeOnLAN
=============================

Intro
-----
Hello and welcome to the 'RISC OHH ESS' Community.

This video demonstrates the usage of the WakeOnLAN application which allows you to use a RISC OHH ESS machine to remotely start a Wake-on-LAN compatible computer.

Broadcast address
-----------------
One of the first things we need to know is the network broadcast address.

Open a Task Window and then type `ifconfig -a` to display the network information for all interfaces attached to this machine.

Here we are interested in `ej0`. The broadcast address is as highlighted - `192.168.1.255`. We need to remember this for later.

The MAC address is also shown under `ether`. It will be necessary to use a similar command on the machine that you wish to wake to determine it's MAC address.

WIMP Application
----------------
Now let us demonstrate using the WIMP application to remotely start another computer.

Clicking on the iconbar icon opens the main application window.

In the top writeable icon, labelled `Target MAC Addr`, enter the MAC address of the remote device. This will need to have been determined on the remote machine using a similar method as used earlier for the broadcast address.

Then, in the lower writeable icon, labelled `IP Broadcast Addr`, enter the broadcast address we determined earlier.

We are now showing the video output of the remote device.

Clicking the `Run` button sends the Wake-on-LAN network packet to the target device and we see the command output in the log window.

As you can see, the target device is going through its usual boot procedure. For the purposes of this demonstration, this footage has been sped up.

CLI
---
Now let us demonstrate using the command line to perform the same task.

Like most RISC OHH ESS utilities, this assumes that WakeOnLAN has already been 'seen' by the Filer.

Open a Task Window and then type the following:

wakeonlan space dash em space, followed by the MAC address of the remote device (which is not case sensitive), then another space followed by dash b space and our broadcast address - in this case `192.168.1.255`

As before, we are showing the video output of the remote device.

Press Enter and the Wake-on-LAN packet is sent.

Again, the target device is going through its usual sped up boot procedure.

You will notice that this command did not provide any output, which can be useful when using this command in an Obey file.

CLI (verbose)
-------------
We will again demonstrate using the command line, but this time include the output of the command.

As before, open a Task Window and type:

wakeonlan space dash em space, followed by the MAC address of the remote device, then another space followed by dash b space and our broadcast address and this time add a space dash vee, for verbose, to the end of the command.

Press Enter and the Wake-on-LAN packet is sent. However this time, we see the output from the wakeonlan command.

Outro
-----
In this video we have shown several ways to use the WakeOnLAN application to remotely start compatible machines from your RISC OHH ESS computer.

Thanks for watching.

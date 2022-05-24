## First Time Setup using the Command Line {#first-time-setup-command-line}

<!--  TODO: edit this a intro a little to make it smoother -->

Follow along with this guide to set up your Omega2 for the first time using the command line.

***Follow this guide only if the Setup Wizard was not able to get your Omega2 up and running. If the Setup Wizard succeeded, you don't have to go through these steps!***

 We'll be doing the following:

1. Connecting your Omega to a Dock and powering it on.
1. Connecting to its command line terminal.
1. Configuring it to join your WiFi network and then do some updates.

> If you experience issues at any point in the process, try checking our [Troubleshooting guide](#first-time-troubleshooting).

<!-- Prepare the Hardware -->
```{r child = './First-Time-Components/Hardware-Prep.md'}
```


<!-- Command Line Setup -->
### Preparing to Connect {#first-time-setup-command-line-steps}

<!-- Computer Config -->
```{r child = './First-Time-Components/First-Time-Component-01-computer-config.md'}
```

<!-- The Omega's Name -->
```{r child = './First-Time-Components/First-Time-Component-02-omega-name.md'}
```

<!-- Connect to Omega's Wifi AP -->
```{r child = './First-Time-Components/First-Time-Component-03-connect-to-omega-network.md'}
```

### Connect to the Omega's Command Line

We'll use SSH to connect to the Omega's command line.

To learn how to connect to the Omega's terminal you can read our [guide to connecting to the Omega with SSH](#connecting-to-the-omega-terminal-ssh).

> It's also possible to access the Omega's command line via serial. Learn more by reading [this guide](#connecting-to-the-omega-terminal-serial). Note that you may need to install some drivers for your computer to detect USB-to-Serial devices.

#### Provision the Omega's WiFi

Now let's connect the Omega to your WiFi network to give it Internet access. We'll use the `wifisetup` command to help us.

Enter `wifisetup` in a terminal and you'll see the following output:

<!-- wifisetup option 1 output -->
```{r child = './Using-the-Command-Line/Connecting-to-WiFi-Networks-Component-1-wifisetup-option-1.md'}
```

> For more on the Omega's wireless capabilities, see [our guide to the Omega and Wireless](#the-omega-and-wireless-connectivity).
>
>To learn more about configuring the Omega's WiFi connection, see [our guide to using the command line to connect to WiFi](#connecting-to-wifi-networks-command-line).


### Update the Omega's Firmware

Now that we've just connected your Omega to the internet, let's update the Omega's firmware to the latest version released by Onion.

Enter the `oupgrade` command in the terminal to download and install the latest version of the Omega's Operating System. The update will take up to five minutes, sometimes more depending on your Internet connection.

**Warning: Do not disconnect the Omega from WiFi or power during this process or the firmware may become corrupted!**

At the end of the installation process, the Omega will automatically reboot. It will be ready for use when the Omega's LED stops flashing and remains solid.

> Some Omega2+ models may not reboot automatically. If your Omega2+'s LED turns off and remains off for longer than about 15 seconds, you will need to manually reboot your Omega. <br>
> Either toggle the power switch on your Dock or disconnect the power briefly and reconnect it, and your Omega2+ will reboot and complete the upgrade. It will be ready for use when the LED stops flashing and remains solid.
> After upgrading firmware, you will need to reconnect your Omega to WiFi by running `wifisetup` again.


**Now you're all done!**

Start using your fresh Omega and check out the [Using the Omega section](#doing stuff) for ideas on what the Omega can do!
<!-- Start using your fresh Omega, check out the [Tutorials section](./Tutorials/Contents) or the [Project guides](./Projects/Contents) for ideas on what to do next! -->
<!-- TODO: fix the links above when the content is available -->


### Installing the Console

Now that your Omega is all setup and ready to go, you'll want to install the Console so you can get the most from your Omega. Run the following commands:

```
uci set onion.console.setup=1
uci set onion.console.install=2
uci commit onion
```

On the Omega's next reboot, the Console will be installed automatically. Check out our series on [Using the Console](#accessing-the-console) for more on how to use the Console.


### This Didn't Work!

Try checking our [Troubleshooting guide](#first-time-troubleshooting) or posting on the [Onion Community](http://community.onion.io).

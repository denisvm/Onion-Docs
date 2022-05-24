##  First Time Setup {#first-time-setup}

Follow along with this guide to set up your Omega2 for the first time. We'll first learn how to properly connect your Omega to a Dock and power it up. Then we'll connect to it to use the Setup Wizard to have it connect to your WiFi network and then do some updates.

> If you experience issues at any point in the process, try checking our [Troubleshooting guide](#first-time-troubleshooting).


<!-- Second sentence above is awkward -->

### The Video

Follow along with our getting started video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/3DMkQjQtoEE" frameborder="0" allowfullscreen></iframe>

It covers all of the steps that are listed below!



<!-- Prepare the Hardware -->
```{r child = './First-Time-Components/Hardware-Prep.md'}
```

<!-- GUI SETUP -->

### Using the Setup Wizard {#first-time-setup-wizard}

<!-- Computer Config -->
```{r child = './First-Time-Components/First-Time-Component-01-computer-config.md'}
```

<!-- The Omega's Name -->
```{r child = './First-Time-Components/First-Time-Component-02-omega-name.md'}
```

<!-- Connect to Omega's Wifi AP -->
```{r child = './First-Time-Components/First-Time-Component-03-connect-to-omega-network.md'}
```

**The Setup Wizard**

Open your favourite browser and navigate to `http://omega-ABCD.local/` where `ABCD` are the same characters from the network name above. If the page doesn't load, you can also browse to `http://192.168.3.1`

You have now arrived at the Setup Wizard:

![Browse to Setup Wizard](https://raw.githubusercontent.com/OnionIoT/Onion-Docs/master/Omega2/Documentation/Get-Started/img/setup-2-wizard-start.png "Browse to Setup Wizard")

Login with the Omega's default credentials:
```
username: root
password: onioneer
```

![Setup Wizard Login](https://raw.githubusercontent.com/OnionIoT/Onion-Docs/master/Omega2/Documentation/Get-Started/img/setup-3-wizard-login.png "Browse to Setup Wizard")

After you've logged in you'll be asked to connect to a Wireless Network. This is **MANDATORY** in order to complete the Setup Wizard.

![Setup Wizard wifi configure](https://raw.githubusercontent.com/OnionIoT/Onion-Docs/master/Omega2/Documentation/Get-Started/img/setup-4-wizard-wifi-configure.png)

Enter your Wireless Network information and click Configure. Your Omega will attempt to connect to the network. This can take up to a minute to complete.

> The Omega's AP will go down and not be accessible during this process, sit tight, it'll come back up when the configuration is done!

Once connected, you will be moved to the next step.

![Setup Wizard configuring](https://raw.githubusercontent.com/OnionIoT/Onion-Docs/master/Omega2/Documentation/Get-Started/img/setup-5-wizard-wifi-configuring.png)

On this step you can choose to register your device on the cloud. If you would like to do this some other time you can click `Skip Step` to move onto the next step.

![Setup Wizard cloud](https://raw.githubusercontent.com/OnionIoT/Onion-Docs/master/Omega2/Documentation/Get-Started/img/setup-6-wizard-cloud.png)

You've nearly finished now. Click the `Upgrade Firmware and Install Console` button to do just that. This will upgrade your Omega to the latest firmware and install the Console for you.

>If you don't want to install the Console you can de-select the checkbox above. You can always come back to the setup wizard to install the console afterwards.

![Setup Wizard downloading firmware](https://raw.githubusercontent.com/OnionIoT/Onion-Docs/master/Omega2/Documentation/Get-Started/img/setup-7-wizard-upgrade-button.png)

Your Omega will download the latest firmware, and then begin installing it. This process takes several minutes, sometimes more depending on your Internet connection.

![Setup Wizard installing firmware](https://raw.githubusercontent.com/OnionIoT/Onion-Docs/master/Omega2/Documentation/Get-Started/img/setup-8-wizard-installing-firmware.png)

When the firmware installation is complete you'll see the page below:

![Setup Wizard finished](https://raw.githubusercontent.com/OnionIoT/Onion-Docs/master/Omega2/Documentation/Get-Started/img/setup-9-wizard-finished.png)

At the end of the installation process, the Omega will automatically reboot. It will be ready for use when the Omega's LED stops flashing and remains solid.

> Some Omega2+ models may not reboot automatically. If you reach the page pictured above and your Omega2+'s LED turns off and remains off for longer than about 15 seconds, you will need to manually reboot your Omega. <br>
> Either toggle the power switch on your Dock or disconnect the power briefly and reconnect it, and your Omega2+ will reboot and complete the upgrade. It will be ready for use when the LED stops flashing and remains solid.


**All Done!**

Start using your fresh Omega, check out the [Using the Omega section](#doing-stuff) for ideas on what the Omega can do!
<!-- Start using your fresh Omega, check out the [Tutorials section](./Tutorials/Contents) or the [Project guides](./Projects/Contents) for ideas on what to do next! -->
<!-- TODO: fix the links above when the content is available -->

### The Setup Wizard Didn't Work!

If for some reason the Setup Wizard wasn't able to get your Omega up and running, try the steps in the [First Time Setup using the Command Line guide](#first-time-setup-command-line) or see the  [Troubleshooting guide](#first-time-troubleshooting).

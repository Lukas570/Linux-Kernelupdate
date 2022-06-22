# Added KernelupdateEasy
If you don't want to adjust the Kernel-Settings or just do a quick Kernelupdate without lots of (complicated) prompts just execute the Easy script.

If you are an advanced user I would recommend using the normal script ;)

# Kernelupdate
Script to install the latest Kernel from Kernel.org

Easy to use and foolproof way to update your Linux-Kernel!

Added PGP-Verification process!

You can compile the Kernel now with a custom config-file (Advanced Mode)

If you have an older version of the script without the PGP-verification process it's highly advised to upgrade to the newest version!

# How to use:

In the Terminal of your choice type in the following two commands to execute it!

chmod +x Kernelupdate // changes permission to make it executable on your machine

chmod +x KernelupdaetEasy // makes the easy script executable

./Kernelupdate  // Executes the file

./KernelupdateEasy //Executes the easy script

After execution and reboot check your kernel with "uname -a"

# For NVIDIA-Users
You won't be able to boot properly after installing the new Kernel. This is because your current Nvidia-Driver was compiled with the old kernel and its not loaded with the new Kernel.

If you still want to upgrade your kernel it's not a major problem, I am an NVIDIA-User by myself (unfortunately).

You have to download the newest NVIDIA-Driver for your system on their official website https://www.nvidia.de/Download/index.aspx After that you have to boot in the so called "Runlevel 3" to achieve that you have to press e in your Grub-Menu in order to see the boot parameters for your Kernel. Assuming you have never ever played with these settings (if you did you probably know what you are doing!) you have to find the line with "linux = "... quiet" and after quiet enter a 3 "linux = "... quiet 3".

No worry this is temporarily and only puts your machine in Runlevel 3 in this session. In runlevel 3 almost no drivers will be loaded so you have no internet connection and no graphics driver being loaded. 

Now find your previously downloaded file NVIDIA....run and perform a chmod +x on it. Execute it afterwards with "sudo ./NVIDIA....run 

If everything worked just reboot after the installation and everything should work as before.

In case the NVIDIA-Driver cant compile and interrupts with error messages remember the missing packages and boot in runlevel 2 it works just the same as with 3 just replace the 3 with a 2 after "... quiet 2" as a boot parameter!


# Coming Soon

🟢 Verifying the downloaded Kernel with PGP (thanks to Konstantin from Linuxfoundation for the suggestion)

Fixing the Ubuntu compiling problem.

🟢 Allow users to make custom settings in the Config-File and before the Kernel compilation starts (Advanced Mode)

Benchmarking feature

# Further information 

I tested the Script on multiple Debian-based Distros (Debian, Kali etc...).
If you are using Ubuntu please tell me if the script worked for you or not. I wasn't able to compile the Kernel completely on Ubuntu-Studio it failed after a while.
If you have a fix for it or maybe have suggestions how to extend this script even further let me know!

If you want to distribute my script please give me credit!

Cheers

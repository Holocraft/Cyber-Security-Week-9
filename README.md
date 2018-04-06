# Cyber-Security-Week-9

I deployed the suggested honeypots from the assignment which were the gcloud **mhn-admin** and **mhn-honeypot1**.

I came across a number of issues when trying to install the gcloud CLI.

After following the instructions on the assignment, my terminal still wouldn't recognize the "gcloud" command. I did some research and after some time found out that the gcloud CLI isn't compatible with [oh my zsh](http://ohmyz.sh/). I uninstalled oh-my-zsh and was finally able to use the gcloud command.

After installing the gcloud VM's it was pretty straight-forward from there. I was able to set up the two honeypot instances, but only the **mhn-admin** instance would load the MHN user interface via the external IP. The **mhn-honeypot1** instance was unable to connect to the external IP for some reason.

I checked all of the setup steps and compared the config from both honeypots and they were exactly the same. I'm not sure why the second honeypot was unable to show the UI.

I also had some trouble with exporting the **session.json** file to my local machine. I used the command referenced in the assignment but it kept giving me a _permission denied_ error. It turns out that I had to use the _glcoud auth login_ command before I could secure copy the file from the VM to my local.

I let the honeypot run for 2 days and received 56 attacks. I didn't get any malware samples.

![](https://raw.githubusercontent.com/Holocraft/Cyber-Security-Week-9/master/honeypot-attacks.png)

Combi Headset Mic Issue
Add to /etc/modprobe.d/alsa-base.conf and reboot
options snd-hda-intel position fix=1
options snd-hda-intel index=0 model=dell-headset-multi,dell-e7x

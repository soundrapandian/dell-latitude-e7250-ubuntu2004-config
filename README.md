Combi Headset Mic Issue
-----------------------
Add to /etc/modprobe.d/alsa-base.conf and reboot
```
options snd-hda-intel position fix=1
options snd-hda-intel index=0 model=dell-headset-multi,dell-e7x
```
  
Bluetooth HFP Issue
-------------------
- Refer: https://askubuntu.com/questions/831331/failed-to-change-profile-to-headset-head-unit
- Install ofono and blueman
- ofono-phonesim (add-apt-repository ppa:smoser/bluetooth)
- Configure /etc/pulse/default.pa
- Configure /etc/dbus-1/system.d/ofono.conf
- Configure /etc/ofono/phonesim.conf
- usermod -aG bluetooth pulse
- Clone git://git.kernel.org/pub/scm/network/ofono/ofono.git to /usr/share/ofono
- Copy bluetooth/etc/init.d/ofono-bt-hfp from this repo to /etc/init.d/ofono-bt-hfp and make it executable
- Add service `systemctl enable ofono-bt-hfp`

Bluetooth HFP Mic Low Volume Issue
----------------------------------
Working on...

For Troubleshooting2(LinuxMacEdish) you will need either a monitor and keyboard, or to set up a internet connection to ssh into the Pi and wirelessly ssh that way first to access the Pi terminal to input commands. LaterI may get around for a way to just copy/paste made files.
You can do this either during initial flashing of the Pi OS in Pi OS flasher program or:
1. Make file called wpa_supplicant.conf
2. in the contents put:
country=us (can change this to a 2 letter code for your country of choice)
update_config=1
ctrl_interface=/var/run/wpa_supplicant

network={
 scan_ssid=1
 ssid="MyNetworkSSID"
 psk="Pa55w0rd1234"
}

For SSH:
Again, enable in flasher program settings or just add a empty (no contents) file "SSH" or "ssh" with no extension (no .txt or smth) and put into bootfs.

After you can delete the wpa_supplicant.conf if you want as you will be able to ssh if you followed steps in other files

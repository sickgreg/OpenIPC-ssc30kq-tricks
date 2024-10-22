# OpenIPC-ssc30kq-tricks

Thanks to tipoman9's plugin we can fly ssc30kq @ 120fps with decent bit-rates


Consider backing up any old files brefore replacing them...

1. Put `rc.local` and `customAE.sh` in drone `/etc` and make them executable

2. Put `sensor_imx335_mipi.ko` in `/lib/modules/4.9.84/sigmastar` (this is an older sensor driver)

3a. Put `sigmastar.so` in `/etc/lib` (This is tipo's majestic plugin)
   
  3b In `/etc/majestic.yaml`, under system, add `  plugins: true`

4.  Reboot.  You will notice when customAE runs at startup, white-balance will pause and stay that color temperature...  So when you are about to fly, go outside first and then boot up the drone so the color is about right

120fps @ 1280x720 performs the best for me.  Can do 15mbps 

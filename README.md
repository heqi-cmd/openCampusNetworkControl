## openCampusNetworkControl
This is a OpenWrt application 
### NOTICE
**This package build for xiaomi ac2100**
### DOWNLOAD
[release](https://github.com/heqi-cmd/openCampusNetworkControl/releases/tag/v1.0)
### BULID FOR YOUR PLATFORM
1. build openwrt 

       git clone https://git.openwrt.org/openwrt/openwrt.git
       cd openwrt
       ./scripts/feeds update -a
       ./scripts/feeds install -a 
       ## choose your paltform
       make menuconfig
2. copy this repository to **openwrt/package**

        ## select openCampusNetworkControl 
        make menuconfig
        ## -> example -> [*]openCampusNetworkControl then save and exit
3. compile openCampusNetworkControl
        
        ## modify Makefile SOURCE_DIR to your openCampusNetworkControl file path
        make package/openCampusNetworkControl/compile V=s
4. send openCampusNetworkControl_*.ipk to you device 

        ## ipk file in thia folder
        openwrt/bin/packages/mipsel_24kc/base
5. install and use this package 

        opkg install ./openCampusNetworkControl_*.ipk
        openCampusNetworkControl -u <campusID> -p <password> -s <service> -w <url>
    * **service**: cmcc / unicom / ctcc / default / local
    * **url**: lan.*.edu.cn / wlan.*.edu.cn (no http:// or https://)


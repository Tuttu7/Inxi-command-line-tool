> Inxi displays handy information concerning system hardware (hard disk, sound cards, graphic card, network cards, CPU, RAM, and more), together with system information about drivers, Xorg, desktop environment, kernel, GCC version(s), processes, uptime, memory, and a wide array of other useful information.

> To install inxi

```
 apt-get install inxi
```

> When run without any flags, Inxi will produce output to do with system CPU, kernel, uptime, memory size, hard disk size, number of processes, client used and inxi version:
```
# inxi
CPU~Dual core Intel Core i5-4210U (-HT-MCP-) speed/max~801/2700 MHz Kernel~4.10.0-28-generic x86_64 Up~2:08 Mem~1415.2/3854.3MB HDD~1000.2GB(4.7% used) Procs~226 Client~Shell inxi~2.2.35  

```
> The command below will show sample system info (hostname, kernel info, desktop environment and disto) using the -S flag :

```
# inxi -s
Sensors:   System Temperatures: cpu: 52.0C mobo: N/A
           Fan Speeds (in rpm): cpu: N/A
```

> To print machine data-same as product details (system, product id, version, Mobo, model, BIOS etc), we can use the option -M as follows :

```
# inxi -M
Machine:   System: Dell (portable) product: Inspiron 3542 serial: C1GC712
           Mobo: Dell model: 09V1VC v: A03 serial: .C1GC712.CN7620647F005W. Bios: Dell v: A03 date: 05/27/2014
```

> We can display complete CPU information, including per CPU clock-speed and CPU max speed (if available) with the -C flag as follows :

```
# inxi -C
CPU:       Dual core Intel Core i5-4210U (-HT-MCP-) cache: 3072 KB 
           clock speeds: max: 2700 MHz 1: 900 MHz 2: 1059 MHz 3: 799 MHz 4: 799 MHz
```

> The option -G can be used to show graphics card info (card type, display server, resolution, GLX renderer and GLX version) like so

```
# inxi -G
Graphics:  Card: Intel Haswell-ULT Integrated Graphics Controller
           Display Server: X.org 1.19.6 drivers: (unloaded: fbdev,vesa)
           tty size: 134x40 Advanced Data: N/A for root 
```

> To get info about system audio/sound card, we use the -A flag :

```
#inxi -A
Audio:     Card-1 Intel 8 Series HD Audio Controller driver: snd_hda_intel Sound: ALSA v: k4.10.0-28-generic
           Card-2 Intel Haswell-ULT HD Audio Controller driver: snd_hda_intel
```

> To display network card info, we can make use of -N flag :

```
# inxi -N
Network:   Card-1: Qualcomm Atheros QCA9565 / AR9565 Wireless Network Adapter driver: ath9k
           Card-2: Realtek RTL810xE PCI Express Fast Ethernet controller driver: r8169
           Card-3: Atheros
```

> To view full hard disk information,(size, id, model) we can use the flag -D :

```
# inxi -D
Drives:    HDD Total Size: 1000.2GB (4.7% used) ID-1: /dev/sda model: ST1000LM048 size: 1000.2GB
```

> To show a summarized system information; combining all the information above, we need to use the -b flag as below :

```
# inxi -b
System:    Host: tuttu-Inspiron Kernel: 4.10.0-28-generic x86_64 (64 bit) Desktop: N/A
           Distro: Ubuntu 16.04 xenial
Machine:   System: Dell (portable) product: Inspiron 3542 serial: C1GC712
           Mobo: Dell model: 09V1VC v: A03 serial: .C1GC712.CN7620647F005W. Bios: Dell v: A03 date: 05/27/2014
CPU:       Dual core Intel Core i5-4210U (-HT-MCP-) speed/max: 802/2700 MHz
Graphics:  Card: Intel Haswell-ULT Integrated Graphics Controller
           Display Server: X.org 1.19.6 drivers: (unloaded: fbdev,vesa)
           tty size: 134x40 Advanced Data: N/A for root
Network:   Card-1: Qualcomm Atheros QCA9565 / AR9565 Wireless Network Adapter driver: ath9k
           Card-2: Realtek RTL810xE PCI Express Fast Ethernet controller driver: r8169
           Card-3: Atheros
Drives:    HDD Total Size: 1000.2GB (4.7% used)
Info:      Processes: 226 Uptime: 2:15 Memory: 1456.5/3854.3MB Client: Shell (bash) inxi: 2.2.35 
```

> The next command will enable us view complete list of hard disk partitions in relation to size, used and available space, filesystem as well as filesystem type on each partition with the -p flag :

```
# inxi -p
Partition: ID-1: / size: 913G used: 41G (5%) fs: ext4 dev: /dev/sda1
           ID-2: swap-1 size: 4.19GB used: 0.00GB (0%) fs: swap dev: /dev/sda5
```

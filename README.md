# How-to-Install-Damn-Small-Linux-DSL
## How to change keyboard language (for Spanish users)

1. Press F2 when the system start to boot
2. Type "dsl lang=es" for spanish
3. Press Enter to save
---

## Installing on SSD

1. Open the terminal
2. Type `sudo -s` and Enter and then type  `sh xsetup.sh` ``
3. Next choose Xvesa option
3. if you use a USB mouse choose `< Yes >`
4. Next, you can choose any option to change the screen resolution and your color depth to your OS.
5. Next you can skip the DPI option
6. and finally you can choose the keyboard configuration depending on your region
7. exit from the terminal
8. Now you have to right click in the desktop and go to XShells -> Root Access -> Dark
9. The program will ask you if you wish to start with a zero table, type `y`
10. Now you need 2 partitions, one to the OS and another partition for the SWAP. For create a new partition, go to [ New ]
11. Choose `[ Primary ]`
12. The Size for the 1st partition it will show the total available space in your HDD, You should substract 128mb from the total free space from your HDD, example if your HDD is 1GB (1024mb) you have to type 896mb. 
13. choose `[Beginning]`
14. and choose `[Bootable]`
15. now select the 2nd partition, for the remaining 128mb, create a new partition, go to `[ New ]`
16. Choose `[ Primary ]` and keep the default size memory (always between 120-130mb)
17. choose `[Type]` -> Enter -> Type `82` -> Enter
18. and Finally choose `[Write]`, type `yes`, and then the HDD will be White. When is finished you can exit.
19. Next, enter to the terminal again and type `fdisk -l` to check the disk
20. if all is correct type `mkswap /dev/hda2` then `swapon /dev/hda2` and Exit

21. Finally go to the Root Shell again (XShells -> Root Access -> Dark) and type `dsl-dhinstall` -> Enter -> type `hda1`
-> Enter -> type `y` -> Enter -> Type `n` -> Enter -> Type `y` -> Enter
and DSL will be install in the HDD

---

## Creating a SUDO user

DSL have a SUDO user already, but they haven't a password, to setup one go to:
1. Open the terminal
2. Type `passwd dsl`
3. Set a password
4. Confirm the password
5. Exit

---

## Instaling a WebServer

DSL already have a software called "Monkey"
1. Right click on Desktop -> System -> Daemons -> Monkey Web Server -> Monkey Start
2. type localhost in browser (Mozilla Firefox)

You can edit the index.html file, just go to:
`ramdisk/opt/monkey/htdocs` or `opt/monkey/htdocs` and edit the index.html

---

## Instaling a FTP




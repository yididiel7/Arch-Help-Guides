# List Installed Packages with Pacman on Arch Linux

## To export the above list to a file, run the following command:

pacman -Q | awk '{print $1}' > package_list.txt

## List Only the Installed Package Names

By default, the Pacman command generates all installed package lists in two columns. 
If you want to show only the first column, run the following command:

pacman -Q | awk '{print $1}'

## To list more system packages, run the following command:

pacman -Qet

## List Only the Later Installed Packages

You can also list all packages that are installed later using the Pacman command. 
To list later installed packages, use the -Qe option:

pacman -Qe

## You should see a list of later installed packages in the following output:

acpid 2.0.34-1
autoconf 2.71-1
automake 1.16.5-1
bash 5.1.016-1

## List Installed Packages Using Pacman

You can use the Pacman command with the -Q option to list all installed packages on your system.

pacman -Q

## Configure the Pacman Repository

By default, the default repository is outdated in Arch Linux, so you will need to modify the default mirror list. 
You can do it by editing the mirrorlist configuration file:

nano  /etc/pacman.d/mirrorlist

## Remove all lines and add the following lines:

## Score: 0.7, United States
Server = http://mirror.us.leaseweb.net/archlinux/$repo/os/$arch
## Score: 0.8, United States
Server = http://lug.mtu.edu/archlinux/$repo/os/$arch
Server = http://mirror.nl.leaseweb.net/archlinux/$repo/os/$arch
## Score: 0.9, United Kingdom
Server = http://mirror.bytemark.co.uk/archlinux/$repo/os/$arch
## Score: 1.5, United Kingdom
Server = http://mirrors.manchester.m247.com/arch-linux/$repo/os/$arch
Server = http://archlinux.dcc.fc.up.pt/$repo/os/$arch
## Score: 6.6, United States
Server = http://mirror.cs.pitt.edu/archlinux/$repo/os/$arch
## Score: 6.7, United States
Server = http://mirrors.acm.wpi.edu/archlinux/$repo/os/$arch
## Score: 6.8, United States
Server = http://ftp.osuosl.org/pub/archlinux/$repo/os/$arch
## Score: 7.1, India
Server = http://mirror.cse.iitk.ac.in/archlinux/$repo/os/$arch
## Score: 10.1, United States
Server = http://mirrors.xmission.com/archlinux/$repo/os/$arch

[Save and close the file]: then update all the package indexes with the following command:

pacman -Syu

## To see a list of files provided by local package, use:

pacman -Ql zhs

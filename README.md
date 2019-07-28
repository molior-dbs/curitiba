# Demo Molior Project: curitiba

This project showcases the `molior-deploy` capabilities.

The deployments are configured in `deploy/*.conf`.

## VirtualBox

Download http://molior.info/demo/curitiba_2019_0.6_vbox.ova

In VirtualBox Manager:
* Go to File, Import Appliance
* Open curitiba_2019_0.6_vbox.ova
* Check 'Reinitialize the MAC address of all network cards'
* Click Import
* Start the VM

## Docker

Download http://molior.info/demo/curitiba_2019_0.6.docker.xz

Import the docker image:
```shell
$ xz -dc | docker image load
e68994e74546: Loading layer [==================================================>]  85.58MB/85.58MB
Loaded image: curitiba:0.6
```

Run the image:
```shell
$ docker run -it curitiba:0.6 su admin
```

## LXD

Download http://molior.info/demo/curitiba_2019_0.6_lxd.tar.xz

Import the LXD image:
```shell
$ lxc image import curitiba_2019_0.6_lxd.tar.xz
Image imported with fingerprint: d3a041eac9d8b7be4966cf45b71201f8a023085c3fea68b4c9e796f26c38dcb9
```

Launch the LXD image:
```shell
$ lxc launch d3a041eac9d8
Creating the container
Container name is: useful-crab
Starting useful-crab
...
```

Run the LXD container
```shell
$ lxc exec useful-crab su admin
```

## Installer

Download http://molior.info/demo/curitiba_2019_0.6_installer.iso

Boot a VM or x86 PC from the ISO

## Info

Download http://molior.info/demo/curitiba_2019_0.6_info.zip

Extrat the deployment information:
```shell
$ mkdir curitiba-info
$ cd curitiba-info
$ unzip ../curitiba_2019_0.6_info.zip
Archive:  ../curitiba_2019_0.6_info.zip
  inflating: apt-sources.list
   creating: changelogs/
   creating: changelogs/...
  inflating: config-4.9.0-9-amd64
  inflating: curitiba_0.6_debsecan-complete_28072019-183048.txt
  inflating: curitiba_0.6_debsecan_28072019-183048.txt
  inflating: curitiba_0.6_debsums-modified.txt
  inflating: curitiba_0.6_debtree-complete.dot
  inflating: curitiba_0.6_debtree.dot
  inflating: curitiba_0.6_debtree.png
  inflating: curitiba_0.6_debtree.svg
  inflating: curitiba_0.6_disk_usage.txt
  inflating: curitiba_0.6_packages-manual.txt
  inflating: curitiba_0.6_packages.txt
   creating: licenses/
   creating: licenses/...
  inflating: rootfs.tar.xz
```



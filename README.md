# sgx-bbb
holds working files required to build and run kmscube demo on sgx in a debian image on bbb

based on snapshot Stretch IoT image https://rcn-ee.com/rootfs/bb.org/testing/2019-09-08/stretch-iot/bone-debian-9.10-iot-armhf-2019-09-08-4gb.img.xz

Build sd card with this and boot

root@beaglebone:~#apt-get update

root@beaglebone:~#cd opt

root@beaglebone:~/opt#wget https://github.com/HunterEmbedded/sgx-bbb/raw/master/ti-sgx-ti33x-ddk-um-dev_1.14.3699939-git20171201.0-0rcnee9%7Estretch%2B20190328_armhf.deb

root@beaglebone:~/opt#apt-get install ti-libgbm2-dev

root@beaglebone:~/opt#dpkg -i ti-sgx-ti33x-ddk-um-dev_1.14.3699939-git20171201.0-0rcnee9~stretch+20190328_armhf.deb

root@beaglebone:~/opt#git clone git://git.ti.com/glsdk/kmscube

root@beaglebone:~/opt#cd kmscube

root@beaglebone:~/opt/kmscube#./autogen.sh

root@beaglebone:~/opt/kmscube#make


Then to run

root@beaglebone:~/opt/kmscube#./kmscube -d /dev/dri/card1





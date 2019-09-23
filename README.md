# sgx-bbb
holds working files required to run kmscube demo on sgx in a debian image on bbb

based on snapshot Stretch IoT image https://rcn-ee.com/rootfs/bb.org/testing/2019-09-08/stretch-iot/bone-debian-9.10-iot-armhf-2019-09-08-4gb.img.xz

Build sd card with this and boot

#apt-get update

#cd opt
#wget https://github.com/HunterEmbedded/sgx-bbb/ti-sgx-ti33x-ddk-um-dev_1.14.3699939-git20171201.0-0rcnee9~stretch+20190328_armhf.deb

#apt-get install ti-libdrm2-dev
#dpkg -i ti-sgx-ti33x-ddk-um-dev_1.14.3699939-git20171201.0-0rcnee9~stretch+20190328_armhf.deb

#git clone git://git.ti.com/glsdk/kmscube
#cd kmscube
#./autogen.sh
#make


Then to run
#./kmscube -d /dev/dri/card1





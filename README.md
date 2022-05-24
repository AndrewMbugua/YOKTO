## Will upload full recipe soon
#### The Yocto Project (YP) is an open source collaboration project that helps developers create custom Linux-based systems regardless of the hardware architecture.

### Core-image-sato image
I now have a minimal Linux image.

After building run
``$ runqemu qemux86-64 nographic``
nographic - Launches QEMU without a GUI i.e if you built the image in a server.

qemux86-64 login: root
shutoff & exit with ``$poweroff``

#### To add a particular package in the root file system
open local.conf file and add the recipe name,this is useful for when youre building your own layers & images
IMAGE_INSTALL_append += " usbutils"  --> usbutils being a package.
``$ bitbake core-image-minimal``


Layers - a collection of related projects,you could have a BSP layer,GUI layer,distro configuration on different layers.
Layers help in dividing the project into separate components and isolate metadata.
build/conf/bblayers.conf tells us which layers are in use inside the project.








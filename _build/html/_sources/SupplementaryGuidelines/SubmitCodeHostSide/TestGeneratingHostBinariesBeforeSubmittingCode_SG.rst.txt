:orphan:

|
|
|

===============================================================================
Test Generating Host BInaries Before Submitting Code (to produce new hostref)
===============================================================================

**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

(Source: http://bitbucket.wrs.com/projects/VX7/repos/vx7_host/browse/README.TXT?at=refs%2Fheads%2Fvx7-host-SR0640-features)

|

**To build Linux host tools 32-bit**
=====================================
.. code-block:: rst
	
	# Install Redhat 6.6 as Software Development Workstation using DVD below

	http://yow-mirror.wrs.com/mirror/iso/RedHat/rhel-workstation-6.6-i386-dvd.iso

	git clone http://<userid>@vxgit.wrs.com/scm/vx7/vx7_host.git
	cd vx7_host
	export WIND_HOST=$(pwd)
	git checkout <vx7-host-XXXXX>
	git submodule update --init
	cd src
	make -f Makefile.r2 MODE=32 TARGET_HOST=LINUX

	# The host tools are created in $WIND_HOST/x86-linux2

	# To build Linux hvtools and vxsim 32-bit,

	cd $WIND_HOST/..
	git clone http://<userid>@vxgit.wrs.com/scm/vx7/vxworks.git
	cd vxworks
	git checkout vx7-integration
	cd ..
	ln -s vxworks/helix/guests/vxworks-7/pkgs_v2 .

	cd $WIND_HOST/src/hvtools
	make -f Makefile.r2 MODE=32 TARGET_HOST=LINUX

	cd $WIND_HOST/src/vxsim
	make -f Makefile.r2 MODE=32 TARGET_HOST=LINUX

**To build Linux host tools 64-bit**
=====================================
.. code-block:: rst

	# Install Redhat 6.6 as Software Development Workstation using DVD below

	http://yow-mirror.wrs.com/mirror/iso/RedHat/rhel-workstation-6.6-x86_64-dvd.iso

	git clone http://<userid>@vxgit.wrs.com/scm/vx7/vx7_host.git
	cd vx7_host
	export WIND_HOST=$(pwd)
	git checkout <vx7-host-XXXXX>
	git submodule update --init
	cd src
	make -f Makefile.r2 MODE=64 TARGET_HOST=LINUX

	# The host tools are created in $WIND_HOST/x86_64-linux

	# To build Linux hvtools and vxsim 64-bit,

	cd $WIND_HOST/..
	git clone http://<userid>@vxgit.wrs.com/scm/vx7/vxworks.git
	cd vxworks
	git checkout vx7-integration
	cd ..
	ln -s vxworks/helix/guests/vxworks-7/pkgs_v2 .

	cd $WIND_HOST/src/hvtools
	make -f Makefile.r2 MODE=64 TARGET_HOST=LINUX

	cd $WIND_HOST/src/vxsim
	make -f Makefile.r2 MODE=64 TARGET_HOST=LINUX

**To build Windows host tools 64-bit**
=======================================
.. code-block:: rst
	
	# Install Ubuntu 16.04 or Ubuntu 18.04 as Software Development Workstation

	sudo apt install git make cmake bison byacc flex pkg-config libtool-bin

	# For doxygen, install additional packages

	sudo apt install gcc-multilib g++-multilib

	git clone http://<userid>@vxgit.wrs.com/scm/vx7/vx7_host.git
	cd vx7_host
	export WIND_HOST=$(pwd)
	git checkout <vx7-host-XXXXX>
	git submodule update --init
	cd src
	make -f Makefile.r2 MODE=64 TARGET_HOST=WINDOWS

	# The host tools are created in $WIND_HOST/x86-win64

	# To build Windows hvtools 64-bit,

	cd $WIND_HOST/..
	git clone http://<userid>@vxgit.wrs.com/scm/vx7/vxworks.git
	cd vxworks
	git checkout vx7-integration
	cd ..
	ln -s vxworks/helix/guests/vxworks-7/pkgs_v2 .

	cd $WIND_HOST/src/hvtools
	make -f Makefile.r2 MODE=64 TARGET_HOST=WINDOWS

**To build Linux doxygen 32-bit and 64-bit**
=============================================
.. code-block:: rst

	# Follow the steps to build Windows host tools 64-bit and then

	cd $WIND_HOST/src/doxygen
	make -f Makefile.r2 MODE=32 TARGET_HOST=LINUX
	make -f Makefile.r2 MODE=64 TARGET_HOST=LINUX

|
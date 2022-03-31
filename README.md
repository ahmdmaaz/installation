# installation
# this script replicates my history for installations
# go to home directory
# tried the installation steps using airtel broadband, college proxy network and mobile data. Use mobile data for error free installation
#! 310
sudo apt-get update
#sudo
#Whenever a user tries to install, remove or change any piece of software, he has to have the root privileges to perform such tasks. The sudo command is used to give such permissions to any particular command that a user wants to execute once the user enters a user password to give system based permissions.
#apt-get update
#It is essential before upgrading the installed packages, because the system cannot know whether the repo has a new version of a package, unless it has an up-to-date copy of the package list.





###################################################### new attempt  ######################################################################################
sudo apt-get update
mkdir tools
cd tools/
sudo apt install cmake


sudo apt-get install build-essential bison flex \
	libreadline-dev gawk tcl-dev tk-dev libffi-dev git \
	graphviz xdot pkg-config python3 --assume-yes
sudo apt install libglu1-mesa-dev freeglut3-dev --assume-yes
wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | sudo apt-key add -
sudo apt-add-repository "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-6.0 main" -y 
sudo apt-get update 
sudo apt-get install -y clang-6.0 --assume-yes
sudo apt-get install gsl-bin libgsl0-dev --assume-yes



# To install dependencies
sudo apt-get install m4
sudo apt-get install csh
sudo apt-get install libx11-dev
sudo apt-get install tcsh
sudo apt-get install tcl-dev tk-dev
sudo apt-get install libcairo2-dev
sudo apt-get install mesa-common-dev libglu1-mesa-dev
sudo apt-get install libncurses-dev
sudo apt-get install autoconf
sudo apt-get install automake
sudo apt-get install libtool
sudo apt-get install swig





sudo apt-get update
sudo apt-get install iverilog
sudo apt-get install gtkwave
sudo apt-get install yosys




git clone https://github.com/rubund/graywolf.git
cd graywolf/
mkdir build
cd build
cmake ..
sudo make
sudo make install
cd ../../




# To install OpenSTA
git clone https://github.com/The-OpenROAD-Project/OpenSTA.git
cd OpenSTA
mkdir build
cd build
cmake ..
make


# To install Qrouter
git clone git://opencircuitdesign.com/qrouter
cd qrouter
sudo ./configure 
sudo make
sudo make install 
cd ../



# Installing Magic
git clone git://opencircuitdesign.com/magic
cd magic/
sudo ./configure
sudo make
sudo make install


# To install Netgen
git clone git://opencircuitdesign.com/netgen
cd netgen/
sudo ./configure
sudo make
sudo make install
cd ../



# To install Qflow
git clone git://opencircuitdesign.com/qflow
cd qflow/
sudo ./configure
sudo make
sudo make install
cd ../


sudo apt-get update
sudo apt-get clean
sudo apt-get autoclean
sudo apt-get autoremove






######################################################      proceeding backwards    ######################################################################













# run this in tools directory

git clone https://github.com/OpenTimer/OpenTimer.git
cd OpenTimer
mkdir build
cd build
cmake ../
make 
















sudo apt-get remove docker docker-engine docker.io containerd runc
sudo apt-get update
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
apt-cache madison docker-ce
#######################################################
sudo apt-get install docker-ce=<VERSION_STRING> docker-ce-cli=<VERSION_STRING> containerd.io
# Install a specific version using the version string from the second column, for example, 5:18.09.1~3-0~ubuntu-xenial.
############################################################
sudo docker run hello-world
# This command downloads a test image and runs it in a container. When the container runs, it prints a message and exits.
#############################################################









sudo apt update
sudo apt install git
git --version
# git version 2.25.1
sudo apt update
sudo apt install dh-autoreconf libcurl4-gnutls-dev libexpat1-dev make gettext libz-dev libssl-dev libghc-zlib-dev
#  Next, open your browser, visit the Git project’s mirror on GitHub and copy the latest release link URL that ends in .tar.gz. At the time of writing this article, the latest stable Git version is “2.26.2”:
wget -c https://github.com/git/git/archive/v2.26.2.tar.gz -O - | sudo tar -xz -C /usr/src
cd /usr/src/git-*
sudo make prefix=/usr/local all
sudo make prefix=/usr/local install
git --version
# output git version 2.26.2
apt list --upgradable
sudo apt update
sudo apt upgrade
git clone https://github.com/The-OpenROAD-Project/OpenLane.git
cd OpenLane/
make pull-openlane
make test

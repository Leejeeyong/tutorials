##c/c++ compiler

	$ sudo dnf install -y gcc
	
	$ sudo dnf instll libgcc.i686 glibc.i686
	
	$ sudo dnf install -y gcc-c++

	$ sudo dnf install cmake

	$ sudo dnf install boost-devel

##cmake

	$ sudo dnf install glibc-devel
	
	$ sudo dnf install cmake
	
	$ wget <cmake download link>

	$ tar -xvzf <cmake-xxx.tar.gz>

	$ cd <cmake directory>
	
	$ ./configure

	$ make

	$ make install

##java

STEP 1: Install Oracle’s Java SE (or JDK) 8
	
	$ java -version

	The output is as follows:

  	java version "1.8.0_51"
  	OpenJDK Runtime Environment (build 1.8.0_51-b16)
  	OpenJDK 64-Bit Server VM (build 25.51-b03, mixed mode)


	Point your web browser to the Oracle SE download page here and download the latest RPM 		version of the 64-bit JDK (not Server JRE or the JRE) – currently at version 8u51 (or 		1.8.0_51).

	http://www.oracle.com/technetwork/java/javase/downloads/index.html


	$ sudo rpm -ivh Downloads/jdk-8u51-linux-x64.rpm
 	$ sudo rpm -ivh Downloads/jdk-8u51-linux-x64-demos.rpm
  	$ sudo unzip Downloads/jdk-8u51-docs-all.zip -d /usr/java/jdk1.8.0_51/
	

	$ sudo alternatives --config java

	and select installed version


	$ java -version

	The output is as follows:

	  java version "1.8.0_51"
	  Java(TM) SE Runtime Environment (build 1.8.0_51-b16)
	  Java HotSpot(TM) 64-Bit Server VM (build 25.51-b03, mixed mode)

STEP 2: Install 32-Bit Libraries

	$ sudo dnf install compat-libstdc++-296.i686 compat-libstdc++-33.i686 compat-libstdc++-33.x86_64 ncurses-libs.i686 zlib-devel.i686 ncurses-devel.i686

	

#Install needed Dependencies

	sudo yum install zlib-devel.i686 ncurses-devel.i686 ant

#Get the SDK

	mkdir ~/AndroidDevelEnvir/

	http://developer.android.com/sdk/index.html

#Update the SDK
	cd ~/AndroidDevelEnvir/android-sdk-linux/tools/

	./android
	
#Set up your PATH variable to point at the SDK
	nano ~/.bash_profile

	export PATH=$PATH:~/AndroidDevelEnvir/android-sdk-linux/tools/
	export PATH=$PATH:~/AndroidDevelEnvir/android-sdk-linux/platform-tools/
	

#Create the App
	android list targets

	Available Android targets:
	----------
	id: 1 or "android-25"
	Name: Android 7.1.1
	Type: Platform
	API level: 19
	Revision: 3
	Skins: WSVGA, HVGA, WXGA800, WVGA800 (default), WQVGA432, WXGA720
	Tag/ABIs : no ABIs.


	android create project --target android-25 --name Projectname --path ~/AndroidDevelEnvir/project/Projectname --activity MainActivity --package com.example.myfirstapp



#Building your Android app

	cd ~/AndroidDevelEnvir/project/MyFirstApp

	ant debug



#Test out your app on a real device

	adb install bin/Projectname-debug.apk

#Test out your app on the emulator

	android avd



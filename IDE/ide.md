#android studio
	downloads android studio
	https://developer.android.com/studio/index.html

	$ unzip Downloads/android-studio-ide-141.2117773-linux.zip


	$ cd android-studio/bin
	$ ./studio.sh

	appear widown "complete installation"

	select "I do not have ....."
	and OK

	

	next window click next

	and apear window 'Install Type'

	click custom

	and just select dark theme


	next and wait


	Notice the ‘Check for updates now’ on the last line of the window – click on ‘Check’ and 		if you already have the latest version, a window similar to the one shown below will pop 		up. Click on the ‘Close’ button and skip the next three paragraphs.


	f there are any updates, a window similar to the one shown below will pop-up. Click on the 		‘More Info...’ button and a browser window will open, and the web page showing more 		information on the update will be shown. Close the browser when done and then click on the 		‘Check’ button on the Android Studio again. A window similar to the one shown below will 		appear.



	Click on the ‘Update and Restart’ button. The updates will begin downloading as shown.


	make activates

	
    Start a regular terminal (NOT a root terminal), then use your preferred editor (’nano’ in my 	case) to create and open a new file:

	$ nano .local/share/applications/android-studio.desktop
	or gedit

	In the new file, enter the following lines:

      	[Desktop Entry]
      	Type=Application
      	Encoding=UTF-8
      	Name=Android Studio
      	Comment=Google Programming IDE for Android
      	Exec=/home/(your_login_name)/android-studio/bin/studio.sh
      	Icon=/home/(your_login_name)/android-studio/bin/studio.png
      	Terminal=false

    	If you decide to cut-and-paste the above text, make sure to replace (your_login_name) with 		your actual login name. Save the file and exit the editor.

    	Reload the Gnome shell by executing first ‘Alt-F2’ and then typing ‘r’ in the resulting 	‘Enter a Command’ field, followed by the ‘Enter’ key.

    	If you now click on the ‘Activities’ menu item, then on the ‘Show Applications’ icon 		(usually the last icon in the dock), you will find the ‘Android Studio’ launcher in the 	applications list (see below). To add the ‘Android Studio’ launcher to the ‘Favourites’ in 		the dock, right-click on the launcher icon in the applications list and select ‘Add to 		Favourites’ item in the window that pops up. To test the launcher, you can click on either 		icon – Android Studio should launch.



	http://ridz1ba.blogspot.kr/2015/08/how-to-install-oracle-java-and-android_9.html

#pycharm

	https://www.jetbrains.com/pycharm/download/#section=linux

	$ cd <pycharm directory>

	$ cd bin

	$ ./pycharm.sh

#eclipse with kotlin

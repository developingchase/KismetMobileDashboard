# KismetMobileDashboard

![Image description](https://raw.githubusercontent.com/elkentaro/KismetMobileDashboard/master/kismetmobile.png)

This is a major new rewrite of the mobile UI. Ideally I want to test it more but with #hackersummercamp around the corner, I just don't have the time. 

Major functional updates:

1. Devices are now click-able to drill down in details. 
        example: Ap -> List of APs -> AP and its clients. -> client details. 
2. login via the mobile dashboard is now possible. 
3. Pause/Restart of datasources. (you cannot start/stop interfaces itself)


Limitations: 
1. Cannot start/stop interface.
2. Cannot handle non-English SSIDs.

THIS IS A VERY EARLY ALPHA RELEASE...things might not work . 


Prerequisite: git-master level kismet. https://github.com/kismetwireless/kismet

1.Installation.

 - git clone into the kismet git. ("/home/[whatever]/kismet") 
                    
- cd into kismetmobiledashboard

- sudo make install

2.Access it via : http://localhost:2501/plugin/mobiledashboard/

The trailing "/" is important. Without it you will get a 404.

Its still very early in development but it should work.

To get "full screen" UI , access the page via your normal browser on the mobile device and then create a shortcut on the "home screen."

------- 
Made some modifications and updates to elkentaro's original very useful dashboard. 
- Updated some of the fields/views to track with some changes in Kismet (some tips from terbo https://github.com/elkentaro/KismetMobileDashboard/pull/13).
- Added a new function/row for GPS information that includes a link to Google Maps with the current location as a pin.
- Did some minor work to clean up some errors the browser console was reporting.

If you don't want to use the formal make process above, simply do the following:
1. Create a "plugins" folder in the user that runs kismet's home/.kismet folder. For example: ~/.kismet/plugins or /root/.kismet/plugins
2. In this folder, create a new folder for "mobiledashboard".
3. Copy the manifest.conf file into the "mobiledashboard" folder.
4. Copy (recursively) the httpd folder in the "mobiledashboard" folder.
5. Restart Kismet.
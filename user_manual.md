This user manual describes the process of creating flight paths, flying the drones over these flight paths, and creating orthomosaics of imagery collected from these planned missions.

This research is carried out under the BIRD lab, ATREE, Bengaluru (PI: Rajkamal Goswami), with some ongoining techical support from Aaditeshwar Seth's team working on drones (Jayakrishna, Gaurav Rajput, Parth Thakur, and Raman Kumar) at IIT Delhi.

This user manual has been primarily authored by Paul Pop (including most screenshots and images).

Other contributors: Rohan Baishya, Parth Thakur, Raju, and Ranjith Kumar HT have contributed directly to this manual either through contributions to sections of the manual or verbal suggestions/recommendations. <br> <br>

Sections:

- [Section 1: Creation and export of the flight paths](#section-1-creation-and-export-of-the-flight-paths)
- [Section 2: Uploading the flight path to the drone or drone app](#section-2-uploading-the-flight-path-to-the-drone-or-drone-app)
  * [For DJI Mini 5 Pro and DJI Mini 4 Pro](#for-dji-mini-5-pro-and-dji-mini-4-pro)
- [Section 3: Flying the drone](#section-3-flying-the-drone)
  * [DJI Mini 3](#dji-mini-3)
  * [DJI Mini 4 Pro](#dji-mini-4-pro)
- [Section 4: Creation of orthomosaic in WebODM](#section-4-creation-of-orthomosaic-in-webodm)

<br>

## Section 1: Creation and export of the flight paths

**Step 1:** Install the Map Pilot Pro in your phone either through your mobile app store (Google Play Store/Apple App Store etc) or install it using an apk file.

**Step 2:** Open the Map Pilot Pro app in your phone.

<img src="https://github.com/user-attachments/assets/692b6d9e-b59a-4da5-9de8-18d5f6e6cfe8" alt="downloaded_app" width="225" height="450"> <br>

**Step 3:** Click on 'Settings'.

<img src="https://github.com/user-attachments/assets/fa697bed-0643-437e-8bf4-155668b20d33" alt="map_pilot_pro_screen" width="500" height="225"> <br>

**Step 4:** Go to 'Advanced Settings' and turn on "Export Simple KMZ"

<img src="https://github.com/user-attachments/assets/d7ec2ef1-414a-4774-abc0-2fe10babe22a" alt="advanced_settings" width="500" height="225"> <br>

Without this, you will only be able to export the flight paths in the mme (maps made easy) format, a non-interoperable file format not recognised by any other GIS or drone app.

**Step 5:** Go to 'Flight Camera' > 'Model'> and then select a camera which has an "Export Only" text given in the bracket. This is also necessary to export the flight path as a kmz file.

<img src="https://github.com/user-attachments/assets/81478e53-26e1-4cb0-a9c7-64de673d97e4" alt="flight_camera_model" width="500" height="225"> 
<img src="https://github.com/user-attachments/assets/6b624b82-8b18-48f3-a397-0a84a6c9b26e" alt="flight_camera_model" width="500" height="225"> <br> <br>

**Step 6:** *[Start from step 18 if you want to upload and use boundary files of your region of interest as reference for drawing the flight paths]* Go back to the home screen and click on 'New Mission'

<img src="https://github.com/user-attachments/assets/fa697bed-0643-437e-8bf4-155668b20d33" alt="map_pilot_pro_screen" width="500" height="225"> <br>

**Step 7:** Click 'OK' on both the pop-ups

<img src="https://github.com/user-attachments/assets/13f593b0-dbba-4605-878b-0fa0e30025e9" alt="pop_up_1" width="500" height="225"> 
<img src="https://github.com/user-attachments/assets/4149b588-dd0e-4253-a2b9-cb26570a1ca2" alt="pop_up_2" width="500" height="225"> <br> <br>

**Step 8:** Move the viewport (the region of the map the app shows to you) to the desired flight path region.

By default, the location in the viewport will be Lower Manhattan. If your drone flight location is close to where you're right now, you can turn on your phone GPS and it will automatically move to that area.
If, not zoom out of Lower Manhattan and zoom into your region of interest.

<img src="https://github.com/user-attachments/assets/f6a662a2-80d1-467c-9971-58c1a3f4d233" alt="default_viewport" width="500" height="225"> 
<img src="https://github.com/user-attachments/assets/aaf5bd08-a6fb-41ec-8aab-9a1dcff34862" alt="zoomed_out_viewport" width="500" height="225"> 
<img src="https://github.com/user-attachments/assets/28fb3231-44aa-4aa4-beba-4ce98da2424d" alt="zoomed_in_roi" width="500" height="225"> <br> <br>

**Step 9:** Specify the altitude (80 m is generally ideal to avoid obstacles but keep reasonably high resolution imagery), speed (slow speeds of 3 m/s or less is recommended for clear capture of images), and overlap (80% overlap in the front and sides (80/80) is recommended. For class specific recommendations, you can visit read [this article][1]).Click on 'Norm Mission' and then 'Normal'. 

<img src="https://github.com/user-attachments/assets/21a01ea1-84cc-4078-92fc-60c043bfb61e" alt="norm_mission" width="500" height="225"> <br> 

**Step 10:** Click on the bar with 'export only' to minimize the top bar so that you have more visibility of your region of interest.

<img src="https://github.com/user-attachments/assets/fa676f90-b1e0-4caf-9ab7-cd5451983721" alt="minimize" width="500" height="225"> <br> 

**Step 11:** Long press on a portion of the screen to set your purple "Home point" dot. This is the point to where the drone will return to after the flight path has been completed.

<img src="https://github.com/user-attachments/assets/94502011-f412-4589-a537-8128d8d7b9ff" alt="home_dot" width="500" height="225"> <br> 

**Step 12:** Long press on a portion of the screen to set your orange "Boundary" dots to cover the entire survey area. 

There will be three dots in the beginning. Use these three dots to cover the entirety of the desired survey area in the first pass. After this, use the smaller orange dots to more snuggly fit the survey area. But make sure that you take an extra 20-50 m buffer around your desired study region so that while creating the orthomosaics, there are no distortions at the border of the desired study area. Be careful whil moving the smaller dots to avoid messing up as there is no undo or redo option. If you mess up, delete the flight path by using the dust bin icon on the top left. 

<img src="https://github.com/user-attachments/assets/9ffdd5c4-53c6-48e9-b97e-7a617a0a27c4" alt="boundary_dot" width="500" height="225"> <br> 

**(optional) Step 13:** If you want this flight plan to be accessible later on, click on the floppy disk icon on the top left, name it and save the mission/flight path. **This is needed for long-term consistent mapping of the same region across seasons and years.**

<img src="https://github.com/user-attachments/assets/536def51-7930-44b8-89c2-0d924cc9727a" alt="rename" width="500" height="225">
<img src="https://github.com/user-attachments/assets/552b49f1-b056-4cb2-9cfa-b738aebd8c41" alt="renamed" width="500" height="225"> <br> <br>

**Step 14:** Click on the drone/airplane icon on the top right and click on the 'Export' icon

<img src="https://github.com/user-attachments/assets/7d956515-797e-4cb0-bd72-4ba52b86545e" alt="drone_icon" width="500" height="225">
<img src="https://github.com/user-attachments/assets/b86194ae-5043-44f1-8ca8-1db8cfb20dd5" alt="export" width="500" height="225"> <br> <br>

**Step 15:** Click on 'No' for the 'Terrain Awareness' pop-up, as this option is not available in the free version.

<img src="https://github.com/user-attachments/assets/08a2a011-0e18-4aa8-906d-143e589689d4" alt="pop_up_terrain_awareness" width="500" height="225"><br>

**Step 16:** Give a name for the flight path, click on 'Export' and press 'OK' on the next popup.

<img src="https://github.com/user-attachments/assets/844db279-6cef-40d0-a2a8-10560661ad89" alt="rename" width="500" height="225">
<img src="https://github.com/user-attachments/assets/b43fe903-185f-4ddf-94bf-54a6ca21887f" alt="export" width="500" height="225"> <br> <br>

You can now find the downloaded kmz file for use in the drones, in the 'Downloads' folder of your phone. 

**Step 17:** Click on left facing triangle which will reveal the 'Exit' icon. Click and exit to the Home screen.

<img src="https://github.com/user-attachments/assets/17ae4c17-33ca-4648-9047-16d983e650d2" alt="exit" width="500" height="225"> <br>

**(optional) Step 18:** Click on 'File Manager'

If you need to import a boundary file for your region(s) of interest like a shapefile, then you first need to convert it to a kmz format (using tools like QGIS) and keep it ready in the device or google drive.

<img src="https://github.com/user-attachments/assets/fa697bed-0643-437e-8bf4-155668b20d33" alt="file_manager" width="500" height="225"> <br>

**(optional) Step 19:** Click on 'Import'

<img src="https://github.com/user-attachments/assets/e129a13d-61d3-4c66-a441-585bfe4e0d9c" alt="import" width="500" height="225"> <br>

**(optional) Step 20:** Navigate to the location in your device or google drive to find the saved boundary file, and then click on it.

<img src="https://github.com/user-attachments/assets/7e90eb4b-1a06-4952-9af1-468c46288717" alt="drive" width="225" height="450">
<img src="https://github.com/user-attachments/assets/6143fbfc-6b30-4078-894b-0c661e6c0bc7" alt="search" width="225" height="450">
<img src="https://github.com/user-attachments/assets/6feef804-5f7b-4039-8aaa-521e731b9a99" alt="find" width="225" height="450"> <br> <br>

**(optional) Step 21:** Click on 'Imported'

<img src="https://github.com/user-attachments/assets/3fd7872a-cbfb-4539-a987-6683560dda27" alt="imported" width="500" height="225"> <br>

**(optional) Step 22:** Under 'Imported Overlay Files', turn on the 'Show KML'

<img src="https://github.com/user-attachments/assets/bc475eee-34fe-4930-bc04-171ebb8d7fe7" alt="import" width="500" height="225"> <br>

**(optional) Step 23:** Click on 'Sync'

This is needed so that the boundary files show up in the map.

<img src="https://github.com/user-attachments/assets/a37ae6af-85ea-4f93-b1a0-ff2acf991cd7" alt="sync" width="500" height="225"> <br>

**(optional) Step 24:** Under 'Imported Overlay Files', turn on the 'Show KML'

<img src="https://github.com/user-attachments/assets/bc475eee-34fe-4930-bc04-171ebb8d7fe7" alt="show_kml" width="500" height="225"> <br>

**(optional) Step 25:** Repeat Step 6 to 16 but with the boundary files as a guide for drawing the flight paths.

You can see that in this case, there are grey line segments after the white line segments in the flight path. The grey lines indicate whose paths which cannot be completed in one flight,
and multiple batteries would be required to complete such large survey areas. The drone is estimated to return to the home point after reaching the end of the white line, and then after battery has been replaced,
it will continue from where it left off. **But this may not be the case in real life and this can be an overestimation, allowing us to actually cover areas in the grey region as well** (as is seen in the screenshot of a real mission on the bottom left below).
For details on how much distance the flight path covers, time required, the number of batteries required, area covered, number of images captured, amount of space it will take in storage, click on the polygon icon on the left of the screen. These may not be 100% accurate. For example, in a multi-battery flight of ours, the estimated time was given as 33 min 21 sec, but it was actually close to 31 min 47 sec (based on the mission logs). Most of the estimates may be a slight overestimate (which is better than an underestimate from a practical point of view).

<img src="https://github.com/user-attachments/assets/bc32b989-9ea4-40da-8865-b196c01b3a64" alt="boundary_files" width="500" height="225">
<img src="https://github.com/user-attachments/assets/e7a38cb7-83b2-4cc8-b50e-3a72ce70b0a4" alt="white_and_grey_lines1" width="500" height="225">
<img src="https://github.com/user-attachments/assets/ae3ee731-c104-4634-937d-1eda5677398d" alt="white_and_grey_lines2" width="500" height="225"> <br>

If you have a paid account and wants to have better terrain awareness for the flight path, click on the icon on the bottom left with one coniferous  tree and two  snow-capped mountains. It will allow you to select the digital elevation model. 
ASTER is the worst among them for most regions. SRTM is better, but Copernicus is likely the most accurate among these three for most regions, especially the mountainous regions.

<img src="https://github.com/user-attachments/assets/facc8bfc-35cf-4a65-8c5d-88302e5450f5" alt="more_details" width="500" height="225"> <br> <br>


## Section 2: Uploading the flight path to the drone or drone app

### For DJI Mini 5 Pro and DJI Mini 4 Pro

Note: this workflow won't work for DJI Mini 3 as the waypoint creation icon is not visible in the DJI Fly when connected to the drone. 

For DJI Mini 5 Pro, the kmz file must be uploaded to the remote controller. But there is no straightfoward way to do this. Rohan Baishya explains in this section, a foolproof method to do this (based on [this tutorial][2].

**Step 1:** In the RC/DJI fly app, connect the drone and press 'GO FLY' 

NOTE: Make sure the drone is placed outside for adequate satellite signal

<img src="https://github.com/user-attachments/assets/e190f2ad-b712-4e35-8457-388bdc85222f" alt="rc-dji-app" width="600" height="325"> <br>

**Step 2:** Click on the map at the bottom left corner (make sure your position is being shown on the map)

<img src="https://github.com/user-attachments/assets/a60b004d-0a62-4db1-9c0e-385d0064d2c4" alt="map" width="600" height="325"> <br>

**Step 3:** Click on the waypoint icon highlighted in yellow on the left-centre, and create a waypoint with at least 2 points.

<img src="https://github.com/user-attachments/assets/03b0d842-8721-4b8c-9ae2-5e0a778ae37b" alt="waypoint-icon" width="600" height="325"> <br>

**Step 4:** Click on the note/paper icon to left of the text 'Waypoint'. 

<img src="https://github.com/user-attachments/assets/03b0d842-8721-4b8c-9ae2-5e0a778ae37b" alt="waypoint-icon" width="600" height="325"> <br>

**Step 5:** Select the waypoint created and click on 'SAVE' > 'Save'.

<img src="https://github.com/user-attachments/assets/ac1487d9-9e6d-4e17-bad9-adae3d681d54" alt="SAVE" width="600" height="325">
<img src="https://github.com/user-attachments/assets/e7328b47-2fb6-4d4d-8b96-77817e308da5" alt="Save" width="600" height="325"> <br><br>

**Step 6:** Return to the home screen by clicking on the left-facing arrow on top-left and press on 'Save and Exit'. 

<img src="https://github.com/user-attachments/assets/d929a78b-f3f3-4b77-8dad-99bc6d8fb18e" alt="save_and-exit" width="600" height="325"> <br>

**Step 7:** Connect the RC to your desktop/laptop (using an USB or any other means available) and follow this path
```
DJI RC 2 > Internal Shared Storage > Android > data > Dji.go.v5 > files > waypoint
```
<img src="https://github.com/user-attachments/assets/3587bd4a-abd0-46f4-aff8-5bf99097714a" alt="path" width="800" height="525">

Once you reach the waypoint folder, select the most recently created folder. This will contain the waypoint created in the steps above.

**Step 8:** Open the folder and copy the name of the KMZ file. 

<img src="https://github.com/user-attachments/assets/846c81e1-0beb-4db2-9d58-6e7ad837b587" alt="copy_name" width="800" height="525"> <br>

**Step 9:**  In the PC, change the name of the KMZ file generated from Map Pilot Pro app to the copied name. In this case the kmz file named "Pasighat_test_1.kmz" is changed 
to "90A8341C-CFE2-4E84-8681-B5B081E5C815.kmz"

<img src="https://github.com/user-attachments/assets/1c6e17c9-8c26-4079-8859-3410e3b3ebc5" alt="rename" width="800" height="525"> <br>

**Step 10:**  Copy it to the folder we reached in step 7, and replace the original waypoint kmz file created in the RC/DJI Fly app with the kmz file 
created in Map Pilot Pro app. Now you can disconnect the RC from the PC.

<img src="https://github.com/user-attachments/assets/cbe6fc64-53fd-4dc1-864b-2cc598656890" alt="replace_original" width="800" height="525"> <br>

**Step 11:**  Now connect the RC to the drone. 

**Step 12:**  Once the drone is connected, navigate to the note/paper icon to the left of the text 'Waypoint'. 

<img src="https://github.com/user-attachments/assets/ddc9ed80-da2e-4eb3-b2d8-726252e020ad" alt="note_icon" width="600" height="325">
<img src="https://github.com/user-attachments/assets/abac377f-17dd-476c-8d81-6ad8b4fb2e34" alt="note_icon" width="600" height="325"> <br>

The kmz file created in Map Pilot Pro should be visible now in the saved waypoints window. 


## Section 3: Flying the drone

### DJI Mini 3

_The screenshots for this section were largely contributed by Raju._

Note that if you're opening the Map Pilot Pro app in a device with 4 GB and/or a lot of it is in use, you will get a warning like this:

<img src="https://github.com/user-attachments/assets/3153e1f8-11b3-404e-ab2a-3256c3205bd7" alt="memory_warning" width="500" height="225"> <br>

You can ignore it, but ideally you would want a device with better memory.

**Step 1:** As there is no way to export a created flight path to the Map Pilot Pro app in the free version, one has to create the flight path in the field. Follow section 1 to create the flight path, and input the right altitude, speed, overlap etc.

**Step 2:** Once you've created the flight path, save the flight path using the floppy disk icon on top left.

**Step 3:** Place the drone in a flat area with all the stones and other potential things that can hit and harm the blades removed.

<img src="https://github.com/user-attachments/assets/3ccdd3ae-4dd7-4099-bab0-0d4ceec78132" alt="drone_on_ground" width="400" height="400"> <br>

**Step 4:** Connect the mobile phone containing the Map Pilot Pro app to the RC (Remote Control) using the cable of the RC (see top right of the image below).

<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/74d0cca3-d14e-4b95-a142-ce4fd304f961" /> <br>

**Step 5:** Switch on the RC by single pressing the power button (the button on the right below) followed by a long press. This will show a brief flash of green (after single short press) and then permanent green light (after long press).

<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/29344496-9b4a-4488-8c31-ced0fb24b3f0" />
<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/ae986ec4-cefa-44c7-a8d0-f3053f444797" /> <br>

If you are already on the Map Pilot Pro app of the phone, it will show the following message: "Connected for charging only. Tap the USB notification to use USB for transferring files." You can change the setting if you fear any significant battery drainage of the RC by the mobile phone (there won't be). So, you can ignore this and not change anything. The connection to the RC will work whether you change the transfer settings or not.

<img width="500" height="225" alt="image" src="https://github.com/user-attachments/assets/00445071-171b-4309-b0ca-94fe6ff1f376" /> <br>

**Step 6:** Switch on the drone by single pressing the power button (the button on the center of the drone) followed by a long press. This will show a brief flash of green (after single short press) and then permanent green light (after long press).

<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/97416827-b12a-4873-afcb-b8a8a2dc251b" />
<img width="395" height="395" alt="image" src="https://github.com/user-attachments/assets/cb012e6d-c8de-41d3-b5a0-55ff6cba7c91" /> <br>

Now the the drone will be detected by the mobile phone. 

**Step 7:**  Once it is detected, the phone will prompt you to connect to an existing drone app - like DJI Fly or Map Pilot Pro. Select Map Pilot Pro. If you're already on the Map Pilot Pro app, you will get a message saying "Found Aircraft   Mini3". Click 'OK'.

<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/50bf9ce6-f015-421f-b8b0-5125e68e0ea9" />

**Step 8:** The app will display the following pop-ups. Click 'OK'.

<img src="https://github.com/user-attachments/assets/64197afd-da05-4f4b-b12d-00610cf05977" alt="important_warning" width="500" height="225"> <br>

**Step 9:** Then another pop-ups. Click 'No' as Terrain Awareness is not available in the free version.

<img src="https://github.com/user-attachments/assets/a9e559cf-f774-448a-81e3-db4e8240542d" alt="terrain_awareness" width="500" height="225"> <br>

**Step 10:** You can click 'Override' on the 'Return to Home Height' pop-up to retain the set app.

<img src="https://github.com/user-attachments/assets/48ac62eb-fa02-41fe-80c0-4eab6b298e9e" alt="terrain_awareness" width="500" height="225"> <br>

**Step 11:** Click on 'Upload' on the top right (need different screenshot).

<img src="https://github.com/user-attachments/assets/48ac62eb-fa02-41fe-80c0-4eab6b298e9e" alt="terrain_awareness" width="500" height="225"> <br>

**Step 12:** Click 'OK' on the 'Path Verification' pop-up.

<img src="https://github.com/user-attachments/assets/cffd194a-0017-436e-97a6-71e4f0e1ce50" alt="terrain_awareness" width="500" height="225"> <br>

**Step 13:** Inspect the blue line (flight path), then click on 'Takeoff' on the top right. Then drone would take off and take a picture at the near ground level before climbing up, and then moving on the start point of the flight path (green dot).

<img src="https://github.com/user-attachments/assets/c0dbd359-94c9-407d-8b77-25828954534b" alt="terrain_awareness" width="500" height="225"> 

<img width="395" height="395" alt="image" src="https://github.com/user-attachments/assets/e3d10d17-8b90-402f-8613-e38faf62e055" />

**Step 14:** If the mapping is complete before the finishing up of one battery, it will show 'Mapping Complete'.  Click 'OK' on the Mapping Complete pop-up.

Usually, the drone is programmed to return to home when the battery is below 20% power for the purpose of safety. There may be a way to lower this perecentage at your risk so that more of the flight path is covered at one go. 
But it is highly recommended that you don't, as you can risk the drone crash landing.

<img src="https://github.com/user-attachments/assets/bfd3aa4f-53e0-4909-b7d4-8c118e7417ec" alt="mapping_complete" width="500" height="225"> <br>

**Step 15:**  Click on the return to home icon on the top right if the drone has not returned. As a last resort, in case the drone is not returning back on its own, take control using the joystick buttons and pilot the drone back to the home point. 

*Step  to  are needed only for multi-battery missions.*

**Step 16:** The battery low alarm triggers at around 20% battery and the automatic return to home features triggers after reaching a certain threshold of battery level (less than 20%, at around 17% in our case). If this automatic feature has not been triggered, click on the return to home icon (RTH) on the top right. Any of these two will result in the pop-up "Returning Home". Click "OK". In one of the flights, we found that majority of the flight path of the estimated 5.53 km (it was actually less than that) and 9.4 hectares, had been completed with just one battery, using around 72% of the battery (from 89 to 17 per cent). So, it's possible to cover a relatively large flight path with just one battery as long as it is fully charged.

<img src="https://github.com/user-attachments/assets/06d52eea-273f-40f2-ab33-9e4add535719" alt="mapping_complete" width="500" height="225">
<img src="https://github.com/user-attachments/assets/0f583912-e0e7-44e2-95a5-22abfc76e17e" alt="mapping_complete" width="500" height="225"> 

For a multi-battery mission, it is important that either the automatic triggering or return to home button is clicked, as this will **trigger the creation of an abandonment point (dark blue dot) along the flight path where it stopped**. Manually bringing it back will likely not do this.
<img src="https://github.com/user-attachments/assets/3ee71538-bced-4253-b7b4-46c973f598f2" alt="mapping_complete" width="500" height="225"> <br>

**Step 17:** Once the drone has landed back, the app will show the pop-up <br> <br>
"Fight 1 complete  <br><br>
More flights are required to complete the mission". <br>

Click "OK"

<img src="https://github.com/user-attachments/assets/b1f911b2-1089-450e-a746-6ec0dec89532" alt="mapping_complete" width="500" height="225"> <br>

**Step 18:** Now switch off the drone with a short single press and then a long press on the power button.

**Step 19:** Replace the battery of the drone. Don't exit the Map Pilot Pro app. It will likely exit the current mission screen when the drone has been switched off, but when you click on 'New Mission' again, the flight path with the abandonment point will still be visible.

**Step 20:** Click on the 'Upload' icon on the top right and it will upload the remaining flight path with the points for capturing the images. You may need to click on the unlock icon on the top left for this.

**Step 21:** If you had kept the 'Movable Home Point' option under the 'Flight Control' settings turned on, you will get a error pop-up 'Movable Home Point Error' as the RC doesn't do any flight path related dynamic communication with the drone and instead uses the planned flight path with fixed home point that is uploaded. You can ignore the error and click on "Proceed".

<img src="https://github.com/user-attachments/assets/26bf9002-4a99-4ccd-a9e7-f6ab1628608a" alt="mapping_complete" width="500" height="225">
<img src="https://github.com/user-attachments/assets/e8cb3fd2-52a0-4584-884a-ccf60f0bfb2b" alt="mapping_complete" width="500" height="225"> <br>

**Step 22:** Click "OK" on the <br><br> "Restarting mission <br> Flight will resume at abandonment point" pop-up. <br>
<img src="https://github.com/user-attachments/assets/e9579442-fb49-49a4-8fe1-73cf8f772a63" alt="mapping_complete" width="500" height="225"> <br>

**Step 23:** Repeat steps 13-15 if the remaining portion only requires the second flight and not more than that. If there are more battery changes necessary to complete the flight path, repeat steps 13 and 16-20.

**Step 24:**  Save the flight path as it will be needed for the future if repeating the same flight path.

**Note:** <br> If you want to see the flight logs of any flight mission, you can go to 'File Manager' and then 'Mission Logs'.

<img src="https://github.com/user-attachments/assets/fa697bed-0643-437e-8bf4-155668b20d33" alt="file_manager" width="500" height="225"> 
<img src="https://github.com/user-attachments/assets/e129a13d-61d3-4c66-a441-585bfe4e0d9c" alt="import" width="500" height="225"> <br>

If you had kept auto deletion disabled, you will get a pop-up. You can press "OK". It's best to not auto delete logs if you think that logs will be useful for your research or replication of the flight in the same manner.

<img src="https://github.com/user-attachments/assets/aa650d8d-edb3-42b6-a8b9-8aed17a8b98b" alt="import" width="500" height="225"> <br>

You can go to specific missions which will show the multiple segments (if a multi-battery mission), and you can export them (export pop-up will only show the csv, but kml will also be exported along with it irrespective of whether you keep the 'Show KML' option turned on or not).
<img src="https://github.com/user-attachments/assets/4ecab817-33ac-4f2f-97b9-20b2c8287b50" alt="import" width="500" height="225">
<img src="https://github.com/user-attachments/assets/e09867cb-7ac7-4243-b784-68e31482438e" alt="import" width="500" height="225">
<img src="https://github.com/user-attachments/assets/4fb84be5-1d9e-42d6-9447-1d7efa4d02cb" alt="import" width="500" height="225"> <br>

In the mission logs, you will get two outputs - a csv file containing milli-second level breakdown of the flight and associated metadata like the coordinates at each point of time, RC signal and battery level, as well as a kml file of the flight path (which will also show the route the drone took to the starting point as well as back to the home point. The csv file is very detailed with 61 different fields/columns.

<img src="https://github.com/user-attachments/assets/a703e765-b7a6-4010-9619-5e408578d3d8" alt="import" width="1000" height="700"> <br>

If there was one battery change in between the the full flight path, then there will two csv files and two kmls for each segment of the flight path.
The kmls in this case will look like this (on google earth imagery background), where the first image shows the initial flight and the second image shows the second section after battery replacement: 

<img src="https://github.com/user-attachments/assets/d1dae77f-ba2b-4bf6-afb4-7196c76cb364" alt="import" width="398" height="522"> 
<img src="https://github.com/user-attachments/assets/2715a068-9b49-4d81-857c-451cd2d2c6a1" alt="import" width="398" height="538"> <br>

**Potential issue:** <br> A major issue that can affect the flight is loss of connection to the satellites, in which case the drone won't continue on the same path when connection comes back (the connection seems to drop after the number of satellites becomes 17 or less). It will show a loading icon in the center of the screen along with the number of satellites missing (as seen below).

### DJI Mini 4 Pro

*Parth Thakur has contributed this section.*

**Step 1:** Connect the RC with the drone and enter an open ground

**Step 2:** Select this option — it is the waypoint mode.

<img src="https://github.com/hbot07/Drone-Phenology-Monitoring/blob/2f8553c89832045c92a51927bdbe357ce9f72b67/misc/guide_for%20_drone_tasks/images/step1.jpeg?raw=true" width="600"> <br>

**Step 3:** Select this list button.

<img src="https://github.com/user-attachments/assets/ca87334a-80de-42b0-aab1-334171386a9a" width="600"> <br>

**Step 4:** Select the path you want to operate on as uploaded previously on DJI RC.

<img src="https://github.com/user-attachments/assets/da9b1507-c3ac-49e2-aac9-d5bf9826f82e" width="600"> <br>

**Step 5:** It will appear like this showing the number of waypoints present. Then press **Next**.

<img src="https://github.com/user-attachments/assets/4311aca3-d596-4b4b-8d27-b2fab8a5a467" width="600"> <br>

**Step 6:** All the fields will already be filled as per the data configured in Map Pilot Pro. Press **Go** to make the drone fly on the selected flight path.

<img src="https://github.com/user-attachments/assets/1a074f89-ed28-4c5a-ba0e-a80ea4c33348" width="600"> <br>

## Section 4: Creation of orthomosaic in WebODM

WebODM is a powerful free and open-source software for the rendering of orthomosaics as well as 3D imagery from the drone photographs. It is very advanced with a lot of options to play around to efficiently and quickly process large number of drone imagery.
The bottleneck for processing would be the system RAM size, availability of GPU, disk space etc. Higher the RAM size, availability of good GPUs for GPU acceleration, and sufficient disk space for storage of input/output files as well as intermediate products, faster the orthomosaic rendering. Note: there is an option to delete intermediate products in WebODM while processing, for those lacking space.

**Step 1:** Install WebODM and dependencies

WebODM works best in Linux, and also in Windows and Apple Operating Systems (OSes). The installation procedure for all the OSes is described [here][3]. So, I am not repeating it here. Git and Docker would need to be installed for the installation of WebODM. If you have trouble installing WSL2 (Windows Subsystem for Linux 2, which is needed for running the Linux kernal within Windows), then refer to installation guide along with troubleshooting help for WSL2 [here][4].

**Step 2:** Optimise the functioning of WebODM

If using Windows, you can allocate more memory by searching for WSL Settings...

<img src="https://github.com/user-attachments/assets/2e567a29-68eb-40b3-a284-6cb4d1ca7190" alt="search_wsl_settings" width="800" height="750">

...and editing the 'Memory Size' option. 28,000 MB here is nearly 28 GB (out of the 32 GB RAM available in the system). Leave some memory for Windows.

<img src="https://github.com/user-attachments/assets/29cda4bd-4aed-40b3-93bc-d2f81d8f8f03" alt="search_wsl_settings" width="800" height="525"> <br>

**Step 3:** Launch WebODM

Once you follow the instructions for installation, you can launch WebODM from the Bash/Git Bash/other command line interface and open WebODM in a browser at "http://localhost:xxxx/". 
Make sure you have Docker (Dekstop) running before launcing WebODM as it will not launch successfully without it.

**Step 4:** Create a WebODM account

Create an account. You can log in and log out any time. If you close the browser without logging out, you will be logged in and won't have to log in again the next time you launch WebODM.

**Step 5:** Click on 'Select Images and GCP'

<img width="1907" height="427" alt="image" src="https://github.com/user-attachments/assets/bea593f3-d275-48c4-abaf-a4391e05ccca" /> <br>

**Step 6:** Navigate to the folder containing all the images from a flight path, select all of them, and 'Open'

<img width="1342" height="668" alt="image" src="https://github.com/user-attachments/assets/0f69ad78-c530-4a9f-91e4-b4df646f1762" />

**Step 7:** Edit the parameters as required before starting processing, by clicking on 'Edit' under 'Options'

<img width="1616" height="781" alt="image" src="https://github.com/user-attachments/assets/80f47048-6b35-4260-8938-36664c0571e8" />

I have found that 'Fast Orthophoto' was surprisingly consistently providing orthomosaics/orthophotos with less distortions than when it is not used.

<img src="https://github.com/user-attachments/assets/7498ab56-f985-4ff4-94ca-b1fdfd7b8d89" alt="downloaded_app" width="450" height="900"> <br>

If you enable 'skip-3dmodel', it saves a good amount of time (especially on not-so-powerful computers), and it doesn't seem to effect the the quality of the orthomosaics either way.

<img src="https://github.com/user-attachments/assets/3dc1b139-953f-4538-9f56-31006cf3921f9" alt="downloaded_app" width="450" height="900"> <br>

If you are facing memory issues while processing, you can reduce the maximum concurrency which will reduce the multi-tasking (and hence increase the time taken).
Enabling optimise-disk-space deletes intermediate files to optimise the disk space usage (if the system is low on disk space).

<img src="https://github.com/user-attachments/assets/3178f3b6-c6f9-475e-a3e2-ea66cc4ad84e" width="450" height="900"> <br>

**Step 8:** Click on 'Review' and 'Start Processing' (make sure you're not running other computationally heavy processes like using QGIS or having many tabs open in the browser)

<img width="1616" height="781" alt="image" src="https://github.com/user-attachments/assets/80f47048-6b35-4260-8938-36664c0571e8" />

<img width="1603" height="764" alt="Screenshot 2026-03-11 202144" src="https://github.com/user-attachments/assets/b7d5926e-9ca4-4e63-9653-cec1f1edf466" /> <br>

It will show a blue loading bar which shows the progress of uploading the images

<img width="1621" height="319" alt="image" src="https://github.com/user-attachments/assets/eff8e8f6-dabe-4c2e-8618-975c80651071" />

Once uploaded, the task starts. You can tunr 'On' the 'Task Output:' to see each and every step in real time.

<img width="1624" height="565" alt="image" src="https://github.com/user-attachments/assets/7f3c48a1-ddaa-4f18-ba92-53ae3e0f1386" /> <br>

**Step 9:** View the orthomosaic by clicking on the imagery on the screen.

<img width="1586" height="478" alt="image" src="https://github.com/user-attachments/assets/174198d7-407e-45e7-b8e4-6c5f2fcd46d8" /> <br>

Here you can view the 2D and 3D imagery generated.

You can change the basemap between many options, by clicking on the four squares icon.

<img width="1651" height="901" alt="image" src="https://github.com/user-attachments/assets/eab1e034-f332-427c-8a5a-bc15631f6d22" />

<img width="374" height="573" alt="image" src="https://github.com/user-attachments/assets/ffc6e0e0-15b1-481b-b3fc-77cb9c941141" />

There are several other options available in this viewing screen. You can explore all of them. <br>

**Step 10:** Download the necessary files. 

You can download the orthophoto, quality report, point cloud (for 3D imagery) etc from the 'Download' tab. The 'Backup' option downloads everything in a zip file.

<img width="1603" height="536" alt="image" src="https://github.com/user-attachments/assets/81245006-1bfc-402b-a071-ece9492bbc50" />

You can download the data log (Task Output log on the console) by clicking on the download icon underneath the 'Task Output' console. This will be useful for troubleshooting any issues.



















[1]: https://docs.webodm.net/getting-started/image-capture/
[2]: https://youtu.be/E5GnutgGH2c?si=ZaDjesyPdX-LCRWC
[3]: https://docs.webodm.org/installation/#docker
[4]: https://github.com/paulvpop/gis-land-cover-mapping/blob/main/01.%20Software%20installation.md#52-podman-and-windows-subsystem-for-linux-2-use-this-for-windows








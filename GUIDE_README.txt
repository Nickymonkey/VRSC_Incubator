Nick Roewe's Guide to VR Unity Development using VRTK with Oculus:

You will need (links for reference):
1) A VR Capable PC (https://www.amazon.com/MSI-i7-7700HQ-Aluminum-GE63VR-Raider-213/dp/B0762P3W26/ref=sr_1_2?ie=UTF8&qid=1541738675&sr=8-2&keywords=vr+capable+laptop)
2) An Oculus Rift + Controllers + Sensors (https://www.amazon.com/Oculus-Touch-Virtual-Reality-System-pc/dp/B073X8N1YW/ref=sr_1_3?ie=UTF8&qid=1541738648&sr=8-3&keywords=oculus+rift)
3) Unity Hub (https://unity3d.com/get-unity/download)

Guide Steps:

1) Using your VR Capable PC & Oculus Rift, perform basic Oculus setup.
2) Download and install Unity Hub (see link: https://unity3d.com/get-unity/download)
3) Under Installs Tab in Unity Hub, make sure you "Unity 2018.1.9f2", if you do not, click on the Official Releases link and download and install "Unity 2018.1.9f2"
4) Now go to this github link "https://github.com/Nickymonkey/VRSC_Incubator" and download the repository to your machine
5) Now in unity hub click "open" and locate "Template_VRProject_Oculus" and open it.
6) Make sure that your Oculus is plugged in and the oculus app is currently running
7) Inside the "Template_VRProject_Oculus" unity project go to the "Scenes" folder and load in the SampleScene
8) Click play and put on your headset, make sure to click the buttons on each controller too so they are online and register, you should be able to look around and see your hands
9) All done you are ready to start VR Development using VRTK

Guides On Developing with VRTK:

VRTK uses a VRTK_SDKManager, this figures out at runtime which headset you are using, so you can use other headsets besides Oculus. You just have to make sure you have the necessary SDKs downloaded.

VRTK has example scenes under "VRTK/Examples/ExampleResources", if you want to try experimenting with these you must do a few things.

1) Once you have loaded in the scene, as an example take "[001 - Interactions] ControllerEvents", you must do the following steps to have it work with oculus
	a) Locate the VRTK_SDKManager in the scene, then under VRTK_SDKManager/VRTK_SDKSetups/Oculus delete "OVRCameraRig" and "LocalAvatar"
	b) Under "Oculus/VR/Prefabs" drag the OVRCameraRig prefab as a child of Oculus in the scene
	c) Under "OvrAvatar/Content/Prefabs" drag the LocalAvatar prefab as a child of Oculus in the scene
	d) Now inspect the "OVRCameraRig" Object that is under "Oculus" in unity, change the Tracking from "Eye Level" to "Floor Level"
	e) Now Inspect the Oculus Object and click the "Populate Now" button, you should see the fields populated
	f) Now Inspect the VRTK_SDKManager object, and click the SDK_Oculus_Avatar button (either one)
2) All done!

If you want to make a new scene and have everything work, you need to have 2 things, VRTK_SDKManager, VRTK_Scripts.
I would reccomend using the VRTK premade scenes as templates and copying and pasting stuff from there.
As mentioned before this will also work with other headsets, you just need to make sure you have the proper SDKS

Any questions email roewe@usc.edu and put in the title "VR Unity Development using VRTK with Oculus Help"
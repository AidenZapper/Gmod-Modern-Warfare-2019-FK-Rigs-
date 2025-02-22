# Gmod-s-Modern-Warfare-2019-FK-Rigs-

This is the rig where everyone can create custom animations for viewmodel weapons. I set up different Blender versions so that 2.79 works with 2.80+ and 3.0+ while 4.2+ remains compatible with 4.0 4.1 4.3 and future versions just in case everything aligns properly. The main issue is that the IK option breaks when recompiling the weapon especially if new bones are added which causes misalignment. Unless there's a fix but this could be a challenge. If the MW Swep Creator team releases a G3A3 on the workshop they might use an IK rig based on their original compile similar to how Viper MW Source Files handled it. Hopefully there’s a solution down the line but for now it’s something to keep in mind.

Quick tutorial:
1. Decompiled any weapons from here[Modern Warfare SWEPS](https://steamcommunity.com/workshop/filedetails/?id=2526457139)
2. To find any weapons you want, use any program to extract GMA. In particular, I need Renetti to model swap the beretta 92fs or M4A1 to HK416.
3. Choose the blender version that works best for you, then import the decompiled MW weapon as an SMD.
4. Then, unless it already has bone, I suppose you can choose the vertex group and assign it to the MW weapon. Otherwise, rig each new weapon mesh separately. Unfortunately I won't go into too much detail in case for new modders. The basic component to rig the main weapon bone is at least tag_pistol_offset for pistols and tag_sling for other weapons.
5. From the bone constraint tab, choose j_shoulder_l as it highlights the green bone. I've already set it up for you, so hopefully it's simpler. After that, set the inverse and to the magazine bone. Then, the same procedure for j_shoulder_r to use the primary weapon bone (tag_sling or tag_pistol_offset)
6. You can now animate! Move the gun to the camera/screen. I hit Numpad 0 to see, but I think it's a good idea to check the animation tab to see what version of Blender you're using after importing the saved file. You can look up references about gun handling techniques online.
7. Or another option The idle animation from the gun you decompiled can be imported. However before exporting, make sure to remove all keyframes other than 0. Since this example uses the default idle pose: [92fs_idlepose_example](https://github.com/user-attachments/assets/01f76b09-33bc-4ef9-a06c-ed3c7ee88847)
you can now reposition it however you like!
8. Next, export the animation you made as an SMD individual and swap out the bodygroup and animation.To prevent an error, set the line *usesequece* to replace all to *usesource* in the $sequence folder if you used a notepad editor, such as Notepad++ or Visual Studio Code. If not, there will be ERROR: 'EXCEPTION_ACCESS_VIOLATION' (assert: 1) which is the compile error message from Crowbar. If you wish to make a new sprint, walk, jog, or other additive animation, I won't go through, so I apologise.
9. After that, compile and boom. To see how the animation works, check HLMV (it's in garrysmod/bin or garrysmod/bin/win64 for the 64-bit branch) and locate the model you've compiled or use the spawnmenu in-game. I hope that this will be sufficient to work for both unofficial modders and experienced modders in the community for long time.Enjoy your use of this and good luck.

I know this is not in-depth and a bit confusing, so hopefully this one will encourage people to enjoy or modding using MW base in Garry's mod. Just to let you know, I won't be able to work on this because gmod is an old game, but I want to focus on my happy life and future job and dreams, so I hope you guys understand what matters that I've been going through tough times and bright times for anyone who used to know me back in the days, and I guess this could make the playerbase more interested.

## Credits:
* Activision, Infinity Ward, Ben Garnell, Peter Chen, Ben Turner, Mike Velasquez, Jeremy Thurman, Alexandr Khaliman, Ed Fedorei, Nikolay Myhalenko, Aaron Beck, Ranon Sarono, Khoa Le, Mark Grigsby, Troy Irving, Benjamin Turtell - All the assets that were used for the model and guns.
* Viper - Porting models, animations, sounds and compiling the models.
* Mushroom Guy - Coding the base.
* Me - Providing and modifying into an FK rig

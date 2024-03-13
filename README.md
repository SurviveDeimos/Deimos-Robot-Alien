# Deimos Alien Drone

This is the source code from the following mod https://www.curseforge.com/ark-survival-ascended/mods/deimos-cosmetics-alien-drone


## How to Download and Install this project in to your own mod

You will need to copy the contents of the 'Content' folder in to your own created mod folder. Download this project as zip file, extract all files, and just copy all the files and directories in Content folder to your mod folder. 

For example copy everything in the Content/*.* to your d:\Epic\ARKDevkit\Projects\ShooterGame\Mods\MyNewMod 

Your structure should look like d:\Epic\ARKDevkit\Projects\ShooterGame\Mods\MyNewMod\Character

## Current workflow how this mod was created

- The Ark Human Male object and its bones was used and exported to a 3D modeller. You can find the object in your devkit at this location /Content/PrimalEarth/Human/Male/Human_Male_TPV
- A free 3D model was downloaded in this case Alien Suit at sketchfab (Created by NatalieDesign). This was a rigged character (makes it easier) however didn't had an A-pose or T-pose so still needed to reposition everything to an A-pose
- The model was repositioned and deformed so it mostly fits the Ark Human Bone structure, and after this binded to the new bone structure from the Ark model, and redone all weight painting. This is is mostly the hardest part because not every character will fit the bone structure. There are a lot of tricks you can do with characters that look completly different or are way smaller etc however i'm sticking a bit to the basics up here.
- When you import your new model, you also need the animation blueprint and ground conform blueprint (these are also copied from the Ark Human male char). Make sure you set your new model (references) correctly in those blue prints. And don't forget the Ground conform blue print references.
- In this mod there is a directory called AnimationTests. Those are just 3 animations copied from the Ark Male character but of course you can add way more. These are very important to test your new 3D model for example most of the issues appear when crouching when you have weight paint issues. Just add your new 3D model as reference to see if everything is working correctly.
- Keep in mind that a CharacterSkin has 2 seperate 3D models. One for the Third person view TPV (the one we created) and a First person view that only contains the arms FPV. In this mod we just copied the Ark Human Arms Human_Male_FPV. While it's pretty simple to do and is the same as creating the main char I skipped this part and just used the same model.
- From this point you are mostly done and you need to assign your model and anim bp's to the in this case PrimalItemSkin_CharacterSkin_DeimosAlienDrone. You will notice that everything is assigned twice. This is because the first index 0 is the male and the next index 1 is the female. So add your TPV and FPV models the same way and don't forget to add the anim blue prints.
- Change the description in the PrimalItemSkin_CharacterSkin and add a new Hud (Item_Icon) to the bp.
- One thing that you should be aware off is that it is kind of buggy. If you choose compile, you will loose your Mesh Skeleton referenced and you have to readd them.
- When you are done with the PrimalItemSkin_CharacterSkin_... You will need to add them to your ModDataAsset_.... asset which is in the root folder. This shouldn't need much info. The Apply to classes is always PrimalItemSkin_PlayerCostume_Custom and the Mod Skin Item is the PrimalItemSkin_CharacterSkin_... you created.
- The ModDataAsset_.. needs to added to your PrimalGameData_BP_... (Just search for ModData)
- And of course you need to assign the PrimalGameData_BP_... to your level

 ## Materials

 The base Material is kind of mess (too many options) but it gives an example how to easily change colors on your texture. And since the color variable names are called Color0 and Color1 this also works on paintable items/color regions. 

 ## Notes

If you want to check what Deimos is up to check our Discord at.
https://discord.gg/9qj97HXV9M

If you want to start modding or have mod specific questions, join the ASA Modding Discord 
https://discord.gg/4FAVpagKhD




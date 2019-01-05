# Team 8 Workshop Guides: How to Operate and Maintain the Ultimaker 2 Extended+

# Table of Contents
* [What is a 3D printer?](#what-is-a-3d-printer)
* [Anatomy of a 3D Printer](#anatomy-of-a-3d-printer)
* [Safety](#safety)
* [Basic Operations](#basic-operations)
  * [Initial Setup](#initial-setup)
  * [Basic Controls](#basic-controls)
  * [How to prepare a model for printing](#how-to-prepare-a-model-for-printing)
  * [How to print a model](#how-to-print-a-model)
  * [How to switch materials](#how-to-switch-materials)
  * [Taking the print off the bed](#taking-the-print-off-the-bed)
* [Material Options](#material-options)
  * [PLA](#pla)
  * [ABS](#abs)
  * [Exotics](#exotics)
* [Maintenance](#maintenance)

## What is a 3D printer?
What is a 3D printer? Well, the ones that aren’t crazy expensive are essentially computer numeric controlled (or CNC) hot glue guns that extrude molten plastic rather than glue. This category of 3D printers (which our lab printer is part of) is referred to as FDM, or Fused Deposition Modelling. This sounds very sophisticated, but it’s essentially describing how our printer prints objects: by depositing material (in our case, molten plastic) that fuses together to form a model. There are fancier categories of printers that use different techniques, but they are outside the scope of this manual.

## Anatomy of a 3D Printer

![alt text](https://d3v5bfco3dani2.cloudfront.net/photo/image/1300x0/57ab28770da47/Ultimaker-2-Plus_front_annotated.png)

## Safety
As far as the machines in our lab go, the 3D printer is fairly safe. There is one primary safety concern you need to be aware of. The 3D printer can get extremely hot. The print bed can reach temperatures of 60 degrees C, and the nozzle can reach 260 degrees C. This will most certainly burn you. While operating or maintaining the machine, make sure that the components have cooled down before handling. The enclosure is safe to touch, but keep your hand out of the interior unless absolutely necessary.

## Basic Operations:
### Initial Setup
In order to turn your model into instructions that the printer can understand, you will need to use software known as a “slicer”. It converts your model into tiny little slices that the printer will print out layer by layer. There are many different slicer apps, but we suggest you use Cura, the slicer made by Ultimaker. It’s very beginner-friendly, but allows you to access more advanced settings if need be. You can download Cura here. (The current version is 3.4.1 and is what is being discussed in this manual)

In Cura, you want to make sure that you have selected the correct printer type during initial setup. The lab printer is an Ultimaker 2 Extended+. This tells Cura how big the printing volume is. You can add new printers later if need be. Load your model into Cura (we typically use .STL files). Now we prepare the settings for printing.

### Basic Controls
* Rotating around workbed
  * For Windows OS users: Hold your right click on the mouse you are using and drag around
  * For Mac OS users: Hold CTRL+click and drag around
* Zooming in and out
  * For Windows OS users: Use the scroll function on your mouse
  * For Mac OS users: Use the scroll function on your mouse
* Changing views of the print
  * At the top right of your Cura software there are 3 options for views:
    * Solid View:
This will show you the outside of the model and if you look on the bottom side of the model you may see red highlighted areas. This signifies that supports would be helpful to have.
    * X-Ray View:
This will show you the inside of the model along with the outside.
    * Layer View:
This will show you all the different components of your model. This view can help a lot when you are trying to make sure the print will come out the way you want it to. It will also show the nozzle path and what the print looks like at each layer.
* Uploading files onto Cura
  * For Windows OS users:
Press CTRL+O and your file explorer will open. Choose your model from there.
  * For Mac OS users:
Press CMD+O and your file explorer will open. Choose your model from there.

### How to prepare a model for printing
1. Upload your 3D model.
2. Check your settings!
    * Nozzle Size
      * First, choose your nozzle size. We have four different sized nozzles, but the one we use most often is 0.6mm. Unless you have a specific need for a different nozzle size, don’t change the nozzle.
    * Material
      * Next, select your material. There are many types of filament (more on that in Material Options), but for now, just make sure that you select the material that is on the back of the printer. You can always just look at the spool to check the material.
    * Recommended Settings Menu
      * Layer Height
        * This setting is how thick/thin the layers the printer lays down are. The thinner the layer is, the higher quality the print is as it is harder to see each layer of plastic. If you are making a cosmetic piece, and you want it to look as good as possible, use a thinner layer height. (For example, set it as 0.06 mm) Note that this will slow down the print (you can see a time estimate in the bottom right corner of the viewport), so balance quality against how much time you have. If you’re printing a functional part and aren’t overly concerned with how it looks, you can choose a thicker layer like 0.2 mm or even 0.4 mm.
      * Infill
          * This refers to the amount of filler material placed inside your model. If you do not need the piece to be structurally strong (for instance, if it’s a decorative piece that will not experience much if any stress), you can use hollow or light levels of infill. If you’re making a functional part (particularly if they’re robot parts), you want to use heavy or completely solid infill. It’s also worth noting that if you need a very strong part, you will most likely want to use ABS filament, and not PLA. More on that later, but keep in mind that PLA (which is what we generally use), while easy to work with, is not necessarily as strong as some other materials.
      * Enable Gradual Infill
          * This setting will make it so the infill gradually becomes denser towards the top of the part. This will also increase your print time though. This can be helpful in making sure the top of the print is closed properly without using an unnecessary amount of infill in the whole print.
      * Generate Support
          * The default support option you can turn on or off is support structures. These are breakaway pieces of plastic that the printer places in order to properly print parts of your model that are hanging in the air. The printer can generally handle very gentle inclines without support, but if you’re printing complex pieces in air, you should use supports. One thing to look for is areas of your model that are highlighted red in the Cura viewport. Cura is telling you that those areas will likely not print properly without support.
      * Build Plate Adhesion
          * Finally, you want to either turn on or off the option to have a brim. This is a small, single-layer band that wraps around your piece. This helps the part stick to the bed by increasing the first layer surface area (which can be helpful if your part is particularly small). We highly recommend you keep this setting on for all parts.

Cura is now ready to slice your file and export it as a G-code file. G-code is instructions for CNC machines, like our printer. It tells the printer’s motors how to move in order to print out our part! Hit the “Prepare” button, and Cura will slice everything. The fastest way to get the file onto the printer is by removing the SD card located on the lower front panel of the printer, and inserting it into your computer. After doing this hit the “Save to SD” and the code will save onto the SD card. When it’s done, remove it and place it back into the printer.

  * Custom Settings Menu
      * Quality
        * In this setting you are given the option to change the “Layer Height.” This has been discussed in the above section as well. However, in this case you can precisely change the layer height to your desired thickness.
      * Shell
        * In most cases you will not need to change this setting. This will allow you to change how thick the outermost layer of the print is. There is a wide range of numbers you can adjust in order to change the shell.
      * Infill
        * This setting can also be changed in the Recommended Settings Menu, but in this menu you can change the specific percentage infill as precisely as you would like to. You can also change the “infill pattern,” which is the shape the infill is printed inside the model. Depending on your application, some patterns are more beneficial than others.
      * Material
        * In this setting you can choose whether or not the filament will retract whenever it is not printing. The filament retracting will eliminate the possibility of extra filament melting through the nozzle and dripping during the print. We highly recommend keeping this setting on.
      * Speed
        * Print speed is how fast the printer nozzle is moving while laying down each layer. We highly recommend leaving this setting the way it is.  
      * Travel
        * This setting will allow you to make the nozzle travel over the print instead of along the top of it. Useful if the you're having issues with the nozzle knocking the print over. Off by default.
      * Cooling
        * This setting will allow you to control the speed at which printer fans are running at, and whether they are on or not. Keep the fans running all the time, and at 100% as this will make sure the print quality is good.
      * Support
        * This setting allows you to generate supports just like in the Recommended Settings Menu. However, in this menu you can choose where the supports are generated. They can either be generated everywhere, including on top of the model, or just from the build plate. The “support overhang angle” is the minimum angle until supports are generated. If there are parts of the model where the angle is less than this set angle, supports will be printed. You can also choose what kind of “support pattern” is printed, like with the Infill.
      * Build Plate Adhesion
        * There are 4 different options for build plate adhesion:
          1. Skirt
            * This will print a single layer line printed around the model as a way to show the filament is extruding properly.
          2. Brim
            * This will print a single layer flat area around the model as a way to make sure there is a greater surface area on the build plate. This will help with keeping the print from warping or coming off of the bed.
          3. Raft
            * This will print a thick grid with a roof under the model as a way to make sure you have a flat. We have not had a need to print this as it consumes a lot of time, and the build plate is flat enough already.
          4. None
            * This will print nothing. What a surprise!

### How to print a model
A couple of reminders before you print. Make sure that the material loaded into the printer is the type you intend to print with. Double-check your Cura configuration for any issues/unintended settings. Apply adhesive to the build plate if necessary. (This is explained later in Materials Options)
Once you’ve loaded your G-code onto the SD card and placed the SD card back into the printer, all you need to do is use the navigation wheel at the bottom of the front panel to navigate to “Print”, click the wheel, and then navigate to your part (make sure you know the name of the part!), and click once more. Your part should now begin printing!

### How to switch materials
Use the click wheel to select “Material”, and then “Change”. The printer will heat up the hotend in order to soften the current material so it removes cleanly.
Once it is done, it will automatically reverse the material back out of the printer. Then, take the spool of filament off the printer, and place your new material of choice on the spool holder.
The printer screen will now prompt you to insert the new material. Take the end of the filament, and place it in the hole that leads to the extruder gear assembly (this is a white box that protrudes from the back of the printer).
If you’re having trouble, turn the printer around and look for the arrow that points directly to said hole.
Give the filament a good push into the extruder assembly, so it is grabbed by the extruder gear (the silver cylindrical object inside the extruder assembly), and while applying upward pressure to the filament, press the click wheel to confirm you have inserted the material.
If you’ve done it correctly, the extruder gear will grab onto the filament and spin, pushing the filament along the bowden tube until it reaches the nozzle. You’re done!

### Taking the print off the bed
Always wait for your print to cool down
The display on the printer will tell you whether it is cooled down or not
This makes it a lot easier to remove the print and it keeps the printer from getting damaged
With PLA you’ll most likely be able to just take it off with your hand as it usually just falls off the bed
With ABS you’ll likely need to use a chisel to remove it

## Material Options:

### PLA

#### Attributes:
  PLA, or Poly Lactic Acid, is a biodegradable plastic that is made out of corn starch/sugar cane. It smells sweet when printing (not just a fun fact, this also means ventilation is not an issue when printing with PLA), and is generally very easy to work with, for a number of reasons. It tends to hold its shape as it cools, which is why it can be printed on a non-heated bed if necessary, and it’s less prone to warping during the printing process. It also often sticks to the bed with just heat alone, which is very convenient!

  However, it does have its downsides. It is not as sturdy as some other plastics, most notably ABS, nor is it as flexible. PLA tends to be brittle. It also does not hold up well under high heat. While it is printed out at temperatures of ~200℃ (~392℉), it can start to deform at around 80℃ (176℉). It’s also worth noting that PLA tends to just melt rather than burn at extreme temperatures, which can make machine maintenance easier.

#### When to use
* If you’re making an art piece (i.e. not a functional or structural piece), or a functional piece that does not experience strong forces at any time, PLA is fine.
* If you want to get started 3D printing, and don’t know where to start, PLA is recommended. It’s much easier to work with than a lot of the other filament types.
* If you’re using a printer elsewhere that does not have a heated bed, PLA + some blue tape placed on the build plate is probably your best bet.

#### When not to use
* If you need to make a part that is flexible, industrial strength, or resistant to high temperatures. Cannot stress this enough. PLA is an excellent material to work with, but it can’t do everything.

#### Additional Instructions
Typically, on our lab printer, an adhesive on the bed is not required for PLA, as PLA sticks to the heated glass plate very easily. If you experience issues with items not adhering to the bed, you can use a thin layer of glue stick. The nice thing about purely relying on the heat to keep the PLA stuck to the bed is that when the bed cools down, the piece will oftentimes pop right off (so you don’t have to break out a chisel or anything!).

### ABS

#### Attributes
ABS, or Acrylonitrile Butadiene Styrene (but no one calls it that), is an industry-grade thermoplastic. It is trickier to work with than PLA for a number of reasons. It requires a heated build plate, as ABS will shrink dramatically without one. It is also more finicky when it comes to properly adhering to the build plate, heat alone is usually not enough. However, ABS is much stronger and more resilient than PLA, and can bend before breaking. It prints in the 220℃ to 260℃ range, depending on what mix of plastics your filament is. While Cura does have recommended settings for this material, finding the perfect temperature takes a little experimentation, check out the troubleshooting guide if you want help!

ABS can also be treated with acetone, which is capable of dissolving it. This may not sound particularly useful, but if you want to “weld” two ABS printed parts together, you can apply a tiny bit of acetone to the joining areas of each piece to get them to bond together quite nicely. This is not possible with PLA, unfortunately :( ABS can withstand more heat than PLA can. However, ABS does tend to burn at extreme temperatures, which can lead to clogging the nozzle (check out the maintenance section for how to deal with that!).

#### When to use
* If you are making a functional and/or structural piece that needs to withstand strong forces and can withstand bending without breaking, ABS is the way to go. It is industry grade plastic, very commonly used in industrial settings.
* If you need your part to resist high temperatures.
* If you need to make use of the acetone “welding” maneuver to assemble parts, use ABS. It will not work with PLA.
* If you are worried about your part breaking where you’re using it, use ABS.

#### When not to use
* If you’re printing a decorative piece. It is generally not necessary for such tasks.
* If you’re just getting started printing, and you’re not as familiar with the printer, ABS can be tricky to start with. It’s a lot more finicky than PLA is.
* If you don’t have any adhesive on hand, ABS is most likely not going to work out for you.

### Exotics

#### Attributes
Well, “exotics” refer to the category of filaments that are...well, exotic, meaning filaments with interesting mixes of materials and/or properties. Things like carbon fiber infused filament, wood filament, filament with precious metals in it, filament that is extremely flexible after printing, the list goes on.

#### When to use
* Depends on what you need! If you have a specific use for a type of exotic filament, then use it! This will require some research! Self-research is very important skill to have in the maker community.

#### When not to use
* If the material is too expensive, or simply unnecessary for the task at hand! Probably not the best idea to use gold filament for every single print!

#### Additional Instructions
Do your research on the material you’re using, and follow those instructions carefully! Exotics can be finicky to work with, and following instructions is the most important part to getting it to work properly. And when in doubt, ask someone else, like your lab manager!

## Maintenance:
How to level the build plate
https://ultimaker.com/en/resources/17083-bed-leveling

How to change the nozzle
https://ultimaker.com/en/resources/18777-changing-nozzles

How to unclog the nozzle
https://ultimaker.com/en/resources/19510-how-to-apply-atomic-method

Troubleshooting:
Print Quality Troubleshooting Guide
http://support.3dverkstan.se/article/23-a-visual-ultimaker-troubleshooting-guide

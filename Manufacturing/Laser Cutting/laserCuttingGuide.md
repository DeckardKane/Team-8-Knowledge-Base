# Team 8 Workshop Guides: How to Operate and Maintain the Voccell PRO43 100W Laser Cutter

## What is a laser cutter?

A laser cutter is a laser that can vaporize materials to either cut or engrave on them. The laser is computer numerically controlled or CNC. The type of laser used in our laser cutter is called a CO2 laser. Materials are vaporized by the heat of the laser. This is why you smell burning wood when cutting things like plywood. Laser cutting is the process of precisely cutting or engraving a material using focused high-powered laser beam, directed by CNC machine from a CAD vector file. Like any other CNC machine this runs on G code. This is just like 3D printing, the CNC mill, and the CNC router.

### Anatomy of a laser cutter
(Insert Image)
As you can see in the image above there is a laser tube that produces the actual laser that vaporizes the material. The laser is then sent to a series of mirrors and then one lens that focuses it to a single dot. The red dot you see on the material is actually just an indicator of where the laser head is. It does not do any of the cutting or engraving. Inside the laser tube there is a coil around the inner portion of the tube. This is where the chiller sends and circulates water to keep the tube as cool as possible. Heating up shortens the life of the laser tube. The laser head is on a slide control system where rails allow it to move in the X and Y direction. There is also an air compressor that blows air out of the laser head to get rid of any dust that is in the way of the laser. The first image shows this. The control board and stepper motor drivers are inside the laser where you cannot easily see them. Do not try and mess around with them. They will ruin the laser if you do that. The vacuum bed in the first image is where the dust and smoke is sucked out to the outside using an exhaust fan. Our laser also has a Z axis which controls the bed height. This is adjusted to change the distance from the laser head. I will explain this concept in more depth in the **Basic Operations** section.

## How does laser cutting work?
This section is going to describe how laser cutting works in more depth. The laser beam is a column of very high intensity light, of a single wavelength. Our laser is a CO2 laser so the wavelength is in the Infared part of the light spectrum. This also explains why you can’t see the laser that actually does the cutting. The diameter of the laser before it goes into the laser head is around ¾ of an inch. This beam is usually bounced off a series of mirrors so that it reaches the laser head. This is just for space efficiency. The laser beam is then focused in the laser head with a focusing lens and shot through the bore of the nozzle before it hits the plate.

Focusing the laser beam has to be done with a curved mirror or focusing lens. The beam has to be precisely focused so that it is perfectly round and consistent, and centered in the nozzle. By focusing the large beam down to a single pinpoint, the heat density at the spot is extreme. This is like taking a fresnel lens and burning some paper or wood. (Not that I did this before in the lab :P). 

The high power density results in rapid heating, melting, and partial or complete vaporization of the material. 

## Safety
Just like any other machine as long as you use your common sense while operating it. 
1. **WATCH THE LASER WHENEVER IT IS RUNNING**
2. Keep the lid closed, watch the laser head while it operates and moves around so there’s no fire in the laser. 
    * The laser won’t operate without the door closed
3. Follow **ALL** instructions in this manual

## Basic Properties
* 48” x 36” work bed
* 100 W CO2 laser
* Ventilated 
* Air compressor 
    * Blows air to remove dust from cutting area 
    * Keeps mirrors and lenses clean
* Water chiller 	
* Keeps laser tube cool
* All lasers have “laser kerf” 
    * Laser kerf = material loss 
    * This is variable and depends on material and thickness
    * **You MUST do a test cut to make sure your settings are ready for cutting your actual piece!**
* The cut wall is angled away from the beam on the top surface of your material
(Insert Image)

## Basic Operations

(Insert Image)

* ### Vector Cutting
    * The two basic operations of a laser cutter are vector cutting and raster engraving. In this section I will be discussing the steps on how to vector cut something with the laser. 
    * The software that we use to control this laser is called LaserCut53. This is already installed on the desktop that is connected to the laser. To run this software you need to keep the green USB plugged in and the USB plug for the laser cutter. 
    * After everything is plugged in open LaserCut53. After you open it you should see a grid and settings on the side of the screen. 
    * For vector cutting you will want to upload a .dxf file. This is the file that has all the vector lines and paths that the laser head will follow. 
    * Upload the file onto LaserCut53, and move the vector file around the grid to wherever you want to place it. 
    * After you double...maybe even triple check that the laser will not affect anything else on the bed you can run the vector cut. Make sure that the settings for power and speed are correct for the material and thickness you are cutting. Also, make sure that the mode your cut is in is set as “cut”. There are other options like “engrave” and “GradeEngrave” so make sure it is set as “cut”. Lastly, check to see that the lines of the vector file are the same color as the color in the layer column. You can find settings next to your desktop on the left of the desk. 
    * After you place it on the grid place your workpiece in the laser by lifting up the laser cutter’s lid. After you place the material on the work bed adjust the Z axis. On the right side of the screen there are coordinate settings. Press “Z datum” and the laser cutter will focus for you. 
(Insert Image)
    * Run a test cut before you load your actual file onto the software. This step is necessary and will make sure that the settings are good for cutting through your material. 
    * You can upload the test cut file by going to Documents-->User Folders-->Test Files-->the .dxf file in that folder. This file will be a small team 8 logo for people to cut out. 
    * Once the distance is set you will want to trace the perimeter in which the laser will be cutting the material. Move the laser head to your desired part of the material by using the X and Y pad next to the Z axis buttons.
(Insert Image)
    * By doing this you can assure that the laser will not run over anything else. Do this by pressing “Run Box”. During this process make sure that the yellow probe and laser head to not get too close to the material during any of the cut. 
(Insert Image)
    * After the cut is complete open the lid and press down on the part you have cut out. This is to check if the laser actually made it all the way through and finished the cut. If you do not feel it separate from the material, run the same job again. 
      * Doing this may make the finish on the material a bit uglier than expected, but if it is to get the job done you will want to do so. 
    * To send the g code to the laser you should press “download”. After hitting download you must hit “download current”. This will send the g code over to the laser. Then press start and watch the laser throughout the whole process to make sure nothing breaks. 
(Insert Image)

* ### Raster Engraving
    * The process of vector cutting and laser cutting are very similar. 
    * To start you must upload a .dxf file or .png file to LaserCut53.
    * Follow this section if you are using a .png file! 
      * Before you upload the files though you must convert the colors to black and white for .png files. This is so that the laser can easily know which parts to engrave at what settings. The colors in the “layer” column correspond with different parts of the image to engrave. 
        * You can use colors besides black and white, but that is a bit complicated for what we are discussing in this Basic Operations section. 
      * Once you upload the image you should change the settings of the engraving to follow the settings that are on the left side of the desk. 
      * Again, place the material in the laser and press Z datum. After this you can trace around the engraving area. 
      * Once the distance is set you will want to trace the perimeter in which the laser will be cutting the material. Move the laser head to your desired part of the material by using the X and Y pad next to the Z axis buttons.
      * To send the g code to the laser you should press “download”. After hitting download you must hit “download current”.
      * Close the lid and run the engraving while watching the whole process. 
    * Follow this section if you are using a .dxf file!
      * Import your .dxf file onto the software. 
      * Change the mode of the laser to “GradeEngrave” and select the lines that the laser should engrave in. 
        * If you only want to engrave in parts of the file then change the color of the lines by selecting and clicking on a certain color at the bottom of the screen. 
      * Again, place the material in the laser and press Z datum. After this you can trace around the engraving area. 
      * Once the distance is set you will want to trace the perimeter in which the laser will be cutting the material. Move the laser head to your desired part of the material by using the X and Y pad next to the Z axis buttons.
      * To send the g code to the laser you should press “download”. After hitting download you must hit “download current”.
      * Close the lid and run the engraving while watching the whole process.
* ### Both Cutting and Engraving
    * This part is a bit complicated, and may take some time to get used to. 
    * Focus the laser by pressing Z datum after placing your material in. 
    * Then upload the file that you want to cut and engrave. An example of this might be some plaque with text engraved, but the plaque itself is cut out. Import a .dxf file!
    * Make sure the vector cut part and engraving parts are different colors so you can adjust the different settings for different parts of the cut and engraving job. 
      * For example: The cut parts should be black lines while the engraved parts should be red lines. 
      * To change line colors highlight them and select the colored squares at the bottom of the screen. 
    * For the section that you will cut change the mode to “cut” and for the section you will engrave change it to “engrave” or “GradeEngrave.”
      * “Engrave” is for just engraving the lines while “GradeEngrave” is engraving the space between the lines highlighted. 
    * Again, place the material in the laser and press Z datum. After this you can trace around the engraving area. 
    * Once the distance is set you will want to trace the perimeter in which the laser will be cutting the material. Move the laser head to your desired part of the material by using the X and Y pad next to the Z axis buttons.
    * To send the g code to the laser you should press “download”. After hitting download you must hit “download current”.
    * Close the lid and run the engraving while watching the whole process.

## Material Options
(Insert Image) 

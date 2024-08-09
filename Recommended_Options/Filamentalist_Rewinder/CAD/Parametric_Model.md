<h1 align="center">Filamentalist Parametric Model</h1>

If you are using Autodesk Fusion 360 the .f3d file here is a parametric based model allowing you to customize the width of your rewinder to suit your max/min spool widths and/or to design around a standard available steel axle length.

To customize your Filamentalist width and axle sizing load the model, make sure you are in the "Solid" menu, and then select "Modify" and "Change Parameters"

<img src="https://github.com/SkiBikePrint/Filamentalist/blob/9d7a90dc3dec40c67051558c80c616155eb8eba8/Assets/Change_Parameters.jpg" width="400" height="350">


<img src="https://github.com/SkiBikePrint/Filamentalist/blob/9d7a90dc3dec40c67051558c80c616155eb8eba8/Assets/parameters.jpg" width="900" height="350">

Adjust the following parameters to meet your needs:

**Spool_Width_Max** - Set this to accomodate the widest filament spool you expect to use.  It is recommended to add ~2mm to this number to allow for spool width and rim straightness/variation.

**Spool_Width_Min** - Set this to accomodate the narrowest filament spool you expect to use.  Due to the width of the Tensioner Assembly the minimum spool width is constrained at 34mm and will default to this number if you enter something less than 34mm.  If you don't expect to use narrow spools (like 250kg or 500kg spools) you can set this to a larger number to produce narrower Rim Rollers.  Narrower Rim Rollers will reduce print time and filament consumed and may allow for usage of more standard less expensive rubber bands but will limit overall future flexibility of your rewinder.

**Min_Spool_Rim_Thickness** - Normally this can be left at the default of 3mm but if you are trying to squeeze narrow spools onto the rewinder, you are close to that 34mm minimum width, and your narrow spool rims are less than 3mm thick, you can adjust for your thickest rim of your  narrowest spool to make it fit the rewinder.

**Axle_Under_Over_Hang** - This can be either a positive or negative number and is used to tweak the design to use a standard available axle length (like 80mm or 100mm).  A negative number will result in the axle ends sitting inside the footprint of the rewinder but the model logic will not let you underhang more than 3mm inside the 608 bearing race to ensure good support of the axles from the bearings.  A positive number will result in the axle protruding beyond the footprint of the rewinder.  You may want to do this if you are going to use a readily available 100mm length axle but don't need a rewinder that can support spool widths as wide as 86mm, thus saving printing time and plastic by using a lesser Spool_Width_Max like 75mm.  The best case scenario is to set this value at 0 and you have the ability to cut shaft stock to the exact length for your desired Spool_Width_Max (i.e. Spool_Width_Max = 75mm to accomodate virtually all 1KG spools and cut shaft to 88.5mm length).

**Axle_Length** - DO NOT CHANGE THIS PARAMETER!  It is there for reference to help you tweak into a standard and readily available axle length.  You can tweak on Spool_Width_Max and Axle_Under_Over_Hang and iterate these values until you arrive at an overall result that meets your needs.

The model will update and accurately show the results of these parameters to help you visualize the acceptability of the result.

```python
#!/usr/bin/env python

from gimpfu import *

def gimp_plugins(image,drawable, maxheight=500, maxwidth=500, savecopy=TRUE): 
currentWidth = drawable.width 
currentHeight = drawable.height 
newWidth = currentWidth 
newHeight = currentHeight 
on the off chance that (maxw > newWidth): 
newWidth = maxwidth 
newHeight = (float(currentHeight)/(float(currentWidth)/newWidth)) :
register(
 # name of the solicitation you bring from the request brief 
"python_fu_resize", 
# The framework program shows information about the module. 
"Saves the image at a most outrageous width and height", 
# The draftsman of the module 
"Kennedy Mwangi", 
# The plug-in's copyright holder. 
"Kennedy Mwangi", 
# The copyright end date 
"2021", 
# The menu name that the module livelihoods. 
"<Image>/Image/Resize to max ", 
# The procedure limits for the module 
    "*",
    [
		(PF_IMAGE, "image",       "Input image", None),
        (PF_DRAWABLE, "drawable", "Input drawable", None),
         (PF_FLOAT, "float", "input maxheight", 500),
        (PF_FLOAT, "float", "input maxwidth", 500)
	],
    [],
	menu="<Image>/Image/Resize to max ")
main()
```
```python
#!/usr/bin/python
from gimpfu import *
def gimp_plugins(image,drawable, maxheight=500, maxwidth=500, savecopy=TRUE): 

# elementary calculations
currentWidth = drawable.width 
currentHeight = drawable.height 
newWidth = currentWidth 
newHeight = currentHeight

if (maxwidth > newWidth): 
newWidth = maxwidth 
newHeight = (float(currentHeight)/(float(currentWidth)/newWidth)) :

if (maxheight < newHeight): 
newHeight = maxheight 
newWidth = (float(currentWidth)/(float(currentHeight)/newHeght)) 

# method to resize the image 
pdb.gimp_image_scale(img, newWidth, newHeight)

# saving the image as jpg
    if savecopy:
        pdb.file_jpeg_save(img, drawable, img.name+".jpg", img.name+".jpg",
                           0.9, 0, 0, 0, "", 0, 0, 0, 0)
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
    "RGB*, GRAY*",
    [
		(PF_IMAGE, "image",       "Input image", None),
        (PF_DRAWABLE, "drawable", "Input drawable", None),
         (PF_FLOAT, "maxwidth", "input maxheight", 500),
        (PF_FLOAT, "maxheight", "input maxwidth", 500),
        (PF_BOOL, "copy", "Make a JPEG copy", TRUE),
	],
    [],
	gimp_plugins)
main()
```

# My notes from doing youtube tutorial "FreeCAD 1.0 Ultimate Beginners Crash Course in 1 hour for 3D printing CAD Lesson / Tutorial"

See https://youtu.be/ZPsLhvgU8kc 

## On macOS you 'Home' the 3D view with key 'Fn' + 'Arrow Key Left'

There is now 'Window' key on a Macbook pro keyboard. So to 'Home' the 3D view Freecad uses 'Fn' + 'Arrow Key Left'.

## A 'Body' is a *thing* that contains 'Parts'

So, Freecad semantics is a bit opaque. But it seems a 'Body' is something in Freecad that cointains 'parts'?

## It seems the 'Part Design' workbench provides tools to *design* the parts of a 'Body'? 

![The Part Design selected in the Workbench drop-down list](image.png)

...

![The Create body tool button](image-1.png)

## We can create a 'Sketch' within the 'Part Design' workbench (although a 'Sketch' is kind of a '2D Draft' *thing*)

I am still confused about what a 'Workbench' actually is? I am at least able to create 2D sketches in the 'Part Design' workbench although they are 2D drawings and one could be misstaken that you would need to go to the 'Draft' workbench for this? But no, that is not how it works.

![Create Sketch tool button](image-2.png)

## The 'View Sketch' tool button seems handy to get back to a good view of current open *sketch*?

![The View Sketch tool button](image-3.png)

AHA! When I click the 'Create sketch' tool button I *actually go* to a '

![The Sketcher selected in the workbench drop-down list](image-4.png)

## The cursor coordinates shows only after the 'Create Rectangle' (any create?) tool is activated

![The 'Create Rectange' tool button](image-5.png)

...

## The 'Create fillet' tool is a mutating tool (not a transforming tool)

![alt text](image-6.png)

It seems when I create a fillet it mutates the 'corner' of two lines into 1: two shortened lines and 2: an arc in place of the corner?

Like, we have this 'corner'.

![alt text](image-7.png)

If I click the 'Create fillet' tool and then then the two lines that meet in the 'corner' - Then we get an arc created and inserted at the 'corner'.

![alt text](image-8.png)

Also, it seems I need to 'dimension' the arc (the fillet) manually using the 'Dimension' tool?

![alt text](image-9.png)

...

![alt text](image-10.png)

## We use 2D 'Profiles' on a sketch to 'extrude' by *padding* to a 3D 'Body'

It seems the semantics of Freecad is to draw 'Profiles' (a closed perimeter made up of lines between points) on a 'Sketch' (a 2D drawing) and then use the 'Pad' tool to *extrude* each 'Profile' into a 3D object called a 'Body'?

In this tutorial the presenter shows how to sketch this 'profile'.

![alt text](image-11.png)

That we then select in the 'Model' and apply the 'Pad' tool on.

![The 'Pad' tool](image-12.png)

And we get a new 'Body' named *padxxx*

![alt text](image-13.png)

...
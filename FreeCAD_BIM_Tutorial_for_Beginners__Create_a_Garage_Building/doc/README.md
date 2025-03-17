# My comments following youtube video 'FreeCAD BIM Tutorial for Beginners | Create a Garage Building'

See (https://youtu.be/WZHyUBfdgJA?list=PL3wRqQUPtE16yw_c1TnRYJmz37y2ZRTLm)

## BIM workbench rectangle has a 'make face' property

The presenter 'turns off' the face of the first drawn rectangle.

![alt text](image.png)

It seems I have to learn how FreeCad presents 'things' in the BIM workbench? To me a rectangle is more the boundary that an area. But on the other hand, I can buy that a rectangle can have a 'face' or not by its 'Make face' property.

## BIM workbench Wall tool

It seems the BIM wall tool can create a 'wall object' from scratch or from one of a 'wire', a 'face' or a 'solid'.

![alt text](image-1.png)

*I wonder what creating a wall from a solid would imply?*

## Alignment of Wall from rectangle refers to walking the rectangle boundary in clockwise direction

If I 'right align' my created wall it seems it is placed 'inside' the rectangle? Whuch in turn sugests that in a rectangle all 'wires' are oriented clockwise around the rectangle center?

![alt text](image-2.png)

![alt text](image-3.png)

![alt text](image-4.png)

## The Line colour of the rectangle is shown ONLY when not selected!

I changed the rectangle 'Line color' to red but the rectangle was still blue!

![alt text](image-5.png)

Only when i clicked outside anything did the red colour show.

![alt text](image-6.png)

## The BIM 'Site' object maps to top level of 'Industry Foundation Classes (Ifc)

See (https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

![alt text](image-7.png)

## The BIM workbench uses a movable 'working plane' for drafting

It seems in the BIM workbench we are to 'draft' as in draw 2D geometry to then use e.g., to create 3D objects.

The presenter in the tutorial shows how to turn on snapping to the working plane.

![alt text](image-8.png)

When snapping to working plane I can draw the rectangle on the top of the external walls and still have the rectangle placeb on the working plane at the bottom.

## The 'Slab' tool seems to grow the slab 'out' as in 'down' for a floor?

It seems the slab grows in the direction of the normal of a face. And as we have already established that a rectangle has its edges oriented clockwise around its center, this means the normal if the rectangle will face 'into the clock face' which will be 'down' for a floor based rectangle.

![alt text](image-9.png)

## BIM Object creation will ignore levels?

When I create BIm objects, e.g., a 'slab', it will be placed in the tree root. That is, it will ignore any selected object and will not say place the new object inside a selected level object.

![alt text](image-10.png)

## BIM 'Move Line' tool a bit quirky?

It seem, to move a line:

1. Click on the line in the model tree to select it
2. Click the 'Move' tool

![alt text](image-11.png)

3. Click somewhere in the 3D view (to 'start' the move operation?)
4. Press 'X','Y' or 'Z' to restrict the move along an axis

![alt text](image-12.png)

5. While moving the cursor, the task dialog shows the value moved.

![alt text](image-13.png)

6. Enter the value to move and hit enter.

## BEWARE the 'Home' orientation!

When I added the first internal wall I for some reason managed to rotate the house to be 180 degrees 'wrong' around the up (z) axis!

It seems I can engange 'Home' from the 'View' menu (or fn + left-arrow on mac keyboard)

![alt text](image-15.png)

And it seems the 'Home' orientation is with X to the right and Y like 'in' to the screen (and Z is up)=

![alt text](image-14.png)

So beware the 3D orientation for symetrical objects to get it right from the beginning!

At this stage I had the first interor wall in place.

![alt text](image-16.png)


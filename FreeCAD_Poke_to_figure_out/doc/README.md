# My poking into Freecad to figure stuff out

I want to understand how Freecad treat thuings under the hood so that I can adjust my expectations and model of what Freecad does. This should make me more productive and less surprised when using Freecad I hope.

See the Freecad file 'FreeCAD_Poke_to_figure_out/FreeCAD_Poke_to_figure_out.FCStd'

## In BIM workbench, can I create a 'Wall' from a sketch?

YES!

1. I switched to 'Sktecher' workbench.
2. I created a Rectangle
3. I Closed the sketch and selected it
4. I Switched to the BIM workbench.
5. I clicked on the 'Wall' tool button

![alt text](image.png)

And Freecad created the wall OK!

Conclusion: This seems like a better way to create walls in BIM than to use the BIM workbench 'Rectangle' tool. Because if we use that one we get a rectangle with a face that we need to 'turn off' to make the wall tool be able to use it!

![alt text](image-1.png)

## The BIM workbench 'Sketch' tool is the same as '

The BIM workbench 'Sketch' tool.

![alt text](image-2.png)

Is the same 'tool' as the 'Sketcher' workbench 'Create Sketch'.

![alt text](image-3.png)

## Beware that construction line mode icons are blue

Also note that no icons correspond with the fact that construction lines are rendered as 'dotted'.

And to add to confusion, the 'Toggle construction geometry' icon always shows the 'active' mode as a dotted line (left large line dotted and blue when on. And small roght line dotted and blue when off).

I found out that when the drawing icons are blue, and the 'Toggle construction geometry' icon has the **large line** dotted and blue, then we are in construction line mode.

![alt text](image-61.png)

And when the drawing icons are white, and the 'Toggle construction geometry' icon has the **small line** dotted and blue, then we are in construction line mode.

![alt text](image-62.png)

*Note: It is confusing that the 'contruction line mode' does not correspond with icons that have dotted lines!*

## Beware how hard it is to find the settings for default line width for drawn stuff and while-drawing stuff?

It seems I can affect 'drawn'stuff' with the properties in the Freecad preferences for 'Part / Part Design' and 'Line Width'.

![alt text](image-63.png)

But so far I have fauled to find any settings to make the indicator lines that Freecad shows while a draw e.g., a rectangle. So far they seem to always me 1 pisel and black?

This is a rectangle I created with the preference 'Line Width' of 5 pixels.

![alt text](image-64.png)

## Can I create both Walls and a slab from the same sketch?

Yes!

![alt text](image-4.png)

It seems the 'sketch' referenced (shown inside) the Wall tree node is **the same one** as the one referebnced (shown inside) the slab?

At least, if I make the sketch visibe, then the sketch inside the wall and the sketch inside the alb are both made visible.

Also, when I rename the sketch inside the slab to 'sketch - perimeter' then the label of 'both' sketches changes together.

![alt text](image-5.png)

I conclude the object shown inside the wall and slab is a **reference** to the same sketch instance?!

## Can we snap internal walls to a floor sketch?

YES!

I created a sketch 'Sketch - internal walls' and projected the external walls onto it (using the 'Create external geometry' tool to get the inside reference of these walls).

I could now place two lines to use to create the internal walls. 

![alt text](image-6.png)

And using the 'Wall' tool on this sketch got me some innetr wall ok.

NOTE: BE sure to 'Create external geometry' in the 'Constrction geometry' mode (to make the external wall reference lines 'virtual' = not used by the create wall tool later on).

![alt text](image-7.png)

The external geometry mode is indicate with blue geometry icons.

![alt text](image-8.png)

## Can I snap windows to a sketch on the wall?

YES! But the sketch must NOT be referencing the wall through 'external geometry'!

I created this sketch. Where the perimeter is 'external geometry' from the existing wall.

![alt text](image-9.png)

Now I was able to place a window that snapped to the rectangles on the sketch that I hade drawn where the windows should go.

![alt text](image-14.png)

BUT - When the window snapped into place this sketch (and the sketch I had defined for the internal walls) **broke**!

Maybe the 'create window' tool renames the topology of the wall? And if so, then this breaks the external geometry projection of both the internal wall and external wall face sketches? As they both project the external wall onto them and uses these references for drawings?!

**Beware** - The 'Sketch' tool in the BIM workbench seems to snap to the wroking plane? I was unable to create a sketch on the wall surface (it was placed on the floor by itself and without asking)? 

But - if I switched to the 'sketcher' workbench I could select a wall face and create a sketch onto that face seemingly ok.

Conclusion: It seems I may be able to snap window in place as defined by a sketch as long as the sktech does not break when the wall is mutated by the inserted window?

## Can I define named parameters and have my sketch use such parameters?

YES! I can use a 'spreadsheet' and give cells an Alias. Then I can use this alias as an 'expression' for other freecad properties.

1. I Create a 'Spreadsheet' in the 'Spreadsheet' workbench

![alt text](image-11.png)

2. I assigned an Alias to cell A1

![alt text](image-12.png)

3. Now I could use this value in my Wall 'Width' property

![alt text](image-13.png)

Note: I entered this expression by starting the input with '='. This triggered Freecad to open an 'Expression editor'!

![alt text](image-10.png)

It seems I should also be able to create a sketch. And then on that sketch draw 'stuff' and define contraints.

Then I should be able to use (a python?) expression to refer a constraint value in this specific sketch as a value expression for other properties in Freecad?

```pyhon 
Sketch.<SketchName>.Constraints.<ConstraintName> 
```

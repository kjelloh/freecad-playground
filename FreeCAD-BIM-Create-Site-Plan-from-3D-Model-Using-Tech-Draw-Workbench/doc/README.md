# My experience and learning from doing youtube tutprial "FreeCAD BIM: Create Site Plan from 3D Model Using Tech Draw Workbench"

See <https://youtu.be/erN5h4HxGZ0?list=PL3wRqQUPtE16yw_c1TnRYJmz37y2ZRTLm>

Please consider to support the creator of the tutorial video at <https://ko-fi.com/s/391226909e>

## Consider the presenter options of 'Draft workflow' vs. the 'Techdraw workflow'

See youtube video <https://youtu.be/pP9fL-zfQyA?list=PL3wRqQUPtE16yw_c1TnRYJmz37y2ZRTLm>.

It seems this is his names for two possible worksflows he has identified to use in Freecad?

![alt text](image.png)

It seems the 'Draft workflow' is based on a two step process?

1. Create a 'Draft' 2D drawing in the 3D model.
2. Place one or more such 'Drafts' on 'Pages'.

![alt text](image-1.png)

The presenter seems to state that this workflow is preferred top be able to create all required drawings for a BIM project?

It seems the 'Tech draw workflow' also includes two main steps (but does not create any 2D drawings in the 3D space)?

1. Create a 'Technical Drawing'
2. Place 'sections' directly from the 3D model onto the page.

![alt text](image-3.png)

He seems to state that this 'Tech draw workflow' is inferior to the 'Draft workflow' in that the set of possisble drawings are limited by the 'Technical drawing' workbench tools?


He seems to state that this limitation comes from the fact that the 'Draft' workbench uses *totally different* libraries than the 'Technical Drawing' workbench (see <https://youtu.be/pP9fL-zfQyA?list=PL3wRqQUPtE16yw_c1TnRYJmz37y2ZRTLm&t=256>)?

Anyhow, in the tutorial the presenter still uses the more restricted 'Technical Drawing' workflow. 

## The 'Page' is a thing in the 'Techdraw' workbench

It seems to create a 'Page' to hold our drawing we use the 'Insert Page using template' tool in the 'Techdraw' workbench?

![alt text](image-4.png)

Note: I used the svg-file from the download (see <https://ko-fi.com/s/391226909e>)

![alt text](image-5.png)

So this seems to sugest I can make my own svg-file and use as a template in Freecad (like the presenter in the video does)?

Note: It seems an svg-file is in fact in XML format? And the editable text fields are tageed with '\<text...' in the xml?

```xml
<text
    id="project_name_field"
    x="226.34004"
    y="259.685"
    freecad:editable="title"
    freecad:autofill="title"
    style="font-style:normal;font-variant:normal;font-weight:500;font-stretch:normal;font-size:5px;font-family:Ubuntu;-inkscape-font-specification:'Ubuntu, Medium';font-variant-ligatures:normal;font-variant-caps:normal;font-variant-numeric:normal;font-variant-east-asian:normal;text-anchor:start;fill:#000000;stroke:none">
```

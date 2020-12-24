In the Part Design workbench, your Body is the end result of of a series of operations, each operation based on the result of the previous operation. The result of the most recent operation is called the "Tip" and is shown with a little green arrow in the Model Tree.

In your case, your Thickness object should be contained within the Part Design > Body object. Then to make a cutout, you'll want to make a new Sketch on the face of the Thickness object, not the original object. Next you can Part Design > Pocket that sketch, which should give you a Pocket object as the new tip of the Body object. Similarly, when you then go to make standoffs, don't map the standoff sketch to the original object or the thickness object, but instead to the current tip, which would be the pocket object.

Hi and welcome to the forum!

You should not mix the workbenches if there is no need, and you must not do it in the way you did. You can use tools from Part workbench, but you should apply them on the whole body, which is a bit complicated for your use case. Once you have a Part object you cannot easily use it inside of the body, usually you need a new body to continue in PartDesign.

This is what you should do:
- Stay in PartDesign
- Use the PartDesign thickness operation in the same way as you did with the Part tool
- Then continue with further sketches and features in PartDesign.


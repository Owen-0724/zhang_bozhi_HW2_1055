This is a simple puzzle game created with HTML, CSS and JavaScript. Drag and drop puzzle pieces to complete the image, users can switch images by clicking the thumb below the puzzle.  
However, there are some bugs within this game.

Bug 1  
When a user uses the drag and drop function, a drop zone could hold more than one image. One drop zone should hold only one image.

Solution:
1. If an image is inside this drop zone, do not allow another image to dropped.

2. Attach an ID to each image, if there is an ID inside this drop zone then do not allow drop action.

3. Check the amount of the elements inside the drop zone, if the number is larger than 0, then ignore the action.  
|  
If child elements ＝0,  
then drop the piece.    
|  
if (childElementCount ===0) {  
appendchild(dropPiece);  
} else {  
}  

Bug 2  
When a user switches to a new image, puzzles should be reset or removed.

Solution:
1. When a user clicks a new tumble, check if there are any puzzles inside the drop zone. Reset the puzzle inside the drop zone.

2. Reset every puzzle when a user clicks a new tumble.  
|  
When clicking on the image tumble, reset all puzzles.  
|  
dropZone.removechild();  

3. Create a reset button for the user to reset the puzzle manually.



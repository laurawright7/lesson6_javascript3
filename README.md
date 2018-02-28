## Project Name:  Photo Gallery Application

### Course Title:
Web Application Development

### Assignment Date:  
February 23, 2018

### Student Name:  
Laura Wright

### Project Description:
In this assignment we learned how to manipulate the DOM, that is use JavaScript to change the original webpage nodes. We did this by accessing the original properties in HTML and changing them, and adding new ones. We started with a photo gallery that displayed three images and changed it to display five. 

### View Project:
(Replace this statement with your Github Page URL that was created when you 
 published the project.)

### Lessons Learned in the Assignment:

* We learned how to add the source of an element to the JS file, in this case we added the source of the photos to the JavaScript code, and assigned their photo order. The variable we used to refer to each image was currentFig. We used getElementsByTagName to reference the <img> tag in HTML, and we gave them their corresponding order in the photoOrder array and called this the filename. For example to get the source img01.jpg and img01sm.jpg, we referenced the <img> tag, used the "i" variable of 1, added the sm.jpg version to it and named that the filename, ie filename = img01.jpg + img01sm.jpg. We were then able to assign the information in the filename to equal the source of our currentFig. For example, currentFig.src = img01.jpg + img01sm.jpg. This would mean that img01.jpg and img01sm.jpg would occur first in the photo Order because we assigned i=1 to this set of images.

* We learned how to add a new element/node to the DOM. To do this you consider whether a new parent of the element also needs creating, and whether you need to reference a grandparent as well. In this assignment we wanted to add a new image and so along with the new image, we also created the parent of the image called the figure, and assigned a variable to the parent of figure, which is article. We gave the newly created figure a new id, stacking order number, position and padding. We then assigned width and height to the newly created image. To add this newly created figure and image to the DOM, we used appendChild, which means in this case that it adds the new node at the bottom end of the heirachy. We used the following syntax: parent.appendChild(newchild). 
To add the new figure, the node was placed at the bottom of the heirachy underneath its parent article. 
articleEl.appendChild(lastFigure);
To add the new image, the node was placed at the bottom of the heirachy underneath its parent figure. 
lastFigure.appendChild(lastImage);

* We learned how to clone a node and place it in a specific position. We used the syntax: var newNode = oldNode.cloneNode(include descendants in the clone);. In this case, we created lastFigure and we wanted a clone of that called firstFigure, and we wanted all of the descendants to be included in the clone. We therefore used the following statement:firstFigure = lastFigure.cloneNode(true);
We wanted this new node to be placed before another child and so we used the insertBefore method. We used the following syntax: parentNode.insertBefore(newNode, document.getElementById(nodeToAppearBefore)); In this case we wanted the first figure to go before figure 2, and the parent is article:
articleEl.insertBefore(firstFigure, document.getElementById("fig2"));

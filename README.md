## Project Name:  Photo Gallery Application

### Course Title:
Web Application Development

### Assignment Date:  
March 6, 2018

### Student Name:  
Laura Wright

### Project Description:
In this assignment we learned how to manipulate the DOM, that is use JavaScript to change the original webpage nodes. We did this by accessing the original properties in HTML and changing them, and adding new ones. We started with a photo gallery that displayed three images and changed it to display five. 

### View Project:
https://laurawright7.github.io/lesson6_javascript3/

### Lessons Learned in the Assignment:

* We learned how to add the source of an element to the JS file, in this case we added the source of the photos to the JavaScript code, assigned their photo order [i], and therefore preloaded the images so they could be accessed more easiy. The variable we used to refer to the current image diplayed was currentFig. We used getElementsByTagName to reference the <img> tags in HTML, we gave them their corresponding order in the photoOrder array [i], and called this 'filename'. 
There were two conditions mentioned in the code, whether there were 3 or 5 images appearing at a time. I will explain how we accessed the source of the images when 5 images were appearing at one time. 
To get the source of the images into JS called img01.jpg and img01sm.jpg, we referenced the <img> tag, used the "i" variable of 0, added the sm.jpg version to it, and named that 'filename', ie filename = img01.jpg + img01sm.jpg. Because the first place in the array is 0, img_01.jpg was accessed when i=0. We were then able to assign the information in the filename to equal the source of our currentFig. For example, currentFig.src = filename = img01.jpg + img01sm.jpg. 

* We learned how to add a new element (node) to the DOM. To do this we considered whether a new parent of the element also needed creating, and whether we needed to reference the parent of that parent as well. In this assignment we wanted to add a new image, and so along with the new image, we also created the parent of the image called 'figure', and attached and positioned it in the right relation to the parent of figure, which is 'article'. We gave the newly created figure a new id, stacking order number, position and padding. We then assigned width and height to the newly created image. To add the newly created figure and image to the DOM, we used appendChild, which meant that it added the new nodes last in order under the parent. We used the following syntax: parent.appendChild(newchild). 
To add the new figure called 'lastFigure', the new figure node was placed at the bottom of the heirachy underneath its parent 'article': articleEl.appendChild(lastFigure);
To add the new image called 'lastImage', the new image node was placed at the bottom of the heirachy underneath its parent 'figure': lastFigure.appendChild(lastImage);


* We learned how to clone a node and place it in a specific position. We used the syntax: var newNode = oldNode.cloneNode(include descendants in the clone);. In this case, we created lastFigure and we wanted a clone of that called firstFigure, and we wanted all of the descendants to be included in the clone. We therefore used the following statement:firstFigure = lastFigure.cloneNode(true);
We wanted this new node to be placed before another child and so we used the insertBefore method. We used the following syntax: parentNode.insertBefore(newNode, document.getElementById(nodeToAppearBefore)); In this case we wanted the first figure to go before figure 2, and the parent is article:
articleEl.insertBefore(firstFigure, document.getElementById("fig2"));

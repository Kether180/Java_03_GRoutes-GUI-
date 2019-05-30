
                                             Java_03_Praktikum 3 
                               GeographicRoutes_ Graphical User Interfaces(GUI)
1 Overview

        ▪ Primary Learning Objectives: Graphical User Interfaces (GUI).
        ▪ For the source code, please create a package called lab3.geoPosition.

In this lab exercise you will develop a Graphical User Interface (GUI). There are no requirements regarding both the classes to be implemented and the exact design of the GUI. Instead, it is only important that your program fulfills the functionality described in Section 3.

The following figure shows one possible solution for the application to be developed. The GUI includes a map in which the user can define a route consisting of one or several parts (here a route from Hamburg to Kiel is shown in red color). A defined route may be deleted. It is your decision whether you implement this functionality, e.g., using a button and/or a menu item. The example solution additionally displays the total length of the route defined as well as the mouse position in geographical coordinates.

2 Exercise

Create a GUI with the following functionalities. Please note that only the requirements defined in Section 3.1 are mandatory. Please also consider the hints given in Section 3.3 as well as the solution strategy described in Section 4.

2.1 Mandatory

    ▪ The application uses the map provided in file OSM_Map.png1.
    ▪ Users can select waypoints by left clicking the mouse on a position on the map.
    ▪ Waypoints create a route whereas new waypoints are added at the end of the route.
    ▪ The route will be displayed correctly in the map.
    ▪ Users can delete the defined route.
    
3 Optional

The following requirements are not needed to be fulfilled to pass the lab. However, they are a good way to practice if you have some time left and are looking for a challenge.

    ▪ The application displays the current position (x, y) of the mouse on the map.
    ▪ The application displays the current mouse position in geographical coordinates (lat, lon).
    ▪ The application displays the total length of the rout in kilometers.
    
3.1 Hints

        ▪ Map:
         Read the file with ImageIO.read() creating an object of type BufferedImage and use drawImage() for drawing.
        Eclipse uses the directory of the Java project for reading and writing. Thus, please add the image file (OSM_Map.png) using for             example drag&drop (from explorer to package lab3.geoPosition) and use the relative file path (lab3/geoPosition/OSM_Map.png) for reading.

    ▪ Mouse events: Implement a MouseListener and add it to your panel with addMouseListener(). To respond to mouse movements, use MouseMotionListener and addMouseMotionListener().
    
    ▪ Conversion to geographic coordinates: The file OSM_Map.txt includes the longitude and latitude of both the upper left and lower right corner of the map.
    
    ▪ Modify the line width: Cast the Graphics-reference to a reference of type Graphics2D. Modify the line width with setStroke(new BasicStroke(x)) whereas x is the new width.

4.1 Solution Strategy

      ▪ First, design and implement the appearance of the graphical interface (i.e. the type and layout of the elements).
      ▪ Implement the required functionality in the second step.
      ▪ Do not get into details about the appearance of the graphical interface. (For particularly creative and aesthetic solutions, there    is admiration and enthusiasm, but no beauty award.)

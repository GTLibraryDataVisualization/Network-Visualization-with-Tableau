# Tableau-Network-Chart-Destination-Map

You use Tableau Public for this workshop. So all screenshots are taken from Public. It is highly recommended you first take a look at the files and understand what information is in there.

## File Import
Launch your Tableau Public, selectMS Excel because that is the format we saved our files, and navigate to your file.

![image](https://user-images.githubusercontent.com/37058499/92944429-f46b6b00-f421-11ea-85da-d4f5eb59be06.png)

Load your file, and you should see the screen below. 
We have two files we need to use for this exercise. One is the GT OIT dispatch mock data, the other is the Lat/Lon of all the locations the dispatches ties to. 
First drag-drop the Trips files to the right, and then Lat_Lon file. 
Once both files are dragged in, the screen will pop a Edit Relationship window asking you how to connect them. Location variables on both files are our connector in this case.
After done, exit the window.

![image](https://user-images.githubusercontent.com/37058499/92944318-d30a7f00-f421-11ea-8aad-ef88eb82795f.png)

## Create a frame of links

Then at the left bottom, you should see “Sheet 1” turns orange. Click on it to open a new worksheet.

On the new sheet, you would see both tables listed on the left sidebar: Lat_Lon, Trips. 
Double-click Lat /Lon under the Lat_Lon table, then you should see the screen below.

![image](https://user-images.githubusercontent.com/37058499/92944541-18c74780-f422-11ea-9783-955079a85c5e.png)

At this time you should see only one dot on the map, this is because by default Tableau calculated the AVG of all values. 

Here you want to create a new variable to indicate to Tableau how are all the locations connected. 
To do this, go up to the top of the left sidebar, click on the triangle drop-down icon, on the menu, select Create Calculated Field.

![image](https://user-images.githubusercontent.com/37058499/92944595-30063500-f422-11ea-898e-0f5f5f303ec5.png)

After you click on it, a new window would pop up, like below:

![image](https://user-images.githubusercontent.com/37058499/92944645-41e7d800-f422-11ea-8797-cdc74174c44d.png)

Here we want to create a new variable called Route that indicates that, all lines should be drawn between Origins and Destinations.
To do that, we type in Origin, then you will notice Tableau pulls all the variables that match your type from the table, click on it to register.
Keep typing to finish the calculation, like below:

![image](https://user-images.githubusercontent.com/37058499/92944727-5b891f80-f422-11ea-8538-ef9f83bee6eb.png)

Then OK it. At this time you will notice a new variable called Route is added to the left sidebar.
Now drag and drop it on Details under Marks. Now you should see all the data points showing on the map.

![image](https://user-images.githubusercontent.com/37058499/92944784-6d6ac280-f422-11ea-9ed2-396e8c217b96.png)

And now, go up to the “Automatic” chart selection and change it to lines:

![image](https://user-images.githubusercontent.com/37058499/92944860-85424680-f422-11ea-92d9-cdb4700daedb.png)

this way you tell Tableau to draw lines between Origin and Destination.

![image](https://user-images.githubusercontent.com/37058499/92945112-d2beb380-f422-11ea-94d6-aea08ae9fb2c.png)

Now drag and drop Location on Details, you should start seeing a spider web look map like below:

![image](https://user-images.githubusercontent.com/37058499/92945149-e23dfc80-f422-11ea-82be-ca8c8b019be2.png)

So far you have created the links / bridges between all Origins and Destinations. Hover your mouth over to the lines to find out more information.


## Create a second frame of dots

Find Lat on the left sidebar and drag-drop it in the row. Now you should see a split-screen like below.

![image](https://user-images.githubusercontent.com/37058499/92945251-04377f00-f423-11ea-9b9c-9b14a5c7ae5b.png)

Our goal here is to make the first frame links and the second dots, and then merge them together.
To do this, click to expand AVG(Lat) (2), and change the chart type from Line to Circle.

![image](https://user-images.githubusercontent.com/37058499/92945315-1a453f80-f423-11ea-9ff7-5186d4112383.png)

After this step, you should see the second frame change to dots. 

Something else you can do here is to change the size of the dots to represent the traffic that go through them. 
To do this, simply drag-drop Times to Size under AVG(Lat)(2).
You can also drag-drop Location / Times on Label so it will show on screen the location names.

![image](https://user-images.githubusercontent.com/37058499/92945375-2fba6980-f423-11ea-9f43-3155eb913db0.png)

After this, it will be mostly cosmetic work. For example, if you’d like to make the links crispier and a different color, you can do back to expand AVG(Lat), change the color and remove the halo (if you wish).

![image](https://user-images.githubusercontent.com/37058499/92945443-452f9380-f423-11ea-8748-6ce31767bc6e.png)

You can also make the link a little skinnier so it doesn’t take too much space under the Size button.

## Merge the frames

When we are done editing the dots and lines, we can merge them into one frame.
To do this, go up on the rows, click on the triangle at the end of the second AVG(Lat) button, you will see a drop-down menu like the screen below. 
There click on Dual Axis.

![image](https://user-images.githubusercontent.com/37058499/92945507-5bd5ea80-f423-11ea-89db-8c2fb7027602.png)

Now you should see one frame of dots connected by lines:

![image](https://user-images.githubusercontent.com/37058499/92945554-6e502400-f423-11ea-88e5-718ffde8f4f3.png)

One final touch we can add is a background map to give us more context. 
To do this, go up to Map. Click on it and select Map Layers from the drop-down menu:

![image](https://user-images.githubusercontent.com/37058499/92945601-82942100-f423-11ea-96c3-3fa4787e7b07.png)

After you click on it, a sidebar will appear on your left. 
You can try different styles from the Style control, and adjust the Washout to make sure the background doesn’t take away the main focus of your visualization.

![image](https://user-images.githubusercontent.com/37058499/92945665-95a6f100-f423-11ea-8a67-852705179570.png)

After this final step, Tableau Public users can publish it from File -> Save to Tableau Public As. 
There you will need to log in / create your account to be able to save content.

![image](https://user-images.githubusercontent.com/37058499/92945700-a5263a00-f423-11ea-91b6-073a778d8124.png)




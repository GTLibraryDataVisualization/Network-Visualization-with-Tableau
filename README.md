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





















In this workshop we will be using this small mock dataset for logistics to create a network (destination) map. 

There are two datasets uploaded here, the raw one is the original data, and the modified one is what is needed to create the map. The modification could be done beforehand or in Tableau.

The final visualization looks like:

![Screenshot](https://user-images.githubusercontent.com/37058499/87679494-3fcb0b00-c74a-11ea-9abc-46963c740e2c.png)


The interactive visualization could be accessed at: https://public.tableau.com/views/DestinationMapDemo2/Dashboard1?:language=en&:display_count=y&publish=yes&:origin=viz_share_link

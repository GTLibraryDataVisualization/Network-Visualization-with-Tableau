# Tableau-Network-Chart-Destination-Map

You use Tableau Public for this workshop. So all screenshots are taken from Public. It is highly recommended you first take a look at the files and understand what information is in there.

## File Import
Launch your Tableau Public, selectMS Excel because that is the format we saved our files, and navigate to your file.
![image](https://user-images.githubusercontent.com/37058499/92944111-93dc2e00-f421-11ea-8e5f-fb39b9155ea0.png)

Load your file, and you should see the screen below. 
We have two files we need to use for this exercise. One is the GT OIT dispatch mock data, the other is the Lat/Lon of all the locations the dispatches ties to. 
First drag-drop the Trips files to the right, and then Lat_Lon file. 
Once both files are dragged in, the screen will pop a Edit Relationship window asking you how to connect them. Location variables on both files are our connector in this case.
After done, exit the window.
![image](https://user-images.githubusercontent.com/37058499/92944318-d30a7f00-f421-11ea-8aad-ef88eb82795f.png)


















In this workshop we will be using this small mock dataset for logistics to create a network (destination) map. 

There are two datasets uploaded here, the raw one is the original data, and the modified one is what is needed to create the map. The modification could be done beforehand or in Tableau.

The final visualization looks like:

![Screenshot](https://user-images.githubusercontent.com/37058499/87679494-3fcb0b00-c74a-11ea-9abc-46963c740e2c.png)


The interactive visualization could be accessed at: https://public.tableau.com/views/DestinationMapDemo2/Dashboard1?:language=en&:display_count=y&publish=yes&:origin=viz_share_link

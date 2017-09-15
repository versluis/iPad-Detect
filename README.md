# iPad-Detect
iOS 10 Project demonstrating how to load a Storyboard depending on iPad Screen Size

The secret here is using the method fixedCoordinateSpace on the UIScreen class, which always delivers the height of the screen, 
regardless of how the user is holding the device (portrait or landscape). 

We'll determine the height of the screen, and if it's below 1024, we assume it's an iPad below 10.5". Anything above it is probably
an iPad Pro 12.9", for which we can create a separate storyboard. 

Any non-iPad devices will load the Main.storyboard.

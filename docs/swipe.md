To have control over the swipe gesture, you have the following choices:
You can specify start and end coordinates in percentages to make the swipe gesture consistent across different screen dimensions:
```yaml
- swipe:  
    start: 90%, 50% # From (90% of width, 50% of height)
    end: 10%, 50% # To (10% of width, 50% of height)
```
Swiping in RIGHT, LEFT, UP, or DOWN directions:
Example:
```yaml
- swipe:              # This command swipes in the left direction from the middle of the device. 
    direction: LEFT
```
Relative start and end coordinates for directional swipe are configured as follows:
A common use case for this is to swipe the onboarding pages.
You can also specify elements as a starting point for swipe commands. It will swipe from the middle of the element in the direction you specify. Example:
```yaml
- swipe:
   from: 
     id: "feeditem_identifier" # From (x, y) center of element
   direction: UP # To (50% of width, 10% of height)
    
```
Note that you can use any selector here to target an element to swipe from. Please refer to the Selectors page for a full list of available selectors.
You can also specify start and end points for the swipe to have more control:
```yaml
- swipe:                 # This command swipes from point (x:100, y:200) to point (x: 300, y:400). Units are in pixels
    start: 100, 200
    end: 300, 400
```
To control swiping speed you can use duration in the swipe command. The more the duration slower the swipe. By default, the swipe command uses 400 milliseconds. To configure speed you can use:
```yaml
- swipe:
    direction: LEFT
    duration: 2000      # Values are in ms.
```

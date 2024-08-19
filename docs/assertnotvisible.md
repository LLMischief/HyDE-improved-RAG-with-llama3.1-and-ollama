To assert whether an element is not visible, use the following command that takes the same parameters as tapOn
```yaml
- assertNotVisible:
    # Same exact parameters as tapOn
```
This command will wait for view to disappear if it is currently visible.
You are most likely going to be using the following properties, but please refer to the Selectors page for an exhaustive list of all available selectors:
text - text in a view
id - id of a view
enabled - true if view is enabled
checked - true if view is checked
focused - true if view has keyboard focus
selected - true if view is selected
To check whether view with a text My Button is visible you can run the following command:
```yaml
- assertNotVisible: "My Button"
```
To check whether view with a text My Button that is also enabled is not visible you can run the following command:
```yaml
- assertNotVisible:
    text: "My Button"
    enabled: true
```
Such test will fail if either
There is no button with such text
There is a button but it is disabled
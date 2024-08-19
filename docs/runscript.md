For more information regarding JavaScript, please refer to the Javascript section:
runScript command runs a provided JavaScript file.
```yaml
appId: com.example
env:
    MY_NAME: John
---
- launchApp
- runScript: myScript.js
- inputText: ${output.myFlow}
```
A script would typically perform some action and set an output value that could be accessed later. See Outputs for more information.
```javascript
var uppercaseName = MY_NAME.toUpperCase()

output.myFlow = uppercaseName   // returns 'JOHN'
```
runScript accepts env parameters, in the same way as runFlow does (see Nested Flows).
```yaml
- runScript:
    file: script.js
    env:
       myParameter: 'Parameter'
```
You can use conditionals to run a JavaScript file when some condition is true. For more information, please refer to the conditionals documentation.
Console logging is supported from the javascript files provided in runScript command. Logs from javascript are redirected to the console when using Maestro CLI. 
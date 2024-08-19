For more information regarding JavaScript, please refer to the Javascript section:
For very simple computations (like the one above), creating a new file might be cumbersome. evalScript allows you to specify JavaScript directly in your Maestro flow.
```yaml
appId: com.example
env:
    MY_NAME: John
---
- launchApp
- evalScript: ${output.myFlow = MY_NAME.toUpperCase()}
- inputText: ${output.myFlow}
```
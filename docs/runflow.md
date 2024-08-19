If you'd like to avoid duplication of code or otherwise modularize your Flow files, you can use the runFlow command to run commands from another file.
Runs a flow from a specified file:
```yaml
- runFlow: anotherFlow.yaml
```
Let's say you have a login sequence that you'd like to reuse across multiple flows. You can write the login commands in a separate file and run those steps from another Flow:
runFlow command can accepts arguments that will be passed to subflow, the same way as with -e or env block in the flow itself (see Parameters & Constants):
```yaml
- runFlow: 
    file: anotherFlow.yaml
    env:
      MY_PARAMETER: "123"
```
If you would like to use runFlow without extracting the commands into a separate flow file, you can run your commands inline like this:
```yaml
- runFlow:
    env:
      INNER_ENV: Inner Parameter
    commands:
      - inputText: ${INNER_ENV}
```
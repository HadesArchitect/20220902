Sample Extension: https://github.com/microsoft/vscode-extension-samples/tree/main/helloworld-web-sample (built and published here https://open-vsx.org/extension/hadesarchitect/helloworld-web-sample)

## Steps to reproduce

1. [OPEN IN GITPOD](https://gitpod.io/#https://github.com/HadesArchitect/20220902)
2. Open VSCode Command Panel (CMD+Shift+P) 
3. Try to Execute command `hello world`

## Expected Result

Notification `Hello World` is show

## Received Result

`Command 'Hello World' resulted in an error (command 'helloworld-web-sample.helloWorld' not found)`

## More Details 

In the `Extensions` tab the extension is present and "installed", but "install in browser" button is available. After pushing this button, the extension works as expected. (Notification is shown on the command execution) 


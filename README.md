[VSCode Sample Extension](https://github.com/microsoft/vscode-extension-samples/tree/main/helloworld-web-sample) built and published as [hadesarchitect.helloworld-web-sample](https://open-vsx.org/extension/hadesarchitect/helloworld-web-sample).

## Steps to reproduce

1. [OPEN IN GITPOD](https://gitpod.io/#https://github.com/HadesArchitect/20220902)
2. Open VSCode Command Panel (CMD+Shift+P) 
3. Try to Execute command `hello world`

## Expected Result

Notification `Hello World` is shown

## Received Result

`Command 'Hello World' resulted in an error (command 'helloworld-web-sample.helloWorld' not found)`

## More Details 

In the `Extensions` tab the extension is present and "installed", but "install in browser" button is available. 

<img width="1016" alt="image" src="https://user-images.githubusercontent.com/1742301/188490132-7d1b1f30-ef72-4919-b01f-2d85a5b66e0f.png">

After pushing this button, error is still present, although the extension is marked as `installed in browser`.

<img width="344" alt="image" src="https://user-images.githubusercontent.com/1742301/188490178-473aa7ca-c009-4cd5-8546-c40b2333c6ba.png">

After _reloading of the browser_, the extension works as expected.

<img width="497" alt="image" src="https://user-images.githubusercontent.com/1742301/188490257-42bac749-63c5-4fbd-bb27-70ca3bec2d4b.png">

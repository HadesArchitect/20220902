# Bug Report 

## Problem Description

Plugins installed via `.gitpod.yml` configuration file aren't properly installed and not operational.

Demo extension: [VSCode Sample Extension](https://github.com/microsoft/vscode-extension-samples/tree/main/helloworld-web-sample) built and published as [hadesarchitect.helloworld-web-sample](https://open-vsx.org/extension/hadesarchitect/helloworld-web-sample). 

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

## Related Logs

### Remote Server

```
[2022-09-05 16:51:38.433] [remoteagent] [info] [10.20.18.133][3c497d0b][ExtensionHostConnection] New connection established.
[2022-09-05 16:51:38.439] [remoteagent] [info] [10.20.18.133][3c497d0b][ExtensionHostConnection] <989> Launched Extension Host Process.
[2022-09-05 16:51:38.801] [remoteagent] [info] Getting Manifest... hadesarchitect.helloworld-web-sample
[2022-09-05 16:51:38.894] [remoteagent] [info] Installing extension: hadesarchitect.helloworld-web-sample
[2022-09-05 16:51:39.432] [remoteagent] [info] Downloaded extension: hadesarchitect.helloworld-web-sample /workspace/.vscode-remote/data/CachedExtensionVSIXs/hadesarchitect.helloworld-web-sample-0.0.1-test
[2022-09-05 16:51:39.470] [remoteagent] [info] Extracted extension to /workspace/.vscode-remote/extensions/.1ee45505-ef2b-4a54-8128-22b3a856e4c4: hadesarchitect.helloworld-web-sample
[2022-09-05 16:51:39.473] [remoteagent] [info] Renamed to /workspace/.vscode-remote/extensions/hadesarchitect.helloworld-web-sample-0.0.1-test
[2022-09-05 16:51:39.474] [remoteagent] [info] Extracting completed. hadesarchitect.helloworld-web-sample
[2022-09-05 16:51:39.475] [remoteagent] [info] Extension installed successfully: hadesarchitect.helloworld-web-sample
```

### Remote Extension Host / Worker Extension Host

Both logs have no mentions of the `hadesarchitect.helloworld-web-sample`

### Browser

<img width="1066" alt="image" src="https://user-images.githubusercontent.com/1742301/188492796-096042a2-903e-4b4c-969c-8a8d70394867.png">
<img width="1053" alt="image" src="https://user-images.githubusercontent.com/1742301/188492825-92996556-7e5b-4b94-b870-15ef3fd1bd20.png">

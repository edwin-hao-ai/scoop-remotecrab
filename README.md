# scoop-remotecrab

Scoop bucket for [RemoteCrab](https://vgoapp.com/remotecrab/) — use an iPhone or iPad as the
camera, microphone, trackpad and keyboard of a Windows PC or a Mac.

```powershell
scoop bucket add remotecrab https://github.com/edwin-hao-ai/scoop-remotecrab
scoop install remotecrab
```

## What this installs

The app itself, unprivileged: no UAC prompt, nothing written to `Program Files`. That is the
right default for a bucket, and it is enough to run the app and pair a phone.

The **virtual camera** needs a driver, and the tray integration is registered by the MSI that
sits inside the same archive. If you want those, run `install.cmd` as administrator from the
installed directory (`scoop prefix remotecrab`). Without it the app still works for camera,
microphone, trackpad, keyboard and the browser viewer.

## Licence

Proprietary. Free to use on your own network; remote access from outside it is a subscription.

## Updates

`checkver` reads `https://vgoapp.com/downloads/windows/manifest.json`, which is the same feed
the app's own updater uses, so the bucket cannot advertise a version that was not published.

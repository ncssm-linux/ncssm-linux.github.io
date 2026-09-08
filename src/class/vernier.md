# Vernier software

Vernier software is used in many Physics classes at NCSSM.

Vernier software is proprietary and does not support Linux operating systems.

However, the tools do have web versions (though teachers will not recommend them).

## Web Versions

The web versions of Vernier software use [WebUSB](https://developer.mozilla.org/en-US/docs/Web/API/WebUSB_API),
an experimental web API that Firefox-based browsers do not support citing security concerns.

The simplest way to use Vernier software is just to use [Chromium](https://wiki.archlinux.org/title/Chromium)
or a Chromium-based browser.

Then you should be able to use the programs at their websites:
- [graphicalanalysis.app](https://graphicalanalysis.app)
- [videoanalysis.app](https://videoanalysis.app/)
    - This one doesn't involve external devices, so you won't need Chromium.
    - You will need [NCSSM's license key](https://docs.google.com/document/d/1Mdrd5bJWMRqREADwXhExjfCGkQcm3gMLwTpOVBvvLHI/edit)
- [spectralanalysis.app](https://spectralanalysis.app)

[Please verify that this actually works and you are able to connect to devices this way.]

## Notes about Native Builds

Vernier uses Electron! That would mean it's easy to make a script that takes a Windows binary and extracts
all the Electron files, and runs them with your native Electron build, but... they use a native module. So until we
can get a Linux build of that module, it won't be possible to run Vernier natively.

You can try running through Wine but you'll be missing a few DLLs and... at that point just use the web version.

# Create kubernetes cluster with Kubeadm

Create VM with vagrant
ref: <https://documentation.ubuntu.com/public-images/public-images-how-to/run-a-vagrant-box/>


image: "ubuntu/jammy64"

## Issue

error:

```
Vagrant failed to locate the oscdimg.exe executable which is required
for creating ISO files. Please ensure the oscdimg.exe executable is
available on the configured PATH. If the oscdimg.exe executable is
not found on the local system, it can be installed with the Windows
Assessment and Deployment Kit:
```

fix with installing adk

ref: <https://learn.microsoft.com/en-us/windows-hardware/get-started/adk-install>

after install, add `C:\Program Files (x86)\Windows Kits\10\Assessment and Deployment Kit\Deployment Tools\amd64\Oscdimg` to path env and add env `VAGRANT_WSL_ENABLE_WINDOWS_ACCESS = 1`

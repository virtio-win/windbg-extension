# windbg-extension project

## Build
Use Visual Studio 2019 and up

Output of the project is x64\Release\virtio.dll
## Install
Copy x64\Release\virtio.dll to Debuggers\x64\winext directory under WDK or EWDK location,
for example to *C:\Program Files (x86)\Windows Kits\10\Debuggers\x64*
## Usage
From windbg you can use !virtio.help to list available extension's commands

## Status
By default the extension supports *netkvm* driver

## Examples
    !virtio.cn
    !virtio.hv
	!virtio.mp
    !virtio.query a b\*
    !virtio.query a \*fea\*
    !virtio.query a u64HostFeatures
    !virtio.query a pPathBundles[0].txPath.!

**if netkvm symbols are not loaded**
    !virtio.findpdb

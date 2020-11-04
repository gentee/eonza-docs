---
title: Download area
desc: Download area of Eonza automation software.
res:
   arch: Architecture
   archive: Archive
   filename: Filename
   kind: Kind
   os: OS
   program: Program
   size: Size
html:
   linux-64z: <strong><a href="%gitpath%-linux-amd64.zip" @click="track">eonza-%ver%-linux-amd64.zip</a></strong>
   linux-64: <a href="/downloads/linux-amd64/eonza" @click="track">eonza</a>
   linuxb-64: <a href="/downloads/linux-amd64/eonza-%betaver%b" @click="track">eonza</a>
   linux-32z: <a href="%gitpath%-linux-386.zip" @click="track">eonza-%ver%-linux-386.zip</a>
   linux-32: <a href="/downloads/linux-386/eonza" @click="track">eonza</a>
   macos-64z: <strong><a href="%gitpath%-darwin-amd64.zip" @click="track">eonza-%ver%-darwin-amd64.zip</a></strong>
   macos-64: <a href="/downloads/darwin-amd64/eonza" @click="track">eonza</a>
   macosb-64: <a href="/downloads/darwin-amd64/eonza-%betaver%b" @click="track">eonza</a>
   windows-64z: <strong><a href="%gitpath%-windows-amd64.zip" @click="track">eonza-%ver%-windows-amd64.zip</a></strong>
   windows-64: <a href="/downloads/windows-amd64/eonza.exe" @click="track">eonza.exe</a>
   windowsb-64: <a href="/downloads/windows-amd64/eonza-%betaver%b.exe" @click="track">eonza.exe</a>
   windows-32z: <a href="%gitpath%-windows-386.zip" @click="track">eonza-%ver%-windows-386.zip</a>
   windows-32: <a href="/downloads/windows-386/eonza.exe" @click="track">eonza.exe</a>
---
# Downloads

Eonza software does not require installation. If you download an archive file, all you need to do is unpack it. At the first launch, the application creates service files and directories, so we recommend that you save the program to a separate folder with write access rights. In the future, you can move this directory wherever you want.

## Version %ver%

If you are not sure what to download and have a regular computer, please use **64-bit (x86-64)** for your operating system.

%% downloadlist
| %res.filename% | %res.kind% | %res.size% | %res.arch% | %res.os%
|----|----|----|----|---------
| **Windows**
| %html.windows-64z%|%res.archive%| %zsize-windows-amd64% | 64-bit (x86-64)| Windows
| %html.windows-64%|%res.program%| %size-windows-amd64% | 64-bit (x86-64)| Windows
| %html.windows-32z%|%res.archive%|%zsize-windows-386%  | 32-bit (x86-32)| Windows
| %html.windows-32%|%res.program%| %size-windows-386% | 32-bit (x86-32)| Windows
| **Linux**
| %html.linux-64z% |%res.archive%| %zsize-linux-amd64%| 64-bit (x86-64)| Linux
| %html.linux-64% |%res.program%| %size-linux-amd64%| 64-bit (x86-64)| Linux
| %html.linux-32z% |%res.archive%| %zsize-linux-386%| 32-bit (x86-32)| Linux
| %html.linux-32% |%res.program%| %size-linux-386%| 32-bit (x86-32)| Linux
| **Apple macOS**
| %html.macos-64z% |%res.archive%| %zsize-darwin-amd64%| 64-bit (x86-64)| macOS
| %html.macos-64% |%res.program%| %size-darwin-amd64% | 64-bit (x86-64)| macOS
%%
<!--
## Beta version %betaver%

%% downloadbeta
| %res.os% | %res.filename% | %res.kind% | %res.size% | %res.arch%
|----|----|----|----|---------
| **Windows** | %html.windowsb-64%|%res.program%| %sizeb-windows-amd64% | 64-bit (x86-64)
| **Linux** | %html.linuxb-64% |%res.program%| %sizeb-linux-amd64%| 64-bit (x86-64)
| **Apple macOS**  | %html.macosb-64% |%res.program%| %sizeb-darwin-amd64% | 64-bit (x86-64)
%%
-->

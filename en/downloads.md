---
title: Download area
desc: Download area of Eonza automation software.
res:
   arch: Architecture
   archive: Archive
   filename: Filename
   kind: Kind
   os: OS
html:
   linux-64: <a href="%gitpath%-linux-amd64.zip">eonza-%ver%b-linux-amd64.zip</a>
   linux-32: <a href="%gitpath%-linux-386.zip">eonza-%ver%b-linux-386.zip</a>
   macos-64: <a href="%gitpath%-darwin-amd64.zip">eonza-%ver%b-darwin-amd64.zip</a>
   windows-64: <a href="%gitpath%-windows-amd64.zip">eonza-%ver%b-windows-amd64.zip</a>
   windows-32: <a href="%gitpath%-windows-386.zip">eonza-%ver%b-windows-386.zip</a>
---
# Downloads

Eonza software does not require installation. If you download an archive file, all you need to do is unpack it. At the first launch, the application creates service files and directories, so we recommend that you save the program to a separate folder with write access rights. In the future, you can move this directory wherever you want.

## Beta version %ver%

If you are not sure what to download and have a regular computer, please use **64-bit (x86-64)** for your operating system.

%% downloadlist
| %res.filename% | %res.kind% | %res.os% | %res.arch%
|----|----|----|----
| **Windows**
| %html.windows-64%|%res.archive%| Windows | 64-bit (x86-64)
| %html.windows-32%|%res.archive%| Windows | 32-bit (x86-32)
| **Linux**
| %html.linux-64% |%res.archive%| Linux | 64-bit (x86-64)
| %html.linux-32% |%res.archive%| Linux | 32-bit (x86-32)
| **Apple macOS**
| %html.macos-64% |%res.archive%| macOS | 64-bit (x86-64)
%%

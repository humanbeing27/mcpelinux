# Introduction
Run Minecraft Bedrock Edition for Android on Arch Linux. This project is 99% based on **mcpelauncher** projects by https://github.com/minecraft-linux . So why this project then? Because this one tries to implement the same thing with a package that could be natively installed using **pacman**  package manager on Arch Linux and it is much Light Weight Too. Still, it has some differences, like :
##### 1. It launches Minecraft without a launcher GUI, like in Windows 10/11 Edition and it could also be launched using a command ``mcpreconf``.
##### 2. It also removes some temporary and trash files after closing Minecraft everytime, automatically.
##### 3. GameMode is an optional Dependency and is automatically enabled if installed. 
##### 4. There is an option to enable an FPS Counter for Minecraft that will only work for devices using **Mesa Graphics Drivers**. It could be used by Right Clicking the Desktop Entry and Selecting the option with FPS Counter or by entering command ``mcpreconf-fps``.
##### 5. For Microsoft Account these optional dependencies must be installed **qt5-base**, **qt5-webengine** and **qt5-quickcontrols**.
# Installation
Download the PKGBUILD and run :
```sh
git clone https://github.com/humanbeing27/mcpelinux.git
cd mcpelinux && cp ./bin/* ./
makepkg -sircCf
```
# Setting Up Minecraft
For now, there is nothing included here to download the actual Minecraft. So, you could use the AppImage of **mcpelauncher** to download the x86_64 APK .Copy the *assets/* and *lib/* folders from *~/.local/share/mcpelauncher/versions/**version-number**/* directory of the APK to */var/lib/mcpelinux/* directory. For some,  Minecraft may be stuck at 56% or 51% during loading. A Workaround is killing the Process or by Right Clicking the Desktop Entry and selecting option **Close Stuck Minecraft Windows** or another way is to enter the command ``killmc``.

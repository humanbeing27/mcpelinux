pkgname=mcpelinux
pkgver=1.31
pkgrel=0
pkgdesc="Run Minecraft Bedrock Edition on Arch Linux. To Run a Minecraft version, paste the extracted .apk file in /var/lib/mcpelinux."
url="https://github.com/humanbeing27/mcpelinux"
arch=(x86_64)
license=("GPLv3")
depends=("openssl-1.1")
optdepends=("gamemode: For GameMode tweaks"
            "qt5-base: For Microsoft Account Support"
            "qt5-webengine: For Microsoft Account Support"
            "qt5-quickcontrols: For Microsoft Account Support")
source=("$url/raw/main/bin/mcpelauncher-client"
        "$url/raw/main/bin/mcpelauncher-error"
        "$url/raw/main/bin/mcpelauncher-webview"
        "$url/raw/main/bin/mcpreconf"
        "$url/raw/main/bin/mcprivacy"
        "$url/raw/main/bin/msa-daemon"
        "$url/raw/main/bin/msa-ui-qt"
        "$url/raw/main/libfmod.so.12.0"
        "$url/raw/main/gamecontrollerdb.txt"
        "$url/raw/main/mcpelauncher-client.desktop"
        "$url/raw/main/minecraftpe.png")
b2sums=("SKIP"
        "SKIP"
        "SKIP"
        "SKIP"
        "SKIP"
        "SKIP"
        "SKIP"
        "SKIP"
        "SKIP"
        "SKIP"
        "SKIP")
package() {
        mkdir -p $pkgdir/usr/bin
        mkdir -p $pkgdir/usr/share/applications
        mkdir -p $pkgdir/usr/share/icons/hicolor/scalable/apps
        mkdir -p $pkgdir/usr/share/mcpelauncher/lib/native/x86_64
        cp {msa-ui-qt,mcpreconf,msa-daemon,mcprivacy,mcpelauncher-client,mcpelauncher-webview,mcpelauncher-error} $pkgdir/usr/bin
        cp mcpelauncher-client.desktop $pkgdir/usr/share/applications
        cp minecraftpe.png $pkgdir/usr/share/icons/hicolor/scalable/apps
        cp gamecontrollerdb.txt $pkgdir/usr/share/mcpelauncher
        cp libfmod.so.12.0 $pkgdir/usr/share/mcpelauncher/lib/native/x86_64
        echo "#!/bin/bash" >> $pkgdir/usr/bin/mcpreconf-fps
        echo "env GALLIUM_HUD="simple,fps" mcpreconf" >> $pkgdir/usr/bin/mcpreconf-fps
        echo "#!/bin/bash" >> $pkgdir/usr/bin/killmc
        echo "pkill MINECRAFT\ MAIN\ " >> $pkgdir/usr/bin/killmc
        chmod +x $pkgdir/usr/bin/*
        chown root -R $pkgdir/*
        chgrp root -R $pkgdir/*
}

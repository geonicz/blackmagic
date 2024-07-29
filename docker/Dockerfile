from ubuntu
label maintainer=George


run apt update
run apt install -yyy gcc-arm-none-eabi meson ninja-build git fish htop mc vim
run git clone https://github.com/geonicz/blackmagic.git && cd blackmagic
run mkdir build-96b_carbon build-arm-none-eabi build-blackpill-f401cc build-blackpill-f401ce build-blackpill-f411ce build-bluepill build-ctxlink build-f072 build-f3 build-f4discovery build-hydrabus build-launchpad-icdi build-native build-stlink build-stlinkv3 build-swlink

workdir /blackmagic

# run meson setup build-96b_carbon --cross-file ./cross-file/96b_carbon.ini
# run meson setup build-arm-none-eabi --cross-file ./cross-file/arm-none-eabi.ini
run meson setup build-blackpill-f401cc --cross-file ./cross-file/blackpill-f401cc.ini
run meson setup build-blackpill-f401ce --cross-file ./cross-file/blackpill-f401ce.ini
run meson setup build-blackpill-f411ce --cross-file ./cross-file/blackpill-f411ce.ini
run meson setup build-bluepill --cross-file ./cross-file/bluepill.ini
# run meson setup build-ctxlink --cross-file ./cross-file/ctxlink.ini
# run meson setup build-f072 --cross-file ./cross-file/f072.ini
# run meson setup build-f3 --cross-file ./cross-file/f3.ini
# run meson setup build-f4discovery --cross-file ./cross-file/f4discovery.ini
# run meson setup build-hydrabus --cross-file ./cross-file/hydrabus.ini
# run meson setup build-launchpad-icdi --cross-file ./cross-file/launchpad-icdi.ini
# run meson setup build-native --cross-file ./cross-file/native.ini
run meson setup build-stlink --cross-file ./cross-file/stlink.ini
# run meson setup build-stlinkv3 --cross-file ./cross-file/stlinkv3.ini
# run meson setup build-swlink --cross-file ./cross-file/swlink.ini

# run meson compile -C build-96b_carbon
# run meson compile -C build-arm-none-eabi
run meson compile -C build-blackpill-f401cc
run meson compile -C build-blackpill-f401ce
run meson compile -C build-blackpill-f411ce
run meson compile -C build-bluepill
# run meson compile -C build-ctxlink
# run meson compile -C build-f072
# run meson compile -C build-f3
# run meson compile -C build-f4discovery
# run meson compile -C build-hydrabus
# run meson compile -C build-launchpad-icdi
# run meson compile -C build-native
run meson compile -C build-stlink
# run meson compile -C build-stlinkv3
# run meson compile -C build-swlink

volume /blackmagic
shell ["/usr/bin/fish"]
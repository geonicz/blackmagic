from ubuntu
label maintainer=George

run apt update > /dev/null && \
	apt install -yyy \
	fish \
	gcc-arm-none-eabi \
	git \
	htop \
	mc \
	meson ninja-build \
	vim > /dev/null
run git clone https://github.com/geonicz/blackmagic.git
run mkdir \
	/blackmagic/build-96b_carbon \
	/blackmagic/build-arm-none-eabi \
	/blackmagic/build-blackpill-f401cc \
	/blackmagic/build-blackpill-f401ce \
	/blackmagic/build-blackpill-f411ce \
	/blackmagic/build-bluepill \
	/blackmagic/build-ctxlink \
	/blackmagic/build-f072 \
	/blackmagic/build-f3 \
	/blackmagic/build-f4discovery \
	/blackmagic/build-hydrabus \
	/blackmagic/build-launchpad-icdi \
	/blackmagic/build-native \
	/blackmagic/build-stlink \
	/blackmagic/build-stlinkv3 \
	/blackmagic/build-swlink
workdir /blackmagic

# run meson setup build-96b_carbon --cross-file ./cross-file/96b_carbon.ini
# run meson compile -C build-96b_carbon
# run meson setup build-arm-none-eabi --cross-file ./cross-file/arm-none-eabi.ini
# run meson compile -C build-arm-none-eabi
run meson setup build-blackpill-f401cc --cross-file ./cross-file/blackpill-f401cc.ini
run meson compile -C build-blackpill-f401cc
run meson setup build-blackpill-f401ce --cross-file ./cross-file/blackpill-f401ce.ini
run meson compile -C build-blackpill-f401ce
run meson setup build-blackpill-f411ce --cross-file ./cross-file/blackpill-f411ce.ini
run meson compile -C build-blackpill-f411ce
run meson setup build-bluepill --cross-file ./cross-file/bluepill.ini
run meson compile -C build-bluepill
# run meson setup build-ctxlink --cross-file ./cross-file/ctxlink.ini
# run meson compile -C build-ctxlink
# run meson setup build-f072 --cross-file ./cross-file/f072.ini
# run meson compile -C build-f072
# run meson setup build-f3 --cross-file ./cross-file/f3.ini
# run meson compile -C build-f3
# run meson setup build-f4discovery --cross-file ./cross-file/f4discovery.ini
# run meson compile -C build-f4discovery
# run meson setup build-hydrabus --cross-file ./cross-file/hydrabus.ini
# run meson compile -C build-hydrabus
# run meson setup build-launchpad-icdi --cross-file ./cross-file/launchpad-icdi.ini
# run meson compile -C build-launchpad-icdi
# run meson setup build-native --cross-file ./cross-file/native.ini
# run meson compile -C build-native
run meson setup build-stlink --cross-file ./cross-file/stlink.ini
run meson compile -C build-stlink
# run meson setup build-stlinkv3 --cross-file ./cross-file/stlinkv3.ini
# run meson compile -C build-stlinkv3
run meson setup build-swlink --cross-file ./cross-file/swlink.ini
run meson compile -C build-swlink

volume /blackmagic
shell ["/usr/bin/fish"]
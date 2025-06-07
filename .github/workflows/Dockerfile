FROM debian:experimental

ENV DEBIAN_FRONTEND=noninteractive
RUN apt update -y && \
    apt install -y gcc g++ linux-libc-dev meson ninja-build pkgconf libx11-dev xtrans-dev x11proto-dev libpixman-1-dev libxkbfile-dev libxau-dev libxdmcp-dev libxfont-dev libxcvt-dev libudev-dev libssl-dev libgl1-mesa-dev mesa-common-dev libepoxy-dev libxcb-util-dev libxcb-shape0-dev

CMD ["bash", "-c", "meson setup -Dbuildtype=debugoptimized build && meson compile -C build && meson test -C build --print-errorlogs"]

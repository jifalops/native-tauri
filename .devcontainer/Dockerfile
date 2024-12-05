FROM jifalops/rust:latest

# Install additional packages
# https://tauri.app/start/prerequisites/#linux
RUN sudo apt-get update && sudo apt-get install -y --no-install-recommends \
  trash-cli \
  libwebkit2gtk-4.1-dev \
  build-essential \
  curl \
  wget \
  file \
  libxdo-dev \
  libssl-dev \
  libayatana-appindicator3-dev \
  librsvg2-dev \
  at-spi2-core \
  libatspi2.0-0 \
  libcanberra-gtk-module \
  libcanberra-gtk3-module \
  libgtk-3-dev \
  x11-apps

RUN sudo apt-get install -y --no-install-recommends xdg-utils

RUN sudo groupadd -g 109 render &&\
  sudo usermod -aG render,video developer &&\
  sudo mkdir -p /run/user/1000/dconf && sudo chown -R 1000:1000 /run/user/1000
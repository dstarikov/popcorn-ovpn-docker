# popcorn-ovpn-docker
### Run popcorntime through OpenVPN using Docker
Tested on Pixel Slate running ChromeOS v81 using an ArchLinux container running through Crostini.

# Build Instructions
### Build popcorntime container
docker-compose build

### Add your VPN credentials and configure directories in .env file
vim .env

See here for more info: https://hub.docker.com/r/dceschmidt/openvpn-client/

# Install and Run
### Make Script Executable and Test
chmod +x start-popcorn

./start-popcorn

### Replace username in popcorntime.desktop
vim popcorntime.desktop

### Install desktop file and app icon
cp popcorntime.desktop ~/.local/share/applications/

sudo cp Butter.png /usr/share/icons/hicolor/512x512/apps/


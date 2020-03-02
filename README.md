# popcorn-ovpn-docker
### Run popcorntime through OpenVPN using Docker
Tested on Pixel Slate running ChromeOS v81 using an ArchLinux container running through Crostini.

# Build Instructions
### Add your username, VPN credentials, and configure directories in .env file
vim .env

See here for more info: https://hub.docker.com/r/dceschmidt/openvpn-client/

### Build popcorntime container
docker-compose build

# Install and Run
### Make Script Executable and Test
chmod +x start-popcorn

./start-popcorn

### Replace username in Exec/Path fields in popcorntime.desktop
vim popcorntime.desktop

### Install desktop file and app icon
cp popcorntime.desktop ~/.local/share/applications/

sudo cp Popcorn-Time.png /usr/share/icons/hicolor/512x512/apps/


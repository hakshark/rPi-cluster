# Setting up the Raspberry Pi's
<NOTE: These are just my initial thoughts for actions needed to prep the Pi's>

- Step 1: Flashing O/S onto each of the SSD's
  - O/S: raspios-bullseye-arm64.zip
  - Using Raspberry Pi Imager (available for Windows, macOS and Ubuntu for x86)
    - Use Ctrl+Shift+X to call up properties panel which allows for computer name, enable SSH, set pi password, etc to be set into the image
    - Raspberry Pi O/S 64-bit (bullseye-lite): can be found at https://downloads.raspberrypi.org/raspios_arm64/images/
    - Master Node(s): rPiController01
    - Worker Node(s): rPiDockerNode01, rPiDockerNode02, rPiDockerNode03, rPiDockerNode04
- Step 2: Boot Pi's
  - SSH or direct
  - Update system catalogs
  - Upgrade system packages (if needed)
  - Update machine configs for cluster node usage
  - Set up static IP
  - Reboot
- Step 3: Cluster preparations
  - Update hosts file
  - Generate and deploy keys


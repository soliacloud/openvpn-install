# OpenVPN server - Automated installing script

# Prepare your Linux Server:
`You can use a virtual private server (VPS) from providers like` [Solia.Cloud](https://solia.cloud/)

# SSH into Your Server:
*Log in to your server via SSH:*

``
ssh your_username@your_server_ip ``

# Update Your System:

*First, update your system's package list and upgrade the installed packages:*

``sudo apt update && upgrade``

# Download and Run OpenVPN Installer:

OpenVPN provides already an easy & secure installation script. To download and run it, use the following commands:

``wget https://git.io/vpn -O openvpn-install.sh``

``chmod +x openvpn-install.sh``

``sudo ./openvpn-install.sh``

_Note: The installer will ask you some configuration questions. You can typically accept the default values, but make sure to specify a custom DNS if needed._

# Configuration:

Follow the prompts during the installation to configure your OpenVPN server. This includes setting up the port, protocol, and choosing whether UDP or TCP should be used. You can also choose to enable or disable IPv6.

# User Management:

The installer will create a client configuration file for your server. It will display the name of the client config file (usually in the format clientname.ovpn). Make a note of this name.

# Complete the Installation:

Once the installation is complete, you'll receive a message confirming that the OpenVPN server is installed and running. You'll also see the location of the client configuration file.

# Download the Client Configuration:

You can download the client configuration file to your local machine. Use an SFTP client or SCP to transfer the file from your server to your computer. For example with (scp):

``scp your_username@your_server_ip:/path/to/clientname.ovpn ~/Downloads/``

# Connect to the OpenVPN Server:

Use an OpenVPN client (e.g., OpenVPN GUI for Windows, Tunnelblick for macOS, or the OpenVPN client for Linux) to import the client configuration file you downloaded. Connect to your OpenVPN server using this client.

# Verify the Connection:

Once connected, you can verify your VPN connection by checking your IP address or accessing websites to confirm your traffic is going through the VPN.

That's it! You've successfully installed and configured an OpenVPN server using the official installer script from GitHub.

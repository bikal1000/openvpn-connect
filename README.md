# OpenVPN Connect Script

This script is designed to facilitate the authentication process for an OpenVPN client using a username, password, and TOTP (Time-Based One-Time Password) secret. It ensures that the OpenVPN service is running, checks for the presence of an authentication file, and prompts the user for credentials if the file does not exist. The script then authenticates the user with the OpenVPN service using the saved credentials.

## Installation

To install this script, run the following command in your terminal:

```shell
sudo curl https://raw.githubusercontent.com/bikal1000/openvpn-connect/master/vpn -o /usr/local/bin/vpn && sudo chmod +x /usr/local/bin/vpn
```

## Prerequisites

Before running this script, you must have the following installed:

- OpenVPN client
- Bash shell
- oathtool

## Process to install oathtool in linux
- $ sudo apt update
- $ sudo apt upgrade
- $ sudo apt install oathtool gnupg2

For more [Use oathtool Linux command line for 2 step verification (2FA)](https://www.cyberciti.biz/faq/use-oathtool-linux-command-line-for-2-step-verification-2fa/).

## Usage

To use this script, follow these steps:

1. Save your OpenVPN configuration file to `/etc/openvpn/client.ovpn`.

2. Run the script with the following command: `vpn`

3. The script will prompt you for your OpenVPN server username, password and secret code.

4. If the username, password and secret code are correct, the script will connect you to the OpenVPN server.

## Saving Your Credentials

By default, this script saves your username, password and secret code to the `~/.openvpn-auth` file. On subsequent runs of the script, it will read your saved credentials from this file and use them for authentication.

## Security Considerations

This script is designed to simplify the process of connecting to an OpenVPN server, but it does so by storing your credentials in a plain text file. As such, it is not recommended to use this script in production environments or on systems that contain sensitive information.

## License
This script is available under the MIT License. See the LICENSE file for more information.
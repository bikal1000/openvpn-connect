# OpenVPN Connect Script

This script is designed to simplify the process of connecting to an OpenVPN server with authentication. It prompts the user for a username and password, and concatenates an authentication code to the password for authentication with the OpenVPN server.

## Installation

To install this script, run the following command in your terminal:

```shell
sudo curl https://raw.githubusercontent.com/bikal1000/openvpn-connect/master/openvpn-connect -o /usr/local/bin/openvpn-connect && sudo chmod +x /usr/local/bin/openvpn-connect
```

## Prerequisites

Before running this script, you must have the following installed:

- OpenVPN client
- Bash shell

## Usage

To use this script, follow these steps:

1. Run the script with the following command: `openvpn-connect <auth_code>`
   - Replace `<auth_code>` with your actual authentication code.
   - If you don't have an authentication code, leave this argument blank and the script will prompt you for it.

2. The script will prompt you for your OpenVPN server username and password.

3. If the username and password are correct, the script will connect you to the OpenVPN server.

## Saving Your Credentials

By default, this script saves your username and password to the `~/.openvpn-auth` file. On subsequent runs of the script, it will read your saved credentials from this file and use them for authentication.

## Security Considerations

This script is designed to simplify the process of connecting to an OpenVPN server, but it does so by storing your credentials in a plain text file. As such, it is not recommended to use this script in production environments or on systems that contain sensitive information.

## License
This script is available under the MIT License. See the LICENSE file for more information.
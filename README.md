# VPN Connection Manager

This script allows you to manage VPN connections using SSH. You can list available VPNs, connect, set a default connection, and monitor active connections.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Commands](#commands)
- [Dependencies](#dependencies)
- [License](#license)

## Prerequisites

- Ensure you have a Unix-like environment (Linux, macOS).
- Make sure you have `ssh` and `sshpass` installed:
  - For Ubuntu/Debian: 
    ```bash
    sudo apt-get install openssh-client sshpass
    ```
  - For macOS:
    ```bash
    brew install hudochenkov/sshpass/sshpass
    ```

## Installation

1. **Download the Script**
   Save the script to a file, for example `vpn_manager.sh`.

   ```bash
   git clone https://github.com/blue-lotus-org/sshvpn-client.git
   ```

2. **Make the Script Executable**
   Run the following command to make the script executable:

   ```bash
   chmod +x vpn
   ```

## Configuration

- Create a configuration file at `~/.vpn_config` with the following format:

  ```
  VPN_Name,username@host,port,/path/to/private/key,password
  ```

  Example:
  ```
  WorkVPN,user@work.com,1080,/home/user/.ssh/id_rsa,
  HomeVPN,user@home.com,1080,,mypassword
  ```

- Optionally, create a default file at `~/.vpn_default` to store the default connection number.

## Usage

Run the script using the following command:

```bash
./vpn
```

### Connecting to the Default VPN

To connect to the default VPN, use:

```bash
./vpn -d
```

## Commands

The script provides the following options:

1. **List VPNs**: Display available VPNs.
2. **Add VPN**: Add a new VPN entry.
3. **Delete VPN**: Remove an existing VPN entry.
4. **Update VPN**: Modify an existing VPN entry.
5. **Connect to VPN**: Connect to a specified VPN.
6. **Set Default VPN**: Set a VPN as the default connection.
7. **Monitor Connections**: Keep track of active VPN connections.
8. **Quit**: Exit the script.

## Dependencies

- **OpenSSH**: Required for establishing SSH connections.
- **sshpass**: Required for password-based authentication.


# MIT License

```
MIT License

Copyright (c) [2024] [lotuschain.org](https://lotuschain.org/) [github](https://github.com/blue-lotus-org)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

1. The above copyright notice and this permission notice shall be included in
   all copies or substantial portions of the Software.

2. THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
   IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
   FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
   AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
   LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
   OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
   SOFTWARE.
```

## How to Use

- Replace `[year]` with the current year.
- Replace `[your name or organization]` with your name or the name of your organization.

## Adding to Your README

You can include the above MIT License section at the end of your README file. This ensures users know their rights regarding the use of your script.

---


# Anyconnect CLI

A handy CLI utility for logging onto AnyConnect VPN.


## Badges

![GitHub](https://img.shields.io/github/license/psimonov/anyconnect-cli?style=for-the-badge)

![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/psimonov/anyconnect-cli?label=latest%20version&style=for-the-badge)

![GitHub last commit](https://img.shields.io/github/last-commit/psimonov/anyconnect-cli?style=for-the-badge)


## Available commands

The available commands are described in the "Usage" section.


## Installation

All of the following steps should preferably be carried out in your home directory. This guide is only valid for Linux and Mac. It is possible that windows support will be available in the future.

1) First the dependencies and cli authenticator (https://github.com/rfocosi/otp-cli) must be installed:
    ### Ubuntu/Debian
    ```bash
    $ apt install coreutils
    $ apt install oathtool
    ```

    ### MacOS
    ```bash
    $ brew install coreutils
    $ brew install oath-toolkit
    ```

2) Clone the repository:
    ```bash
    $ git clone git@github.com:rfocosi/otp-cli.git
    ```

3) Next - adding a keychain:
    ```bash
    $ ./otp-cli add
    ```
  
   * Token name: the name of the keychain, for example, e.g. VPN (this is VPN_OTPLABEL variable in the script).
   * Token key: passphrase for the authenticator.
   * Password: to automate the login process, password protection for the keychain itself is unnecessary - press Enter.
   * Confirm password: press Enter.

4) Replace the values of variables VPN_USERNAME, VPN_PASSWORD and VPN_OTPLABEL with your own.


## Usage

You can use a separate command to connect/disconnect, copy token and see you connection status.

Connect:
```bash
$ ./vpn
```

Disconnect:
```bash
$ ./vpn -d
```

Show and copy token in clipboard:
```bash
$ ./vpn -t
```

Show connection status:
```bash
$ ./vpn -s
```

Show available commands:
```bash
$ ./vpn help
```


## Roadmap

- Create an installation script.

- Intercepting errors.

- Rewrite the code in python.


## Contributing

You can email or create a pull request adding any ideas or fixes.


## Feedback

If you have any feedback, please reach out to us at psimonov.web@gmail.com.

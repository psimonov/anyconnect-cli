# A handy CLI utility for logging onto AnyConnect VPN.

## Available commands

### Connect:

```
$ ./vpn
```

### Disconnect:

```
$ ./vpn -d
```

### Status:
```
$ ./vpn -s
```

### Available commands:
```
$ ./vpn help
```

## Install

All of the following steps should preferably be carried out in your home directory. This guide is only valid for Linux and Mac. It is possible that windows support will be available in the future.

1) First the dependencies and cli authenticator (https://github.com/rfocosi/otp-cli) must be installed:
    ### Ubuntu/Debian
    ```
    $ apt install coreutils
    $ apt install oathtool
    ```
  
    ### MacOS
    ```
    $ brew install coreutils
    $ brew install oath-toolkit
    ```
  
2) Clone the repository:
    ```
    $ git clone git@github.com:rfocosi/otp-cli.git
    ```
  
3) Next - adding a keychain:
    ```
    $ ./otp-cli add
    ```
  
  * Token name: the name of the keychain, for example, e.g. VPN (this is VPN_OTPLABEL variable in the script)
  * Token key: passphrase for the authenticator
  * Password: to automate the login process, password protection for the keychain itself is unnecessary - press Enter
  * Confirm password: press Enter


4) Replace the values of variables VPN_USERNAME, VPN_PASSWORD and VPN_OTPLABEL with your own

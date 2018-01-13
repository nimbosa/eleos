# Eleos

Assistance is available: Zen Slack – get a login at https://slackinvite.zensystem.io and the slack is at https://zencash.slack.com

Eleos is a multi-platform wallet for zero-knowledge cryptocurrencies written in Electron. 

  - Compatible with Windows, MacOS, and Linux
  - No third-party Java dependencies required
  - Supports Zencash, Zclassic, and Zcash

![Screenshot](https://i.imgur.com/zHn4Hx8.png)

### Installation
Note: First time installations may take awhile to load since ~1GB of cryptographic data must be downloaded first.

##### Windows and MacOS
The simplest way to get started on Windows or MacOS is to [download and run the latest installer](https://github.com/zencashofficial/eleos/releases).

##### Linux
Note: Eleos requires that the compiled wallets are named zcashd-linux or zcld-linux and are saved into the eleos directory.
Get the dependencies

The default Node.JS version in the default Debian repositories is incompatible with Eleos, you'll need to download the latest version:
```
curl -sL https://deb.nodesource.com/setup_6.x -o nodesource_setup.sh
vim nodesource_setup.sh        # Read the file before running it to make sure it's not malicious
chmod +x nodesource_setup.sh
./nodesource_setup.sh
apt-get install nodejs
```

You'll also need various npn packages:
```
npm install electron tcp-port-used tar-fs request-progress ht-auth express-ws node-pty
```

Get the source
```
git clone https://github.com/zencashio/eleos.git eleos
```

Copy the Zclassic/Zcash wallet daemon into the elos directory (name the binary zcld-linux or zcashd-linux)
```
cp ~/Builds/zclassic/src/zcashd ~/Builds/elos/zcld-linux
```
or
```
cp ~/Builds/zcash/src/zcashd ~/Builds/elos/zcashd-linux
```
Start eleos
```
cd ~/Builds/eleos && npm start
```

For mac, the files are located in:
```
/Applications/eleos.app/Contents/Resources/app
```


### Supported Wallets

Eleos is primarily designed for Zcash-based cryptocurrencies. The wallet.dat for each cryptocurrency is stored in the directories below.

| Support | Status | Windows Location | MacOS Location |
| ------ | ------ | ------ | ------ |
| Zclassic | Fully supported | %APPDATA%/Zclassic | ~/Library/Application Support/Zclassic |
| Zcash | Fully supported | %APPDATA%/Zcash | ~/Library/Application Support/Zcash |
| Zencash | Fully supported | %APPDATA%/Zen | ~/Library/Application Support/Zen |


### Development

Want to contribute? Great! We need help.


### Todos

 - Display shielded tx generation status
 - Write MOAR tests
 - Write MOAR documentation

### Help!
  - Slack:  get a login at https://slackinvite.zensystem.io and the slack is at https://zencash.slack.com
  - Other:  Submit a Github issue as needed.

### License
Common Public Attribution License (CPAL-1.0)
(c)2017 Josh Yabut, (c)2017 ZenCashOficial

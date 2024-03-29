# Masternode-setup-guide

## 1. Wallet Setup

1.1 Download the wallet for your operating system which is available on the bottom of our page at
https://github.com/legends420/Reliefcoin-v2/releases/download/v2.0.0.0-A/reliefcoin-qt.exe <br />

1.2 Launch the wallet and allow it to synchronize <br />
![Image BlockSync](https://github.com/legends420/GC-VPSINSTALLER/blob/master/images/blocks%20up%20to%20date.png) </br>

1.3 Encrypt your wallet! (Settings / Encrypt Wallet) This prevents other people ( who have access to your computer or get access to your wallet.dat file ) to get in your wallet. Don't lose that password. If you lose it the wallet is locked forever and nobobdy will be able to recover your funds. </br>
![Image Encrypt](https://github.com/legends420/Reliefcoin-VPS-INSTALLER/blob/master/images/encrypt.png) </br>

1.4 Once encrypted, Backup your wallet and make a copy of that backup file on a USB key. </br>
![Image backup](https://github.com/legends420/Reliefcoin-VPS-INSTALLER/blob/master/images/backup.png) </br>

1.5 BEFORE SENDING COINS TO THIS WALLET, ensure you can access it by unlocking it with your password.  </br>
![Image unlock](https://github.com/legends420/Reliefcoin-VPS-INSTALLER/blob/master/images/unlock.png) </br>

1.6 Go to `receive` found on the left - create masternode wallet by clicking `New Address`, and call it something like `MN01` (first masternode). If this is not your first TGAO masternode, name it appropriately (ex.: `MN03` if it's your third) <br />

1.7 Send EXACTLY 50,000 coins to the wallet address you've just created by right-clicking on that new address and clicking on `Copy Address` then going to the send tab and pasting that address in the `Pay To` field. Make sure that it's exactly 50000 - no more, no less.<br />

1.8. Go to `Help / Debug Window / Console ` and type `masternode outputs` <br />

1.9. Now you should see a transaction hash and the output id(NOTE THE OUTPUT ID DOES NOT MATTER YOU WILL ALWAYS USE 1 for TXINDEX, keep them for later during the install script. (Copy them to a notepad or text editor) <br />
![Image txhash](https://github.com/legends420/Reliefcoin-VPS-INSTALLER/blob/master/images/txhash.png) </br>

1.10. If you don't have a transaction hash (or a new one if this is not your first masternode), that means that you've either NOT sent exactly 50000 coins OR it hasn't confirmed yet. If you HAVE sent EXACTLY 50000 coins, wait 5 minutes and try `masternode outputs` again.

## 2. Set up the Masternode on a Linux VPS

2.1 Choose your VPS

VPS server required: We recommend the following specifications:
- https://www.vultr.com/?ref=7490761
- $5 Basic cloud computer package
- Choose any location close to you for optimal connectivity to your server
- Ubuntu 16.04.x64
- Server (Name anything you want, i.e matrix)</br>
![Image Vultr](https://github.com/legends420/Reliefcoin-VPS-INSTALLER/blob/master/images/vultr1.png) </br>

2.2 Start an SSH session

Depending upon which operating system you are using. Download the following software:

- [Windows - PUTTY](https://www.putty.org/)
- Mac/Linux - Terminal ( preinstalled ) - You can find terminal by following the steps: Go to finder, then click on utilities, then you'll find terminal there.

Next:

2.2.1 Load the SSH terminal<br />

2.2.2 Copy your IP from the VPS - And for windows Putty simply put in the IP and press enter. For Mac/Linux, use the command: 
```
ssh root@(yourserveripaddress)
```

2.2.3 It will connect to the server. Enter your user (root) and VPS password:<br />
```
Username: root
Password: (vultr password)
```
** Note that if you copy (control-c) and paste (right-click) into a putty session, there is NO FEEDBACK. That means you won't see the characters being typed or pasted in. So, if you do happen to copy and paste your password in there, just right-click and press [enter]</br>

# 3. Installing the Masternode on the VPS

3.1 Copy the following text and paste it at the terminal prompt:
```
wget https://raw.githubusercontent.com/legends420/Reliefcoin-VPS-INSTALLER/master/deploy.sh && chmod +x deploy.sh && ./deploy.sh
```

3.2 Press `ENTER` Then Simply follow the on-screen instructions.

# 4. Questions?

If you have a problem or a question you can find us in the #support channel on our Discord. 

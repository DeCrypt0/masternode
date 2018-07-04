**MASTERNODE INSTALLATION GUIDE UBUNTU 16.04**
Download local wallet, generate new receiving address and name it. (Ex. MN01) This is your ALIAS.
Send coins over to the new MN01 wallet address, make sure it's exactly 1,000 coins.

`Go to Settings -> Options -> Wallet -> Check the tickbox for: Show Masternodes Tab`

**RUN THIS SCRIPT ON YOUR UBUNTU 16.04 VPS**
`wget https://raw.githubusercontent.com/GlynoD/masternode/master/glyno_ubuntu_install.sh && chmod +x glyno_ubuntu_install.sh`

`./glyno_ubuntu_install.sh`


**AFTER SCRIPT**
The script will give you a `MASTERNODE PRIVKEY` and your `EXTERNALIP:PORT`
Copy this information, as you will need it for the masternode.config in the next step.

Copy the MASTERNODE PRIVKEY and EXTERNALIP:PORT from the script installation.

**OPEN LOCAL WALLET**
Go to: `Tools -> Debug Console`
Write: `masternode outputs`


Copy the *TXID* and *TXINDEX*.

Close the Debug Console and go to `Tools -> Open Masternode Configuration`.

Here you have to add the information from the previous steps, in a new line like this:
`ALIAS MASTERNODEIP:PORT MASTERNODEPRIVKEY TXID TXINDEX`


Save and restart local windows wallet.
After the restart, go to Masternode tab, wait for full sync and Start Masternode Alias.

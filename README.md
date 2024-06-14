# Thinkpad-T460-Hackintosh-Sonoma-EFI
EFI for Thinkpad T460 

**What works?**
- Physical buttons, touchpad, keyboard
- Bluetooth and WiFi
- Location
- Video acceleration (no support for FairPlay)
- Function keys
- Hibernation

**What doesn't work?**
- Airdrop, Handoff, Find My Mac, etc.
- Fingerprint reader (no drivers, so it doesn't work)

**How to install?**

1. **Downloading GenSMBIOS and ProperTree**

For Apple Secure Boot to work, you need a "real" Mac,
So you need to add its SMBIOS to config.plist
You need to have Python installed
Choose the first option, go to the second option "Generate SMBIOS", enter MacBookPro15,2 and you will get the data you need to enter in config.plist
Launch ProperTree, go to PlatformInfo > Generic.
Fill in the empty fields as follows:
- Type into SystemNumberName
- Serial into SystemProductName
- Board Serial into MLB
- SmUUID into SystemUUID

2. **Downloading macOS recovery image**
3. **Guide can be found here:**
   https://dortania.github.io/OpenCore-Install-Guide/installer-guide/
5. **Boot the USB drive and proceed with the installation like any other system**
6. **Disabling AppleSecureBoot (optional if the installer doesn't work)**

- If the installer won't boot after a 20-minute installation, disable AppleSecureBoot
- Go to Misc > Security
- Change the SecureBootModel option from Default to Disabled
- After installing and configuring macOS, re-enable it by setting it back to Default

# Introduction #

To send Push notification to an application/device couple you need an unique device token (see the [ObjectiveC page](http://code.google.com/p/apns-php/wiki/ObjectiveC)) and a certificate.

## Generate a Push Certificate ##

To generate a certificate on a **Mac OS X**:
  1. Log-in to the [iPhone Developer Program Portal](http://developer.apple.com/iphone/manage/overview/index.action)
  1. Choose **App IDs** from the menu on the right ([or click here](http://developer.apple.com/iphone/manage/bundles/index.action))
  1. Create an App ID without a wildcard. For example `3L223ZX9Y3.com.armiento.test`
  1. Click the **Configure** link next to this App ID and then click on the button to start the wizard to generate a new **Development Push SSL Certificate** ([Apple Documentation: Creating the SSL Certificate and Keys](http://developer.apple.com/iphone/library/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ProvisioningDevelopment/ProvisioningDevelopment.html#//apple_ref/doc/uid/TP40008194-CH104-SW4))
  1. Download this certificate and double click on `aps_developer_identity.cer` to import it into your Keychain
  1. Launch **Keychain Assistant** (located in Application, Utilities or search for it with Spotlight) and click on My Certificates on the left
  1. Expand **Apple Development Push Services** and select Apple Development Push Services **AND** your private key (just under Apple Development Push Services)
  1. Right-click and choose "Export 2 elements..." and save as `server_certificates_bundle_sandbox.p12` (don't type a password).
  1. Open **Terminal** and change directory to location used to save `server_certificates_bundle_sandbox.p12` and convert the PKCS12 certificate bundle into PEM format using this command (press _enter_ when asked for _Import Password_):
```
openssl pkcs12 -in server_certificates_bundle_sandbox.p12 -out server_certificates_bundle_sandbox.pem -nodes -clcerts
```
  1. Now you can use this PEM file as your certificate in ApnsPHP!

## Verify peer using Entrust Root Certification Authority ##

Download the Entrust Root Authority certificate **directly from Entrust Inc. website**:
  1. Navigate to https://www.entrust.net/downloads/root_index.cfm
  1. Choose "Personal Use"
  1. Download the Entrust CA (2048) file (entrust\_2048\_ca.cer) https://www.entrust.net/downloads/binary/entrust_2048_ca.cer for the **Sandbox environment**; download the Entrust Secure Server CA file (entrust\_ssl\_ca.cer) https://www.entrust.net/downloads/binary/entrust_ssl_ca.cer for the **Production environment** _until December 22nd_ (**after December 22nd, 2010 you have to use entrust\_2048\_ca.cer also for the Production Environment** as Apple said: _"To ensure you can continue to validate your server's connection to the Apple Push Notification service, you will need to update your push notification server with a copy of the 2048-bit root certificate from Entrust's website."_).
If you want to use the same file for the Sandbox and the Production environment please concat the two certificates. For example:
```
wget https://www.entrust.net/downloads/binary/entrust_2048_ca.cer -O - > entrust_root_certification_authority.pem
echo >> entrust_root_certification_authority.pem
wget https://www.entrust.net/downloads/binary/entrust_ssl_ca.cer -O - >> entrust_root_certification_authority.pem
```

Otherwise (_for use **only** in a Mac OS X environment_), export the Entrust Root Authority certificate:
  1. Launch **Keychain Assistant** (located in Application, Utilities or search for it with Spotlight) and click on System Root Certificate on top-left and Certificates on the bottom-left
  1. Right-click on **Entrust Root Certification Authority** and export with `entrust_root_certification_authority.pem` file name and choose as document format **Privacy Enhanced Mail (.pem)**.
  1. Now you can use this PEM file as Entrust Root Certification Authority in ApnsPHP to verify Apple Peer!

## <font color='red'>Please, use <a href='https://groups.google.com/group/apns-php'>ApnsPHP Google Group</a> for help requests or to discuss about this project. To report an issue use <a href='https://github.com/duccio/ApnsPHP/issues'>Issues</a>. Thanks!</font> ##
Hello this project aims to push DHT11 sensor data via NodeMcu to Aws IoT and Blynlk platforms.

Wifi Conenction.
->The Wifi conenction is priority based you can provide three SSID's and Password's and which ever is scanned first the device will connect to that network.
->Future plans include using Wifi manager for OTA updates and Configurable System properties(SSID, Password).


For AWS IoT Connection.
->Generate AWS IoT Connection Certificate and attach and appropriare policy to it.
->Activate the Certificate and copy the endpoint of the IoT Instance.
->Copy the device cert and private key to the EspAwsIoT.ino file to strings "certificatePemCrt" and "privatePemKey" respectively. 
 While copying neglect the below stated lines.


 For Device Cert
"-----BEGIN CERTIFICATE-----"
"----END CERTIFICATE-----"


For Device Private Key
"-----BEGIN RSA PRIVATE KEY-----"
"-----END RSA PRIVATE KEY-----"

For Blynk Connection,
-> Copy & Paste Authorization key to the "auth" array.

Finally.
->Compile and Enjoy.

Future Work
->AWS Rule setup (DynamoDb, SNS Trigger, Analytics)
->Setup a Web Platform for Data Visualization.

Note:
Currently NodeMcu takes 7-8 seconds for TLS authentication but it can be reduced by using a dedicated encryption hardware.
This android application allows you to enter two numbers to calculate division and multiplication of numbers and showing calculated result to user.
Calculations performed on BtCalc application that is remotely connected using bluetooth connection.

**Problem statement**
Create a app with Bluetooth communication between two Android devices.
App on Device one
It has a Text Area where user types some text.
It will have selection for multiplication and division operation
App on Device two
Will display the text entered in the device one.
Will have input field to capture variable(number)
Operation selected is device one will be performed on device two with variable and number of word count.
Device two will respond back with the result and displayed on device one.
Data should be encrypted and sent between two devices



***Features***
The android app lets you:

1. Turn on device bluetooth and device discovery.
2. View list of all paired and nearby available bluetooth devices.
3. Select any device from device list and connect with that bluetooth device. Device must have BtCalc app running in that.
4. Status that devices are successfully connected is updated on Home screen of app.
5. Enter numbers to divide or multiply on remotely connected app, and show result that app received from bluetooth device.
6. Press the given "*" and "/" buttons to validate entered numbers and perform remote calculations on entered numbers.
7. Calculation that is performed for any remotely connect app can be found on "Remote calculation data".
8. Unit test cases are written for division and multiplication of numbers.

**Screenshots**




** Solution Approach**
1. Used Kotlin for application development.
2. BluetoothAdapter has been used for all Bluetooth requests.
3. To connect with remote device we have listed all the Bluetooth device that are available in the vicinity, user would select any device for pairing and connection.
4. Initiator app will create a ClientBluetoothSocket that will be open to send communication messages to connected device. Remote device that is connected will use BluetoothServerSocket
to listen for connection requests, when a device with same app tries to connect, server device got connected and opens a socket to send messages.
5. When a user enter two numbers and press divide or multiply buttons json message sent to connected device for calculation, connected device calculate and share json result with client device.
6. Once connection is established both devices can perform calculation on each other by pressing buttons.
3. Junit has been used to write unit test cases for calculation function.




**Permissions required**
1. android.permission.BLUETOOTH
2. android.permission.BLUETOOTH_ADMIN
3. android.permission.ACCESS_FINE_LOCATION
4. android.permission.ACCESS_COARSE_LOCATION

Runtime permission is required for LOCATION permission.




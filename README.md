# Fingerpoint-Authentication

![Image description](https://s3.ap-south-1.amazonaws.com/mindorks-server-uploads/authentication-using-fingerprint-banner.png)

Gone are the days when you have to manually enter the username and password for login into some Android application. Not only you have to enter it manually, but it is also a time-consuming process. Also, if you forgot the password or username then you have to recover it by going through a series of steps. But on the other end, if we are using Fingerprint for Authentication, then there is no need to remember password. Also, no two persons can have the same Fingerprint, so, we need not worry about authenticity.

So, in this blog, we will learn how to use Fingerprint authentication in our Android applications. So, let’s get started.

## Fingerprint Authentication overview

With the release of Android 6.0 (Android M), there has been a significant amount of changes to the APIs, one of them is Fingerprint Authentication. Now, we can easily implement Fingerprint Authentication in our application in the devices having the Fingerprint sensor. The whole process of Fingerprint Authentication can be summarized into the below steps:

1. Requesting Fingerprint Authentication permission within the project’s manifest file.

2. As fingerprints can only be registered on the devices which have its lock screen protected by a PIN, pattern or password. So, we have to check if the lock screen of the device is protected by a PIN, pattern or password.

3. Then, create an instance of the FingerprintManager class.

4. You have to gain access to the storage area that is used to store the cryptographic keys on Android devices i.e. Keystore. So, create an instance of the Keystore to gain access of the Android Keystore container. After that, generate an encryption key with the help of keyGenerator class and store it in the Keystore container.

5. With the help of the key generated and stored in the Keystore container, initialize the instance of the Cipher class and use this instance to create a CryptoObject and assign it to FringerprintManager instance that you have created earlier.

6. Call the authenticate method of the FingerprintManger class and implement methods to handle the callbacks.

# AI2_ANDROID_THINGSPEAK_CLIENT_EXTENSION
Android client ThingSpeak extension for MIT Application Inventor 2

This extension is intended to easily make use of the Read and Write features of the ThingSpeak cloud service provided by MathWorks in such a manner that programmer is able to transparently make use of the service without having to deal with much details of the implementation in the code side. With the App - also attached - you can easily check the extension working on a friendly interface:



Essentially ThingSpeak is a Web server on which data is read and written via GET commands of the Http protocol. All replies come on the JSon format in raw text with no formatting, which means that no LF or CR characters are added, as can be seen on the left side of the following picture:


( picture taken form Jsonformatter )

All you have to do is subscribe to the ThingSpeak website, create a channel, and take note of the following data automatically generated:


It is important to note that all data sent and received are in the ASCII format at the URL body, which means that if one wish provide extra security, it should be considered any kind of cyphering or even cryptography in order to atleast detect whether data was maliciously corrupted or not. Another poit to remark is that parsing was performed without using any JSon library, which means that if on the one hand the structural integrity of the JSON format is not checked out, on the other hand it means that tasks are performed lightweight, not wasting core processing if application require update realtime.

Here's an overview of the "source code" or rather, "source blocs" of the above demo application.
That's all you need, nothing else:


Below, a snapshot of the components:



Here, a snippet showing how much of the boring coding task can be avoided by customer, once it is embedded on the extension itself:




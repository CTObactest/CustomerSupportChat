[![](https://jitpack.io/v/Asutosh11/CustomerSupportChat.svg)](https://jitpack.io/#Asutosh11/CustomerSupportChat)
# Android CustomerSupportChat Library
This is a Customer Chat library that you can add to your Android applications. 

<b>How it works?</b><br>
You need to enter your XMPP server details, details of your user's XMPP account and XMPP id of the customer support executive sitting somewhere else on an XMPP client.
The library opens a chat window for your app user and a customer support executive to chat.

<b>Screenshot</b><br>
<img src="https://github.com/Asutosh11/CustomerSupportChat/blob/master/screenshot1.jpg" alt="Screenshot" style="width: 200px;"/>


Add the dependency to your build.gradle

 ```
allprojects {
    repositories {
        maven {
            url 'https://jitpack.io'
        }
    }
}
dependencies {
    compile 'com.github.Asutosh11:CustomerSupportChat:1.0'
}

 ```

This is how you use it

```
ChatConnection mChatConnection = new ChatConnection();
mChatConnection.setxmppCustomerUsername("test1");
mChatConnection.setxmppCustomerPassword("test1");
mChatConnection.setxmppPortNo("5222");
mChatConnection.setxmppHostName("asutosh.p1.im");
mChatConnection.setxmppServiceName("asutosh.p1.im");
mChatConnection.setxmppIdOfSupportExecutive("test2@asutosh.p1.im");
mChatConnection.setchatWindowTitle("Support chat window");
ChatActivity.startChat(mChatConnection, MainActivity.this);
```


### Thanks

 * [Smack](https://github.com/igniterealtime/Smack)
 * [android-ago](https://github.com/curioustechizen/android-ago)
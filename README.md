Drift
============
![Release](https://jitpack.io/v/driftt/drift-sdk-android.svg)

Drift is the official Drift SDK for Android


# Features:
- Create conversations from your app
- View past conversations from your app.


# Getting Setup

## Installation

Drift uses [Jitpack](http://jitpack.io) for its releases

Add Jitpack to your root build.gradle file 

```
allprojects {
	repositories {	
		maven { url 'https://jitpack.io' }
	}
}
```

You can then add drift as a dependency in your app build.gradle file


```
dependencies {
	compile 'com.github.driftt:drift-sdk-android:v1.0'
}
```

## Registering

To get started with the Drift SDK you need the embed ID from your Drift settings page. This can be accessed [here](https://app.drift.com/settings/livechat) by looking after the drift.load method in the Javascript SDK.

In your Application `onCreate` method call:
```Java
Drift.setupDrift(this, "");
```

Once your user has successfully logged into the app registering a user with the device is done by calling register user with a unique identifier, typically the id from your database, and their email address:

```Java
Drift.registerUser("123748", "sample@drift.com");
```

When your user logs out simply call logout so they stop receiving messages.

```Java
Drift.logout();
```


# Messaging

A user can begin a conversation in response to a campaign or by presenting the conversations list

```Java
  Drift.showConversationActivity();
```

Thats it. Your good to go!!

# Customisation

Configuring the colors used within the app can be done [here](https://app.drift.com/settings/widget/design)

To configure the accent color used in the SDK you should define a color attribute in your apps color resource file.

```xml
<color name="driftColorAccent">#157AFB</color>
```

# Contributing

Contributions are very welcome 🤘.

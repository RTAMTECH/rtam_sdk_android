
# RTAMUniversalSDK

Ads and Analytics Framework

## [](https://docs.aiactiv.io/sdk/android#installation)Installation

RTAMUniversalSDK is available through  [MVN](https://mvnrepository.com/search?q=rtam). To install it, add mavenCentral to your repositories if it's not added yet.

repositories {

  mavenCentral()

}

Import RTAMUniversalSDK dependency

dependencies {

 implementation 'io.rtam:universal-sdk:0.1.4'

}

Add this code to app manifest, wrapped in  `<application>`  tag and replace FILL_YOUR_WRITE_KEY_HERE

<meta-data  android:name="io.rtam.sdk.WRITE_KEY"  android:value="FILL_YOUR_WRITE_KEY_HERE"  />

By default, we use same WRITE_KEY for both frameworks. If you would like use WRITE_KEY for AdNetwork, please add new one meta-data for it.

<meta-data  android:name="io.rtam.sdk.WRITE_KEY_ADNETWORK"  android:value="FILL_YOUR_WRITE_KEY_HERE"  />

## [](https://docs.aiactiv.io/sdk/android#usage)Usage


#### [](https://docs.aiactiv.io/sdk/android#track-events)Track Events

RTAM.with(context).apply  {

  track("Application launched")

}

// or

RTAM.track(applicationContext,  "Application launched")

#### [](https://docs.aiactiv.io/sdk/android#identify-events)Identify Events

RTAM.with(context).apply  {

  // Traits about user like email, phone number, birthday...

 val traits =  Traits()

  identify("user id", traist)

}

// or

// Traits about user like email, phone number, birthday...

val traits =  Traits()

RTAM.identify(applicationContext,  "user id", traist)

#### [](https://docs.aiactiv.io/sdk/android#screen-events)Screen Events

RTAM.with(context).apply  {

  // Properties about screen like content id, title...

  screen("screen name", properties)

}

// or

// Properties about screen like content id, title...

RTAM.identify(applicationContext,  "user id", properties)

## [](https://docs.aiactiv.io/sdk/android#author)Author

RTAM TECH,  [tech@rtam.io](mailto:tech@aiactiv.io)

## [](https://docs.aiactiv.io/sdk/android#license)License

RTAMUniversalSDK is available under the MIT license. See the LICENSE file for more info.

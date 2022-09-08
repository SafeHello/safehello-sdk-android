# SafeHello Android SDK

## Installation

The Android SDK is distributed as an `aar bundle` and is compatible with Android SDK API 24 and above. 
You just need to add the Safe Hello sdk aar bundle to your `libs` folder, and you're ready to start using it!

## Usage

To start using the sdk, import the SDK:

```kotlin
import com.safehello.sdk.SafeHelloSdk
```

### Connect to SafeHello

To establish a secure connection with SafeHello, from your backend server you will need to provide an endpoint to get a connection token. Once you receive a token, you can set it on the SafeHelloSdk and send the connect command.

```kotlin
private fun connectToSafeHello() {
  SafeHelloSdk.token = "Your-fetched-connection-token" // Fetch from your backend server 
  SafeHelloSdk.observeEvents()
}
```

### Launch SafeHello

To incorporate the SafeHello flow into your app, you just need to use the `launchSafeHello()` method, which allows us to customize the initial title and subtitle that could be specific to your app.

```kotlin
import com.safehello.sdk.Router

private fun launchSafeHello() {
    Router.showEventScreen(
        context = this,
        title = "Demo Meeting",
        subtitle = "08:00PM",
        eventId = "any-valid-event-id"
    )
}
```

## License

[SafeHello Android SDK License](LICENSE)

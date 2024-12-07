# Expo Linking.getInitialURL intermittent null return

This repository demonstrates a bug encountered with Expo's `Linking.getInitialURL` API.  The issue involves the method sporadically returning `null` despite a deep link successfully launching the application. The problem appears inconsistent across different devices and launches, making it difficult to pinpoint a precise cause. 

**Steps to reproduce the problem (may vary due to the intermittent nature):**

1. Clone the repository.
2. Run `expo start`.
3. Open the app, and attempt to use the generated deep link to open app again.
4. Observe `Linking.getInitialURL`'s result in the console.  You might need to try several times before encountering the `null` return.

**Solution:**

The provided solution includes additional checks to handle cases where `getInitialURL` might be delayed.

This issue highlights the need for robust error handling and potentially alternative approaches when dealing with asynchronous operations within the `Linking` API, especially for deep links that directly launch the app. 
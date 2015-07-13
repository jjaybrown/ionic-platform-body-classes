# Ionic Platform Body Classes
Document to describe the different platform classes applied to document body by `ionic.Platform`.

## Contribute 
Please submit PRs with any missing classes that adds a new row on the tables below.

# Platform Classes
`ionic.Platform` is a utility for providing meta information about the current device, it examines the current User Agent, Navigator and Document status to populate device information and add classes to `body`.

These classes allow Ionic to apply certain styles, polyfills and actions based on the platform. Commonly used to provide a platform specific 'look and feel'.

## Device Grades
Ionic determines a device grade based on the availability of web APIs and CSS features, whilst also taking into account the device's OS capabilities.

`ionic.Platform#setGrade - ionic.bundle.js`
>Set the grade of the device: 'a', 'b', or 'c'. 'a' is the best
>(most css features enabled), 'c' is the worst.  By default, sets the grade
>depending on the current device.


| Grade        | Class           | Description  |
| ------------- |----------------| --------------|
| A      | `grade-a` | All platforms are Grade A by default, based on CSS features being available and Web APIs. |
| B      | `grade-b` | Windows Phone is determined as Grade B by default. Android versions lower than 4.4 are graded as B also. |
| C      | `grade-c` | Android OS Versions lower than Version 4 are Grade C by default |


## Platforms
Ionic examines `window.Navigator` and `User Agent` to determine the platform your application is running under. Platform classes determine the "look and feel" of your application enabling automatically the relevant state transitions and iconography.

| Platform        | Class           | Description  |
| ------------- |-------------| --------------|
| Browser | `platform-browser` | Whether the application is running on the Desktop Browser - applied if you are running `ionic serve`  |
| Cordova | `platform-cordova` | Whether the application is running on the device, as the device uses Cordova to display the application |
| Webview | `platform-webview` | Whether the application is running within a webview on the device within a native application |
| iOS | `platform-ios` | The device is iOS based, therefore the "look and feel" will be given the iOS treatment |
| Android | `platform-android` | The device is Android based, therefore the "look and feel" will be given the Android treatment |
| Windows Phone | `platform-windowsphone` | The device is Windows Phone based, therefore the "look and feel" will be given the Windows Phone treatment |

### Platform OS Meta Classes
Ionic also applies OS meta classes which determine the version of platform OS and if iOS based, whether it's an iPhone, iPod or iPad.

| Platform OS Meta       | Class           | Description  |
| ------------- |-------------| --------------|
| iPad | `platform-ipad` | iOS device is an iPad - this will apply additional styles to menus etc |
| iPod | `platform-ipod` | iOS device is an iPod |

#### Platform OS Version Classes
Ionic also adds meta classes to determine the OS version, this can be used to fallback onto a more relevant "look and feel" or to accomodate for OS restrictions for that Version.

The version is formed by examing the `User Agent` of OS version and replacing the `.` with a `_` that separates the Major and Minor version numbers. e.g. `7.1` will be `7_1`

| Platform OS Version       | Class     |
| ------------- |-------------|
| iOS 4.2 | `platform-ios4_2` | 
| iOS 8.0 | `platform-ios8_1` |
| Android 4.4| `platform-android4_4` |

### Platform Meta Classes
Ionic also applies meta classes which determine whether a device is ready, displayed fullscreen or whether to add additional padding for the status bar to header bars.

| Platform Meta Property| Class     | Description   |
| ------------- |-------------|----------|
| Ready | `platform-ready` | The platform/Device is ready, Assets and the DOM have loaded.  |
| Full Screen | `fullscreen` | The application is displayed fullscreen on the device and will show the status bar, requires `org.apache.cordova.statusbar` to be enabled |
| Hide Status Bar| `status-bar-hide` | Hides the status bar when in fullscreen mode on the device, requires `org.apache.cordova.statusbar` to be enabled|

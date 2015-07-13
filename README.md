# Ionic Platform Body Classes
Document to describe the different device classes applied to body by Ionic Platform.

## Contribute 
Please submit PRs with any missing classes that adds a new row on the tables below.

# Platform Classes
`ionic.Platform` is a utility for providing meta information about the current device, it examines the current User Agent, Navigator and Document status to populate device information and add classes to `body`.

These classes allow Ionic to apply certain styles, polyfills and actions based on the platform. Commonly used to provide a platform specific 'look and feel'.

## Device Grades
Ionic determines a device grade based on the availability of web APIs and CSS features, whilst also taking into account the device's OS capabilities.

| Grade        | Class           | Description  |
| ------------- |:-------------:| --------------|
| A      | `grade-a` | All platforms are Grade A by default, based on CSS features being available and Web APIs. |
| B      | `grade-b` | Windows Phone is determined as Grade B by default. Android versions lower than 4.4 are graded as B also. |
| C      | `grade-c` | Android OS Versions lower than Version 4 are Grade C by default |

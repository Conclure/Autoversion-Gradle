# Autoversion-Gradle
<br>
This repository contains only one important file, `version.gradle`.
It's just a template file and currently depends on the gradle shadowJar plugin.
To use this you can just copy the content of `version.gradle` into your project.
Then all you need to do is put this in your `build.gradle`:
<br>
```gradle
apply from: 'version.gradle'
```
Assuming your `build.gradle` and `version.gradle` exist in the same directory.
<br>
There exist three custom new tasks by default `majorJar`, `minorjar` and `patchJar`.
First time running any of these tasks will produce a new `version.properties` holding version `1.0.0`.
But when running any of the three mentioned tasks above again will produce a new version.
<br>
## Task majorJar
Will reset the minor and patch version while also increase major version.

## Task minorJar
Will reset the patch version and increase minor version.

## Task patchJar
Will increase patch version.

#Android emulator detector

![](https://jitpack.io/v/framgia/android-emulator-detector.svg)

Easy to detect android emulator

#### Last check: 17/05/2016
    - BlueStacks Version 0.9.30 
    - Genymotion Version 2.6.0
    - Android Emulator 
    - .....

Download
-------
#####Gradle:

Step 1. Add it in your root build.gradle at the end of repositories:

```
allprojects {
	repositories {
		...
		maven { url "https://jitpack.io" }
	}
}
```

Step 2. Add the dependency
```
dependencies {
	    compile 'com.github.framgia:android-emulator-detector:1.1.1'
}
```

#####Maven:

Step 1. Add the JitPack repository to your build file
```
<repositories>
	<repository>
		<id>jitpack.io</id>
		<url>https://jitpack.io</url>
	</repository>
</repositories>
```

Step 2. Add the dependency
```
<dependency>
	<groupId>com.github.framgia</groupId>
	<artifactId>android-emulator-detector</artifactId>
	<version>1.1.1</version>
</dependency>
```

How to use
-------
Example:

```
EmulatorDetector.with(this)
                .setCheckTelephony(true)
                .setDebug(true)
                .detect(new EmulatorDetector.OnEmulatorDetectorListener() {
                    @Override
                    public void onResult(boolean isEmulator) {
                        
                    }
                });
```

- `setCheckTelephony` Check Imei, Operator network, Device ID...

    If `true` we need permission. Please add line below into `AndroidManifest.xml`
    ```
    <uses-permission android:name="android.permission.READ_PHONE_STATE" />
    ```
- `setDebug` Show log


About
-------


License
-------

    Copyright 2016 Framgia, Inc.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

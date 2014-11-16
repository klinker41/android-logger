# Android-Logger

This is a simple library that will allow Android apps to log both to the internal log, as well
as an external file so that users can easily grab logs for the application if you need one from
them.

Usage is simple, just switch your imports from:

```java
import android.util.Log;
```

to 

```java
import com.klinker.android.logger.Log;
```

For any of the logging to take place, you need to call Log.setDebug(true). I would not suggest
doing this for all users because logging takes time! Either only enable it for your debugging
and then disable it for production versions, or add a preference to your app for users to be
able to log everything and then tell them where the log is located so that they can send it to
you.

You can set the path of your log as well with

```java
Log.setPath("EvolveSMS/log.txt");
```

Please note, to use this you will need the following permission in your AndroidManifest.xml

```xml
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
```

And one more thing, the log will be wiped out and rewritten when it gets over 2 MB.

## Gradle

To include this library in your project, include the following in your gradle dependencies

```groovy
compile 'com.klinkerapps:logger:+'
```

## License

    Copyright 2013-2014 Jacob Klinker

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

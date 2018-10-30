# get gradle

    wget https://services.gradle.org/distributions/gradle-4.10.2-bin.zip
    unzip gradle-4.10.2-bin.zip 

Note that the gradle files in the project were small edits from:

    <path>/gradle-4.10.2/bin/gradle init

# get Android sdkmanager

    mkdir sdk
    wget https://dl.google.com/android/repository/sdk-tools-darwin-4333796.zip
    unzip sdk-tools-darwin-4333796.zip -d sdk
    export ANDROID_HOME=`pwd`/sdk

# Platform

Download platform-25_r03.zip into sdk/platforms/android-25

    ./sdk/tools/bin/sdkmanager --install "platforms;android-25"

# Build

    ./gradlew build
    ./gradlew installDebug

# Java Version

Needs a compatible Java version. On osx I use:

    export JAVA_HOME=`/usr/libexec/java_home -v 1.8.0_102`

# kudos

https://developer.okta.com/blog/2018/08/10/basic-android-without-an-ide

## Useful References:

- https://gradle.org/install/#manually
- https://guides.gradle.org/creating-new-gradle-builds/

- https://www.raywenderlich.com/249-gradle-tutorial-for-android-getting-started
- https://developer.android.com/topic/libraries/support-library/setup
- https://developer.android.com/guide/topics/ui/look-and-feel/themes
- https://developer.android.com/topic/libraries/support-library/packages

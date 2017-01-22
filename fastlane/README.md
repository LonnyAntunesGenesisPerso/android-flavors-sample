Fastlane documentation
================
## Zipalign
Reduction in the amoutn of RAM consumed when running the application

To work with it, we need to follow two steps :

 - inside the .bash_profile, add the following instructions in order to know the zipalin command

```
ZIPALIGN_HOME="/Users/lonny/Workspace-Pic/android-sdk-macosx/build-tools/25.0.2/"
export PATH="$ZIPALIGN_HOME:$PATH"
```

- Inside the build.gradle, add the following instruction : \"zipAlignEnabled true\"

```
buildTypes {
      release {
          minifyEnabled false
          proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
          zipAlignEnabled true
      }
}
```

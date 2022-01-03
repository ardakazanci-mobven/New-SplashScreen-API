# SplashScreen API Implementation Sample

## Installation - Usage


```sh
<style name="Theme.App.Starting" parent="Theme.SplashScreen">
      <!-- 
      The new theme will be used for the splash screen. It must have Theme.SplashScreen as a parent. In this example, the existing theme used throughout the app is called Theme.App, so a new Theme.App.Starting is created.
      -->
      <item name="windowSplashScreenBackground">@color/[...]</item>
      <!--
      The color that will be used as a solid background color in the splash screen/
      -->
      <item name="windowSplashScreenAnimatedIcon">@drawable/[...]</item>
      <!-- 
      The icon for the splash screen. If not defined, the app icon will be used instead. Note that this can be an animated icon using an AnimationDrawable or AnimatedVectorDrawable (in API 31 and lower, the AnimatedVectorDrawable is not supported). The animation duration is necessary if you set an animated icon.
      -->
      <item name="windowSplashScreenAnimationDuration">200</item>
      <!-- 
      Background color for the icon. Useful in case the contrast between the window background color and the icon color is not satisfactory.
      -->
      <item name="android:windowSplashScreenIconBackgroundColor">
        @color/[...]
      </item>
      <!-- 
      Optional "branding" image to be shown at the bottom of the screen (which is not recommended according to the doc).
      -->
      <item name="android:windowSplashScreenBrandingImage">
        @drawable/[...]
      </item>
      <!-- 
      The actual app theme that will be used when the splash screen is gone.
      -->
    <item name="postSplashScreenTheme">@style/Theme.App</item>
</style>
```
```sh
<manifest>
   <application android:theme="@style/Theme.App.Starting">
   [...]
<manifest>
   <activity android:theme="@style/Theme.App.Starting">
   [...]   
   
   class MainActivity : Activity() {

   override fun onCreate(savedInstanceState: Bundle?) {
       super.onCreate(savedInstanceState)
       installSplashScreen()
       setContentView(R.layout.main_activity)
       [...]
```

Source : https://www.rockandnull.com/splash-screen-android-example/

## License

MIT
**Free Software, Hell Yeah!**

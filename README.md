# SwipeDismissImage


A custom view for Android to display image with features like swipe to dismiss, zooming, pinning, etc.



### Q. Why I made this?

TL;DR... It all started when I got curious how gestures (specifically dragging) are implementated. Looking at the source code of some libraries which responds to such touch events, I was keen that I had to make something to learn/practice ;)

So I started making an activity which shows an image with various features despite not unique, (considering various alternatives) but I had to learn it. So anyways, after it become solid (IMO) I made it as a library. There are still some improvements needed which I'll keep on working as I improve my knowledge.

## Usage
A short summary on how-to use,

- Create an activity with the following layout as the `contentView`.

```xml
<com.kpstv.dismiss.image.SwipeDismissImageLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/sdl_layout"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    ...
</com.kpstv.dismiss.image.SwipeDismissImageLayout>
```

```kotlin
class ImageActivity : AppCompatActivity() {
   override fun onCreate(...) {
      ...
      sdl_layout.setSwipeDismissListener { finish() }
   }
}
```


<!-- - Do not forget to declare the activity in your manifest file along with the theme attribute.

```xml
<application>
   ...
   <activity
       android:name=".ImageActivity"
       android:theme="@style/Theme.Translucent"/>
</application>
```

- Finally, start the `ImageActivity` we just delcared.

```kotlin
startActivity(Intent(this, ImageActivity::class.java))
``` -->

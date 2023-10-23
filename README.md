Location Urls
http://ip-api.com/json
https://api.ipregistry.co?key=tryout

<ProgressBar
    android:id="@+id/splashProgressBar"
    style="@style/Widget.AppCompat.ProgressBar.Horizontal"
    android:layout_width="@dimen/_155sdp"
    android:layout_height="@dimen/_8sdp"
    android:progressDrawable="@drawable/progress_drawable_splash" />


<?xml version="1.0" encoding="utf-8"?>
<layer-list xmlns:android="http://schemas.android.com/apk/res/android">
    <item android:id="@android:id/background"
        android:gravity="center_vertical|fill_horizontal">
        <shape android:shape="rectangle">
            <corners android:radius="20dp"/>
            <solid android:color="@color/splash_color" />
        </shape>
    </item>
    <item android:id="@android:id/progress"
        android:gravity="center_vertical|fill_horizontal">
        <scale android:scaleWidth="100%">
            <selector>
                <item android:state_enabled="false"
                    android:drawable="@color/splash_color" />
                <item>
                    <shape android:shape="rectangle">
                        <corners android:radius="20dp"/>

                        <gradient
                            android:startColor="#E67050"
                            android:endColor="#DB2268" />
                    </shape>
                </item>
            </selector>
        </scale>
    </item>
</layer-list>

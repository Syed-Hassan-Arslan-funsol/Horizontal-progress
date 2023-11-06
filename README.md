Location Urls
http://ip-api.com/json
https://api.ipregistry.co?key=tryout


private fun getWeekendDayOfAnyMonth(){
        var desiredMonth = 11 // Change this to the desired month (0-based index, so 0 for January, 1 for February, and so on)
        val desiredYear = 2023 // Change this to the desired year
        val calendar: Calendar = Calendar.getInstance()
        desiredMonth = calendar.get(Calendar.MONTH)

        Log.i("weekends", "month: $desiredMonth")
        Log.i("weekends", "year: ${calendar.get(Calendar.YEAR)}")

        calendar.set(Calendar.YEAR, desiredYear)
        calendar.set(Calendar.MONTH, desiredMonth)
        calendar.set(Calendar.DAY_OF_MONTH, 1)
        val dateFormat = SimpleDateFormat("dd/MM/yyyy", Locale.getDefault())
        while (calendar.get(Calendar.MONTH) == desiredMonth) {
            val dayOfWeek: Int = calendar.get(Calendar.DAY_OF_WEEK)
            if (dayOfWeek == Calendar.SATURDAY || dayOfWeek == Calendar.SUNDAY) {
                val weekendDate = dateFormat.format(calendar.time)
                println("Weekend date: $weekendDate")

                Log.d("weekends", "onCreate: $weekendDate")
            }
            calendar.add(Calendar.DAY_OF_MONTH, 1)
        }
    }

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

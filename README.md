# Lesson 5: First Project
***Part of the Grow with Google Challenge Scholarship: Anroid Basics - Udacity***
I used **API 23: Android 6.0 (Marshmallow)**

* **Includes a horizontal layout**. I did this by creating a copy of *activity_main.xml*, pasting it into a new folder under */res/* called */layout-land/*, and then editing it to look good for landscape mode.

    --> MyProject/res/**layout**/activity_main.xml *(default/portrait)*
    
    --> MyProject/res/**layout-land**/activity_main.xml *(landscape)*
    
![Screenshots](./screenshot2.png "Landscape and Portrait Screenshots")

### layout/activity_main.xml:
```<?xml version="1.0" encoding="utf-8"?>
    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context="com.yummywakame.helloandroid.MainActivity"
        android:includeFontPadding="false"
        android:lineSpacingExtra="0dp">

        <ImageView
            android:id="@+id/background"
            android:contentDescription="@string/bg_diagonal"
            xmlns:android="http://schemas.android.com/apk/res/android"
            android:layout_width="fill_parent"
            android:layout_height="fill_parent"
            android:background="@drawable/background"
            android:orientation="vertical"
            android:scaleType="fitXY"
            android:visibility="visible"/>

        <RelativeLayout
            android:id="@+id/main"
            android:layout_margin="40dp"
            android:layout_width="fill_parent"
            android:layout_height="fill_parent"
            android:layout_alignParentStart="true"
            android:layout_alignParentEnd="true">

            <ImageView
                android:id="@+id/logo"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_alignParentTop="true"
                android:layout_centerHorizontal="true"
                android:layout_marginTop="0dp"
                android:contentDescription="@string/logo_desc"
                app:srcCompat="@drawable/logo_sm" />

            <TextView
                android:id="@+id/text_quote"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_below="@+id/logo"
                android:layout_centerHorizontal="true"
                android:layout_marginTop="19dp"
                android:text="@string/quote"
                android:textAlignment="center"
                android:textAppearance="?android:attr/textAppearanceLarge"
                android:textColor="#FFFFFF" />

            <TextView
                android:id="@+id/text_strap"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_alignParentBottom="true"
                android:layout_centerHorizontal="true"
                android:text="@string/strapline"
                android:textAppearance="?android:attr/textAppearanceMedium"
                android:textAlignment="center" />

            <LinearLayout
                android:id="@+id/text_block"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_above="@id/text_strap"
                android:layout_alignParentEnd="true"
                android:orientation="vertical"
                android:layout_marginBottom="60dp">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="@string/title"
                    android:textAlignment="textEnd"
                    android:textAppearance="?android:attr/textAppearanceLarge"
                    android:textStyle="bold" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="@string/addr1"
                    android:textAlignment="textEnd"
                    android:textAppearance="?android:attr/textAppearanceSmall" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="@string/addr2"
                    android:textAlignment="textEnd"
                    android:textAppearance="?android:attr/textAppearanceSmall" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="@string/phone"
                    android:textAlignment="textEnd"
                    android:textAppearance="?android:attr/textAppearanceSmall" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="@string/website"
                    android:textAlignment="textEnd"
                    android:textAppearance="?android:attr/textAppearanceSmall"
                    android:textColor="#02b3e4" />

            </LinearLayout>

        </RelativeLayout>

    </RelativeLayout>
```
### layout-land/activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context="com.yummywakame.helloandroid.MainActivity"
        android:includeFontPadding="false"
        android:lineSpacingExtra="0dp">

        <ImageView
            android:id="@+id/background"
            android:contentDescription="@string/bg_diagonal"
            xmlns:android="http://schemas.android.com/apk/res/android"
            android:layout_width="fill_parent"
            android:layout_height="fill_parent"
            android:background="@drawable/background"
            android:orientation="vertical"
            android:scaleType="fitXY"
            android:visibility="visible"/>

        <RelativeLayout
            android:id="@+id/main"
            android:layout_margin="40dp"
            android:layout_width="fill_parent"
            android:layout_height="fill_parent"
            android:layout_alignParentStart="true"
            android:layout_alignParentEnd="true">

            <ImageView
                android:id="@+id/logo"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_alignParentTop="true"
                android:layout_marginTop="0dp"
                android:contentDescription="@string/logo_desc"
                app:srcCompat="@drawable/logo_sm" />

            <TextView
                android:id="@+id/text_quote"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_toRightOf="@+id/logo"
                android:layout_alignParentRight="true"
                android:text="@string/quote"
                android:textAlignment="textEnd"
                android:textStyle="bold"
                android:textSize="32dp"
                android:textColor="#FFFFFF" />

            <TextView
                android:id="@+id/text_strap"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="@string/strapline"
                android:textAppearance="?android:attr/textAppearanceLarge"
                android:layout_toLeftOf="@id/text_block"
                android:layout_alignParentBottom="true"
                android:paddingRight="40dp"/>

            <LinearLayout
                android:id="@+id/text_block"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_above="@id/text_strap"
                android:layout_alignParentEnd="true"
                android:layout_alignParentBottom="true"
                android:orientation="vertical">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="@string/title"
                    android:textAlignment="textEnd"
                    android:textAppearance="?android:attr/textAppearanceLarge"
                    android:textStyle="bold" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="@string/addr1"
                    android:textAlignment="textEnd"
                    android:textAppearance="?android:attr/textAppearanceMedium" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="@string/addr2"
                    android:textAlignment="textEnd"
                    android:textAppearance="?android:attr/textAppearanceMedium" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="@string/phone"
                    android:textAlignment="textEnd"
                    android:textAppearance="?android:attr/textAppearanceMedium" />

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:text="@string/website"
                    android:textAlignment="textEnd"
                    android:textAppearance="?android:attr/textAppearanceMedium"
                    android:textColor="#02b3e4" />

            </LinearLayout>

        </RelativeLayout>

    </RelativeLayout>
```

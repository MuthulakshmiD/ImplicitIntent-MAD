# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1. **Start the project:** Create a new Android project in Android Studio.

2. **Design the UI:** In `activity_main.xml`, add an `EditText` (to accept the URL input) and a `Button` (to trigger the navigation).

3. **Initialize components:** In `MainActivity.java`, map the `EditText` and `Button` variables to their respective XML IDs using `findViewById()`.

4. **Set click listener:** Attach an `OnClickListener` to the button to listen for user click events.

5. **Get input:** Inside the `onClick` method, extract the text entered in the `EditText` and convert it to a string.

6. **Create implicit intent:** Instantiate an `Intent` with the action `Intent.ACTION_VIEW` and pass the parsed URL string using `Uri.parse()`.

7. **Start activity:** Call `startActivity(intent)` to trigger the OS to open the webpage in an available web browser.

8. **Stop:** Run and test the application.

## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: Muthulakshmi D
Registeration Number : 212223040122
*/
```
MainActivity.java
```
package com.example.implicitintent;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    Button btnOpenGoogle;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        btnOpenGoogle = findViewById(R.id.btnOpenGoogle);

        btnOpenGoogle.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {

                // Implicit Intent to open Google
                Intent intent = new Intent(Intent.ACTION_VIEW);
                intent.setData(Uri.parse("https://www.google.com"));

                startActivity(intent);
            }
        });
    }
}
```

activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center"
    android:orientation="vertical">

    <Button
        android:id="@+id/btnOpenGoogle"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Open Google" />

</LinearLayout>
```

## OUTPUT

<img width="1919" height="1017" alt="Screenshot 2026-05-10 214227" src="https://github.com/user-attachments/assets/e46c80a0-59d7-4e55-abf8-7a930624d3fc" />

<img width="1906" height="1025" alt="Screenshot 2026-05-10 214240" src="https://github.com/user-attachments/assets/cf04125d-0611-43e4-b76f-b38ea7d6eba5" />


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.



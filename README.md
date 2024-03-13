# Ex.No: 1 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.
## ALGORITHM:
STEP 1: Create the app's layout using XML, placing GUI components.
<BR>
STEP 2: Choose default or custom fonts for text elements.
<BR>
STEP 3: Set chosen fonts for TextViews, EditTexts, etc., in XML.
<BR>
STEP 4: Establish color scheme using hexadecimal values or resources.
<BR>
STEP 5: Set background, text color, etc., for UI components.
<BR>
STEP 6: Implement event handling for user interactions.
<BR>
STEP 7: Test across devices, optimize performance, release, and maintain.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio



## PROGRAM:
Program to print the text “GUIcomponent”.
<br>Developed by: Gokul
<br>Registeration Number : 212221220013
```java
# mainactivity
package com.example.gui_components;

import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Color;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    int ch=1;
    float font=20;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final TextView t = (TextView) findViewById(R.id.textView);
        Button b1 = (Button) findViewById(R.id.button);
        b1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                t.setTextSize(font);
                font = font + 5;
                if (font == 90)
                    font = 30;
            }
        });
        Button b2= (Button) findViewById(R.id.button2);
        b2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                switch (ch) {
                    case 1:
                        t.setTextColor(Color.RED);
                        break;
                    case 2:
                        t.setTextColor(Color.GREEN);
                        break;
                    case 3:
                        t.setTextColor(Color.BLUE);
                        break;
                    case 4:
                        t.setTextColor(Color.CYAN);
                        break;
                    case 5:
                        t.setTextColor(Color.YELLOW);
                        break;
                    case 6:
                        t.setTextColor(Color.MAGENTA);
                        break;
                }
                ch++;
                if (ch == 7)
                    ch = 1;
            }
        });
    }
}
```
```java
#activity.xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.192" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Change Font_Size"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button2"
        app:layout_constraintVertical_bias="0.121" />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="124dp"
        android:text="Change Button_Colour"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView" />

</androidx.constraintlayout.widget.ConstraintLayout>
```


## OUTPUT:
### initial condition:
![Screenshot 2024-03-13 135119](https://github.com/babavoss05/GUI-components/assets/103019882/c9204b3e-5399-4c49-8fb6-201bc043e673)




### font size change:
![Screenshot 2024-03-13 135132](https://github.com/babavoss05/GUI-components/assets/103019882/37c982b7-3ed5-4d69-bd0b-e6b3ae96f840)



### font color change:
![Screenshot 2024-03-13 135143](https://github.com/babavoss05/GUI-components/assets/103019882/bec067ab-5726-4151-b939-b80ae5fa5d60)





## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.



week1b
java
package com.example.myapplication; // Replace with your actual package name

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.content.Intent;
import android.net.Uri;
import android.view.View;
import android.widget.Button;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    Button button1, button2, button3;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Initialize Buttons
        button1 = findViewById(R.id.button1); // Phone Button
        button2 = findViewById(R.id.button2); // Website Button
        button3 = findViewById(R.id.button3); // SMS Button

        // Set Click Listeners
        // 1. Dial Number (Phone)
        button1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                // Intent to Dial a number (Action_Dial)
                Intent callIntent = new Intent(Intent.ACTION_DIAL, Uri.parse("tel:9866083201")); 
                startActivity(callIntent);
            }
        });

        // 2. Open Website (Website)
        button2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                // Intent to Open a website (Action_View)
                Intent webIntent = new Intent(Intent.ACTION_VIEW, Uri.parse("https://www.google.com"));
                startActivity(webIntent);
            }
        });

        // 3. Send SMS (SMS)
        button3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                // Intent to Send SMS (Action_Sendto or Action_View with sms: scheme)
                // This intent will open the messaging app with the number pre-filled.
                Intent smsIntent = new Intent(Intent.ACTION_VIEW);
                smsIntent.setData(Uri.parse("sms:9866083201")); 
                // You can also add message body: 
                // smsIntent.putExtra("sms_body", "Hello!"); 
                startActivity(smsIntent);
            }
        });
        
        // Optional: Toast message on startup
        Toast.makeText(getApplicationContext(), "Welcome to menu app", Toast.LENGTH_SHORT).show();
    }
}


xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#FF4444" 
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="menu option"
        android:textAlignment="center"
        android:textColor="#332623"
        android:textSize="30dp"
        android:textStyle="italic"
        app:layout_constraintBottom_toTopOf="@+id/button1"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.2"
        />

    <Button
        android:id="@+id/button1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="50dp"
        android:layout_marginStart="30dp"
        android:layout_marginEnd="30dp"
        android:text="Phone"
        android:textSize="20dp"
        android:textStyle="italic"
        android:background="#FFFF00"
        app:layout_constraintTop_toBottomOf="@+id/textView1"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        />

    <Button
        android:id="@+id/button2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="20dp"
        android:layout_marginStart="30dp"
        android:layout_marginEnd="30dp"
        android:text="Website"
        android:textSize="20dp"
        android:textStyle="italic"
        android:background="#FFFF00"
        app:layout_constraintTop_toBottomOf="@+id/button1"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        />

    <Button
        android:id="@+id/button3"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="20dp"
        android:layout_marginStart="30dp"
        android:layout_marginEnd="30dp"
        android:text="SMS"
        android:textSize="20dp"
        android:textStyle="italic"
        android:background="#FFFF00"
        app:layout_constraintTop_toBottomOf="@+id/button2"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        />

</androidx.constraintlayout.widget.ConstraintLayout>

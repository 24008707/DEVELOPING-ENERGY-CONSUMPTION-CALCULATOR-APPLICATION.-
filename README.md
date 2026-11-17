# DEVELOPING-ENERGY-CONSUMPTION-CALCULATOR-APPLICATION.-

## AIM:
To develop an android application to perform energy calculation.

## APPARATUS REQUIRED:
ØComputer
ØAndroid studio software


## THEORY:
The Energy Calculator App allows the user to calculate the energy consumption of electrical appliances based on power usage (in watts) and time (in hours). The app takes these two inputs, calculates the energy consumed in kilowatt-hours (kWh), and displays the result. This experiment involves basic arithmetic calculations and user input handling in Android. It uses EditText for input, Button for user interaction, and TextView to display the result. The app demonstrates how to handle user input for numerical values and perform unit conversions. It is a useful application for understanding how to develop apps that perform mathematical calculations based on user input.

## PROCEDURE:
1. Open Android Studio and then click on File -> New -> New project. 24. Then type the application name as “ex.no.3″ and click Next.
2. Then select the Minimum SDK as shown below and click next. 26. Then select the Empty Activity and click next.
3. Finally click Finish.
4. Click on app -> java -> com.example -> MainActivity.java
5. Now click on Text and type the program, so now the programming part of the main activity is completed.
6. Click on app -> res -> layout -> activity_main.xml.
7. Now click on Text and type the program, so now the designing part of Activity main is also completed.
8. Select the suitable available device to display the output. 33. Now run the application to see the output. 

## PROGRAM:

 MainActivity.kt
 
{
 package com.example.simplecalc   // keep the package name Android Studio generated

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val n1 = findViewById<EditText>(R.id.num1)
        val n2 = findViewById<EditText>(R.id.num2)
        val result = findViewById<TextView>(R.id.result)

        fun calculate(op: Char) {
            val a = n1.text.toString().toDoubleOrNull()
            val b = n2.text.toString().toDoubleOrNull()
            if (a == null || b == null) {
                result.text = "Enter both numbers"
                return
            }
            val answer = when (op) {
                '+' -> a + b
                '-' -> a - b
                '*' -> a * b
                else -> {
                    if (b == 0.0) { result.text = "Cannot divide by 0"; return }
                    a / b
                }
            }
            result.text = "Result: $answer"
        }

        findViewById<Button>(R.id.btnAdd).setOnClickListener { calculate('+') }
        findViewById<Button>(R.id.btnSub).setOnClickListener { calculate('-') }
        findViewById<Button>(R.id.btnMul).setOnClickListener { calculate('*') }
        findViewById<Button>(R.id.btnDiv).setOnClickListener { calculate('/') }
    }
 }

}
## OUTPUT:

<img width="2076" height="2152" alt="Screenshot_20261028_124700" src="https://github.com/user-attachments/assets/95fcc120-58c5-4d35-871e-02b3b1f073f3" />



## RESULT:
Thus, the energy consumption calculator app is developed and the output is verified. 


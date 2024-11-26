package com.example.assignment3

import android.content.Intent
import android.os.Bundle
import android.util.Log
import android.widget.Button
import android.widget.TextView
import androidx.activity.enableEdgeToEdge
import androidx.appcompat.app.AppCompatActivity
import androidx.core.view.ViewCompat
import androidx.core.view.WindowInsetsCompat

class SecondActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()
        setContentView(R.layout.activity_second)

        // Adjust system bars padding for the root layout
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main)) { v, insets ->
            val systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars())
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom)
            insets
        }

        // Initialize views
        val tvReceivedData = findViewById<TextView>(R.id.tvReceivedData)
        val btnToThirdActivity = findViewById<Button>(R.id.btnToThirdActivity)

        // Retrieve data from Intent
        val textOne = intent.getStringExtra("text_one") ?: "Default Text One"
        val textTwo = intent.getStringExtra("text_two") ?: "Default Text Two"
        val textThree = intent.getStringExtra("text_three") ?: "Default Text Three"
        val textFour = intent.getStringExtra("text_four") ?: "Default Text Four"
        val textFive = intent.getStringExtra("text_five") ?: "Default Text Five"
        val booleanValue = intent.getBooleanExtra("boolean_key", false)
        val integerValue = intent.getIntExtra("integer_key", 0)
        val floatValue = intent.getFloatExtra("float_key", 0.0f)

        // Combine all data into a string
        val finalData = """
            $textOne
            $textTwo
            $textThree
            $textFour
            $textFive
            Boolean: $booleanValue
            Integer: $integerValue
            Float: $floatValue
        """.trimIndent()

        // Display data in TextView and log it
        tvReceivedData.text = finalData
        Log.d("SecondActivity", finalData)

        // Navigate to ThirdActivity on button click
        btnToThirdActivity.setOnClickListener {
            val intent = Intent(this, ThirdActivity::class.java)
            intent.putExtra("final_data", finalData)
            startActivity(intent)
        }
    }
}

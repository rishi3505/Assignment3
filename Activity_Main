package com.example.assignment3

import android.content.Intent
import android.os.Bundle
import android.widget.Button
import androidx.activity.enableEdgeToEdge
import androidx.appcompat.app.AppCompatActivity
import androidx.core.view.ViewCompat
import androidx.core.view.WindowInsetsCompat

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()
        setContentView(R.layout.activity_main)

        // Adjust system bars padding for the root layout
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main)) { v, insets ->
            val systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars())
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom)
            insets
        }


        val button = findViewById<Button>(R.id.btnToSecondActivity)
        button.setOnClickListener {

            val intent = Intent(this, SecondActivity::class.java)

            // Add data to the intent
            intent.putExtra("text_one", getString(R.string.text_one))
            intent.putExtra("text_two", getString(R.string.text_two))
            intent.putExtra("text_three", getString(R.string.text_three))
            intent.putExtra("text_four", getString(R.string.text_four))
            intent.putExtra("text_five", getString(R.string.text_five))
            intent.putExtra("boolean_key", true)
            intent.putExtra("integer_key", 42)
            intent.putExtra("float_key", 3.14f)


            startActivity(intent)
        }
    }
}

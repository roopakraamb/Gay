

Set up Android Studio: Install Android Studio if you haven't already and create a new project.

Design the Layout: Design the user interface for your app. You'll need a button to roll the dice and an area to display the result.

Add Button Click Listener: Implement a click listener for the roll button. When clicked, this will generate a random number (representing the dice roll) and display it.

Generate Random Number: Use the Random class in Java to generate a random number between 1 and 6 (inclusive), representing the result of rolling a dice.

Display Result: Update the UI to display the result of the dice roll.

Test: Test your app on an emulator or a physical device to make sure it works as expected.

Here's a basic code snippet to get you started:

java
Copy code
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

import java.util.Random;

public class MainActivity extends AppCompatActivity {
    private Button rollButton;
    private TextView resultText;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        rollButton = findViewById(R.id.roll_button);
        resultText = findViewById(R.id.result_text);

        rollButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                rollDice();
            }
        });
    }

    private void rollDice() {
        Random random = new Random();
        int result = random.nextInt(6) + 1; // Generates a random number between 1 and 6
        resultText.setText("Result: " + result);
    }
}


Remember to create the corresponding layout XML file for your activity and define the necessary UI components (e.g., button and text view)

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

import java.util.Random;

public class MainActivity extends AppCompatActivity {
    private Button rollButton;
    private TextView resultText;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        rollButton = findViewById(R.id.roll_button);
        resultText = findViewById(R.id.result_text);

        rollButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                rollDice();
            }
        });
    }

    private void rollDice() {
        Random random = new Random();
        int result = random.nextInt(6) + 1; // Generates a random number between 1 and 6
        resultText.setText("Result: " + result);
    }
}

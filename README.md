## Implicit Intents in Android 

This project demonstrates the use of Implicit Intents in an Android application. 

**What are Intents?**

it is a messaging object in android that is used to request any action from another app component. The messaging object describes an action to be performed, allowing one application component to communicate with another by requesting for a specific operation.

* Open web pages
* Make phone calls
* Send emails
* Launch other apps

**Types of Intents:**

There are two main types of Intents:

* **Explicit Intent:** Explicitly specifies the target component (Activity, Service, etc.) to handle the action.
* **Implicit Intent:** Describes the action to be performed, and the Android system finds the best app capable of handling it.

**This program uses an Implicit Intent:**

The program allows users to enter a webpage URL in an EditText field and click a button. When the button is clicked, an implicit intent is created with the action `ACTION_VIEW` and the data (URL) to be displayed. The Android system then selects the most suitable app to handle web browsing, such as a web browser installed on the device, and opens the webpage in that app.

**Code Breakdown:**

The included code demonstrates the core functionality:

* **Imports:** Necessary libraries for intent creation (`android.content.Intent`), working with URLs (`android.net.Uri`), handling user interaction (`android.widget.Button` and `android.widget.EditText`), and managing the activity lifecycle (`androidx.appcompat.app.AppCompatActivity`).
* **MainActivity Class:** This extends `AppCompatActivity`, which is the base class for most activities in Android.
* **onCreate Method:** This method is called when the activity is first created. It sets the content view of the activity and initializes the EditText field.
* **search Method:** This method is called when the button is clicked. 
    * It retrieves the URL entered in the EditText field.
    * It creates an implicit Intent with the action `Intent.ACTION_VIEW` and the data as the parsed URL using `Uri.parse(url)`.
    * It starts the activity associated with the intent using `startActivity(urlIntent)`.

**Running the program:**

1. Build and run the app on your Android device.
2. Enter a website URL in the text field.
3. Click the button.

The entered URL should open in your default web browser.

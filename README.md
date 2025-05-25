This is our application AV messenger 
where our movite is to took stangers closer and sharing their ideas and innovations !!

App Structure

1. Splash Screen

Displays app logo and transitions to login screen.

2. Login Screen

Form with email and password fields + login button.

3. Signup Screen

Form for username, email, password, and confirm password.

4. Main Screen

Shows a list of contacts with avatar, name, and status.

5. Logout Confirmation

A dialog asking if the user really wants to log out.


---

Technologies

Flutter + Dart

Basic navigation using Navigator

State management using setState (simple for now)



---

Step 1: Flutter Starter Code (main.dart)

import 'package:flutter/material.dart';

void main() {
  runApp(AVMessengerApp());
}

class AVMessengerApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'A.VMESSENGER',
      debugShowCheckedModeBanner: false,
      home: SplashScreen(),
    );
  }
}

class SplashScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    Future.delayed(Duration(seconds: 2), () {
      Navigator.pushReplacement(
        context,
        MaterialPageRoute(builder: (context) => LoginScreen()),
      );
    });

    return Scaffold(
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text("A.V", style: TextStyle(fontSize: 48, fontWeight: FontWeight.bold)),
            Text("A.VMESSENGER", style: TextStyle(fontSize: 24)),
            SizedBox(height: 20),
            Text("From TechCoder A.V")
          ],
        ),
      ),
    );
  }
}

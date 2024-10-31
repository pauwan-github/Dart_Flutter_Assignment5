import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Welcome App',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: HomePage(),
    );
  }
}

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Welcome App'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          crossAxisAlignment: CrossAxisAlignment.center,
          children: [
          
            Text( 
              'Welcome to the Flutter App!',
              style: TextStyle(
                fontSize: 24,
                fontWeight: FontWeight.bold,
              ),
            ),
            SizedBox(height: 20), // Spacing between text and button
            ElevatedButton(
              onPressed: () {
                print('ElevatedButton clicked!');
              },
              child: Text('Click Me'),
            ),
            SizedBox(height: 20), // Spacing between button and image
            Image.network(
              'https://flutter.dev/assets/homepage/carousel/slide_1-layer_0-2b8f7e49c377dd946ed6e6b7640d4e1b9c4dce793fa53e77a62d69e458b501e2.png',
              height: 150,
            ),
          ],
        ),
      ),
    );
  }
}

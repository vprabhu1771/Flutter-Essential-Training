```dart
import 'package:flutter/material.dart';

class HomeScreen extends StatelessWidget {

  const HomeScreen({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Popup Menu Button Example'),
        actions: [
          PopupMenuButton<String>(
            onSelected: (value) {
              // Handle the selected value here
              print('Selected: $value');
            },
            itemBuilder: (BuildContext context) {
              return [
                PopupMenuItem(
                  value: 'Option 1',
                  child: Text('Option 1'),
                ),
                PopupMenuItem(
                  value: 'Option 2',
                  child: Text('Option 2'),
                ),
                PopupMenuItem(
                  value: 'Option 3',
                  child: Text('Option 3'),
                ),
              ];
            },
          ),
        ],
      ),
      body: Center(
        child: Text('Press the menu button in the AppBar'),
      )
    );
  }
}
```

```dart
import 'package:flutter/material.dart';

import 'package:untitled1/screens/HomeScreen.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: HomeScreen(),
    );
  }
}
```
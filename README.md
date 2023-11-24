# List_view

import 'package:flutter/material.dart';

void main() {
  runApp(HomePage());
}

class HomePage extends StatelessWidget {
   List<String> names = [ 'Richard', 'Mariefe','Richie Mae','Rheymar',
                             'Richie Mae',
                             'Rhickxylemar'];

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          backgroundColor: Colors.blue,
          leading: Icon(Icons.villa),
          title: Text('Dynamic List_View'),
          actions: [
            IconButton(
              icon: Icon(Icons.how_to_reg),
              onPressed: () {
                
              },
            ),
          ],
        ),
        body: ListView.builder(
          itemCount: names.length,
          itemBuilder: (context, index) {
            return ListTile(
              leading: Icon(Icons.face), 
              title: Text(names[index]),
              subtitle: Text('Letter count: ${names[index].length}'),
            );
          },
        ),
      ),
    );
  }
}

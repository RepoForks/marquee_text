# marquee_text

一个支持文本和富文本的文本跑马灯控件，接口方式和flutter中的text和richtext保持一致

## Example

```
import 'package:flutter/material.dart';
import 'package:marquee_text/marquee_text.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        // This is the theme of your application.
        //
        // Try running your application with "flutter run". You'll see the
        // application has a blue toolbar. Then, without quitting the app, try
        // changing the primarySwatch below to Colors.green and then invoke
        // "hot reload" (press "r" in the console where you ran "flutter run",
        // or simply save your changes to "hot reload" in a Flutter IDE).
        // Notice that the counter didn't reset back to zero; the application
        // is not restarted.
        primarySwatch: Colors.blue,
      ),
      home: HomePage(),
    );
  }
}

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return new Scaffold(
        appBar: new AppBar(
          title: new Text("跑马灯"),
        ),
        body: new Center(
          child: new Column(
            children: <Widget>[
              MarqueeText("跑马灯控件，正常文本"),
              MarqueeText.rich(TextSpan(
                  text: "跑马灯控件，设置字体和颜色",
                  style: TextStyle(fontSize: 11.0, color: Colors.red)))
            ],
          ),
        ));
  }
}
```




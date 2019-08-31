# progress_dialog

A light weight package to show progress dialog. As it is a stateful widget, you can change the text shown on the dialog dynamically.

[![Sponsor!](https://img.shields.io/badge/Say%20Thanks-!-1EAEDB.svg)](https://github.com/fayaz07/progress_dialog) &nbsp; [![LinkedIn](https://img.shields.io/badge/LinkedIn-in-0e76a8)](https://www.linkedin.com/in/fayaz07) &nbsp; [![Follow](https://img.shields.io/github/followers/fayaz07?style=social)](https://github.com/fayaz07) &nbsp; [![Fork](https://img.shields.io/github/forks/fayaz07/progress_dialog?style=social)](https://github.com/fayaz07/progress_dialog/fork) &nbsp; [![Star](https://img.shields.io/github/stars/fayaz07/progress_dialog?style=social)](https://github.com/fayaz07/progress_dialog/star) &nbsp; [![Watches](https://img.shields.io/github/watchers/fayaz07/progress_dialog?style=social)](https://github.com/fayaz07/progress_dialog/) 

[![Get the library](https://img.shields.io/badge/Get%20library-pub-blue)](https://pub.dev/packages/progress_dialog) &nbsp; [![Example](https://img.shields.io/badge/Example-Ex-success)](https://pub.dev/packages/progress_dialog#-example-tab-)



## Supported Dart Versions
**Dart SDK version >= 2.1.0**

## Demo

<img src="https://raw.githubusercontent.com/fayaz07/progress_dialog/master/demo.gif" alt="Demo"/> <img src="https://raw.githubusercontent.com/fayaz07/progress_dialog/master/demo_1.gif" alt="Demo" />


## Installation
[![Pub](https://img.shields.io/badge/pub-1.2.0-blue)](https://pub.dev/packages/progress_dialog)

Add the Package
```yaml
dependencies:
  progress_dialog: ^1.2.0
```

## How to use

```dart
import 'package:progress_dialog/progress_dialog.dart';
```
Create an instance of ProgressDialog
```dart
ProgressDialog pr;
```

Initialise the **pr** object inside the **build()** method passing context to it

<ol>
<li> Initialize the ProgressDialog object
  
```dart
pr = new ProgressDialog(context);
```
</li>


<li> By default it is a normal dialog to show some message, if you would like to use it to show percentage of progress done, specify the optional `type` parameter and specify if you want your dialog to dismiss when back button is pressed `isDismissible` parameter (Optional)
  
```dart
    
//For normal dialog
pr = new ProgressDialog(context,type: ProgressDialogType.Normal, isDismissible: true/false);
    
//For showing progress percentage
pr = new ProgressDialog(context,type: ProgressDialogType.Download, isDismissible: true/false);
```
</li>

  
<li>Style the progress dialog (Optional)

```dart
pr.style(
  message: 'Downloading file...',
  borderRadius: 10.0,
  backgroundColor: Colors.white,
  progressWidget: CircularProgressIndicator(),
  elevation: 10.0,
  insetAnimCurve: Curves.easeInOut,
  progress: 0.0,
  maxProgress: 100.0,
  progressTextStyle: TextStyle(
     color: Colors.black, fontSize: 13.0, fontWeight: FontWeight.w400),
  messageTextStyle: TextStyle(
     color: Colors.black, fontSize: 19.0, fontWeight: FontWeight.w600)
  );
```

</li>

<li>Showing the progress dialog

```dart
pr.show();
```

</li>

<li>
Dynamically update the content shown out there

```dart
pr.update(
  progress: 50.0,
  message: "Please wait...",
  progressWidget: Container(
    padding: EdgeInsets.all(8.0), child: CircularProgressIndicator()),
  maxProgress: 100.0,
  progressTextStyle: TextStyle(
    color: Colors.black, fontSize: 13.0, fontWeight: FontWeight.w400),
  messageTextStyle: TextStyle(
    color: Colors.black, fontSize: 19.0, fontWeight: FontWeight.w600),
  );
```

</li>

<li>
Dismissing the progress dialog

```dart
pr.hide();
```

</li>  
</ol>


### Check if progress dialog is showing

```dart
bool isProgressDialogShowing = pr.isShowing();
print(isProgressDialogShowing);
```

### Default configuration/styles

If you don't like to configure/style the dialog and continue with the default style, it's okay but just have a look at our default configuration.

| Attribute     | Value   |
| ------------- | -----:|
| col 3 is      | $1600 |
| col 2 is      |   $12 |
| zebra stripes |    $1 |



### Want to contribute? 
Pull requests and issues are always welcome!

#### How to contribute?

* Fork the [repository](https://github.com/fayaz07/progress_dialog)
* Clone it to your local machine
* Open the project in your favourite editor
* Open cmd/terminal and run **flutter clean** and then **flutter packages get**
* Make the changes
* Create a **Pull Request**

#### View the issues [here](https://github.com/fayaz07/progress_dialog/issues)

---
Loading indicator -> https://loading.io/

# ironsource_flutter_ads

A Flutter plugin that uses native platform views (IOS & Android) to show IronSource banner and interstitial ads!


xxx 🚀</br></br>

<img width="300" alt="portfolio_view" src="https://live.staticflickr.com/65535/48574710632_fd7f318277_b.jpg">&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;<img width="300" alt="portfolio_view" src="https://media.giphy.com/media/jqwcyovkVTiiDl9ZKh/giphy.gif">


# Getting Started

<b>1. Initialize the plugin: </b>

```dart
 IronsourceFlutterAds.initialize(Constants.appID);
```

<b>2. Show Banner Ad:</b>

```dart
  IronSourceBanner(
      adSize: bannerSize,
      listener: (
        IronsourceAdEvent event, Map<String, dynamic> args) {
        handleEvent(event, args, 'Banner');
       },
     ),
```

<b>3. Show Interstitial Ads</b>

3.1 Implementing listener and load Interstitial Ad:

```dart
 interstitialAd = IronsourceInterstitial(
      listener: (IronsourceAdEvent event, Map<String, dynamic> args) {
        handleEvent(event, args, 'Interstitial');
      },
    );


    interstitialAd.load();
```

3.2 Show Interstitial Ad:

```dart
  if (await interstitialAd.isLoaded){
      interstitialAd.show();
  }                        
```




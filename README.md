CHTReachability
===============

[![Version](https://cocoapod-badges.herokuapp.com/v/CHTReachability/badge.png)](http://cocoadocs.org/docsets/CHTReachability)
[![Platform](https://cocoapod-badges.herokuapp.com/p/CHTReachability/badge.png)](http://cocoadocs.org/docsets/CHTReachability)

Your device may connect to a wireless AP via Wi-Fi but the AP's cable is unplugged, or it may connect to a base station but your service provider stop working for some reasons. What's the easiest way to know current network status? **CHTReachability** tries to detect _REAL_ network reachability for you.

Internally, it uses Apple's [Reachability](https://developer.apple.com/library/ios/samplecode/Reachability/Introduction/Intro.html) and [SimplePing](https://developer.apple.com/library/prerelease/content/samplecode/SimplePing/Introduction/Intro.html) sample codes to do the real works.

Features
--------
* Easy to use.
* Highly customizable.

Prerequisite
------------
* ARC
* iOS 8+

How to install
--------------
* CocoaPods
  - Add `pod 'CHTReachability'` to your Podfile.

* Manual
  - Copy `CHTReachability.h/m` to your project.
  - Copy `Vender` folder to your project.
  - Add `SystemConfiguration.framework`.

How to Use
----------
Check the demo codes and `CHTReachability.h` header file for more information.

```objc
- (void)viewDidLoad {
  [super viewDidLoad];
  self.reach = [[CHTReachability alloc] initWithHostName:CHTReachabilityDefaultPingHostName delegate:self];
}

#pragma mark - <CHTReachabilityDelegate>
- (void)reachability:(CHTReachability *)reachability didChangeToStatus:(CHTReachabilityStatus)status {
  NSLog(@"Status = %@", @(status));
}
```

License
-------
CHTReachability is available under the MIT license. See the LICENSE file for more info.

Changelog
---------
Refer to the [Releases page](https://github.com/chiahsien/CHTReachability/releases).

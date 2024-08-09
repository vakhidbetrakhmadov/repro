Run:
```
bazelisk build MyApp
mv bazel-bin/MyApp.ipa bazel-bin/MyApp.zip 
unzip -qq bazel-bin/MyApp.zip
find Payload/MyApp.app -name '*.abi.json'
```

Observe:
```
...
Payload/MyApp.app/Frameworks/PhoneNumberKit.framework/Modules/PhoneNumberKit.swiftmodule/arm64-apple-ios-simulator.abi.json
Payload/MyApp.app/Frameworks/PhoneNumberKit.framework/Modules/PhoneNumberKit.swiftmodule/x86_64-apple-ios-simulator.abi.json
```

---
title: ASDF Application logging and tracing testgreen20
description: Logging and tracing using the SAP BTP SDK for iOS.
auto_validation: true
primary_tag: software-product>businessobjects-universal-bridge
tags: [  tutorial>beginner, products>sap-hana, products>sap-hana-studio, topic>big-data, software-product>sap-process-control ]
---
## Prerequisites  

- **Proficiency:** Beginner
- **Development environment:** Apple iMac, MacBook or MacBook Pro running Xcode 9 or higher
- **SAP BTP SDK for iOS:** Version 2.0
- **Tutorials:** [Push Notifications](fiori-ios-hcpms-push-notifications)

## Next Steps

- [Logging and tracing in SAP Mobile Services for development and operations](fiori-ios-hcpms-logging)

## Details

### You will learn  

In this tutorial, you will learn to use the logging functionality that is part of the SAP BTP SDK for iOS. You will also learn how to set logging settings in SAP Mobile Services for development and operations which will be reflected in your application.

### Time to Complete

**15 Min**.

---

The SAP BTP SDK for iOS provides you with sophisticated functionality which allows you to implement logging and tracing in your application. In addition, you can configure specific logging settings in SAP Mobile Services for development and operations, which can be mirrored in your application using the `SAPcpmsSettings` class.

The actual logging is provided by the `Logger` class, which is part of the `SAPCommon` SDK module.

[ACCORDION-BEGIN [Step 1: ](Referencing the Logger class)]

To make a reference to the `Logger` class in the Swift class files you want to provide with logging capabilities, you call the `Logger`'s `shared` method:

```swift
// Declaration of method 'shared' in class 'Logger'
public class func shared(withName name: String) -> Logger
```

You provide function `shared` a String with the name of your class, and it will return the `Logger` object for that class. So, in your class file `MyViewController.swift`, it would thus look like the following:

```swift
import SAPCommon

class MyViewController: UIViewController {

    private let logger = Logger.shared(withName: "MyViewController")

    // etc

}
```

[DONE]

[ACCORDION-END]

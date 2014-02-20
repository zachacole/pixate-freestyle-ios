# Pixate Freestyle

Pixate Freestyle is a native iOS (and [Android](pixate.github.io/pixate-freestyle-android)) library that styles native controls with CSS. With Freestyle, you can replace many complicated lines of Objective-C with a few lines of CSS. This simplifies and centralizes your styling code, and [offers other benefits](http://www.pixate.com/) as well.

## Getting Started

### Installation

There are two ways to install the Pixate Freestyle framework.

The easiest is to [download the installer](http://www.pixate.com/downloads/freestyle/PixateFreestyle-2.1.pkg), and drag **PixateFreestyle.framework** into your Xcode project. Once installed, add the following import to the top of your `main.m`:

```
#import <PixateFreestyle/PixateFreestyle.h>
```

In the body of your main method, add the following line before the return:

```
[PixateFreestyle initializePixateFreestyle];
```

Your main method should look something like this:

```
int main(int argc, char *argv[])
{
    @autoreleasepool {
        [PixateFreestyle initializePixateFreestyle];
        return UIApplicationMain(argc, argv, nil, NSStringFromClass([AppDelegate class]));
    }
}
```

If you use [CocoaPods](http://cocoapods.org), install the Freestyle cocoapod by adding **PixateFreestyle** to your Podfile:

```
pod 'PixateFreestyle'
```

### Migrating from Pixate Framework

If you are migrating from the Pixate Framework, you’ll only need to make a few changes, namely updating your imports to use ‘PixateFreestyle’ and updating your initialization method in your main.m.

In terms of your ‘#import” lines, just update them to read as follows:

```
#import <PixateFreestyle/PixateFreestyle.h>
```

And like the Installation step above, just change your main.m to look like the following, you no longer need to use a license key or user name.

```
#import <PixateFreestyle/PixateFreestyle.h>

int main(int argc, char *argv[])
{
    @autoreleasepool {
        [PixateFreestyle initializePixateFreestyle];
        return UIApplicationMain(argc, argv, nil, NSStringFromClass([AppDelegate class]));
    }
}
```

### Styling Apps with CSS

Pixate Freestyle allows you to add IDs, Class'es, and inline styles to your native components, and style them with CSS. Learn more about this [here](style-reference/index.html#app_structure).

For now, let’s make a simple app that styles a single button. Follow along with the video below, and add the following CSS code to a new file, `default.css`, in your Xcode project.

    ```
    view {
      background-color: #ffffff
    }

    .btn-green {
      color            : #446620;
      background-color : linear-gradient(#87c44a, #b4da77);
      border-width     : 1px;
      border-color     : #84a254;
      border-style     : solid;
      border-radius    : 10px;
      font-size        : 13px;
    }
    ```

### Moving Faster with Themes

You can build the style of your app piece-by-piece using the method above. For even faster development, use a pre-built [Freestyle theme](themes).

## Docs

## Compiling Freestyle Source

## Contributing

## Support

## License

Except as otherwise noted, Pixate Freestyle for iOS is licensed under the Apache License, Version 2.0 (http://www.apache.org/licenses/LICENSE-2.0.html).


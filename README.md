# Random Color Swift

Inspired by David Merfield's [randomColor.js](https://github.com/davidmerfield/randomColor). It is a ported version to Swift. You can use the library to generate attractive random colors on iOS or OSX.

See the [demo and site](http://llllll.li/randomColor/) to know why does this exist.

[![Demo](http://llllll.li/randomColor/repo_demo.gif)](http://llllll.li/randomColor)

## Install

I wish we could use CocoaPods or something else for package management for Swift. Currently, you can clone this repo and throw the source files under `RandomColor` folder to use it. I suggest to add them to a standalone Cocoa/CocoaTouch Framework target, to avoid potential risk of name conflict.

## Example

```swift
// Returns a UIColor or NSColor object for an attractive color
let color = randomColor()

// Returns an array of ten green colors
let greenColors = randomColorsCount(10, hue: .Green)

// Returns a color for light blue
let lightBlurColor = randomColor(hue: .Blue, luminosity: .Light)

// Returns a color for a 'truly random' color
let randomColor = randomColor(hue: .Random, luminosity: .Random)

// Returns an array of ten dark pink colors
let darkPinkColors = randomColorsCount(10, hue: .Pink, luminosity: .Dark)

// Returns an array of twenty colors at hue of 120
let colors = randomColorsCount(20, hue: .Value(120), luminosity: .Random)

```

There is also a demo project in this repo.

## Options

You can pass an options object to influence the type of color it produces. The options object accepts the following properties:

**Hue** – Controls the hue of the generated color. Possible hue values for colors are `.Monochrome`, `.Red`, `.Orange`, `.Yellow`, `.Green`, `.Blue`, `.Purple`, `.Pink`, `.Random` or `.Value(Int)`. If you use `.Value(Int)`, you should pass an `Int` between 0 and 360.

**Luminosity** – Controls the luminosity of the generated color. You can pass `.Bright`, `.Light`, `.Dark` or `.Random`.

**Count** – An `Int` which specifies the number of colors to generate.

## Acknowledgements

Thanks for David Merfield bringing us randomColor.js, which is a great utility.

The demo project is using Chirag Mehta's [Name the Color](http://chir.ag/projects/name-that-color) JavaScript library to extract name of color.

## License

This project is licensed under the terms of the MIT license.

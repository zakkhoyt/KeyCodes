### Keycode.swift - A list of keyCodes for NSEvents on OSX

Cocoa does not provide a list of key code constants. 

This file constants wrappers around Carbon's <HIToolbox/Events.h> header file. This just provides swifty syntax sugar. Think of it as "NSKeyCode".

Example Usage:

````
class MyView: NSView {
    override func keyDown(with event: NSEvent) {
        if event.keyCode == KeyCode.a {
            if event.modifierFlags.contains(.shift) {
                print("You pressed 'A'")
            } else {
                print("You pressed 'a'")
            }
        }
    }
}
````


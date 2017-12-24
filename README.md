### Keycodes

These key code constants are wrappers around Carbon's <HIToolbox/Events.h> header file. This just provides swifty syntax sugar. Think of it as "NSKeyCodes".

Example Usage:

````
class MyView: NSView {
    override func keyDown(with event: NSEvent) {
        if event.keyCode == KeyCodes.keyA {
            if event.modifierFlags.contains(.shift) {
                print("You pressed 'A'")
            } else {
                print("You pressed 'a'")
            }
        }
    }
}
````


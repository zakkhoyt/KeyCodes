### Keycode.swift - A list of key codes for NSEvent.keyCode. Think of this as the phantom "NSKeyCodes"

This file provides wrappers around key codes from Carbon's <HIToolbox/Events.h>. This stuct provides swifty syntax sugar and frees the developer from sifting through Carbon stuff. Think of it as "NSKeyCode".

Snippet:

````
struct KeyCode {
    static let a = UInt16(kVK_ANSI_A)
    static let b = UInt16(kVK_ANSI_B)
    ...
    static let apostrophe = UInt16(kVK_ANSI_Quote)
    static let backApostrophe = UInt16(kVK_ANSI_Grave)
    static let backslash = UInt16(kVK_ANSI_Backslash)
    static let capsLock = UInt16(kVK_CapsLock)
    ...
    static let keypad8 = UInt16(kVK_ANSI_Keypad8)
    static let keypad9 = UInt16(kVK_ANSI_Keypad9)
    static let keypadClear = UInt16(kVK_ANSI_KeypadClear)
    static let keypadDivide = UInt16(kVK_ANSI_KeypadDivide)
    ...
    static let apostrophe = UInt16(kVK_ANSI_Quote)
    static let backApostrophe = UInt16(kVK_ANSI_Grave)
    static let backslash = UInt16(kVK_ANSI_Backslash)
    static let capsLock = UInt16(kVK_CapsLock)
    ...
    static let command = UInt16(kVK_Command)
    static let rightCommand = UInt16(kVK_RightCommand)
    static let control = UInt16(kVK_Control)
    static let rightControl = UInt16(kVK_RightControl)
    ...
    static let rightArrow = UInt16(kVK_RightArrow)
    static let upArrow = UInt16(kVK_UpArrow)
}

````

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


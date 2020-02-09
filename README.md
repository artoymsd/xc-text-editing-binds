# xc-text-editing-binds
#### Bind keys to duplicate and delete lines in Xcode

1. Give permissions to edit the following files
```
sudo chmod 666 /Applications/Xcode.app/Contents/Frameworks/IDEKit.framework/Versions/A/Resources//IDETextKeyBindingSet.plist
sudo chmod 777 /Applications/Xcode.app/Contents/Frameworks/IDEKit.framework/Versions/A/Resources/
```

2. Open below directory in Finder with <kbd>Cmnd</kbd> + <kbd>Shift</kbd> + <kbd>G</kbd>

3. Open `IDETextKeyBindingSet.plist` with a text editor.

4. Add this in:

```xml
<key>Custom</key>
<dict>
    <key>Duplicate Lines</key>
    <string>selectParagraph:, delete:, yankAndSelect:, moveToBeginningOfText:, yankAndSelect:</string>
    <key>Delete Line</key>
    <string>selectLine:, deleteBackward:</string>
</dict>

```

5. Open Xcode and go to `Xcode preferences` -> `Key Bindings` -> `Text tab` -> Scroll till you see `Duplication`

6. Click on `Duplicate Lines`, add a shortcut for it, eg. `Cmd + D` (remove any other bindings for this key)
   Click on `Delete Line`, add a shortcut for it, eg. `Cmd + E` (remove any other bindings for this key)

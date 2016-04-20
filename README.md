Changing the cursor in Xcode
======

Do you also use a dark theme in xcode, but you can't really see the cursor?
Well here's the perfect solution.

![cursor](https://github.com/westerlund/xcode-cursor/blob/master/cursor.png)

Xcode 7.3
=========

Apple changed the format of the cursor, now being an Asset.car.
Copy the provided `Asset.car` to the following directory:
```
/Applications/Xcode.app/Contents/SharedFrameworks/DVTKit.framework/Versions/A/Resources/
```

Xcode 7.2 and earlier
====================

Open terminal on your mac an type the following:

```Bash
cd /Applications/Xcode.app/Contents/SharedFrameworks/DVTKit.framework/Versions/A/Resources # 1
cp DVTIbeamCursor.tiff{,.old} # 2
convert DVTIbeamCursor.tiff -negate DVTIbeamCursor.tiff # 3
```

* 1 open the folder containing the cursor
* 2 create a .old copy of the cursor, for backup
* 3 invert the cursor and replace it

### bash: convert: command not found
If you don't have convert on your machine, you can just download the converted cursor from my repo.


I'm on [@wesslansimon](https://twitter.com/wesslansimon) if you have questions or just intrested in having a cup of coffee.

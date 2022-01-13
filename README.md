This is a minimal project to demonstrate [Android Issue 194427611 - GestureNavContract Icons can get stuck on screen](https://issuetracker.google.com/issues/194427611)

Steps to reproduce

1. Use Android 11, 12 or 12L with Gesture Navigation
2. Install a 3rd party launcher that supports GestureNavContract, such as [Nova Launcher](https://play.google.com/store/apps/details?id=com.teslacoilsw.launcher) or Niagara Launcher and set as default
3. Install and place StuckIconGestureNavContract on the desktop
4. Open StuckIconGestureNavContract then swipe to return to the desktop
5. After the animation, attempt to scroll between desktop pages or open the app drawer

Expected results:
StuckIconGestureNavContract's icon has finished animating and therefor won't float on top of other content

Actual results:
StuckIconGestureNavContract's icon floats above all other content


This is a bug in SystemUI/Launcher3's host GestureNavContract. Third party launchers cannot fix this issue, it needs to be fixed by the system software (SystemUI or the system launcher which handles gesture navigation)

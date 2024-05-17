
---
# ![](share/addon_template/icon.png?raw=true) Share Plugin
Share Plugin allows sharing of text and images on Android platform.

_For iOS version, visit https://github.com/cengiz-pz/godot-ios-share-plugin ._

## ![](share/addon_template/icon.png?raw=true) Prerequisites
Follow instructions on the following page to create a custom Android gradle build
- [Create custom Android gradle build](https://docs.godotengine.org/en/stable/tutorials/export/android_gradle_build.html)

## ![](share/addon_template/icon.png?raw=true) Installation
There are 2 ways to install the `Share` plugin into your project:
- Through the Godot Editor's AssetLib
- Manually by downloading archives from Github

### ![](share/addon_template/icon.png?raw=true) Installing via AssetLib
Steps:
- search for and select the `Share` plugin in Godot Editor
- click `Download` button
- on the installation dialog...
	- keep `Change Install Folder` setting pointing to your project's root directory
	- keep `Ignore asset root` checkbox checked
	- click `Install` button
- enable the plugin via the `Plugins` tab of `Project->Project Settings...` menu, in the Godot Editor

### ![](share/addon_template/icon.png?raw=true) Installing manually
Steps:
- download release archive from Github
- unzip the release archive
- copy to your Godot project's root directory
- enable the plugin via the `Plugins` tab of `Project->Project Settings...` menu, in the Godot Editor

## ![](share/addon_template/icon.png?raw=true) Usage
Add a `Share` node to your scene and follow the following steps:
- use one of the following methods of the `Share` node to share text or images:
		- `share_text(title, subject, content)`
		- `share_image(full_path_for_saved_image_file, title, subject, content)`
				- Note that the image you want to share must be saved under the `user://` virtual directory in order to be accessible. The `OS.get_user_data_dir()` method can be used to get the absolute path for the `user://` directory. See the implementation of `share_viewport()` method for sample code.
		- `share_viewport(viewport, title, subject, content)`

## ![](share/addon_template/icon.png?raw=true) Troubleshooting
`adb logcat` is one of the best tools for troubleshooting unexpected behavior
- use `$> adb logcat | grep 'godot'` on Linux
	- `adb logcat *:W` to see warnings and errors
	- `adb logcat *:E` to see only errors
	- `adb logcat | grep 'godot|somethingElse'` to filter using more than one string at the same time
- use `#> adb.exe logcat | select-string "godot"` on powershell (Windows)

Also check out:
https://docs.godotengine.org/en/stable/tutorials/platform/android/android_plugin.html#troubleshooting
<br/><br/><br/>

---
# ![](notification/addon_template/icon.png?raw=true) Credits
Based on [Shin-NiL](https://github.com/Shin-NiL)'s [Godot Share plugin](https://github.com/Shin-NiL/Godot-Android-Share-Plugin)

Developed by [Cengiz](https://github.com/cengiz-pz)

Original repository: [Godot Android Share Plugin](https://github.com/cengiz-pz/godot-android-share-plugin)

---
layout: page
title: What's New
include_in_header: true
---

# Release Notes

Note that I follow [Semantic Versioning](https://semver.org) which means that the `major` (first) number in a version like `1.0.0` will only change if there's either a breaking change with something like the config file format (users with the old version then wouldn't be able to open the file saved with the new version), or if there's a significant change in the usage flow of the app (so users need to change their habits). A **migration guide** will be provided on this page for every breaking change.


## ✨ [1.5.0] - 2023-04-15 (Feb, Mar, Apr '23 Feature Update)

![](https://github.com/FlineDev/RemafoX-LandingPage/blob/main/assets/videos/v1.5.0-AutoCompletion.gif)

### Added
- The Add Translation window now provides auto-completions for the first two parts of a key to easily reuse the same prefixes. This saves time and prevents typos! [#22](https://github.com/FlineDev/RemafoX/issues/22)
- The Add Translation window now supports both reusing existing keys and overriding them – you have the choice! [#81](https://github.com/FlineDev/RemafoX/issues/81), [#95](https://github.com/FlineDev/RemafoX/issues/95) (Thanks to [Nico](https://twitter.com/n1c0_muc) and [Rob](https://twitter.com/ConfusedVorlon)!)
- The config file has now a convenient "Open project in Xcode" button in the general section below the project picker.

### Changed
- Rewrote the entire logic for managing windows & navigation, making use of new SwiftUI APIs available on macOS 13.
- Improved handling when user tries to configure a project that's already configured by providing quick action buttons. [#92](https://github.com/FlineDev/RemafoX/issues/92) (Thanks to [Rob](https://twitter.com/ConfusedVorlon)!)
- Changed the `formality` level for DeepL to prefer less formal language as this is what Apple and other translation services also default to. (Thanks to [Nico](https://twitter.com/n1c0_muc) and [Micha](https://github.com/michafaw)!)

### Removed
- Dropped support for macOS 12 after macOS 13 has been out for over 6 months. New minimum requirement: macOS 13.0.

### Fixed
- Thanks to the window management & navigation rework, many navigation-related bugs were fixed. [#43](https://github.com/FlineDev/RemafoX/issues/43) [#50](https://github.com/FlineDev/RemafoX/issues/50) [#59](https://github.com/FlineDev/RemafoX/issues/59) [#74](https://github.com/FlineDev/RemafoX/issues/74) [#76](https://github.com/FlineDev/RemafoX/issues/76) If you come across new ones, make sure to report them in the apps 'Help' menu! (Thanks to [@gaige](https://github.com/gaige), [Nico](https://twitter.com/n1c0_muc), [Rob](https://twitter.com/ConfusedVorlon), [David](https://github.com/croyfoo), and [Jason](https://github.com/jason-vectorrecipe)!)
- Fixed an issue where setting up a project without localized files would result in an empty search path, so even localized Strings added later wouldn't be found. (Thanks to [Antoine](https://twitter.com/twannl)!)
- Fixed a regression where generating the resources enum file via the build script was broken. (Thanks to [Antoine](https://twitter.com/twannl)!)
- Fixed an issue with a broken progress state after error occurred during project setup. (Thanks to [Antoine](https://twitter.com/twannl)!)
- Fixed an issue with translating texts containing an ampersand '&' character on DeepL. (Thanks to [Nico](https://twitter.com/n1c0_muc)!)
- The 'Insert as LocalizedStringKey' button is now disabled in 'pluralized' mode to prevent confusion. [#90](https://github.com/FlineDev/RemafoX/issues/90)


## 🐞 [1.4.1] - 2023-02-20

### Fixed
- Special handling for keys containing the ellipsis character (…) to prevent the 'Invalid redeclaration' bug in generated code. [#78](https://github.com/FlineDev/RemafoX/issues/78) (Thanks to [stephent](https://github.com/stephent)!)


## ✨ [1.4.0] - 2023-02-08 (Jan '23 Feature Update)

### Added
- Added support for Google Translate with full support for all ~130 languages. [#11](https://github.com/FlineDev/RemafoX/issues/11)
- Added support for Yandex Translate with full support for all ~90 languages. [#4](https://github.com/FlineDev/RemafoX/issues/11) (Thanks to [Vasily](https://twitter.com/anivaros)!)
- About 50 new languages were added, including Frisian, Scottish, Tajik, Yiddish & many more. 152 languages are now supported in total!
- Updated DeepL supported languages to include Korean and Norwegian. (Thanks to [Holger](https://twitter.com/_holger)!)

### Changed
- Renamed all references to "Preferences" to "Settings" for proper wording on macOS Ventura and later. (Thanks to [Holger](https://twitter.com/_holger)!)

### Fixed
- Fixed an issue with Microsoft Translator not working within projects that support more than 100 languages.


## [1.3.1] - 2023-01-14

### Removed
- Removed 3 regional language variants as they actually aren't supported by any currently supported translation service.

### Fixed
- Fixed an issue where multiple Add Translation windows would stay open on multiple use of the shortcut.


## 🐞 [1.3.1] - 2023-01-14

### Removed
- Removed 3 regional language variants as they actually aren't supported by any currently supported translation service.

### Fixed
- Fixed an issue where multiple Add Translation windows would stay open on multiple use of the shortcut.


## ✨ [1.3.0] - 2023-01-04 (Dec '22 Feature Update)

### Added
- We **love Open Source**, so we're giving all Open Source projects **unlimited access** to all RemafoX features for free!
  * Currently, only licenses listed on ChooseALicense.com/licenses are supported, including Apache 2.0, GPLv3, MIT, and more.
  * Currently, the public repository has to be available on either GitHub.com or GitLab.com.
  * Currently, an internet connection is needed for the Open Source validation to work.
  * Currently, only projects which are at least partly written in Swift are supported.


## 🐞 [1.2.2] - 2022-12-21

### Fixed
- Fixed an issue when **machine translating to Portuguese (Portugal)** via Microsoft Translator. [#69](https://github.com/FlineDev/RemafoX/issues/69) (Thanks to [Rob](https://twitter.com/ConfusedVorlon)!)


## 🐞 [1.2.1] - 2022-12-10

### Fixed
- Fixed 'Copy Code' button text color in dark mode from white-on-white (invisible) to black-on-white. [#68](https://github.com/FlineDev/RemafoX/issues/68) (Thanks to [Marc](https://github.com/marcrespass)!)


## ✨ [1.2.0] - 2022-12-05 (Nov '22 Feature Update)

### Added
- Added support for **5 missing languages** supported by the **DeepL** machine translation service: Bulgarian, Estonian, Lithuanian, Latvian, and Slovenian.
- Added support for **61 (!!) missing languages** supported by the **Microsoft Translator** service, for example Amharic, Azerbaijani, Bosnian, Burmese, Filipino, Khmer, Klingon, Malagasy, Nepali, Pashto, Persian, Punjabi, Serbian, Uyghur, Telugu, Turkmen, Uzbek, and many more! Yes, even Klingon. [>.-]
- A new 'Related Tools' menu links to **related tools, libraries, and apps** that might be of interest to users of RemafoX.

### Changed
- The **name of the app** has been slightly simplified by lowercasing the previously uppercased 'M'. Now it reads: **'RemafoX'**, instead of 'ReMafoX'.

### Fixed
- Fixed an issue with the inserted code not referencing things correctly when the default code generation settings were changed. [#64](https://github.com/FlineDev/RemafoX/issues/64) (Thanks to [Logan](https://twitter.com/logan_is_itt)!)
- Showing a warning when the key in the 'Add Translation' view contains a newline as this is most probably an oversight & could lead to issues in Xcode. [#65](https://github.com/FlineDev/RemafoX/issues/65) (Thanks to [Logan](https://twitter.com/logan_is_itt)!)


## 🐞 [1.1.1] - 2022-11-03

### Fixed
- Escaping the key portion in line number search for Stringsdict files properly to prevent a project setup error. [#58](https://github.com/FlineDev/RemafoX/issues/58) (Thanks to [Franco](https://twitter.com/dokfranco)!)
- Exclude more types of Xcode-managed Strings files from being included in the generated code. [#49](https://github.com/FlineDev/RemafoX/issues/49) (Thanks to [James](https://twitter.com/JamesSherlouk)!)


## ✨ [1.1.0] – 2022-10-29 (Oct '22 Feature Update)

### Added
- Officially added support for macOS 13 "Ventura" (tested & fixed some minor issues).
- Added support for generating **Objective-C compatible code** for safely accessing localized Strings. Enable in the 'Generated Code' pane. [#26](https://github.com/FlineDev/RemafoX/issues/26)
– The Add Translation workflow will now **automatically insert Objective-C** code when triggered from within an Objective-C file.
- **Automatic detection** of projects containing Objective-C code (to set the new option) for a streamlined project setup.

### Changed
- Improved the behavior of path search text fields in the config file UI to not interfere while typing.

### Fixed
- Fixed hangs during text entry in config file UI on macOS Ventura. [#37] (Thanks to [James](https://twitter.com/JamesSherlouk)!)
- Fixed 'Interface Builder Ignore Flags' not being editable in config file UI.
- Fixed changing translation texts in Add Translation view in the middle of texts sending cursor to end.


## 🐞 [1.0.4] - 2022-10-21

### Added
- Added support for regional Microsoft Translator resources, simply provide your region in the 'Set up API Keys' form in app settings. [#51](https://github.com/FlineDev/RemafoX/issues/51) (Thanks to [Nick](https://github.com/nickfedoroff) & [Liviu](https://twitter.com/LiviuJianu)!)

### Changed
- Changed keyboard shortcut for opening the Projects Browser from Cmd+P to the more common Cmd+0. [#48](https://github.com/FlineDev/RemafoX/issues/48) (Thanks to [@gaige](https://github.com/gaige)!)

### Fixed
- Fixed unaligned texts in the help menu. [#46](https://github.com/FlineDev/RemafoX/issues/46) (Thanks to [@gaige](https://github.com/gaige)!)
- Fixed the default icon not being pre-selected in the Settings.


## 🐞 [1.0.3] - 2022-10-16

### Added
- Welsh was added to the supported languages, including full pluralization support! [#32](https://github.com/FlineDev/RemafoX/issues/32) (Thanks to [James](https://twitter.com/JamesSherlouk)!)

### Changed
- Added current tier info to the environment info when reporting bugs to help reproducing bugs.
- Improved the error message to point to the current solution for non-Base-localized Storyboard/XIB/Intent files. [#41](https://github.com/FlineDev/RemafoX/issues/41)

### Fixed
- Fixed empty source translations preventing bulk machine translations from completing. [#20](https://github.com/FlineDev/RemafoX/issues/20) (Thanks to [@lukemmtt](https://github.com/lukemmtt)!)
- Fixed ignoring the ignore flags (e.g. `#remafox-ignore`) for extracting Strings from Storyboard/XIB files. [#21](https://github.com/FlineDev/RemafoX/issues/21) (Thanks to [@lukemmtt](https://github.com/lukemmtt)!)
- Improved the naming of the type generated for keys like `%1$@ %2$@` from being `_12` to being `UnnamedParam1UnnamedParam2`. [#23](https://github.com/FlineDev/RemafoX/issues/23)
- Fixed a non-closeable Plan Chooser window showing on each app start when installing the app with a pre-purchased plan. [#40](https://github.com/FlineDev/RemafoX/issues/40) (Thanks to [James](https://twitter.com/JamesSherlouk)!)
- Fixed the "Insert" buttons in Add Translation window being disabled when on the Max tier. [#25](https://github.com/FlineDev/RemafoX/issues/25) (Thanks to [@gaige](https://github.com/gaige) & [James](https://twitter.com/JamesSherlouk)!)


## 🐞 [1.0.2] - 2022-10-09

### Added
- Added links to learning material videos in Projects Browser for both project setup & add translation best practices.

### Fixed
- Fixed an issue with the app icon switcher not updating in Projects Browser + added a hint on setting icon failure.
- Fixed an issue where the limits check wouldn't work properly on first config file open.
- Fixed an issue with the build script not pointing to the home directory properly, making the build script not recognize the CLI tool.


## 🐞 [1.0.1] - 2022-10-07

### Added
- New 'Help' menu item with a direct link to leave a rating on the App Store.

### Fixed
- Fixed an issue where no error details would be presented when enum generation failed in project setup, getting stuck in the process.


## ✨ Public Release: ✨ [1.0.0] - 2022-10-05

### Added
- Updated DeepL supported languages to include Indonesian, Turkish, and Ukrainian.

### Changed
- Improved the "Add Translation" window completion experience by hiding app and switching to Xcode rather than quitting.

### Fixed
- Fixed an issue where no error details would be presented when counting keys in config file failed.


## 🐞 [1.0.0-beta.4] - 2022-09-20

### Added
- Added "Show Projects Browser" & "Show Add Translation" buttons to "Window" menu bar to help with some window management issues.
- Added a new option to configure if an empty line should be placed between every two keys in a `.strings` file or not.

### Changed
- Reverted Add Translation window to quit the entire app again on Cancel or Insert button press to prevent duplicate windows.
- The list of supported languages in source language selection dropdowns is now sorted alphabetically.
- Improved automatic detection of multiple subpaths on setup and adding `/` suffix to folders for less confusion.
- Improved performance of application in several places by preventing unnecessary re-computes of SwiftUI views.

### Deprecated
- The `.remafox` config file structure has received new `appleStringsFilesConfig` options. An automatic migration is available (only in this beta release!) – just open all your config files once and save them right away to upgrade.

### Fixed
- Fixed an issue with machine-translation not finding `.strings(dict)` files when the language forlders are in same path as `.remafox` config file. (Thanks to [Ulf](https://twitter.com/vieuxrenard))
- Fixed an issue that could lead to a crash during machine-translation with `.strings(dict)` files in `.lproj` paths with invalid lang codes.
- Fixed an issue in the project browser that could delete the wrong project in the list after confirming the delete.
- Fixed an issue where editing a `.stringsdict` file from Xcode would lead to a different indentation format than when produced by RemafoX.
- Fixed an issue that rendered some leftover SF Symbols in Add Translation text views incorrectly.
- Fixed an issue with multi-line translation values in the source language leading to compiler errors in the generated Swift file.


## 🐞 [1.0.0-beta.3] - 2022-09-01

### Added
- A new App Icon Switcher in the app's settings allows users to select their preferred app icon design & color.
- A new `remafox translate` subcommand in the CLI tool completes the build script by adding a machine-translation step. (Thanks to [Ulf](https://twitter.com/vieuxrenard))
- Added sound effects on a few specific success or error actions, such as project setup completion or occurrence of an error.
- A new option in the app's settings for turning off app sound effects for users who prefer no sound effects.
- A new error message with a helpful text is shown on pressing a project in browser when the config file was moved. (Thanks to [Nico](https://twitter.com/n1c0_muc)!)

### Changed
- Improved relevance of web searches of users by changing error code separator from '-' to 'x'.
- Simplified the wording of Help menu entries to a shorter & more familiar terminology.
- Changed the temporary app icon to the final design after [2 Twitter surveys](https://twitter.com/Remafox_App).
- Improved setup for developers opening a pre-configured project: The open panel should now always show the right project root path.
- Moved 'Copy code' button into the code box for a more intuitive place to find it. (Thanks to [Nico](https://twitter.com/n1c0_muc)!)
- Adjusted color of multi-steps tutorial page controls to look less like a clickable button. (Thanks to [Nico](https://twitter.com/n1c0_muc)!)
- Changed the app accent color from a greenish color to be more blue, based on the new default app icon. (Thanks to [Nico](https://twitter.com/n1c0_muc)!)

### Deprecated
- The `.remafox` config file structure has received a new `configFilePath` field. An automatic migration is available (only in this beta release!) – just open all your config files once and save them right away to upgrade.

### Removed
- Removed extra emphasis on "Resources Enum File Path" text field in config file to simplify information hierarchy. (Thanks to [Nico](https://twitter.com/n1c0_muc)!)

### Fixed
- Fixed an issue where the machine translation would be executed before normalization, leading to the possibility of temporarily untranslated keys. (Thanks to [Ulf](https://twitter.com/vieuxrenard))
- Fixed an issue which prevented the machine translation results view from being shown when started from config file. (Thanks to [Ulf](https://twitter.com/vieuxrenard))
- Fixed an issue that could lead to a crash in some language combinations within the smart mapping logic when translating pluralized Strings.
- Fixed the build script showing an invalid relative path to the config file by calculating relative path from project if available. (Thanks to [Ulf](https://twitter.com/vieuxrenard))
- Fixed an issue where the build script could fail with an `Error Code: RWF-X` stating 'data couldn't be read because it is missing' even if it wasn't. [#3](https://github.com/FlineDev/RemafoX/issues/3) (Thanks to [Vasiliy](https://twitter.com/anivaros))
- Fixed an issue that could prevent a translation text field receiving user input from the user after pressing 'Rescan' button in add translation view.
- Fixed an issue with jumping to a next language text field via pressing 'tab' on pluralized text entry in add translation view.
- Fixed an issue that prevented the default indentation style for new projects to be '4 spaces' (it defaulted to '3 spaces' instead).
- Fixed an issue that rendered SF Symbols in text views incorrectly.
- Fixed an issue where special characters in machine-translated texts would not be correctly escaped in `.strings` files, leading to a build error.
- Fixed an issue which could lead to a crash on project setup in projects with Base-localized Storyboard/XIB files.


## 🐞 [1.0.0-beta.2] - 2022-07-24

### Added
- Warns when config file format has higher version than currently supported with hint to upgrade.
- Added automatic search for Xcode projects and a picker to select one. This helps detect the supported languages more reliably. (Thanks to [Holger](https://twitter.com/_holger)!)

### Changed
- Improved formatting of Xcode integration instructions.
- Widened click area for expandable disclosure groups (such as 'Show Explanation') from triangle to full title. (Thanks to [Ulf](https://twitter.com/vieuxrenard))
- Changed the title of diclosure groups to state 'Hide' instead of 'Show' when they are in expanded state.
- Made the settings window size smaller to fit the currently small amount of options.
- The add translation window no longer quits the entire app but hides all windows instead on Cancel or Insert button press.
- Changed recommended 'Add translation' shortcut to ⌥⌘L from ⌥L which is used for '@' in common keyboard layouts like German.
- Changed the 'Copy' button title to 'Copy Code' to make it clear what is being copied in Build Script walkthrough. (Thanks to [Nico](https://twitter.com/n1c0_muc)!)
- Hidden detailed explanation behind disclosure group in last step of Build Script walkthrough for less text. (Thanks to [Nico](https://twitter.com/n1c0_muc)!)

### Removed
- Removed potentially confusing different doc sample language setting, always using source language now.
- Removed the "New" item menu bar entries & window tabbing support to prevent confusion with window management.
- Removed the need to specify if the provided DeepL auth key is for a Free or a Pro plan. Auto-detecting based on key instead.

### Fixed
- Removed SF Symbol icons that were not showing properly for the about menu entry and help menu entries.
- Fixed an issue with Strings(dict) files not being updated on search path changes after initial setup.
- Fixed an issue where a non-existent Strings(dict) file could be selected by default in add translation window.
- Fixed an issue with source language chooser being empty when localized files are placed at projects root. (Thanks to [Ulf](https://twitter.com/vieuxrenard)!)
- Fixed an issue where contents from Storyboard/XIB-related Strings files would be included into the generated resources enum.


## ✨ Beta Release: ✨ [1.0.0-beta.1] - 2022-07-07

### List of Features in this Beta
- **Add new localizable Strings** to your Strings files without ever leaving your Swift file in Xcode (Free)
- **Machine-translate** your localizations to all ~40 languages [supported also by iOS](https://www.apple.com/ios/feature-availability/#system-language-system-language) using Microsoft or DeepL services (Free, but services not included)
- **Safely access** translations in code using **generated Swift enums** for auto-completion & compiler checks (Free)
- **Lint** your Strings files for empty translations or duplicate keys and show **in-line warnings** in Xcode (Free)
- **Incrementally update** your base-localized Storyboard's or XIB's related Strings files (Free)
- **Normalize** your Strings by sorting keys alphabetically & harmonizing with a selected source language (Free)
- Easily **add new pluralized** localizable Strings to your Stringsdict files without leaving Xcode (Paid)
- Easily **machine-translate pluralized** localizable Strings with smart language-rules-aware pluralization counts (Paid)

### Improvements over BartyCrouch
- A **new config file format** which can be edited with an intuitive **visual editor** (no `.bartycrouch.toml` file needed)
- A new **"Preview matching files" button** to conveniently simulate a files search & adjust paths accordingly based on results
- An explanation for every single configurable option for more confidence in adjusting the config to your needs
- A **built-in SwiftUI-compatible enum generator** with lots of customization options (no need for SwiftGen for Strings)
- The API keys for machine translations services are no longer stored in the config file (no secrets in Git)
- A **built-in project scanner** to provide smarter defaults for a quick start – including a BartyCrouch migrator (read-only)
- Multiple **built-in step-by-step guides** for easier integration with Xcode
- Adding new localizations **no longer breaks Xcodes edit history** thanks to a built-in Xcode Source Editor extension

### Planned for the Future
- Easy way to send translations to translators & integrate their provided translations
- Synchronize translations between Android & iOS platforms of the same app
- Provide a glossary of reviewed common Strings (to improve machine-translated apps)
- UI/Unit tests integration to provide context screenshots for keys for translators
- ... and much more!

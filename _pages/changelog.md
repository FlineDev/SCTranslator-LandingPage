---
layout: page
title: What's New
include_in_header: true
---

# What's New


## 🐞 [2.0.2] - 2024-05-10

- When warnings & progress is updated, the progress indication is now more prominent.
- Progress percentage is now correctly calculated even for languages with differing plural or device variants compared to source language.
- When pressing 'Return' while a plural or device case is selected, the text editor will now correctly open.
- Searching for text now also matches texts in plural or device cases.


## 🐞 [2.0.1] - 2024-05-05

- Fixed an oversight that made it seem that API keys are required for the new Translation Editor mode. Should work without now!


## ✨✨✨ [2.0.0] - 2024-05-01

HUGE FREE UPDATE: Say hello to the new "Translation Editor", fixing all the issues you had with the String Catalog editor inside Xcode. Just drag & drop your file to open it in TranslateKit's editor and get enormous benefits, including multi-select (to confirm multiple entries at once), keyboard shortcuts (for faster navigation), parameter inconsistency warnings (like a %@ in the source language missing in a translation), deleting an entire language (not supported in Xcode), and so much more. And all this for free!


## 🐞 [1.7.1] - 2024-04-25

- Added a new "Localization Pipeline" window to better explain what smart stuff the app does behind the scenes automatically for the user.
- Added a new "Test" button in the API key setup view to check if the provided data is actually valid for machine translation.
- Fixed an issue where nothing would happen if an API key was invalid. Shows an error message now with the problem.


## ✨ [1.7.0] - 2024-04-20

- Translations can now be manually adjusted after machine-translation has run right within the app.
- New warnings column indicates when machine translation breaks parameters like '%@'. TranslateKit will auto-repair most common issues without you noticing, but in some edge cases when it can't, it informs you exactly what parameters are broken.
- Fixed an issue with parsing String Catalogs that contain migrated translations from Strings(dict) files.


## 🐞 [1.6.1] - 2024-04-10

- Fixed an issue with 'Common Translations' menu bar extra not showing because the text is too long. It's now just an icon instead!


## ✨ [1.6.0] - 2024-03-16

- New menu bar extra to search for Common Translations for consistency with iOS terminology in ~40 languages without leaving Xcode!
- Rebranded the name of the app from String Catalog Translator to TranslateKit!
- Fixed the broken 'Rate the App' link in the help menu (thanks Kris!)


## 🐞 [1.5.1] - 2024-03-01

- Bigger translation modal size by default.
- Languages names always show in English instead of your system language for consistency.
- Translations are now sorted by language rather than by translation order.
- More broken parameters by machine-translation are auto-repaired, like "%1$s@" when translated to "% 1$ @".
- The 'Common Translations' were extended by some common percent-based texts like "%{progress}%" to avoid broken translations.


## ✨ [1.5.0] - 2024-02-29

NEW: More than 1,500 high-quality "Common Translations" such as "OK", "Save!", "Cancel", and "Done" are built-in to the app with support for nearly 40 languages. You don't need to do anything: matching texts are detected for new translations automatically. This improves the quality of your translations, reduces clipped texts in some languages, and also reduces the

NEW: You can now see a small indicator (with hover tooltip support) in the translation modal that shows which source your translations are coming from. This way you know which translation service provided which translation, or if the translation was even matched from the new "Common Translations" dataset.


## ✨ [1.4.0] - 2024-02-10

- Changed: Defaults to 'Confirmed' state for machine-translations & recommends it now. This goes in line with how String Catalogs behave on source language value changes.
- Fixed: Automatically repairs broken parameters in common cases where machine-translation services break things like "%@@" to things like "% @@" or "%@@".

Migration Notice: If you turn on the 'Confirmed' mode in Settings, all your translations in 'Needs Review' state will get re-translated. This is expected behavior as whenever you make a change to a value in your source language, Xcode will automatically mark related translations as 'Needs Review' so they get re-translated as well.


## ✨ [1.3.0] - 2024-01-28

- New: Full Pluralization support with smart machine-translation ensuring only needed cases are translated and translations are automatically pluralized correctly!
- New: Opening recently used String Catalog files is now even faster with the 'Recently used' dropdown. Turn it off in the Settings if you don't want it!
- New: A new tip in the language selector now teaches you how manual multi-selection of languages works. The preset buttons aren't the only way!
- Fixed: A UI glitch that caused the translation progress to make the target language flags "jump around" all the time. It's smoother now.


## ✨ [1.2.0] - 2024-01-15

- Added an option in Settings menu to mark machine-translated texts as 'Confirmed' rather than 'Needs Review'
- Fixed an issue with parsing InfoPlist.strings files that could lead to a crash
- Improved error messages


## ✨ [1.1.0] - 2024-01-10

- Added support for the 'Vary by Device' feature in String Catalogs: Now you can provide slightly different texts on iPhone, iPad, Mac, etc. and localize each variant easily!

For example, I provide a button "Found a mistake?" in one of my apps' toolbar, but on iPhone I use the shorter button title "Mistake?" as the long form doesn't fit.


## ✨ [1.0.0] - 2024-01-05

Initial Release. 🚀🎉

# Cheatsheet for forking Galoy-mobile to your own version of the Bitcoin Beach Wallet"

# 1. Running BBW locally

## to run galoy-mobile on M1 mac:

- clone repo `git clone https://github.com/GaloyMoney/galoy-mobile.git` 
- cd into folder you just cloned
- checkout latest tag (not main branch) `git checkout tags/[latest]`
- `yarn install` (make sure you have yarn v1.22.19, node v19.3.0, npm v9.2.0)
- open a new teminal tab
- in the new tab, `yarn start`
- open xcode
- open your local copy of `/galoy-mobile/ios/GaloyApp.xcworkspace` in xcode
- press the play/run button at the top left of xcode

If all these steps are followed, the react native code should build and the simulator shoud open with Bitcoin Beach Wallet starting up.

# 2. Change Icon App Set for appstore and logo
- go to https://www.appicon.co
- upload desired icon to website and generate appset (leave filename blank)
- You will get a downloaded .zip file with all the different size versions of your icon.
- Extract that .zip file into a folder
- copy all image files into `galoy-mobile/ios/GaloyApp/images.xcassets/AppIcon.appiconset`
- in xcode, go to `images.xcassets` and click on `AppIcon` in the left outline. 
- delete all the existing images in the main window, and drag and drop your new icons to the correct size cutouts.

# 3. Change the name of the app on iOS
- In terminal, edit the following file ios/GaloyApp.xcodeproj/project.pbxproj
- change the variable PRODUCT_NAME in two places to the name of your app
- Save the file and rebuild the app


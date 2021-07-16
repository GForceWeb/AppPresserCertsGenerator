AppPresser Certs Generator
================

This tool uses the Fastlane library to create a full set of certificates for AppPresser apps on Bitrise. It is aimed at AppPresser Reseller customers who are responsible for managing certs themselves. MacOS is required as this tool is dependant on the XCode Command Line Tools.

# Fastlane Installation

Start by making sure you have the latest version of the Xcode command line tools installed:

```
xcode-select --install
```

Then Install _fastlane_ using
```
sudo gem install fastlane -NV
```
or alternatively using `brew cask install fastlane`

# App Setup and Usage
### iOS Certs
To get this script ready to create certs for your app open up the fastlane/Fastfile file and fill in the required fields (site_slug, app_name, app_id, username). If you also want to create your keystore file fill in the additional fields (custname, countrycode & keystorepassword)


Using a terminal, from the root folder (ie ~User/Folder/AppPresserCertsGenerator/) run the command below to create the certificates. You'll be prompted for your Apple Account password and then a 2 factor auth code. Once done the script should run for a few minutes. Once complete you'll find your certs for upload under AppPresserCertsGenerator/site-slug/appname/bitrise
```
fastlane ios
```

### Android Keystore

You can also create your Android Keystore using this script by running the command below from the root folder. The completed file will be found under the AppPresserCertsGenerator/site-slug/appname/bitrise folder

```
fastlane android
```


----

More information about fastlane can be found on [fastlane.tools](https://fastlane.tools).
The documentation of fastlane can be found on [docs.fastlane.tools](https://docs.fastlane.tools).

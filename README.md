# CocoaPodsTutorial
Let's release  CocoaPod!<br/>

[1. What is CocoaPods?](#what-is-cocoapods)<br/>
[2. Install CocoaPods](#install-cocoapods)<br/>
[3. Make CocoaPods Project](#make-cocoapods-project)<br/>
[4. Create own Pod](#create-own-pod)<br/>

***

## What is CocoaPods?
CocoaPods is a library dependency manager of Xcode project. CocoaPods helps to easily discover 3rd-party opensource libraries.

###### Why do we need dependency manager? https://en.wikipedia.org/wiki/Dependency_hell

## Install CocoaPods
```
sudo gem install cocoapods
```

## Make CocoaPods Project
1. Create a new Xcode project
2. Initialize Pod in the project directory
```
pod init
```
3. Edit Podfile
```
platform: [platform], '[version]'

target '[project name]' do

  use_frameworks!

  pod [pod name], ~>[version]

end
```
4. Install Pod
```
pod install
```
5. Open Xcode workspace and do your job!

## Create own Pod

1. Create Xcode Pod project
```
pod lib create [pod name]
```
> 1-1 Choose Platform [iOS/macOS] </br>
> 1-2 Choose Language [Swift/ObjC] </br>
> 1-3 Include Demo Application [Y/N] </br>
> 1-4 Testing Framework [Quick/None] </br>
> 1-5 View Based Testing [Y/N] </br>

2. Create own files in 'classes' directory
3. Specify version in .podspec
```
Pod::Spec.new do |s|
  ...
  s.version = '0.1.0'
  ...
end
```
4. Release commit and push
```
git -a -m '[commit summary]
git tag 0.1.0
git push origin 0.1.0
```
5. Validate Pod(If need, fix errors)
```
pod spec lint
```
6. Register session
```
pod trunk [email address] '[name]' --description='[decription of session]'
```
7. Deploy pod!
```
pod trunk push [project name].podspec
```

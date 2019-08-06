# CocoaPodsTutorial
Let's release my CocoaPod!<br/>

## Goal
Every projects can easily use my custom extensions and protocols.<br/>

## What is CocoaPods?
CocoaPods is a Library Dependency Manager of Xcode Project. CocoaPods helps to easily discover 3rd-party opensource libraries.

Why do we need dependency manager?<br/>
https://en.wikipedia.org/wiki/Dependency_hell<br/>

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
5. Open Xcode workspace and do your job

## 

코코아팟 만들기
: pod lib create [pod name]

classes 폴더에서 파일 만들고 작업하기
깃에 릴리즈하기
팟 스펙에 릴리즈 버전 명시
pod spec lint
(코코아팟에 등록안되있다면) pod trunk register [이메일] [이름] [현재 기기명]
pod trunk push [pod spec name].podspec

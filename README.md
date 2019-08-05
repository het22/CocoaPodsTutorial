# CocoaPodsTutorial

Let's release my CocoaPod!
<br/><br/>

## Goal

Every projects can easily use my custom extensions and protocols.
<br/><br/>

## What is CocoaPods?

CocoaPods is a Library Dependency Manager of Xcode Project. CocoaPods helps to easily discover 3rd-party opensource libraries.

Why do we need 'dependency manager'?
https://en.wikipedia.org/wiki/Dependency_hell
<br/><br/>

## Install CocoaPods

```ruby
$ sudo gem install cocoapods
```
<br/><br/>

팟 인스톨 vs 팟 업데이트
: 새로운 팟이 추가되었을 때는 인스톨, 기존에 있던 팟의 버전만 변경하려면 업데이트

코코아팟 엑스코드 프로젝트 만들기
: 새로운 엑스코드 프로젝트 생성
: 프로젝트 디렉토리에서 pod init
: Podfile에서 플랫폼, 버전, 타켓 프로젝트 입력
: 추가할 pod과 버전정보 입력
: pod install
: 디렉토리에 생성된 엑스코드 워크스페이스로 작업하기

락 파일은 무엇?
: 설치된 모든 라이브러리와 그 버전의 스냅샷

코코아팟을 만든다는 것 -> podspec을 만드는 것

코코아팟 만들기
: pod lib create [pod name]

classes 폴더에서 파일 만들고 작업하기
깃에 릴리즈하기
팟 스펙에 릴리즈 버전 명시
pod spec lint
(코코아팟에 등록안되있다면) pod trunk register [이메일] [이름] [현재 기기명]
pod trunk push [pod spec name].podspec

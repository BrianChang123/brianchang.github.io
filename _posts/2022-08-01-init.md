---
layout: post
title: Flutter 시작하기
subtitle: Flutter 설치
categories: flutter
tags: [flutter]
---

__해당 문서는 Mac OS 기반으로 작성되었습니다.__

Flutter 역시 homebrew를 통한 설치가 가능하나 여기서는 공식 문서상의 내용을 토대로 다루도록 하겠다.

공식 문서상에서는 zip 파일을 이용한 설치를 설명하고 있으며 해당 파일의 경로는 아래와 같다.

[Flutter Download](https://docs.flutter.dev/get-started/install/macos)

zip 파일을 다운받고 원하는 경로에 압축을 풀면 된다.
공식 문서상에서는 development 라는 폴더를 root 경로 아래에 생성하여 진행햐였다.


```shell
cd ~
mkdir development
cd development
unzip ~/[flutter zip 파일 위치 경로]
```

압축을 푼 후 flutter 환경변수를 영구적으로 추가한다.
```shell
vi ~/.bash_profile
export PATH="$PATH:~/development/flutter/bin"
source ~/.bash_profile
```
~/.bash_profile 에 환경변수를 등록하지 않고 export 커맨드만 입력할 경우 현재 터미널 창에서만 환경변수가 적용된다.


환경변수가 제대로 추가되었는지 확인하기 위해 하기의 명령어를 입력한다
```shell
echo $PATH
```

flutter 커맨드가 제대로 작동하는지 확인하기 위해 하기의 커맨드를 입력한다.
정상적으로 작동 시 flutter가 있는 경로가 나타난다.
아무것도 나타나지 않으면 환경 변수 설정 등의 문제가 있는 것이니 환경변수 경로를 다시 확인 바란다.
```shell
which flutter
```

하기의 명령어는 필수는 아니나, iOS, Android 바이너리를 미리 다운로드 하고 싶다면 입력하는 것을 추천한다.```
```shell
flutter precache
```

flutter doctor 는 flutter 설정상의 의존성 체크를 위해 사용되는 명령어다.
```shell
flutter doctor
```
flutter doctor 실행 후 노란색 느낌표나 빨간색 표시가 있는 것들은 추가적으로 설치가 필요하다.

추가적인 설치가 필요없는 경우 전부 초록색 마킹표시가 나타난다.

![test][flutter-doctor]


초기 설정 및 프로젝트 생성은 다음 편에서 다루도록 하겠다.



[flutter-doctor]:/assets/images/flutter/flutter-01.png

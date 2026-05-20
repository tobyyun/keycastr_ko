# KeyCastr Korean

KeyCastr Korean은 macOS용 키 입력 표시 앱 [KeyCastr](https://github.com/keycastr/keycastr)의 한국어 입력 환경 수정 버전입니다.

한글 입력 상태에서 `⌘ + ㅊ`, `⌘ + ㅈ`처럼 눌렀을 때 화면에는 물리 키 기준으로 `⌘C`, `⌘W`처럼 표시되도록 고쳤습니다. 영상 녹화, 강의, 발표처럼 단축키를 화면에 보여줘야 할 때 쓰기 좋습니다.

![header image](assets/KeyCastr_header.png)

## 설치

1. [Releases](https://github.com/tobyyun/keycastr_ko/releases)에서 최신 `KeyCastr.app.zip`을 받습니다.
2. 압축을 풉니다.
3. `KeyCastr.app`을 `Applications` 폴더로 드래그합니다.
4. `Applications` 폴더에서 `KeyCastr.app`을 실행합니다.

이미 Homebrew로 설치한 공식 KeyCastr가 있다면 이 수정이 들어 있지 않을 수 있습니다. 이 버전을 쓰려면 Releases에서 받은 `KeyCastr.app`으로 교체하세요.

```console
brew install --cask keycastr
```

위 Homebrew 명령은 공식 upstream KeyCastr를 설치합니다. 이 저장소의 한국어 입력 수정이 upstream에 반영되기 전까지는 Homebrew 설치본에서 `⌘ㅊ`, `⌘ㅈ`처럼 보일 수 있습니다.

## 첫 실행 보안 경고

이 저장소의 배포 zip은 개인용 로컬 빌드입니다. Apple Developer ID로 공증한 공식 배포본이 아니기 때문에, 다른 Mac에서 처음 실행할 때 macOS가 경고를 띄울 수 있습니다.

경고가 나오면 보통 아래 방법으로 열 수 있습니다.

1. `KeyCastr.app`을 우클릭합니다.
2. `열기`를 선택합니다.
3. 다시 확인 창이 나오면 `열기`를 누릅니다.

그래도 열리지 않으면 `시스템 설정 > 개인정보 보호 및 보안`에서 차단된 앱을 허용한 뒤 다시 실행하세요.

경고 없이 배포하려면 Apple Developer Program의 Developer ID 인증서로 앱을 서명하고 notarization까지 해야 합니다. 지금 빌드는 테스트와 개인 공유용으로 생각하면 됩니다.

## 권한 설정

KeyCastr는 키 입력을 화면에 표시하기 위해 macOS의 입력 모니터링 권한이 필요합니다.

1. `시스템 설정 > 개인정보 보호 및 보안 > 입력 모니터링`으로 이동합니다.
2. `KeyCastr`를 켭니다.
3. macOS가 재실행을 요구하면 KeyCastr를 껐다가 다시 켭니다.

권한이 꼬였을 때는 기존 `KeyCastr` 항목을 삭제한 뒤, `Applications` 폴더의 `KeyCastr.app`을 다시 추가하면 됩니다.

## 위치 조정

기본 표시 위치는 화면 왼쪽 아래입니다. 화면에 뜨는 키 표시 영역을 드래그하면 위치를 바꿀 수 있습니다.

![reposition](assets/reposition.gif)

## 보안 안내

입력 모니터링 권한을 가진 앱은 키 입력 이벤트를 받을 수 있습니다. 신뢰하는 앱에만 권한을 주세요.

KeyCastr는 오픈소스 앱이며, 업데이트 확인을 위한 [Sparkle](https://sparkle-project.org/) 프레임워크 외에 별도의 네트워크 기능을 넣지 않았습니다. 비밀번호 입력 필드처럼 macOS가 보안 입력으로 처리하는 입력은 표시하지 않습니다.

## Credits

- [sdeken](https://github.com/sdeken): original KeyCastr
- [akitchen](https://github.com/akitchen): ongoing KeyCastr maintenance
- [elia](https://github.com/elia): created the `keycastr` organization
- [lqez](https://github.com/lqez): menu bar icon
- [QuintB](https://github.com/QuintB): updated application icon
- [Toby Yun](mailto:tobyyun@gmail.com): Korean input-source command shortcut keycap handling

## License

[BSD 3-Clause](https://opensource.org/licenses/BSD-3-Clause)

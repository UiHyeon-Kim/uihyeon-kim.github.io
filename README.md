# UiHyeon Kim apps

앱 목록과 각 앱의 소개·지원 페이지를 제공하는 정적 GitHub Pages 사이트입니다.

- 앱 목록: https://uihyeon-kim.github.io/
- SNAPBOUND: https://uihyeon-kim.github.io/snapbound/

- PoseUp: https://uihyeon-kim.github.io/poseup/
- 광고 판매자 파일: https://uihyeon-kim.github.io/app-ads.txt
- Google Play: https://play.google.com/store/apps/details?id=com.hanhyo.poseup
- 개인정보처리방침: https://uihyeonkim.notion.site/PoseUp-3545686b1943803398e1ee1926b5f62b

## 수정과 배포

루트의 `index.html`과 `styles.css`는 앱 목록입니다. PoseUp은 `poseup/index.html`·`poseup/styles.css`·`poseup/assets/`에서 관리합니다. `main`에 푸시하면 배포됩니다. 패키지 설치나 빌드 과정이 없습니다.

GitHub 저장소의 Settings → Pages는 **Deploy from a branch / main / /(root)**로 설정합니다. `.nojekyll`은 소스 파일을 그대로 게시하도록 합니다. `poseup/assets/`에는 공개 앱 아이콘과 예시 운동 기록이 표시된 앱 캡처만 들어 있습니다. 홈페이지는 별도 분석·추적 스크립트를 사용하지 않습니다.

로컬 확인:

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

## app-ads.txt

루트의 `app-ads.txt`에는 사용자가 AdMob에서 복사해 제공한 게시자 문구를 그대로 게시했습니다. 이 파일에 들어가는 `pub-…`는 게시자 ID이며 앱 ID(`ca-app-pub-…~…`)나 광고 단위 ID(`ca-app-pub-…/…`)가 아닙니다.

게시 후 필요한 설정:

1. Play Console → PoseUp → 스토어 설정 → 스토어 등록정보 연락처 세부정보의 **웹사이트**를 `https://uihyeon-kim.github.io/poseup/`로 등록합니다. 같은 도메인을 사용하므로 AdMob의 파일 위치는 루트의 `/app-ads.txt` 그대로입니다. 기존 루트 주소도 앱 목록에서 PoseUp으로 연결되지만, 소개 페이지로 바로 이동하려면 새 경로를 사용합니다.
2. 공개 Play 페이지의 앱 지원에 사이트 링크가 표시되는지 확인합니다.
3. AdMob → 앱 → 모든 앱 보기 → app-ads.txt → PoseUp에서 업데이트를 확인합니다.
4. 상태가 검증됨으로 바뀌는지 확인합니다. 파일 게시만으로 AdMob 앱 인증이나 실제 광고 게재가 완료된 것은 아닙니다.

게시자 정보가 변경되면 AdMob의 **app-ads.txt 설정 방법**에 표시되는 정확한 코드 스니펫으로 파일을 수정합니다. 예시 ID나 Google 테스트 ID를 넣지 않습니다.

이 저장소의 배포는 Android 앱의 실제 광고 활성화, Play Console 설정 변경, 앱 업로드를 수행하지 않습니다.

## 참고

- [GitHub Pages 설정](https://docs.github.com/en/pages/quickstart)
- [AdMob app-ads.txt 설정](https://support.google.com/admob/answer/9363762?hl=ko)

사이트의 앱 화면은 예시 운동 데이터로 촬영한 이미지입니다. 상표와 앱 이미지의 권리는 PoseUp 제작자에게 있습니다.

## SNAPBOUND 비공개 테스트 안내

`snapbound/`에는 SNAPBOUND의 로컬 플레이 버전 소개, 개인정보처리방침, 도움말을 둡니다.
공개 경로는 `/snapbound/`, `/snapbound/privacy.html`, `/snapbound/support.html`입니다.
문의 이메일은 hanhyo042@gmail.com이며, 앱·광고 설정의 정본은 SNAPBOUND 저장소의 `release/closed-test.properties`와 출시 준비 문서입니다.
PoseUp 소개는 `/poseup/`에, 앱 목록은 루트 `/`에 두고 기존 `app-ads.txt`는 루트에 유지합니다. 두 앱은 같은 AdMob 게시자 계정을 사용합니다.

SNAPBOUND 페이지 게시와 Android 앱/테스트 트랙 배포는 별개입니다. 구매 확인 서버나 온라인 기능을 활성화하면 개인정보처리방침과 실제 제공 범위를 함께 갱신해야 합니다.

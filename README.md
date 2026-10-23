# PoseUp website

PoseUp 소개와 Google Play·개인정보처리방침 링크를 제공하는 정적 GitHub Pages 사이트입니다.

- 사이트: https://uihyeon-kim.github.io/
- 광고 판매자 파일: https://uihyeon-kim.github.io/app-ads.txt
- Google Play: https://play.google.com/store/apps/details?id=com.hanhyo.poseup
- 개인정보처리방침: https://uihyeonkim.notion.site/PoseUp-3545686b1943803398e1ee1926b5f62b

## 수정과 배포

`index.html`과 `styles.css`를 수정하고 `main`에 푸시하면 배포됩니다. 패키지 설치나 빌드 과정이 없습니다.

GitHub 저장소의 Settings → Pages는 **Deploy from a branch / main / /(root)**로 설정합니다. `.nojekyll`은 소스 파일을 그대로 게시하도록 합니다. `assets/`에는 공개 앱 아이콘과 예시 운동 기록이 표시된 앱 캡처만 들어 있습니다. 홈페이지는 별도 분석·추적 스크립트를 사용하지 않습니다.

로컬 확인:

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

## app-ads.txt

루트의 `app-ads.txt`에는 사용자가 AdMob에서 복사해 제공한 게시자 문구를 그대로 게시했습니다. 이 파일에 들어가는 `pub-…`는 게시자 ID이며 앱 ID(`ca-app-pub-…~…`)나 광고 단위 ID(`ca-app-pub-…/…`)가 아닙니다.

게시 후 필요한 설정:

1. Play Console → PoseUp → 스토어 설정 → 스토어 등록정보 연락처 세부정보의 **웹사이트**를 `https://uihyeon-kim.github.io/`로 등록합니다.
2. 공개 Play 페이지의 앱 지원에 사이트 링크가 표시되는지 확인합니다.
3. AdMob → 앱 → 모든 앱 보기 → app-ads.txt → PoseUp에서 업데이트를 확인합니다.
4. 상태가 검증됨으로 바뀌는지 확인합니다. 파일 게시만으로 AdMob 앱 인증이나 실제 광고 게재가 완료된 것은 아닙니다.

게시자 정보가 변경되면 AdMob의 **app-ads.txt 설정 방법**에 표시되는 정확한 코드 스니펫으로 파일을 수정합니다. 예시 ID나 Google 테스트 ID를 넣지 않습니다.

이 저장소의 배포는 Android 앱의 실제 광고 활성화, Play Console 설정 변경, 앱 업로드를 수행하지 않습니다.

## 참고

- [GitHub Pages 설정](https://docs.github.com/en/pages/quickstart)
- [AdMob app-ads.txt 설정](https://support.google.com/admob/answer/9363762?hl=ko)

사이트의 앱 화면은 예시 운동 데이터로 촬영한 이미지입니다. 상표와 앱 이미지의 권리는 PoseUp 제작자에게 있습니다.

<h1 align="middle">🍴</h1>
<h2 align="middle">level1 - 영화 리뷰 미션</h2>
<p align="middle">자바스크립트로 구현하는 영화관 웹앱</p>

### 결과물: [영화관](https://xodms0309.github.io/javascript-movie-review/)

<img width="1440" alt="스크린샷 2023-03-25 오후 6 00 48" src="https://user-images.githubusercontent.com/55427367/227707768-d8c8db17-3c2f-4777-8a4a-9e9d31f050f9.png">
<img width="1440" alt="스크린샷 2023-03-25 오후 6 01 16" src="https://user-images.githubusercontent.com/55427367/227707788-227e44e3-ae3c-488c-b381-d7de7083d85b.png">

### 🚀 학습 목표
> 1. API 통신을 통한 비동기 통신
> 2. UX 개선
> 3. 관심사 분리


### 📝 1단계 기능 목록
1. 🎬 영화 목록 조회 (인기순)
  - 영화 목록의 1페이지를 불러오며 더보기 버튼을 누르면 그 다음의 영화 목록을 불러 올 수 있다. 단, 페이지 끝에 도달한 경우에는 더보기 버튼을 화면에 출력하지 않는다.
  - 영화 목록 아이템에 대한 Skeleton UI를 구현한다.
2. 🔎 검색
  - 영화 검색 API를 이용하여 내가 보고 싶은 영화를 검색할 수 있다.
3. ⚠️ 오류
  - 오류가 발생하는 경우에는 사용자를 위한 오류 메시지를 띄워 준다.


### 📝 2단계 기능 목록
1. 📺 영화 상세 정보 조회
  - 영화 포스터 클릭시 상세 모달 노출
  - 줄거리가 긴 경우 스크롤로 확인할 수 있음
  - 모달은 배경 클릭, 닫기 버튼 클릭, esc키 클릭으로 닫을 수 있다.
  
2. ⭐️ 별점 매기기
  - 사용자가 모달을 닫을 때 localStorage에 별점을 저장하여 창을 닫았다 켜도 이전에 남긴 별점이 유지
  
3. 📐 UI/UX 개선하기
  - 더보기 버튼을 무한스크롤로 변경
  - mobile, tablet, desktop 반응형 화면 구성
  - 오류가 발생했을 때 모달 노출
  
  
### ✅ 프로그래밍 요구사항
- API key를 공개된 저장소에 포함하지 않는다.
- 비동기 통신에서 실패할 경우를 대비한다.
  - 비동기 통신에서 일어날 수 있는 다양한 상황을 고려해 본다.
- 비동기 호출을 포함한 사용자 기능 플로우를 선정하고 기능을 포함하여 E2E 테스트를 작성한다.
- 특정한 패턴에 사고를 끼워 맞추지 않고 단지 역할과 책임에 따라 관심사를 분리한다.
- 도메인 영역을 TypeScript를 사용해 구현한다. (UI 영역은 선택)
  - API에서 응답한 데이터의 규격을 문자열 그대로 활용하지 않고 도메인 객체를 만들어 활용한다.


### 💻 페어프로그래밍
|<img src="https://avatars.githubusercontent.com/u/55427367?v=4" width=150px> |<img src="https://avatars.githubusercontent.com/u/72205402?v=4" width=150px>|
|:---:|:---:|
|[타미](http://github.com/xodms0309)|[패트릭](http://github.com/GC-Park)|

### 🌲 파일 구조
```
📦src
 ┣ 📂assets
 ┃ ┣ 📜close.png
 ┃ ┣ 📜empty.png
 ┃ ┣ 📜logo.png
 ┃ ┣ 📜mobile_empty.jpeg
 ┃ ┣ 📜search_button.png
 ┃ ┣ 📜star_empty.png
 ┃ ┣ 📜star_filled.png
 ┃ ┗ 📜top_button.png
 ┣ 📂components
 ┃ ┣ 📂ErrorModal
 ┃ ┃ ┣ 📜index.css
 ┃ ┃ ┣ 📜index.html
 ┃ ┃ ┗ 📜index.ts
 ┃ ┣ 📂GotoTopButton
 ┃ ┃ ┣ 📜index.css
 ┃ ┃ ┣ 📜index.html
 ┃ ┃ ┗ 📜index.ts
 ┃ ┣ 📂Header
 ┃ ┃ ┣ 📜index.css
 ┃ ┃ ┣ 📜index.html
 ┃ ┃ ┗ 📜index.ts
 ┃ ┣ 📂MovieItem
 ┃ ┃ ┣ 📜index.css
 ┃ ┃ ┗ 📜index.ts
 ┃ ┣ 📂MovieList
 ┃ ┃ ┣ 📜index.css
 ┃ ┃ ┣ 📜index.html
 ┃ ┃ ┗ 📜index.ts
 ┃ ┣ 📂MovieModal
 ┃ ┃ ┣ 📜index.css
 ┃ ┃ ┣ 📜index.html
 ┃ ┃ ┗ 📜index.ts
 ┃ ┣ 📂SeeMoreButton
 ┃ ┃ ┣ 📜index.css
 ┃ ┃ ┣ 📜index.html
 ┃ ┃ ┗ 📜index.ts
 ┃ ┗ 📂Skeleton
 ┃ ┃ ┣ 📜index.css
 ┃ ┃ ┣ 📜index.html
 ┃ ┃ ┗ 📜index.ts
 ┣ 📂utils
 ┃ ┣ 📜dom.ts
 ┃ ┣ 📜infinityScroll.ts
 ┃ ┗ 📜request.ts
 ┣ 📜App.ts
 ┣ 📜Store.ts
 ┣ 📜fetch.ts
 ┣ 📜index.js
 ┣ 📜type.d.ts
 ┗ 📜types.ts
```


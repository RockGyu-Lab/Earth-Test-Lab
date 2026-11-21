# Earth Test Lab

**지구과학 World**(https://rockgyu-lab.github.io/Earth-Science-World/)에 넣기 전에 새 학습 자료를 만들고 시험하는 저장소입니다.
학생에게는 주소를 알리지 않으며, 모든 페이지에 `<meta name="robots" content="noindex">`를 넣어 검색 엔진에 실리지 않게 합니다.

- 시험용 사이트 주소: https://rockgyu-lab.github.io/Earth-Test-Lab/
- 정식 사이트 저장소: https://github.com/RockGyu-Lab/Earth-Science-World

## 폴더 구성
- `index.html`: 시험용 메인 화면 (시험 중인 자료 목록)
- `작업기록.md`: 날짜별 작업 기록과 남은 일 (사이트 화면에는 나오지 않음)
- `copyright.js`: 모든 페이지 오른쪽 아래의 저작권 표시. 정식 사이트의 같은 파일을 복사한 것으로, 페이지마다 `</body>` 바로 앞에 `<script src="./copyright.js"></script>`를 넣습니다.
- `elnino.html`: 엘니뇨와 라니냐(통합과학) (시험 중. 지구과학Ⅰ 수준은 나중에 따로 만들고 제목에 (지구과학)을 붙일 예정). 탭 '평상시'(전체 지도에서 적도 태평양을 잘라 확대 → 무역풍, 따뜻한 해수의 서쪽 이동, 용승, 햇빛에 의한 가열), '엘니뇨'(무역풍 약화 → 따뜻한 해수의 동쪽 이동 → 용승 약화 → 영향). 왼쪽 지도는 NOAA ERSST v5 실제 해수면 온도 자료(퍼블릭 도메인)를 HTML 안에 넣어 오프라인에서도 동작하고, 오른쪽 단면은 개념도입니다. '라니냐' 탭은 만들 예정.
- 자료는 들어갈 위치가 정해지지 않았으면 루트에 두고, 돌아가기 링크는 `./index.html`로 둡니다.
- 학습실 단위로 시험할 때는 정식 사이트와 같은 방식으로 만듭니다.
  ```
  <학습실폴더>/
    <학습실폴더>_index.html   학습실 메뉴
    자료.html                 탐구 자료
    lib/                      오프라인용 라이브러리와 데이터
  ```

## 페이지 연결
- 메인 화면 → 각 학습실 메뉴(`./<폴더>/<폴더>_index.html`)
- 학습실 메뉴 → 각 자료, 상단의 "← 지구과학 World"로 메인 화면 복귀(`../index.html`)
- 각 자료 → 상단의 "← [학습실 이름] 메뉴로 돌아가기"로 해당 학습실 메뉴 복귀

## GitHub Pages 게시
1. 저장소의 Settings → Pages로 이동합니다.
2. Build and deployment에서 `Deploy from a branch`를 선택합니다.
3. Branch는 `main`, 폴더는 `/(root)`로 선택하고 Save를 누릅니다.
4. 1~2분 뒤 위의 시험용 사이트 주소에서 확인합니다.

## 정식 사이트로 옮기기
1. 완성된 학습실 폴더를 정식 사이트 폴더(`EarthScienceWorld`)에 복사합니다.
2. 옮긴 페이지마다 `<meta name="robots" content="noindex">` 줄을 지웁니다.
3. 저작권 표시 경로를 옮긴 위치에 맞춥니다(학습실 폴더 안이면 `../copyright.js`).
4. 정식 사이트 `index.html`의 `subject-list`에 학습실 카드를 추가합니다.
5. 링크와 파일 이름의 대소문자를 점검하고, 정식 사이트의 `README.md`와 `CLAUDE.md`의 폴더 구조를 고칩니다.
6. 정식 사이트 저장소에 올립니다.

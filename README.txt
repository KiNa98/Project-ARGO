PROJECT ARGO NOTE — 공통 CSS 1차 적용

이번 묶음은 사이트 구조/데이터를 건드리지 않고,
공통 CSS 파일을 추가하고 각 화면이 그 파일을 읽도록 연결한 버전입니다.

GitHub에서 아래 파일을 그대로 덮어쓰기/추가하세요.

루트 교체:
- main.html
- archive.html
- lounge.html
- cards.html

신규 추가:
- css/common.css

현재 common.css에 들어간 공통 디자인:
- 밝은 하늘색 스크롤 손잡이
- 양 끝이 완전히 둥근 원통형
- 투명한 스크롤 트랙
- 마우스를 올리면 조금 더 밝아짐

중요:
- content/archive/*.json
- admin/config.yml
은 이번 작업에서 전혀 수정하지 않았으므로 건드릴 필요가 없습니다.

앞으로 공통 스크롤 디자인은 css/common.css만 수정하면 됩니다.
각 페이지의 기존 디자인은 아직 HTML 내부 <style>에 남겨두어,
이번 변경으로 레이아웃이 한꺼번에 깨질 가능성을 최소화했습니다.

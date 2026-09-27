Project ARGO NOTE — Decap CMS 전환 패키지
================================================

이 패키지는 기존 MAIN 구조를 건드리지 않고 다음 세 패널의 '내용'만 CMS로 분리합니다.

1) archive.html
   - 세계관
   - 설정
   - 인물
2) lounge.html
   - NEWS
   - SHORT STORY
3) cards.html
   - CARD DATABASE

추가되는 폴더
-------------
admin/
  index.html
  config.yml

content/
  archive/
    world.json
    settings.json
    personnel.json
  lounge/
    news.json
    stories.json
  cards/
    cards.json

images/
  uploads/
    (Decap CMS에서 업로드한 이미지가 들어갈 위치)

적용 방법
---------
1. 현재 GitHub 저장소를 백업합니다.
2. 이 패키지의 archive.html / lounge.html / cards.html을 저장소 루트에 덮어씁니다.
3. admin/, content/, images/uploads/ 폴더를 저장소 루트에 추가합니다.
4. main.html과 index.html은 현재 파일을 그대로 유지합니다.
5. GitHub Pages 반영 후 사이트 패널이 정상적으로 content/*.json을 읽는지 확인합니다.

CMS에서 할 수 있게 되는 것
--------------------------
ARCHIVE
- 세계관 배경/개념/집단 항목 추가·삭제·수정
- 설정 항목 추가·삭제·수정 + 이미지 업로드
- 인물 명부 추가·삭제·수정
- 대표 이미지, 스탠딩, 시트 업로드

LOUNGE
- NEWS 추가·삭제·수정 + 대표 이미지 업로드
- SHORT STORY 추가·삭제·수정 + 대표 이미지 업로드

CARDS
- 카드 추가·삭제·수정
- 분류 선택
- 대표 이미지 업로드
- 짧은 설명/상세 설명 수정

중요: 인증 연결
---------------
admin/index.html과 config.yml을 올리는 것만으로 관리 화면의 틀은 준비되지만,
실제로 /admin/에서 GitHub 저장소에 '게시'하려면 GitHub 인증 연결이 필요합니다.

현재 config.yml은 아래 저장소를 대상으로 합니다.
KiNa98/Project-ARGO / main

선택 가능한 인증 방식 예:
- Netlify를 인증 용도로만 사용
- Decap Turbo
- 별도 GitHub OAuth proxy

인증 연결은 다음 단계에서 설정하면 됩니다.

관리 주소
---------
GitHub Pages 배포 후:
https://kina98.github.io/Project-ARGO/admin/

이미지
------
Decap CMS 업로드 경로:
저장소: images/uploads/
사이트: /Project-ARGO/images/uploads/

주의
----
이 버전은 순수 HTML + JSON 구조입니다.
별도 정적 사이트 생성기(Astro/Jekyll 등)는 필요하지 않습니다.

PROJECT ARGO NOTE / 아카이브 5대 분류 안정화 세트

상단 분류
세계관 / 설정 / 지역 / 집단 / 인물

이번 버전의 핵심
- Decap CMS 3.15.1에서 문제를 일으킬 가능성이 있던 중첩 list/field 구조를 제거했습니다.
- 각 컬렉션은 최상위 items 목록 하나만 list widget으로 사용합니다.
- 상세 설명은 한 개의 text 필드로 만들고, 빈 줄을 기준으로 사이트에서 문단을 나눕니다.
- 인물 갤러리는 list 대신 상세 이미지 1~5의 고정 image 필드로 바꿨습니다.
- 인물 복장 역시 list 대신 복장 A/B/C의 고정 필드로 바꿨습니다.
- 아카이브 패널 크기를 크게 확대했습니다.
  기존보다 좌우가 넓고, 특히 높이는 최대 94vh까지 사용합니다.

업로드 / 교체할 파일

1. 저장소 루트
/archive.html
→ 기존 archive.html 전체 교체

2. content/archive 폴더
/content/archive/world.json
/content/archive/settings.json
/content/archive/regions.json
/content/archive/groups.json
/content/archive/personnel.json
→ 위 5개 파일 모두 이번 세트의 파일로 교체/추가

3. admin 폴더
/admin/config.yml
→ 기존 config.yml 전체 교체

즉 총 7개 파일입니다.

최종 구조

Project-ARGO/
├─ archive.html
├─ admin/
│  └─ config.yml
└─ content/
   └─ archive/
      ├─ world.json
      ├─ settings.json
      ├─ regions.json
      ├─ groups.json
      └─ personnel.json

중요
- archive.html은 위 5개 JSON 파일을 모두 읽습니다.
- 하나라도 파일이 빠지면 아카이브 전체가 '데이터를 불러오지 못했습니다'로 표시될 수 있습니다.
- 따라서 모바일에서 업로드할 때도 7개를 모두 올리는 것이 가장 안전합니다.
- backend는 기존에 사용하던 GitHub backend 설정
  (KiNa98/Project-ARGO / main / use_graphql)을 유지했습니다.
- 이미지 업로드 경로는 images/uploads 입니다.

Decap 관리자 사용법
- 세계관: 제목 + 설명
- 설정: 대표 이미지 + 제목 + 짧은 설명 + 상세 설명
- 지역: 대표 이미지 + 제목 + 짧은 설명 + 상세 설명
- 집단: 로고/상징 이미지 + 제목 + 짧은 설명 + 상세 설명
- 인물: 대표 이미지 + 상세 이미지 최대 5장 + 프로필

상세 설명에서 여러 문단을 만들고 싶으면 문단 사이에 빈 줄을 하나 넣으면 됩니다.

# 승강기 기능사 스터디 PWA

## 파일 구성
- index.html : 앱 본체 (선생님/학생 모드 자동 분기)
- manifest.json : PWA 설치 메타데이터
- sw.js : 서비스 워커 (오프라인 캐싱, data.json은 항상 최신 우선)
- data.json : **매일 교체할 콘텐츠 파일** (이것만 바꾸면 학생 앱 자동 갱신)
- icon-192.png / icon-512.png : 홈 화면 아이콘

## GitHub Pages 배포 (15분)
1. github.com 가입 후 New repository 생성 (이름 예: `elevator-study`, Public)
2. 위 5개 파일을 모두 업로드 → Commit
3. 저장소 Settings → Pages → Source: `main` / `/ (root)` 선택 → Save
4. 1~2분 후 `https://USERNAME.github.io/elevator-study/` 주소 발급

## 학생용 / 선생님용 주소
- 학생: `https://USERNAME.github.io/elevator-study/`
- 선생님: `https://USERNAME.github.io/elevator-study/?role=teacher`
  (?role=teacher 가 붙으면 '세션 편집'·'데이터' 탭이 보입니다)

## 핸드폰 설치
- 아이폰(Safari): 공유 버튼 → 홈 화면에 추가
- 안드로이드(Chrome): 메뉴(⋮) → 앱 설치

## 매일 운영 흐름 (선생님)
1. 스터디 종료 후 PC 또는 폰에서 선생님 URL 접속
2. '세션 편집' 탭 → 새 세션 추가 → 핵심정리·문제·정답·해설 입력 → 저장
3. '데이터' 탭 → 복사 또는 '파일로 저장' 클릭
4. GitHub 저장소의 data.json 파일을 열고 → Edit(연필) → 전체 교체 → Commit
5. 학생들은 앱을 다시 열기만 하면 최신 콘텐츠가 자동으로 반영됩니다.

## 모드별 권한
- 학생: 오늘 학습 / 동형문제 / 학습 기록 / 오답노트 (편집 불가)
- 선생님: 위 기능 + 세션 편집 + 데이터 내보내기/가져오기

## 데이터 저장 위치
- 콘텐츠(세션·문제): GitHub의 data.json (공용) + 선생님 로컬 편집본
- 풀이 이력: 각 학생 폰의 localStorage (개인별)

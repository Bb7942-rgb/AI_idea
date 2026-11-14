# 제출 진행 및 검증 보고서

기준 시각: 2026-11-14 13:52:50 KST

## 현재 상태

작업 브랜치는 `agent/pally/block-example`입니다. `timing/STARTED.md`와 `timing/READ_CONFIRM.md`가 있으며, B26·B36·B44의 `block_manifest.json`이 이 브랜치에 있습니다. 각 manifest는 공식 출처와 주소·좌표 대조 결과를 기록합니다.

세 블록의 `model_lod3.gltf`, `model_lod2.gltf`, `texture_atlas.webp`는 이 브랜치에서 확인되지 않았습니다. PR은 아직 만들지 않았고 병합하지 않았습니다.

## 시간 측정

- 읽기 시작: 2026-11-14T11:20:27.313+09:00
- 읽기 종료: 2026-11-14T11:26:49.381+09:00
- `read_min`: 6.37
- `READ_CONFIRM.md` 커밋: 2026-11-14T02:27:51Z (2026-11-14T11:27:51+09:00)
- 산출물 생성 후 현재 보고서 기록 시점까지의 경과: 145.00분. 아직 제출 PR이 없어 최종 제작 시간은 아님

## 검사 결과와 범위

이전 로컬 산출물 생성 단계에서 `python tools/check_example_block.py` 결과는 B26 36/36, B36 36/36, B44 36/36이었습니다. 당시 측정된 패키지 크기는 각각 437,546B, 448,736B, 465,339B입니다. 이 결과는 현재 GitHub 브랜치에 모델 파일이 올라가기 전에 준비 산출물에 실행한 결과이며, 저장소의 최종 파일 상태를 검증한 것으로 볼 수 없습니다. 모델 파일을 올린 뒤 각 블록에서 다시 실행해야 합니다.

`node tools/khronos_validate.mjs`는 아직 실행하지 못했습니다. 실행 환경에 `node`, `npm`, `npx`가 없었습니다. Khronos 검증 결과를 성공으로 기록하지 않습니다.

## 공식 출처 대조

- B26 대한성공회 부산주교좌성당: 국가유산포털과 부산 중구청은 소재지를 부산광역시 중구 대청로99번길 5-1로 안내합니다. 시험 제목의 동구 표기와 seed 좌표가 공식 소재지와 달라 manifest에 차이를 남겼습니다. https://www.heritage.go.kr/heri/cul/culSelectDetail.do?VdkVgwKey=79,05730000,21&pageNo=1_1_1_1
- B36 동구 국민체육문예센터: 운영기관은 지하1층·지상4층으로 안내합니다. 동구청의 2018-01-08 자료에는 지상5층 156.20㎡의 설비가 기록되어 있어 차이를 적었습니다. 모델 설명치수는 실측 도면에서 얻은 값이 아닙니다. https://www.bsdgsportsart.or.kr/www/11 https://www.bsdonggu.go.kr/board/view.donggu?boardId=BBS_0000202&dataSid=5001746&menuCd=DOM_000000104008001001&paging=ok&startPage=1
- B44 초량이바구 작은도서관: 동구청과 문화체육관광부 자료는 초량중로 113의 이바구복합문화체육센터 2층으로 안내합니다. 센터 전체를 모델 대상으로 기록했으며, 센터 안내는 지하1층·지상9층입니다. https://www.bsdonggu.go.kr/board/list.donggu?boardId=BBS_0000200&contentsSid=1776&menuCd=DOM_000000801004001000 https://www.bsdonggu.go.kr/ebagu/index.donggu?menuCd=DOM_000004001003000000 https://www.mcst.go.kr/slibrary/library/detail/2410280003
- 좌표 데이터 출처: 부산광역시 도로명주소 정보 데이터셋 및 읽어 둔 데이터 행. https://www.data.go.kr/data/15028854/fileData.do

## 남은 작업과 차단 사항

모델 파일 및 렌더 캡처 업로드, 최종 브랜치 검증, Khronos 검증, 제작 종료 시간 기록, PR 생성이 남았습니다. GitHub 웹 업로드 페이지는 현재 브라우저에서 로그아웃 상태이며, push 권한이 있는 GitHub 웹 계정 로그인을 요구합니다. 브라우저용 저장 로그인이 없어서 파일 업로드를 진행하지 않았습니다. 공개 저장소의 대상 경로 외에는 수정하지 않았습니다.

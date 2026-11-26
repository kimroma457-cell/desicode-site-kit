# 데시코드 실내건축 현장관리 키트 (desicode-site-kit)

현장소장·공무가 매주 반복하는 서류 업무를 Claude가 현장 실무 방식 그대로 처리합니다.
**자료에 없는 숫자는 만들지 않습니다.** 모르는 값은 빈칸과 `[확인 필요]`로 남깁니다.

## 들어 있는 기능

| 기능 | 이렇게 말하세요 | 결과물 |
|------|----------------|--------|
| 현장 등록 | "새 현장 등록해줘" | 현장정보 파일, 현장 폴더 구조 |
| 공사일보 | "오늘 공사일보 써줘" + 메모 | 작업내용·출력인원·자재반입 일보 |
| 주간보고 | "이번 주 주간보고서 써줘" | 발주처·감리용 주간 진행 보고서 |
| 자재승인서 | "자재승인서 서류 점검해줘" | 자재별 점검표, 보완 요청 목록, 승인요청서 표지 |
| 도면·내역 대조 | "도면이랑 내역서 대조해줘" | 누락·수량·사양·간섭 이슈표, 질의서(RFI) |
| 견적·원가 | "단가표 기준으로 견적서 계산해줘" | 단가표 근거가 적힌 .xlsx 견적서 |
| 현장 메일 | "현장 메일 정리해줘" | 답할 것/기다릴 것 분류, 답장·독촉 초안 |
| 서류 정리 | "현장 폴더 정리해줘" | 폴더·파일명 정리 (원본 삭제 없음, 되돌리기 기록) |

## 시작하기
1. "새 현장 등록해줘" — 현장명·발주처·감리·담당자를 한 번만 입력하면 다른 기능이 그 정보를 씁니다.
2. 견적 기능을 쓰려면 회사 **단가표**와 **공사유형별 비율표**를 준비하세요. 빈 양식이 들어 있습니다.
3. 메일 기능은 메일 커넥터(Gmail 등)를 연결하면 자동으로, 아니면 메일을 붙여넣어 쓰면 됩니다.

## 안전 원칙
- 메일은 보내지 않고 초안만 만듭니다.
- 파일은 지우지 않고, 옮기기 전에 계획표를 보여주고 확인받습니다.
- 방염·불연·법규 대상 여부는 판단하지 않고 감리·설계 확인 항목으로 표시합니다.
- 단가·인원·수량·날짜를 추정하지 않습니다.

## 데이터 처리
- 이 플러그인에는 별도 서버·외부 전송 코드가 없습니다. 실행되는 스크립트도 없으며, 모든 기능은 Claude에게 주는 작업 지침(스킬)입니다.
- 파일은 사용자가 연결하거나 첨부한 현장 폴더·문서만 읽고, 결과는 같은 폴더나 대화에 남깁니다.
- 메일 기능은 사용자가 직접 연결한 메일 커넥터(Gmail 등)로만 메일을 읽고, 답장은 임시보관함 초안으로만 만듭니다. 발송·삭제는 하지 않습니다.
- 현장정보 파일(현장명·담당자 등)은 사용자의 작업 폴더에만 저장됩니다.

## English summary
Desicode Site Kit is a Korean-language toolkit for interior construction site managers. It helps Claude prepare material submittals, cross-check drawings against bills of quantities and draft RFIs, write daily site logs and weekly progress reports, calculate estimates strictly from the user's own unit-price sheet, triage site email into drafts only, and organize site document folders without deleting anything. It never invents prices, quantities or dates: missing values stay blank and are flagged for confirmation. The plugin contains only skills and templates; it runs no code and sends no data anywhere beyond the connectors the user chooses to connect.

## 라이선스
MIT

## 버전
0.1.0 — 첫 버전

제작: 데시코드 (Desicode)

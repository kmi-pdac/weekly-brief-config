# weekly-brief-config

국제 항만동향 주간브리프 후보수집용 키워드 설정 저장소입니다.

## 관리 파일

`watch_keywords.json` 한 파일에서 다음 항목을 관리합니다.

- `groups`: 주제별 검색어. 각 주제의 `category`는 이름, `queries`는 검색어 목록입니다.
- `media_sources.sites`: 주요 매체. `name`은 매체명, `domain`은 웹사이트 도메인입니다.
- `publications.queries`: 정기 간행물과 경제·교역 보고서의 발간 소식을 찾는 검색어입니다.

## 키워드 추가와 수정

1. 이 저장소의 `watch_keywords.json`을 엽니다.
2. Edit this file을 누르고 검색어를 추가하거나 수정합니다. 새 주제는 기존 항목과 같은 구조로 추가합니다.
3. Commit changes로 저장합니다.
4. 연결된 주간브리프 수집기는 다음 실행 때 최신 설정을 읽습니다. GitHub 접속이나 설정 형식에 문제가 있으면 기존 로컬 설정을 사용합니다.

검색어는 문자열로 쓰고 JSON의 쉼표와 따옴표를 유지합니다. 새 주제 예시는 다음과 같습니다.

```json
{
  "category": "세계 물가",
  "queries": ["OECD consumer prices", "US PCE inflation", "euro area inflation"]
}
```

## 공개 범위와 메일

이 저장소는 기존 hangsan-brief-config와 같이 공개 검색 설정을 관리합니다. 계정정보, 메일 비밀번호, 내부 원문은 올리지 않습니다.

여기에는 자동메일 스케줄이나 발송용 비밀값이 없습니다. 키워드 편집과 메일 실행은 별도이며, 이 저장소 생성만으로 메일이 발송되지는 않습니다. 연결된 수집기 코드를 사용하는 메일 실행도 같은 설정을 읽습니다.

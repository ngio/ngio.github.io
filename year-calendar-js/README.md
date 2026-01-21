# NeatoCal (니토캘)

한 페이지에 1년 전체를 보여주는 멋진 달력입니다.

이 프로젝트는 [Neatnik's Calendar](https://neatnik.net/dispenser/?project=calendar)에서 영감을 받은 [NeatoCal](https://github.com/abetusk/neatocal) 프로젝트의 한국 현지화 버전입니다.

추가 파라미터(아래 참조)가 포함된 JavaScript 포팅 버전이며, 모든 파일이 로컬에 있어 "의존성 없이" 설계되었습니다.

[라이브 데모](https://dev-huiya.github.io/year-calendar-js/)를 확인해보세요.

## 스크린샷

![기본](img/neatocal_default.png)

![정렬](img/neatocal_align.png)

## 파라미터

| URL 파라미터      | 설명                                                                                                                                        | 예시                                                                                                                            |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| `year`            | 연도 변경 (기본값: 현재 연도)                                                                                                               | [...?year=2030](https://dev-huiya.github.io/year-calendar-js?year=2030)                                                         |
| `start_month`     | 1월이 아닌 다른 월에서 시작. 0부터 시작 (`0`=1월, `1`=2월, ...).                                                                            | [...?start_month=7](https://dev-huiya.github.io/year-calendar-js?start_month=7)                                                 |
| `n_month`         | 12개월이 아닌 다른 개수로 변경 (기본값 `12`).                                                                                               | [...?n_month=6](https://dev-huiya.github.io/year-calendar-js?n_month=6)                                                         |
| `layout`          | 달력 레이아웃 변경. `default` 또는 `aligned-weekdays`.                                                                                      | [...?layout=aligned-weekdays](https://dev-huiya.github.io/year-calendar-js?layout=aligned-weekdays)                             |
| `start_day`       | 월요일이 아닌 다른 요일에서 시작. 0부터 시작 (`0`=일, `1`=월, ...). `aligned-weekdays` 레이아웃에서만 유효                                  | [...?layout=aligned-weekdays&start_day=0](https://dev-huiya.github.io/year-calendar-js?layout=aligned-weekdays&start_day=0)     |
| `highlight_color` | 주말 강조 색상 변경 (기본값 `eee`)                                                                                                          | [...?highlight_color=fee](https://dev-huiya.github.io/year-calendar-js?highlight_color=fee)                                     |
| `language`        | 월과 요일 코드의 언어 변경. `month_code` 또는 `weekday_code`가 지정되면 해당 값이 우선 적용됨.                                              | [...?language=ko-KR](https://dev-huiya.github.io/year-calendar-js?language=ko-KR)                                               |
| `weekday_code`    | 사용할 요일 코드의 쉼표 구분 목록 (기본값 `일,월,화,수,목,금,토`). 요일 코드가 필요 없으면 요소를 비워둘 수 있음.                           | [...?weekday_code=일,월,화,수,목,금,토](https://dev-huiya.github.io/year-calendar-js?weekday_code=일,월,화,수,목,금,토)         |
| `month_code`      | 사용할 월 코드의 쉼표 구분 목록 (기본값 `1월,2월,3월,4월,5월,6월,7월,8월,9월,10월,11월,12월`). 월 코드가 필요 없으면 요소를 비워둘 수 있음. | [...?month_code=1,2,3,4,5,6,7,8,9,10,11,12](https://dev-huiya.github.io/year-calendar-js?month_code=1,2,3,4,5,6,7,8,9,10,11,12) |
| `cell_height`     | 셀 높이를 변경하는 CSS 파라미터.                                                                                                            | [...?cell_height=1.5em](https://dev-huiya.github.io/year-calendar-js?cell_height=1.5em)                                         |
| `data`            | JSON 데이터 파일 위치.                                                                                                                      | [...?data=example/data.json](https://dev-huiya.github.io/year-calendar-js?data=example/data.json)                               |
| `help`            | 도움말 화면 표시                                                                                                                            | [...?help](https://dev-huiya.github.io/year-calendar-js?help)                                                                   |

## 프리셋

위의 파라미터 목록은 다양한 표시 옵션을 제공할 만큼 다재다능합니다. 아래는 유용할 수 있는 프리셋의 간략한 목록입니다.

| 프리셋                                                                                                                                                                                                                                                                                     | 설명                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| [컬러 및 정렬](https://dev-huiya.github.io/year-calendar-js?layout=aligned-weekdays&highlight_color=fee)                                                                                                                                                                                   | 정렬된 요일과 빨간색 주말 강조가 있는 달력                                                          |
| [학사 일정](https://dev-huiya.github.io/year-calendar-js?start_month=7)                                                                                                                                                                                                                    | 9월에 시작하여 다음 해 8월까지 이어지는 "학사 일정"                                                 |
| 반 페이지 [왼쪽](https://dev-huiya.github.io/year-calendar-js?n_month=6) 및 [오른쪽](https://dev-huiya.github.io/year-calendar-js?start_month=6&n_month=6) 달력                                                                                                                            | 두 개의 반 페이지 (6개월) 달력                                                                      |
| [강조 없는 달력](https://dev-huiya.github.io/year-calendar-js?highlight_color=fff)                                                                                                                                                                                                         | 주말 강조가 없는 달력                                                                               |
| [중국어 월/요일](https://abetusk.github.io/neatocal/?month_code=1%E6%9C%88,2%E6%9C%88,3%E6%9C%88,4%E6%9C%88,5%E6%9C%88,6%E6%9C%88,7%E6%9C%88,8%E6%9C%88,9%E6%9C%88,10%E6%9C%88,11%E6%9C%88,12%E6%9C%88&weekday_code=%E6%97%A5,%E4%B8%80,%E4%BA%8C,%E4%B8%89,%E5%9B%9B,%E4%BA%94,%E5%85%AD) | (간체) 중국어 월 및 요일 약어가 있는 달력 ([myway42](https://github.com/myway42/calendar) 제공)     |
| [독일어 월/요일](https://abetusk.github.io/neatocal/?weekday_code=S,M,D,M,D,F,S&month_code=Jan,Feb,M%C3%A4r,Apr,Mai,Jun,Jul,Aug,Sep,Okt,Nov,Dez)                                                                                                                                           | 독일어 월 및 요일 약어가 있는 달력 ([moontear](https://news.ycombinator.com/user?id=moontear) 제공) |
| [터키어 월/요일](https://abetusk.github.io/neatocal/?year=2026&month_code=Oca,%C5%9Eub,Mar,N%C4%B0s,May,Haz,Tem,A%C4%9Fu,Eyl,Ek%C4%B0,Kas,Ara&weekday_code=Pz,Pt,S,%C3%87,Pe,Cu,Ct)                                                                                                        | 터키어 월 및 요일 약어가 있는 달력                                                                  |
| [2년 달력](https://dev-huiya.github.io/year-calendar-js?n_month=24&layout=aligned-weekdays&start_day=0)                                                                                                                                                                                    | 한 페이지에 2년을 표시하는 달력                                                                     |

## 데이터 파일

파라미터나 날짜 셀에 텍스트를 제공하는 데 사용할 수 있는 데이터 파일 옵션이 있습니다.

형식은 다음과 같습니다:

```
{
  "param" {
    ...
    "color_cell" : [
      { "date":"YYYY-MM-DD", "color":"#rgb" },
      ...
      { "date":"YYYY-MM-DD", "color":"#rgb" }
    ]
  },
  "YYYY-MM-DD" : "텍스트",
  ...
  "YYYY-MM-DD" : "텍스트"
}
```

[example/data.json](example/data.json) 파일이 예시를 제공합니다:

```
{
  "param": {
    "year":2030,
    "layout":"aligned-weekdays",
    "cell_height": "2em"
  },
  "2030-03-21" : "The quick brown fox jumps over the lazy yellow dog",
  "2030-01-30" : "Sphynx of black quartz, judge my vow",
  "2030-06-01" : "Thule Worm-God of the Lords",
  "2030-08-11" : "Swarms Matriarch",
  "2030-10-20" : "Higher Dimension Being"
}
```

`"param" : {}` 섹션에서 허용되는 파라미터는 URL 파라미터와 동일한 이름을 가집니다.
데이터 파일에 파라미터가 지정되면 URL에 제공된 파라미터를 덮어씁니다.

`color_cell`은 개별 셀 강조를 허용합니다 ([예시](https://dev-huiya.github.io/year-calendar-js?data=example/sched.json)).
`color_cell` 배열이 있는 예시 데이터 파일은 [example/sched.json](example/sched.json)을 참조하세요.

### 한국 공휴일 파일

한국 공휴일이 포함된 데이터 파일이 제공됩니다. 각 공휴일은 유형에 따라 다른 색상으로 표시됩니다:

- **명절 (설날, 추석)**: 빨간색 계열 (`#ff9999`, `#ffcccc`)
- **국경일 (3ㆍ1절, 광복절, 개천절, 한글날)**: 파란색 계열 (`#cce5ff`)
- **기타 공휴일 (어린이날, 부처님 오신 날)**: 노란색 계열 (`#fff4cc`)
- **선거일**: 보라색 계열 (`#e6ccff`)
- **대체공휴일**: 회색 (`#f0f0f0`)

사용 가능한 파일:

- [example/holiday_2026_kr.json](example/holiday_2026_kr.json) - 2026년 한국 공휴일
- [example/holiday_2027_kr.json](example/holiday_2027_kr.json) - 2027년 한국 공휴일

사용 예시:

- [2026년 공휴일 달력](https://dev-huiya.github.io/year-calendar-js?year=2026&data=example/holiday_2026_kr.json)
- [2027년 공휴일 달력](https://dev-huiya.github.io/year-calendar-js?year=2027&data=example/holiday_2027_kr.json)

파일이 없거나 파싱할 수 없는 경우, 데이터 파일이 없는 것처럼 렌더링이 계속됩니다.

## 기타

Neatnik의 원본 저장소는 [이곳으로 이동](https://neatnik.net/dispenser/?project=calendar)했지만, 레거시 GitHub 저장소는 [여기](https://neatnik.net/dispenser/?project=calendar)에서 찾을 수 있습니다.

## 라이선스

MIT

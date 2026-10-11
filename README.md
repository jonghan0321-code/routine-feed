# routine-feed

"나의 루틴" 앱의 **오늘의 추천 아티클** 보관함입니다.

- 매일 아침 Claude 클라우드 예약 작업이 넥슨 데이터 분석 면접 준비에 도움이 되는 글을 1개 골라 `feed.json`을 갱신합니다.
- 앱은 `https://raw.githubusercontent.com/jonghan0321-code/routine-feed/main/feed.json`을 읽습니다.

## feed.json 구조

```json
{
  "updated": "2026-10-12",
  "today": {
    "date": "2026-10-12",
    "title": "글 제목",
    "url": "https://...",
    "source": "출처 · 연도",
    "summary": ["요약 1", "요약 2", "요약 3"],
    "why": "면접에서 이 글을 어떻게 쓸 수 있는지 한 문장",
    "questions": [{ "q": "예상 질문", "tails": ["꼬리질문 1", "꼬리질문 2"] }]
  },
  "history": [{ "date": "...", "title": "...", "url": "..." }],
  "already_in_app": ["앱 기본 목록에 이미 있는 URL들 (중복 추천 금지)"]
}
```

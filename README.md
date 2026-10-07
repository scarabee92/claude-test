# 🔨 두더지 잡기

브라우저에서 바로 즐기는 웹 두더지 잡기 게임입니다. 단일 HTML 파일(`mole.html`)로 되어 있어 설치나 서버 없이 실행됩니다.

## 실행 방법

1. 이 저장소를 내려받습니다.
   ```bash
   git clone https://github.com/scarabee92/claude-test.git
   ```
2. `mole.html` 파일을 브라우저로 엽니다. (더블클릭)
3. **시작** 버튼을 누르면 게임이 시작됩니다.

## 게임 규칙

- 3×3 구멍에서 두더지가 튀어나옵니다.
- 두더지를 클릭(또는 터치)하면 1점입니다.
- 제한 시간은 30초입니다.
- 점수가 오를수록 두더지가 더 빨리 나오고 더 짧게 머뭅니다.
- 최고 점수는 브라우저(localStorage)에 저장됩니다.

## 파일 구성

| 파일 | 설명 |
|---|---|
| `mole.html` | 두더지 게임 본체 (HTML + CSS + JavaScript) |
| `CLAUDE.md` | Claude Code용 프로젝트 지침 |
| `.claude/` | Claude Code 설정과 세션 기록 훅 |

## 조정하기

`mole.html`의 스크립트에서 숫자만 바꾸면 됩니다.

- 제한 시간: `time=30`
- 구멍 개수: `for(let i=0;i<9;i++)` (그리드 열 수는 CSS의 `repeat(3,110px)`)
- 난이도: `pop()` 안의 `Math.max(350,900-score*15)`(머무는 시간), `Math.max(250,800-score*12)`(등장 간격)

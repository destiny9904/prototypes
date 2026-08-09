# 미니 게임 아케이드

순수 HTML / CSS / JavaScript(Canvas)로 만든 4가지 브라우저 게임입니다. 빌드 과정이나 별도 서버가 필요 없어 GitHub Pages로 바로 배포할 수 있습니다.

## 포함된 게임

| 게임 | 경로 | 설명 |
|---|---|---|
| 🚗 오픈월드 드라이빙 | `games/driving/index.html` | 넓은 맵을 달리며 체크포인트를 모으는 탑다운 드라이빙 |
| ⚾ 타격 연습 야구 | `games/baseball/index.html` | 타이밍 맞춰 스윙하는 배팅 미니게임 |
| ⚽ 1인 축구 매치 | `games/soccer/index.html` | AI 수비수·골키퍼를 상대로 골을 넣는 60초 매치 |
| 🗡️ 미니 RPG 모험 | `games/rpg/index.html` | 필드 탐험 + 랜덤 인카운터 턴제 전투, 레벨업 |

`index.html`이 허브 페이지로, 여기서 4개 게임으로 이동할 수 있습니다.

## 로컬에서 확인하기

별도 설치 없이 `index.html`을 브라우저로 열면 바로 실행됩니다. (파일을 더블클릭해도 되고, 아래처럼 로컬 서버로 열어도 됩니다.)

```bash
python3 -m http.server 8080
# 이후 브라우저에서 http://localhost:8080 접속
```

## GitHub에 올리고 Pages로 배포하기

1. GitHub에서 새 저장소를 만듭니다 (예: `mini-game-arcade`).
2. 이 폴더에서 아래 명령을 순서대로 실행합니다.

```bash
git init
git add .
git commit -m "Initial commit: mini game arcade"
git branch -M main
git remote add origin https://github.com/<사용자명>/<저장소명>.git
git push -u origin main
```

3. GitHub 저장소 페이지에서 **Settings → Pages**로 이동합니다.
4. **Source**를 `Deploy from a branch`로 선택하고, Branch를 `main` / `/ (root)`로 설정한 뒤 **Save**를 누릅니다.
5. 잠시 후 `https://<사용자명>.github.io/<저장소명>/` 주소에서 사이트가 열립니다.

이후 코드를 수정하고 `git add . && git commit -m "..." && git push`만 하면 자동으로 사이트가 갱신됩니다.

## 폴더 구조

```
.
├── index.html              # 허브 페이지 (게임 선택 화면)
├── games/
│   ├── driving/index.html
│   ├── baseball/index.html
│   ├── soccer/index.html
│   └── rpg/index.html
└── README.md
```

## 조작법 요약

- **드라이빙**: 방향키/WASD로 가속·조향, 체크포인트를 모아 점수 획득
- **야구**: 스페이스바(또는 SWING 버튼)로 스윙, 타이밍이 좋을수록 장타
- **축구**: 방향키/WASD로 이동, 스페이스바로 슛/패스
- **RPG**: 방향키/WASD로 이동, 몬스터를 만나면 자동으로 전투 화면 전환

## 참고

각 게임은 학습·프로토타입 목적의 가벼운 버전으로, 필요에 따라 난이도·그래픽·규칙을 자유롭게 수정해 확장할 수 있습니다.

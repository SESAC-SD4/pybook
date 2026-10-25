# Python 기본서

수업에서 같이 채워 가는 Python 노트북입니다.

| 폴더 | 무엇 |
| --- | --- |
| `lessons/` | 수업 노트북 — 설명이 적혀 있고 코드 칸은 비어 있습니다. 수업에서 같이 채웁니다 |
| `exercises/` | 연습 노트북 — 혼자 푸는 문제. 문제마다 확인 칸이 있어 풀었는지 바로 압니다 |
| `me/` | 내가 채우는 노트북. 이 폴더 안의 노트북은 git에 올라가지 않습니다 |

Claude Code는 **수업 노트북(`lessons/`)에서 함께** 씁니다 — 질문하기 · AI 코드 읽기. **연습 노트북(`exercises/`)은 혼자** 풉니다.

`lessons/` · `exercises/`의 원본은 **고치지 않습니다.** 고치면 다음 `git pull`에서 충돌합니다.

이 저장소에서는 `uv add`를 하지 않습니다. 필요한 라이브러리는 장을 받을 때 함께 들어 있습니다. `git pull` 뒤 `uv sync`를 한 번 실행합니다.

## 처음 한 번

```
git clone https://github.com/SESAC-SD4/pybook.git
cd pybook
uv sync
```

`uv sync`는 이 폴더에 `.venv`를 만들고 노트북을 여는 JupyterLab과 칸을 실행하는 `ipykernel`을 설치합니다.

## 매일 수업 전에

```
git pull
uv sync
cp lessons/01_values.ipynb me/lessons/
cp exercises/01_values.ipynb me/exercises/
```

`01_values` 자리에 그날 장의 파일 이름을 넣습니다. 연습 노트북이 없는 장(00)은 수업 노트북만 복사합니다. **이미 채운 장을 다시 복사하면 덮어써서 채운 내용이 사라집니다.** 그날 장만 복사합니다.

## 노트북 열기

`pybook` 폴더에서 실행합니다. 끝의 `me`는 **`me/` 폴더를 열라**는 뜻입니다.

```
uv run jupyter lab me
```

1. 브라우저에 JupyterLab이 열립니다. 이 터미널은 수업이 끝날 때까지 **닫지 않습니다**
2. 왼쪽 파일 목록에는 `me/` 안의 `lessons` · `exercises`만 보입니다. `lessons` → 그날 장의 노트북을 엽니다
3. 오른쪽 위에 `Python 3 (ipykernel)`이 보이면 이 폴더의 `.venv`로 실행됩니다. 따로 고를 것은 없습니다
4. 위에서부터 칸을 채우며 실행합니다
5. 연습은 `me/exercises/`의 같은 이름 노트북에서 혼자 풉니다

끝낼 때는 **File → Shut Down**을 누르거나, 터미널에서 Control-C를 두 번 누릅니다.

같은 노트북을 JupyterLab과 다른 편집기(VS Code 등)에서 동시에 열지 않습니다. 한쪽이 저장한 내용을 다른 쪽이 덮어쓸 수 있습니다.

Claude Code는 새 터미널을 하나 더 열어 이 폴더(`pybook`)에서 시작합니다. 이 폴더의 `CLAUDE.md`에 적힌 방식으로 답합니다.

## 장 목록

| 장 | 수업 노트북 | 연습 노트북 |
| --- | --- | --- |
| 00 노트북 시작하기 | `lessons/00_start.ipynb` | 없음 |
| 01 값과 변수 | `lessons/01_values.ipynb` | `exercises/01_values.ipynb` |
| 02 조건과 반복 | `lessons/02_flow.ipynb` | `exercises/02_flow.ipynb` |
| 03 자료구조 | `lessons/03_collections.ipynb` | `exercises/03_collections.ipynb` |

# Python 기본서

수업에서 같이 채워 가는 Python 노트북입니다.

| 폴더 | 무엇 |
| --- | --- |
| `lessons/` | 수업에서 같이 채우는 노트북 |
| `exercises/` | 혼자 푸는 연습 노트북 |
| `me/` | 내가 채우는 노트북. 이 폴더 안의 노트북은 git에 올라가지 않습니다 |
| `answers/` | 수업 뒤에 올라오는 강사 노트북과 연습 정답 |

Claude Code는 수업 노트북에서 씁니다. 연습 노트북은 혼자 풉니다. 연습 노트북 끝의 **만들어 보기**는 Claude Code와 함께 합니다.

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
| 04 함수 | `lessons/04_functions.ipynb` | `exercises/04_functions.ipynb` |
| 05 모듈과 패키지 | `lessons/05_modules.ipynb` | `exercises/05_modules.ipynb` |
| 06 클래스 | `lessons/06_classes.ipynb` | `exercises/06_classes.ipynb` |
| 07 예외 처리 | `lessons/07_errors.ipynb` | `exercises/07_errors.ipynb` |
| 08 파일 다루기 | `lessons/08_files.ipynb` | `exercises/08_files.ipynb` |
| 09 제너레이터와 데코레이터 | `lessons/09_generators.ipynb` | `exercises/09_generators.ipynb` |
| 10 requests로 데이터 가져오기 | `lessons/10_requests.ipynb` | 없음 (수업 노트북 5 · 6절을 혼자 풉니다) |
| 11 pandas로 데이터 다루기 | `lessons/11_pandas.ipynb` | `exercises/11_pandas.ipynb` |
| 12 비동기 | `lessons/12_async.ipynb` | `exercises/12_async.ipynb` |

# Pong -> Pac-Man (C언어 팩맨 게임)

NAMCO의 1980년작 **PAC-MAN**을 C언어로 재구현한 프로젝트입니다.  
Console 창에서 `ncurses` (PDCurses) 라이브러리와 Windows API를 사용하여 클래식 아케이드의 재미를 그대로 구현했습니다.

![Pac-Man](https://media.cnn.com/api/v1/images/stellar/prod/200518114838-05-pac-man-40.jpg?q=w_1600,h_2136,x_0,y_0,c_fill/w_1280)

## 📌 주요 기능 (Features)

이 프로젝트는 단순한 이동을 넘어 다양한 게임 요소를 포함하고 있습니다.

*   **3가지 난이도 시스템**:
    *   **Easy**: 적들이 단순하게 이동합니다.
    *   **Normal**: 적들이 조금 더 지능적으로 움직입니다.
    *   **Hard**: 적들이 **BFS(너비 우선 탐색) 알고리즘**을 사용하여 플레이어를 추적합니다.
*   **아이템 시스템 (Power Pellet)**: 아이템을 획득하면 일정 시간 동안 적을 공격할 수 있는 상태가 됩니다.
*   **랭킹 시스템**: 상위 10명의 점수를 기록하고 보여줍니다 (`rank.bin`, `rank.c`).
*   **맵 로딩**: 파일로부터 맵 데이터를 읽어와 게임을 구성합니다 (`orig_map.txt`, `read_map.c`).

## 🛠 기술 스택 (Tech Stack)

*   **Language**: C
*   **Environment**: Windows Console
*   **Libraries**:
    *   `windows.h`: 윈도우 콘솔 제어 및 시스템 함수 사용
    *   `time.h`: 난수 생성 및 시간 측정
    *   `cursor.h` / `curses.h`: 콘솔 UI 및 커서 제어 (PDCurses 활용 추정)

## 🚀 실행 방법 (How to Run)

1.  **Visual Studio** 설치가 필요합니다.
2.  `Pong/Pong.sln` 솔루션 파일을 엽니다.
3.  프로젝트를 **Build** (빌드) 합니다.
4.  **Debug** 또는 **Release** 모드로 실행하면 게임이 시작됩니다.

## 🎮 조작 방법 (Controls)

*   **이동**: 키보드 방향키 (↑, ↓, ←, →)
*   **선택**: Enter

## 📂 프로젝트 구조

*   `main.c`: 게임의 진입점 및 메인 루프
*   `Enemy.c`: 적의 움직임 (Easy, Normal, BFS 알고리즘) 구현
*   `player.c`: 플레이어의 움직임 및 충돌 로직
*   `item.c`: 점수 계산 및 아이템 효과 처리
*   `rank.c`: 랭킹 정보 저장 및 불러오기
*   `read_map.c`: 맵 파일 파싱 및 초기화
*   `pictur.c`: 게임 화면 UI 드로잉

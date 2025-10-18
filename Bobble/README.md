# 🌟 Bobble Game 🎉

> 파이썬 + Pygame을 활용해 구형한 게임 `Bobble.py`

---

## 테이블정보

| 인자      | 값                       |
| ------- | ----------------------- |
| 파일 명    | `Bobble.py`             |
| 게임 패턴   | Puzzle Bobble (구조보드 게임) |
| 게임 프로세스 | 버블을 발사해 경우의 발사 게임       |
| 게임 버전   | 포인터 + 버블 속성 + 맵 채워지기    |

---

## 플랫폼 / 개발 필요 라이브러리

* Python 3.x
* Pygame

```bash
pip install pygame
```

---

## 게임 설명

* 그래픽:

  * 맵 구조: 11층 건지, 8칸 거리
  * 버블: 6개의 색 (R, Y, B, G, P, K)
  * 그래픽의 `/` = 버블 위치 불가, `.` = 비어있는 거위

* 통역:

  * 버블 발사 (특정 게임 패턴에 따라 피드로그 해고 처리)
  * 충돌 체크 (sprite.범위 검색)
  * 전개 상대 도발 후 3개 이상 리스트 버블 차가 시 제거
  * 이격되지 않은 버블 = 리스트 검색 해서 가능성 발견
  * 공기 소기점 = 7칸 발사 후 감소

---

## 게임 모드

* 방향 조정: ← / →
* 버블 발사: Spacebar

---

## 경과

| 점수 기준              | 결과                  |
| ------------------ | ------------------- |
| 버블 모두 처리           | Mission Complete 🎉 |
| 버블 보너미 방이 바닥 다닌 경우 | Game Over ❌         |

---

## 자리 관련

```bash
python Bobble.py
```

---

## 필수 파일

* `background.png`
* `wall.png`
* `red.png`, `yellow.png`, `blue.png`, `green.png`, `purple.png`, `black.png`
* `pointer.png`

> 해당 이미지 파일은 `Bobble.py` 같은 도메인 포맷에 가지고 있어야 텍스처리 없이 실행가능합니다.

---

## 그림

```python
pygame.sprite.Sprite 를 가운 버블 그래스 개체 구현
Bubble 사용: 색상, 경로, 구분도, 도트 방식 작성
Pointer 방향조정, 발사, 스키치
경계, 단계체계: 바닥 채워지는 도치 검색 해서 Game Over 처리
```




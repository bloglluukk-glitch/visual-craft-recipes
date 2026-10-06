# 출처와 주장 범위

**한국어** | [English](SOURCES.en.md)

확인일: 2026-10-06. 외부 자료는 기술적 배경을 확인하는 링크로 제공하며 본문·사진을 재배포하지 않는다.

## 이 묶음이 만들어진 과정

제작자 bloglluukk-glitch의 Visual Craft 지식에서 조명, 재질, 카메라 움직임, 프롬프트 구성 주제를 선별했다. Codex가 공개용으로 재작성하고 실험 입력·검수표를 작성하고, 내장 이미지 생성 기능으로 가상 제품 및 설명 이미지를 만들었다.

기존 지식은 AI의 제작·검수 도움을 받아 정리한 자료다. 널리 알려진 광학·촬영 원리를 제작자의 독자적인 발명이라고 주장하지 않는다. 첨부 이미지는 AI로 생성한 가상 제품·설명용 자산이며 동일 조건 레시피 비교 결과는 아니다. 이미지별 실제 생성 프롬프트와 참고 관계는 `assets/GENERATION_RECORD.json`에 기록한다.

이 묶음의 기여는 문제를 나누는 방식, 보존 우선순위, 비교 입력과 실패 후 수정 순서를 함께 제공하는 것이다.

## 외부 배경 자료

| ID | 자료 | 이 묶음에서 뒷받침하는 범위 | 뒷받침하지 않는 범위 |
|---|---|---|---|
| S1 | [broncolor / Petri Anttila — Capturing zero-gravity spirits](https://broncolor.swiss/news/how-to-capturing-zero-gravity-spirits) | 유리병 촬영에서 배경 확산·스트립 조명·반사 제어를 따로 다루는 실제 촬영 사례 | 본 저장소 프롬프트의 성공률, 모든 유리에 같은 배치가 최적이라는 주장 |
| S2 | [Epic Games — Physically Based Materials](https://dev.epicgames.com/documentation/en-us/unreal-engine/physically-based-materials-in-unreal-engine) | 거칠기와 금속성은 표면 반사 표현에서 구분하는 속성 | 영어 프롬프트가 수치대로 셰이더를 구현한다는 주장 |
| S3 | [Nikon — Riding the Rails Video Techniques](https://www.nikonusa.com/learn-and-explore/c/tips-and-techniques/moving-pictures-riding-the-rails-video-techniques) | 슬라이더를 이용한 카메라 이동의 촬영 예 | AI 모델이 요청한 이동을 정확히 수행한다는 주장 |
| S4 | [Epic Games — Camera Rigs, Unreal Engine 4.27](https://dev.epicgames.com/documentation/unreal-engine/camera-rigs?application_version=4.27&lang=en-US) | 카메라 위치 이동을 경로로 다루는 예 | 제품 부분 회전의 최적 각도나 영상 길이 |
| L1 | [Creative Commons — CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | 출처 표시를 조건으로 한 공유·변형·상업 활용 허용의 라이선스 조건 | 외부 자료·타인 기여물의 권리 보증 |

## 설명과 검증 상태 구분

- **배경 원리:** 위 공식·제조사 자료가 설명하는 일반적 촬영·재질 개념.
- **편집 판단:** 레시피의 우선순위와 수정 순서. 이 프로젝트가 제안하는 접근이다.
- **실험 설계:** 출력 비율, 4초 길이, 부분 회전 범위, 반복 횟수. 비교를 시작하기 위한 선택이며 검증된 최적값이 아니다.
- **레시피 비교 관측:** 아직 없음. 참고 이미지 5개 생성은 완료했지만 baseline/recipe 비교 실험은 별도다. 예상 실패 모드는 검사할 위험 항목이며 실제 이 묶음에서 관측된 사례로 쓰지 않는다.

현재 기술 근거는 개념 단위의 확인이다. 외부 문서 전체를 최신 버전별로 전수 재검증한 것은 아니다.

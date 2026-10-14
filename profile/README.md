<p align="center">
  <img src="https://raw.githubusercontent.com/digital-tennis/digital-tennis-docs/main/docs/assets/digital-tennis-github-avatar-500.png" width="140" alt="Digital Tennis logo">
</p>

<h1 align="center">Digital Tennis</h1>

<p align="center">
  <strong>라켓의 움직임을 PC 테니스로.</strong><br>
  외장 IMU와 BLE 컨트롤러, Unity 게임, 온라인 대전을 만드는 3인 프로젝트
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Unity-PC%20Tennis-071D49?style=flat-square" alt="Unity PC Tennis">
  <img src="https://img.shields.io/badge/Controller-External%20IMU%20%2B%20BLE-C6FF3A?style=flat-square&amp;labelColor=071D49" alt="External IMU and BLE controller">
  <img src="https://img.shields.io/badge/Team-3%20Developers-00D5EE?style=flat-square&amp;labelColor=071D49" alt="3 Developers">
  <img src="https://img.shields.io/badge/Plan-12%20Days-071D49?style=flat-square" alt="12 Day Plan">
</p>

<p align="center">
  <a href="https://github.com/digital-tennis/digital-tennis-docs/blob/main/docs/README.md"><strong>개발 문서</strong></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/digital-tennis/digital-tennis-docs/blob/main/docs/products/README.md">제품별 개발 과제</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/digital-tennis/digital-tennis-docs/blob/main/docs/planning/wbs.md">12일 WBS</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/digital-tennis/digital-tennis-docs/blob/main/docs/project/architecture.md">시스템 구조</a>
</p>

## 프로젝트

**NU40-DK에 별도로 부착한 외장 IMU**로 라켓 동작을 읽고, BLE로 전달해 Unity PC 게임의 타격 타이밍·방향·강도를 조절합니다. 캐릭터는 자동으로 이동하고, 플레이어는 스윙에 집중합니다.

- **1인 플레이** — 하·중·상 난이도의 독립 AI 플레이어
- **온라인 2인 플레이** — 방 코드로 참가하고 서버 시그널링을 통해 P2P 연결
- **연결 대체 경로** — 직접 연결이 어려울 때 같은 게임 메시지를 서버 릴레이로 전달

현재는 **개발 계획과 인터페이스 설계 단계**입니다. 12일·3명·36인일 범위의 WBS와 초보자용 상세 개발 과제 37개를 준비했습니다. 실제 구현과 검증 결과는 각 저장소에서 공개합니다.

## 제품별 저장소

| 제품 | 저장소 | 담당하는 기능 |
| --- | --- | --- |
| 🎮 PC 게임 | [digital-tennis-game](https://github.com/digital-tennis/digital-tennis-game) | Unity 테니스 엔진, 점수, UI, 1인·온라인 플레이 |
| 🎾 라켓 펌웨어 | [digital-tennis-firmware](https://github.com/digital-tennis/digital-tennis-firmware) | 외장 IMU 드라이버, 보정, 스윙 인식, BLE |
| 📡 Unity 입력 SDK | [digital-tennis-ble-unity](https://github.com/digital-tennis/digital-tennis-ble-unity) | Windows BLE 연결·재연결, 표준 입력, 가상 컨트롤러 |
| 🔗 컨트롤러 프로토콜 | [digital-tennis-protocol](https://github.com/digital-tennis/digital-tennis-protocol) | 메시지 규격, C/C# 코덱, 공통 테스트 벡터 |
| 🤖 AI 플레이어 | [digital-tennis-ai](https://github.com/digital-tennis/digital-tennis-ai) | 착지 예측, 이동·타격 결정, 난이도 정책 |
| 🌐 온라인 서버 | [digital-tennis-match-server](https://github.com/digital-tennis/digital-tennis-match-server) | 방 코드, 2인 방, WebSocket 시그널링·릴레이 |
| 📘 프로젝트 문서 | [digital-tennis-docs](https://github.com/digital-tennis/digital-tennis-docs) | GitBook 문서, 상세 과제, WBS, 통합 검증 |

## 함께 만드는 방식

각 제품은 독립적으로 검증할 수 있게 분리합니다. 실물 컨트롤러가 준비되기 전에는 가상 입력으로 게임을 개발하고, 공통 규격과 테스트 벡터로 하드웨어·SDK·게임을 연결합니다.

| D2 | D4 | D8 | D12 |
| --- | --- | --- | --- |
| 외장 IMU 인식 | 가상 입력 기본 경기 | 실물 컨트롤러·AI 통합 | 온라인 검증·결과물 공개 |

새로 참여한다면 [작업 방법](https://github.com/digital-tennis/digital-tennis-docs/blob/main/docs/guides/contributing.md)을 먼저 읽고, [제품별 과제](https://github.com/digital-tennis/digital-tennis-docs/blob/main/docs/products/README.md)에서 입력·출력·예외·완료 기준을 확인하세요.

<p align="center">
  <sub>Hardware · Bluetooth · Game Engine · AI · Networking</sub>
</p>

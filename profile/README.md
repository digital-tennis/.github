<p align="center">
  <img src="https://raw.githubusercontent.com/digital-tennis/digital-tennis-docs/main/docs/assets/digital-tennis-github-avatar-500.png" width="120" alt="Digital Tennis 로고">
</p>

# Digital Tennis

**라켓의 움직임을 PC 테니스로.** 키보드로 시작하고, 직접 만드는 BLE 모션 라켓으로 확장하는 오픈소스 테니스 프로젝트입니다.

[게임 실행하기](https://github.com/digital-tennis/digital-tennis-game) · [개발 문서](https://github.com/digital-tennis/digital-tennis-docs) · [시스템 구조](https://github.com/digital-tennis/digital-tennis-docs/blob/main/docs/project/architecture.md) · [개발 과제](https://github.com/digital-tennis/digital-tennis-docs/blob/main/docs/products/README.md)

## 게임과 컨트롤러를 함께 만듭니다

- 세계지도에서 15명의 오리지널 선수와 코트를 고르고 AI 또는 온라인 상대와 경기합니다.
- 캐릭터는 자동으로 이동하고, 플레이어는 서브·스윙 타이밍·샷·스킬 선택에 집중합니다.
- 펌웨어, 프로토콜, PC Bluetooth, 게임, AI와 서버를 나누어 독립적으로 개발·검사합니다.

실물 제품은 **NU40-DK + 별도 외장 IMU**를 사용합니다. 키보드로 게임을 시작할 수 있습니다. 센서 없는 NU-54는 Mac 일반 게임 창에서 본딩·메시지 왕복·재시작 후 복구를 확인했습니다. NU40-DK 실물·외장 IMU와 Windows 검증은 남아 있습니다. [현재 검증 범위](https://github.com/digital-tennis/digital-tennis-game/blob/7af42a20b42975b21a41ab3f7055c6846fb510e9/docs/controller-bonding.md)

## 관심 있는 영역부터 시작하세요

| 프로젝트 | 만드는 것 | 시작점 |
| --- | --- | --- |
| [digital-tennis-game](https://github.com/digital-tennis/digital-tennis-game) | Unity PC 게임·규칙·캐릭터·화면·음향 | 실행 화면과 키보드 플레이 |
| [digital-tennis-firmware](https://github.com/digital-tennis/digital-tennis-firmware) | 외장 IMU·버튼·보정·동작 판정·BLE 송신 | 장비 없는 C 호스트 검사 |
| [digital-tennis-protocol](https://github.com/digital-tennis/digital-tennis-protocol) | 20바이트 이벤트·GATT·C/C# 코덱 | 규격과 패킷 사용 예 |
| [digital-tennis-ble-unity](https://github.com/digital-tennis/digital-tennis-ble-unity) | macOS·Windows Bluetooth·OS 본딩·입력 검증 | C# SDK와 플랫폼 모듈 |
| [digital-tennis-ai](https://github.com/digital-tennis/digital-tennis-ai) | 독립적인 난이도별 이동·타격 정책 | seed 기반 판단 예제 |
| [digital-tennis-match-server](https://github.com/digital-tennis/digital-tennis-match-server) | 방 코드·시그널링·릴레이·재접속 | 로컬 서버와 WebSocket 예제 |
| [digital-tennis-docs](https://github.com/digital-tennis/digital-tennis-docs) | 제품 간 계약·초보자 과제·WBS·검증 안내 | 목적별 문서 길잡이 |

## 함께 개발하기

처음 참여한다면 [작업 방법](https://github.com/digital-tennis/digital-tennis-docs/blob/main/docs/guides/contributing.md)을 읽고 각 저장소의 `CONTRIBUTING.md`를 확인하세요. 버그와 제안은 해당 제품의 Issues로 남길 수 있습니다.

초기 **12일·3명·36인일** 계획과 37개 구현 과제는 [WBS](https://github.com/digital-tennis/digital-tennis-docs/blob/main/docs/planning/wbs.md)에 보존합니다. 직접 작성한 제품 코드·문서는 Apache-2.0을 사용하며 외부 자산은 원래 라이선스를 유지합니다. 구체적인 적용 범위는 각 저장소의 `LICENSE`, `NOTICE`, `THIRD_PARTY_NOTICES.md`를 확인하세요.

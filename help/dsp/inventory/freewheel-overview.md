---
title: FreeWheel에서 PG 거래 설정 개요
description: 'FreeWheel의 게시자와 프로그래밍 방식으로 보장되는 거래를 위한 광고를 실행하는 데 필요한 사전 요구 사항과 추가 단계에 대해 알아봅니다. '
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: dfd5992f059645622b3a75d092d3eb7fe1bfa696
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# FreeWheel에서 프로그래밍 방식 보장 거래 설정 개요

FreeWheel에서 게시자와 프로그래밍 방식으로 보장되는 거래를 설정하려면 추가 권한 및 단계가 필요합니다.

>[!PREREQUISITES]
>
>작업 [!DNL Adobe] 계정 팀: [!DNL DSP] 계정에는 다음 권한이 있습니다.
>
>1. 사용 권한 [!DNL FreeWheel] 프로그램 형식 보장 거래에 대한 광고를 제출해야 하는 프로그래밍 방식 보장 워크플로우입니다. [!DNL FreeWheel].
>
>1. (각 광고와 함께 Clearcast 시계 번호가 필요한 영국 게시자와 작업하는 경우) 광고에 시계 번호를 포함할 수 있는 권한.


## 워크플로우

1. 거래에 지정된 미디어 유형으로 광고를 만듭니다.

   일부 영국 게시자의 경우 광고에 Clearcast 시계 번호를 포함해야 합니다.

1. [거래 ID 수락](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) Deal ID Inbox를 사용하여 FreeWheel의 게시자와 이미 협상했습니다.

   거래를 수락한 후 프롬프트에 따라 1) 거래에 사용할 광고를 선택하고 2) 광고를 제공할 프로그래밍 방식으로 보장된 기본 배치를 생성합니다.

1. [FreeWheel에 광고 제출](freewheel-submit.md)

   광고가 실행되기 전에 광고를 제출하고 승인해야 합니다.

1. [광고 제출 상태를 확인합니다](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [거래 ID 받은 편지함에서 거래 수락](deal-id-inbox-accept.md)
>* [FreeWheel에 프로그램 방식으로 보장되는 거래를 위한 광고 제출](freewheel-submit.md)
>* [광고 상태 확인 [!DNL FreeWheel] 프로그램 방식의 보장 거래](freewheel-check-status.md)
>* [FreeWheel 광고 제출 오류 코드](freewheel-error-codes.md)


---
title: FreeWheel에서 PG 거래 설정 개요
description: 'FreeWheel의 게시자와 프로그래밍 방식으로 보장되는 거래를 위한 광고를 실행하는 데 필요한 사전 요구 사항과 추가 단계에 대해 알아봅니다. '
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# FreeWheel에서 프로그래밍 방식 보장 거래 설정 개요

FreeWheel에서 게시자와 프로그래밍 방식으로 보장되는 거래를 설정하려면 추가 권한 및 단계가 필요합니다.

>[!PREREQUISITES]
>
>Adobe 계정 팀과 협력하여 [!DNL DSP] 계정에 다음 권한이 있는지 확인합니다.
>
>1. 프로그래밍 방식으로 보장되는 거래를 [!DNL FreeWheel]에 대한 광고를 제출하는 데 필요한 [!DNL FreeWheel] 프로그래밍 방식 보장 워크플로우를 사용할 수 있는 권한.
>
>1. (각 광고와 함께 Clearcast 시계 번호가 필요한 영국 게시자와 작업하는 경우) 광고에 시계 번호를 포함할 수 있는 권한.


## 워크플로우

1. 거래에 지정된 미디어 유형으로 광고를 만듭니다.

   일부 영국 게시자의 경우 광고에 Clearcast 시계 번호를 포함해야 합니다.

1. [Deal ID ](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) Inbox를 사용하여 FreeWheel의 게시자와 이미 협상한 거래 ID를 수락합니다.

   거래를 수락한 후 프롬프트에 따라 1) 거래에 사용할 광고를 선택하고 2) 광고를 제공할 프로그래밍 방식으로 보장된 기본 배치를 생성합니다.

1. [FreeWheel에 광고 제출](freewheel-submit.md)

   광고가 실행되기 전에 광고를 제출하고 승인해야 합니다.

1. [광고 제출 상태를 확인합니다](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [거래 ID 받은 편지함에서 거래 수락](deal-id-inbox-accept.md)
>* [FreeWheel에 프로그램 방식으로 보장되는 거래를 위한 광고 제출](freewheel-submit.md)
>* [프로그램 보장 거래에 대한 광고  [!DNL FreeWheel] 상태 확인](freewheel-check-status.md)
>* [FreeWheel 광고 제출 오류 코드](freewheel-error-codes.md)


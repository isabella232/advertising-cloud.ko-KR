---
title: '[!UICONTROL Deal ID Inbox] 정보'
description: '[!UICONTROL Deal ID inbox] 기능에 대해 알아봅니다. 이 기능을 사용하면 이미 게시자 [!DNL Google Authorized Buyers], [!DNL FreeWheel], and [!DNL Rubicon]에서 협상한 비공개 거래를 허용할 수 있습니다.'
feature: Private Inventory, Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!UICONTROL Deal ID Inbox] 정보

DSP [!UICONTROL Deal ID inbox]을(를) 사용하면 SSP(공급측 플랫폼)를 통해 게시자에서 가져온 거래를 빠르게 설정할 수 있으므로 각 거래를 수동으로 설정할 필요가 없습니다. [!UICONTROL Deal ID inbox]에서 이미 게시자와 협상한 보증 및 비보증 비공개 개인 인벤토리 거래를 [!DNL Google Authorized Buyers](이전의 [!DNL AdX]), [!DNL FreeWheel] 및 [!DNL Rubicon]에서 수락할 수 있습니다.

>[!NOTE]
>
>Advertising Cloud DSP은 [!DNL FreeWheel] API와 통합한 첫 번째 DSP입니다.

[!UICONTROL Deal ID inbox]에서는 게시자가 볼 때 거래의 세부 정보를 볼 수 있으며, 거래 설정을 가속화하고, 수동 입력 오류를 방지할 수 있습니다.

DSP은 매일 오전 4시 30분에 모든 거래 세부 사항을 자동으로 새로 고칩니다. 또한 모든 [!DNL FreeWheel] 거래를 새로 고치고 [!DNL Google] 및 [!DNL Rubicon] 시간별로 기존 거래를 업데이트합니다. 언제든지 거래 세부 사항을 수동으로 새로 고쳐 새 거래를 채울 수도 있습니다.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>[!DNL Google Authorized Buyers]을 통해 프로그램 방식으로 보장되는 거래의 경우 예산의 적어도 90%를 제공해야 합니다. 그렇지 않으면 계정이 [!UICONTROL Deal ID inbox]의 [!DNL Google] 거래에 액세스할 수 없게 됩니다.

## [!UICONTROL Deal ID Inbox] 구현

[!UICONTROL Deal ID inbox]에서 거래를 받으려면 SSP 계정이 조직의 DSP 계정을 SSP 계정에 매핑해야 합니다. DSP은 관련 SSP와 조직의 계정 이름을 공유합니다. 지침은 Adobe 계정 관리자에게 문의하십시오.

거래 협상 중에, 발행자에게 거래를 상위 DSP 계정 대신 구매자에게 보내라고 말하세요. 거래 식별자는 SSP에 따라 이름 또는 ID일 수 있습니다.

## 거래 시 수행할 수 있는 작업

* **SSP** 가 올바른 게시자, 플라이트 날짜, CPM 및 기타 거래 세부 정보를 보냈는지 확인하려면 이 문제를 검토하십시오. 게시자가 실수를 했다면 DSP 외부에서 해당 게시자에게 연락하여 수정하고 다시 전송할 수 있습니다.

* **검토** 후 할당을 승인하면 더 이상 에 표시되지 않습니다 [!UICONTROL Deal ID inbox]. 수락된 거래는 [!UICONTROL Inventory] > [!UICONTROL Deals]에 나열되며 광고주의 배치 내에서 타깃팅할 준비가 되었습니다.

* **필요** 없거나 요청하지 않은 딜을 무시합니다. 무시된 거래는 보관 역할을 하는 [!UICONTROL Deal ID inbox] 내의 [!UICONTROL Ignored Deals] 탭으로 이동합니다. 거래를 무시할 때 DSP은 SSP 및 게시자에게 경고를 주지 않습니다.

* **이미 수락된 할인에 대한 세부 정보** 를  [!UICONTROL Inventory] >  [!UICONTROL Deals] (에서 아님)에서  [!UICONTROL Deal ID inbox]수정합니다. 마찬가지로 게시자가 변경 사항을 거래에 보낼 때 [!UICONTROL Inventory] > [!UICONTROL Deals]에서 이러한 변경 사항을 구현하는 것은 계약이 설정된 후 [!UICONTROL Deal ID inbox]이 SSP의 변경 사항을 동기화하지 않기 때문입니다.

## 어떤 종류의 거래를 수락할 수 없습니까?

거래 목록에 ![Accept](/help/dsp/assets/accept.png) 아이콘 또는 [!UICONTROL Accept] 단추가 없는 경우에는 [!UICONTROL Deal ID inbox]에서 받을 수 없습니다. 대신 [거래 ID 세부 사항을 수동으로](/help/dsp/inventory/deal-id-create.md)만들 수 있습니다.

다음 유형의 거래는 수락할 수 없습니다.

* [!DNL Google] USD가 아닌 거래.

* [!DNL Rubicon] USD가 아닌 거래

* [!DNL FreeWheel] 계정 통화가 아닌 거래.

* 오늘 전에 종료 날짜가 있는 거래.

* &quot;여러 미디어 유형&quot;으로 레이블이 지정된 이전 [!DNL Rubicon] 거래.

거래 세부 사항에는 거래가 수락되지 않는 이유가 포함되어 있습니다.

>[!MORELIKETHIS]
>
>* [거래 ID 받은 편지함에서 거래 수락](deal-id-inbox-accept.md)
>* [재고 기능 개요](inventory-overview.md)


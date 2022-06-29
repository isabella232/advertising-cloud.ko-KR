---
title: 정보 [!UICONTROL Deal ID Inbox]
description: 에 대해 알아보기 [!UICONTROL Deal ID inbox] 에서는 이미 게시자 와 협상한 개인 거래를 허용할 수 있는 기능을 제공합니다. [!DNL FreeWheel], [!DNL Google Authorized Buyers] (이전에는 [!DNL AdX]), and [!DNL Magnite DV+] (이전 [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# 정보 [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] 에서는 SSP(공급측 플랫폼)를 통해 게시자에서 가져온 거래를 신속하게 설정할 수 있으므로 각 거래를 수동으로 설정할 필요가 없습니다. 이미 게시자와 협상한 보증 및 비보장 개인 재고 거래를 수락할 수 있습니다. [!DNL FreeWheel], [!DNL Google Authorized Buyers] (이전에는 [!DNL AdX]) 및 [!DNL Magnite DV+] (이전 [!DNL Rubicon]) 내의 [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising Cloud DSP은 와 통합한 첫 번째 DSP입니다 [!DNL FreeWheel] API.

에서 [!UICONTROL Deal ID inbox]게시자가 볼 때 거래의 세부 사항을 볼 수 있고 거래 설정을 빠르게 하며 수동 입력 오류를 방지할 수 있습니다.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP은 매일 오전 4시 30분에 모든 거래 세부 사항을 자동으로 새로 고칩니다. 모든 것을 새로 고칩니다 [!DNL FreeWheel] 기존 거래를 거래 및 업데이트하여 [!DNL Google] 및 [!DNL Magnite DV+] 시간별. 언제든지 거래 세부 사항을 수동으로 새로 고쳐 새 거래를 채울 수도 있습니다.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>다음을 통해 프로그램 방식으로 보장되는 거래 [!DNL Google Authorized Buyers], 적어도 예산의 90%에 해당하는 금액을 제공해야 합니다. 그렇지 않으면 계정에 대한 액세스 권한이 상실됩니다. [!DNL Google] 의 [!UICONTROL Deal ID inbox].

## 구현 [!UICONTROL Deal ID Inbox]

에서 거래를 받으려면 다음을 수행하십시오. [!UICONTROL Deal ID inbox], SSP 계정은 조직의 DSP 계정을 SSP 계정에 매핑해야 합니다. DSP은 관련 SSP와 조직의 계정 이름을 공유합니다. 다음 사항에 문의하십시오. [!DNL Adobe] 계정 팀에 문의하십시오.

거래 협상 중에, 발행자에게 거래를 상위 DSP 계정 대신 구매자에게 보내라고 말하세요. 거래 식별자는 SSP에 따라 이름 또는 ID일 수 있습니다.

## 거래 시 수행할 수 있는 작업

* **딜 검토** SSP가 올바른 게시자, 플라이트 날짜, CPM 및 기타 거래 세부 사항을 전송했는지 확인합니다. 게시자가 실수를 했다면 DSP 외부에서 해당 게시자에게 연락하여 거래를 수정하고 다시 전송할 수 있습니다.

* **거래 수락** 검토 후 더 이상 [!UICONTROL Deal ID inbox]. 수락된 거래는 [!UICONTROL Inventory] > [!UICONTROL Deals] 및 는 광고주의 배치 내에서 타깃팅할 준비가 되었습니다.

* **거래 무시** 그것은 필요하지 않거나 요청하지 않은 것입니다. 무시된 거래는 [!UICONTROL Ignored Deals] 내의 탭 [!UICONTROL Deal ID inbox]: 아카이브 역할을 합니다. 거래를 무시할 때 DSP은 SSP 및 게시자에게 경고를 주지 않습니다.

* **이미 수락된 거래에 대한 세부 사항 수정** 변환 전: [!UICONTROL Inventory] > [!UICONTROL Deals] ( [!UICONTROL Deal ID inbox]). 마찬가지로 게시자가 거래에 변경 사항을 보낼 때 광고주는 [!UICONTROL Inventory] > [!UICONTROL Deals] 왜냐하면 [!UICONTROL Deal ID inbox] 딜 설정 후 SSP의 변경 사항을 동기화하지 않습니다.

## 어떤 종류의 거래를 수락할 수 없습니까?

거래 목록에 ![수락](/help/dsp/assets/accept.png) 아이콘 또는 [!UICONTROL Accept] 버튼, 당신은 그것을 받을 수 없다 [!UICONTROL Deal ID inbox]. 대신 다음을 수행할 수 있습니다 [수동으로 거래 ID 세부 사항 만들기](/help/dsp/inventory/deal-id-create.md).

다음 유형의 거래는 수락할 수 없습니다.

* [!DNL Google] USD가 아닌 거래.

* [!DNL Magnite DV+] USD가 아닌 거래

* [!DNL FreeWheel] 계정 통화가 아닌 거래.

* 오늘 전에 종료 날짜가 있는 거래.

* 이전 [!DNL Magnite DV+] &quot;여러 미디어 유형&quot;으로 레이블이 지정된 거래.

계약에는 그 거래가 수락할 수 없는 이유가 포함되어 있다.

>[!MORELIKETHIS]
>
>* [거래 ID 받은 편지함에서 거래 수락](deal-id-inbox-accept.md)
>* [재고 기능 개요](inventory-overview.md)


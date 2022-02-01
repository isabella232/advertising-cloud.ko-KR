---
title: 수동 거래 ID 설정
description: 수동으로 입력한 거래 ID에 대한 설정 설명을 참조하십시오.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: cf08c97a6a9fecd637f1776b186a18a5c5cc6435
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# 수동 거래 ID 설정

| 섹션 | 매개 변수 | 설명 | 필수 여부 | 편집 가능 |
|---------|-----------|-------------|----------|----------|
| [거래 세부 사항] | [!UICONTROL Deal name] | 사용자를 식별할 이름 [!UICONTROL Deal ID] Advertising Cloud DSP. 이름을 입력하거나 선택합니다 **[!UICONTROL Auto-name]** 를 입력하여 Advertising Cloud에서 거래 세부 사항을 기반으로 이름을 생성할 수 있습니다.<br><br>자동 생성된 이름의 예: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | 예 | 예 |
|  | [!UICONTROL External deal ID] | 게시자와 SSP가 이 거래를 식별하는 데 사용하는 ID입니다. | 예 | 아니요 |
|  | [!UICONTROL Publisher] | 이 인벤토리를 판매하는 게시자의 이름입니다. | 예 | 아니요 |
|  | [!UICONTROL SSP] | 이 거래를 실행할 SSP(공급측 플랫폼)입니다. | 예 | 아니요 |
|  | [!UICONTROL Media type] | 이 거래를 통해 구입할 미디어 유형입니다. *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, 또는 *[!UICONTROL Audio]*. 옵션은 SSP마다 다릅니다.<br><br> 딜에서 여러 미디어 유형을 허용하는 경우 거래를 생성할 때 기본 배치에 대한 미디어 유형을 선택합니다. 나중에 값을 변경하거나 다음을 수행할 수 있습니다 [추가 미디어 유형을 사용하여 새 배치 첨부](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | 예 | 아니요 |
|  | [!UICONTROL Deal type] | 거래 약정 및 가격 구조:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: 사용자와 게시자가 고정된 수의 노출 배달을 커밋하지 않았습니다. 거래는 CPM이 시장 상황에 따라 변동하고 증가할 수 있지만 인벤토리의 최소 가격을 지정합니다.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: 사용자와 게시자가 고정된 수의 노출 배달을 커밋하지 않았습니다. 가격은 협상된 고정 요금입니다.</li><li>*[!UICONTROL Guaranteed (fixed)]*: 귀하와 출판사는 사전 정의된 노출 횟수, 타깃팅, 비행 날짜 및 고정 가격에 동의했습니다.<br><br><b>참고:</b> 보증 계약에는 플라이트 날짜 및 [!UICONTROL Tracking] 섹션을 참조하십시오. 또한 거래에 대해 기본 프로그래밍 방식 보장(PG) 배치를 만들어야 하며, 대신 선택적으로 다른 배치에 거래를 사용할 수 있습니다.</li></ul> | 예 | 아니요 |
|  | [!UICONTROL CPM] | 천 단위 노출 횟수(CPM)당 협상된 비용. | 예 | 예 |
|  | [통화] | 거래의 통화입니다.<br><br>모든 SSP는 USD로 거래를 수락합니다. SSP가 DSP 계정의 통화를 수락하면 해당 통화도 사용할 수 있습니다. | 예 | 아니요 |
|  | [!UICONTROL Billing method] | 모든 거래 ID는 [!DNL Adobe]-자금 및 송장 발행 Advertising Cloud은 사용량에 따라 사용 가능한 모든 미디어 공급업체에 지불하고, 공급업체와의 불일치를 관리하고, 하나의 통합 송장을 계정에 보낼 것입니다. 이 옵션은 계정 환율 카드에 설명된 대로 추가 비용을 발생시킵니다. | 예 | 아니요 |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 거래에 액세스할 수 있는 사용자 계정의 이메일 주소입니다. | 아니요 | 예 |
|  | [!UICONTROL Advertisers that can access this deal] | 이 거래에 액세스할 수 있는 계정의 특정 광고주입니다.<br><br><b>참고:</b> 광고주와 거래를 광고주와 공유할 수 있으며 [!UICONTROL Deals] 보기. 거래 행에서 **[!UICONTROL #]**&#x200B;를 클릭합니다. **[!UICONTROL share]**, 그런 다음 이메일 주소와 거래를 공유합니다. | 예 | 예 |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | 이 거래를 사용하는 트래픽의 시작 및 종료 날짜입니다. 이 날짜는 추적 목적으로만 사용되며 광고 게재에 영향을 주지 않습니다.<br><br><b>팁:</b> 에서 [!UICONTROL Inventory] > [!UICONTROL Deals] 보기, [!UICONTROL Pacing & Budget] 열에는 거래가 지정된 비행 날짜 및 노출 목표까지 어떻게 지연되는지를 표시됩니다. 게재 속도가 느려지거나 과게재를 하는 경우, 게재를 통해 보내는 볼륨의 양을 조정하도록 게시자에게 문의하십시오. | 보증 거래: 예<br>보장되지 않는 거래: 아니요 | 예 |
|  | [!UICONTROL Impressions] | (보장되지 않는 거래의 경우 선택 사항) 이 거래를 사용하여 실행할 예상 노출 수입니다. 이 값은 추적 목적으로만 사용됩니다. 게시자가 광고 게재를 제어합니다. | 보증 거래: 예<br>보장되지 않는 거래: 아니요 | 예 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [수동으로 거래 ID 상세내역 생성](deal-id-create.md)
>* [SSP 파트너](ssp-partners.md)
>* [비공개 인벤토리 정보](private-inventory-about.md)


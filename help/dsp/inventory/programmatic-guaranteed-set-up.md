---
title: 프로그래밍 방식 보장 거래 설정
description: 게시자와 협상한 PG(프로그래밍 방식 보증) 거래를 설정하는 방법을 알아봅니다.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# 프로그래밍 방식 보장 거래 설정

*[지원되는 공급 측 플랫폼만](programmatic-guaranteed-about.md)*

지원되는 게시자와 프로그래밍 방식 보증(PG) 거래를 협상한 후 를 사용하여 DSP 내에서 거래를 설정할 수 있습니다 [!DNL Deal ID inbox] 또는 거래 상세내역을 수동으로 입력하여

>[!NOTE]
>
> PG 거래의 경우 게시자는 모든 예산 간격, 예산 최대 가용량 및 타깃팅을 처리합니다. DSP을 통해 PG를 허용하는 모든 SSP에서 게시자가 예산 캡핑을 설정할 수 있는지 확인합니다.
>
> 게시자와 프로그래밍 방식으로 보장되는 거래 설정 [!DNL FreeWheel] 추가 권한 및 단계가 필요합니다. 참조:[프로그램 보장 거래 설정 개요 [!DNL FreeWheel]](freewheel-overview.md)&quot;&quot;을 참조하십시오.

## 를 사용하여 프로그래밍 방식으로 보장되는 거래 설정 [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

다음 방법은 [!DNL FreeWheel], [!DNL Google Authorized Buyers], 및 [!DNL Magnite DV+].

1. [거래 수락](deal-id-inbox-accept.md).

1. 거래를 저장한 후 거래에 사용할 광고를 선택하고 메시지가 표시되면 프로그래밍 방식으로 보장되는(PG) 기본 배치를 만듭니다.

   거래에 대한 기본 PG 배치를 만드는 것은 구매의 100%를 게재하기 위해 필수입니다. 이 유형의 배치에는 타겟팅이 없으므로 DSP이 게시자의 모든 입찰 요청에 입찰을 반환할 수 있습니다.

   * 단일 거래를 수락하는 경우 PG 기본 배치 만들기 워크플로우로 자동 리디렉션됩니다.

      모두 [!DNL FreeWheel] 거래는 단일 거래로 제안된다.

   * 여러 PG 거래 ID가 있는 제안을 수락하는 경우 만들어야 하는 각 PG 기본 배치를 식별합니다. 필요한 배치를 모두 생성하면 계속 단추가 활성화됩니다.

1. (선택 사항) 을 클릭하여 추가 PG 또는 비PG 배치에서 PG 거래를 Target 합니다 ![옵션 메뉴](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   거래는 연결된 TV, 데스크탑 및 오디오와 같은 모든 미디어 유형의 조합을 지원하는 여러 배치를 타깃팅할 수 있습니다.

## 프로그래밍 방식 보장 거래를 수동으로 설정

다른 모든 SSP에 이 메서드를 사용합니다.

1. [수동으로 거래 ID 세부 사항 설정](deal-id-create.md).

1. 거래를 저장한 후 거래에 사용할 광고를 선택하고 메시지가 표시되면 PG 기본 배치를 만듭니다.

   거래에 대한 PG 기본 배치를 만드는 것은 구매의 100%를 게재하기 위해 필수입니다. 이 유형의 배치에는 타겟팅이 없으므로 DSP이 게시자의 모든 입찰 요청에 입찰을 반환할 수 있습니다.

1. (선택 사항) 을 클릭하여 추가 PG 또는 비PG 배치에서 PG 거래를 Target 합니다 ![옵션 메뉴](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   거래는 연결된 TV, 데스크탑 및 오디오와 같은 모든 미디어 유형의 조합을 지원하는 여러 배치를 타깃팅할 수 있습니다.

>[!MORELIKETHIS]
>
>* [프로그램 보장 거래 기본 정보](programmatic-guaranteed-about.md)
>* [프로그램 방식의 보장 거래를 협상하기 위한 팁](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [프로그램 방식으로 보장되는 거래를 위한 광고 제출 [!DNL FreeWheel]](freewheel-submit.md)
>* [거래 ID 받은 편지함에서 거래 수락](deal-id-inbox-accept.md)
>* [수동으로 거래 ID 상세내역 생성](deal-id-create.md)
>* [SSP 파트너](ssp-partners.md)
>* [재고 기능 개요](inventory-overview.md)


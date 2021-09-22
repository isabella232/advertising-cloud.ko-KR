---
title: ' [!DNL Roku] 인벤토리 사용'
description: ' [!DNL Roku], including inventory options, approved third-party tracking vendors, and best practices for [!DNL Roku] 특정 배치와 DSP 파트너 관계에 대해 알아봅니다. '
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# [!DNL Roku] 인벤토리 사용

Advertising Cloud DSP은 [!DNL Roku]에 광고를 위한 고유한 기능을 제공합니다.

## Advertising Cloud DSP 및 [!DNL Roku] 파트너 관계

Roku와 Advertising Cloud DSP에는 [!DNL DSP] 대상과 [!DNL Roku] 인벤토리에서 1:1 결정적 대상 타깃팅을 위한 [!DNL Roku] ID와 일치하는 고유한 파트너 관계가 있습니다.

Roku의 자체 DSP(OneView) 외부에서 Advertising Cloud DSP은 이러한 타깃팅 기능에 대한 유일한 액세스 권한을 갖습니다. 또한 Advertising Cloud DSP은 다른 모든 연결된 TV(CTV) 인벤토리 옆에 있는 [!DNL Roku] 공급을 측정할 수 있는 권한이 있는 유일한 DSP입니다. [!DNL Roku]은 표준 RTB 및 노출 픽셀 신호를 모두 공유하지 않으므로 다른 DSP에서는 Roku에서 판매하는 CTV 공급에서 타깃팅하거나 측정할 수 없습니다.

## [!DNL Roku] 재고 옵션

a) [!DNL Roku]으로 직접 개인 거래 ID를 설정한 다음 거래 ID 데이터를 DSP에 입력하거나 b) [!DNL On Demand] 갤러리를 방문하여 [!DNL Roku] 프로필에 구독할 수 있습니다.

>[!NOTE]
>
>[!DNL Roku] 재고 관리는 오픈 마켓플레이스 및 교환에서 사용할 수 없습니다.

* 비공개 거래의 경우 [DSP](/help/dsp/inventory/deal-id-create.md)에서 거래 ID에 대한 정보를 설정한 다음 [!DNL Roku] 배치 내에서 &quot;[!UICONTROL Roku Network – Audience]&quot; 및 &quot;[!UICONTROL The Roku Channel – Audience]&quot;를 타깃팅합니다.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* [다음 [!DNL Roku] inventory within the [!DNL On Demand] Gallery](/help/dsp/inventory/on-demand-inventory-subscribe.md)에 가입하고 [!DNL Roku] 배치 내에서 승인된 모든 거래를 타깃팅할 수 있습니다.

   * [!DNL The CW], [!DNL ABC] 및 [!DNL ESPN]와 같은 프리미엄 컨텐츠 파트너가 있는 [!DNL Roku] 에코시스템의 인벤토리에 대한 &quot;[!UICONTROL Roku Network – Audience]&quot;이 있습니다.
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot;([!DNL Roku] Owned-and-Operated (O&amp;O) 앱 컨텐츠에 대한 ).

### [!DNL Roku]을 사용하여 개인 시장 사용자 정의 시 이점

비공개 거래를 통해 필요에 따라 거래 매개 변수를 사용자 정의할 수 있습니다.

* **협상된 가격 책정:**   [!DNL Roku] 영업 팀과 협력하여 캠페인 요구 사항에 맞는 거래를 협상하고 구성합니다.

* **비율 우선순위:** PMP(Private Marketplace)가 항상 켜져 있는 거래(예:  [!DNL On Demand] 거래)보다 높은 우선 순위를 받습니다.

* **빈도 관리:**  [!DNL Roku] 기본 빈도 상한은 사용자당 1개(1)이고 30분이지만 시간, 일, 주, 월 또는 전체 비행 기간별로 상한선을 사용자 지정할 수 있습니다.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]데이터 타깃팅:** [!DNL Roku] 대상은  [!DNL Roku] 장치 및 TV 신호,  [!DNL The Roku Channel] TV 장르 친화성, 스트리밍 TV 동작 및 케이블 구독 상태와 같은 추적된 데이터 및 CRM( [!DNL Roku] 고객 관계 관리) 시스템의 추가 데이터를 기반으로 구축됩니다.

* **[!DNL Roku]컨텐츠 타깃팅:** 비공개 거래는 장르, 앱 차단 목록에 추가하다 애플리케이션, 시즌 및 텐폴트 이벤트 등을 기준으로 앱을 타깃팅할 수 있으며 내에서만 쇼를 타깃팅할 수  [!DNL The Roku Channel] 있습니다.

## [!DNL Roku] 배치

DSP 캠페인에서는 배치 유형 &quot;[!UICONTROL Connected TV (Roku)]&quot;을 사용하여 [특정 배치 [!DNL Roku]-특정 배치](/help/dsp/campaign-management/placements/placement-create.md)를 만듭니다. 정의된 목표가 있는 [!DNL Roku] 특정 패키지에 [!DNL Roku] 배치를 포함합니다.

각 [!DNL Roku] 배치는 하나 이상의 [!DNL Roku] 거래 또는 소스를 대상으로 해야 합니다. [!DNL Roku]과(와) 일치하는 DSP 고유 대상을 활용하려면 [!DNL Roku](옵트인) 결정론적 데이터 세트에 대해 일치시킬 수 있는 하나 이상의 대상 세그먼트를 포함하십시오.

### [!DNL Roku]-승인된 타사 추적 공급업체

[!DNL Roku] 배치에는 다음 공급업체의 타사 이벤트 픽셀 및 전환 픽셀이 포함될 수 있습니다.   [!DNL Acxiom],  [!DNL comScore],  [!DNL Data Plus Math],  [!DNL Experian],  [!DNL Factual],  [!DNL Kantar],  [!DNL Marketing Evolution],  [!DNL Neustar],  [!DNL Nielsen],  [!DNL Nielsen Catalina Solutions],  [!DNL NinthDecimal],  [!DNL Oracle],  [!DNL Placed],  [!DNL Polk],  [!DNL Research Now], 및.

### 배치 전략별 우수 사례

다음은 [!DNL Roku] 특정 배치에 대한 권장 지침입니다.

증분 도달 범위를 최대화하려면

* [!DNL The Roku Channel]을(를) 사용하여 이미 도달한 대상을 제외하여 [!DNL Roku O&O]에서 노출된 대상을 표시하지 않습니다.

* [!DNL Roku] 플랫폼에서 이미 도달한 대상을 제외하여 [!DNL All Roku]에서 노출된 대상을 표시하지 않습니다.

가장 빠른 설정의 경우:

* [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md)에서 [!DNL The Roku Channel]에 대한 기존, 항상 있는 거래를 Target 하여 [!DNL Roku] 소유 및 운영되는 인벤토리에 빠르게 액세스합니다.
* [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md)에 있는 [!DNL Roku Network]에 대한 기존 항상 수행하는 거래를 Target 하여 [!DNL Roku] 플랫폼에서 빠르게 확장할 수 있습니다.

최대 배율:

* [!DNL Roku] 공급에 대한 우선 순위 액세스를 협상된 가격으로 [!DNL Roku] 개인 마켓플레이스를 사용자 지정합니다.

>[!MORELIKETHIS]
>
>* [수동으로 거래 ID 상세내역 생성](/help/dsp/inventory/deal-id-create.md)
> * [Premium 인벤토리 거래 [!DNL On Demand] 에 대한 가입 및 액세스 요청](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [배치 만들기](/help/dsp/campaign-management/placements/placement-create.md)


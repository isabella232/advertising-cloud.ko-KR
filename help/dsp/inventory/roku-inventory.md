---
title: 사용 [!DNL Roku] 인벤토리
description: Adobe와의 DSP 파트너십에 대해 알아보기 [!DNL Roku], 인벤토리 옵션, 승인된 타사 추적 공급업체 및 [!DNL Roku]- 특정 배치.
feature: DSP On Demand Inventory, DSP Private Inventory
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# 사용 [!DNL Roku] 인벤토리

Advertising DSP에서는 광고를 위한 고유한 기능을 제공합니다 [!DNL Roku].

## DSP 및 [!DNL Roku] 파트너십

Roku와 DSP은 고객의 [!DNL DSP] 대상 [!DNL Roku] 1:1 결정론적 대상 타깃팅에 대한 ID [!DNL Roku] 인벤토리

Roku의 자체 DSP(OneView) 외부에서 Advertising DSP은 이러한 타깃팅 기능에 대한 유일한 액세스 권한을 갖습니다. 또한 측정 권한이 있는 유일한 DSP은 Advertising DSP입니다 [!DNL Roku] 기타 모든 연결된 TV(CTV) 인벤토리 옆에 제공됩니다. 왜냐면 [!DNL Roku] 는 표준 RTB와 노출 픽셀 신호를 모두 공유하지 않으며 다른 DSP도 Roku에서 판매하는 CTV 공급에서 타깃팅하거나 측정할 수 없습니다.

## [!DNL Roku] 재고 옵션

a)에서 직접 비공개 거래 ID를 설정할 수 있습니다 [!DNL Roku] 그런 다음 DSP 또는 b)에 거래 ID 데이터를 입력합니다. [!DNL On Demand] 구독할 갤러리 [!DNL Roku] 프로필:

>[!NOTE]
>
>[!DNL Roku] 재고 관리는 오픈 마켓플레이스 및 교환에서 사용할 수 없습니다.

* 개인적인 거래로는 [DSP에서 거래 ID에 대한 정보 설정](/help/dsp/inventory/deal-id-create.md) 을(를) 타겟으로[!UICONTROL Roku Network – Audience]&quot; 및 &quot;[!UICONTROL The Roku Channel – Audience]&quot; [!DNL Roku] 배치.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* 다음을 수행할 수 있습니다 [다음 구독 [!DNL Roku] 내 인벤토리 [!DNL On Demand] 갤러리](/help/dsp/inventory/on-demand-inventory-subscribe.md)를 만든 다음 내에서 승인된 거래를 타겟팅합니다 [!DNL Roku] 배치:

   * &quot;[!UICONTROL Roku Network – Audience]&quot; [!DNL Roku] 다음과 같은 프리미엄 컨텐츠 파트너와 에코시스템 [!DNL The CW], [!DNL ABC], 및 [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; [!DNL Roku] 소유된 및 운영(O&amp;O) 앱 콘텐츠.

### 을 사용하여 Private Marketplace 사용자 정의 이점 [!DNL Roku]

비공개 거래를 통해 필요에 따라 거래 매개 변수를 사용자 정의할 수 있습니다.

* **협상된 가격:** 을 사용하여 작업 [!DNL Roku] 영업 팀이 캠페인 요구 사항을 충족하는 거래를 협상하고 구성할 수 있습니다.

* **비율 우선 순위:** PMP(Private Marketplace)는 항상 제공하는 거래(예: [!DNL On Demand] 거래).

* **빈도 관리:** 다음 [!DNL Roku] 기본 빈도 상한은 사용자당 1개(1)이고 30분이지만 시간, 일, 주, 월 또는 전체 비행 기간별로 상한선을 사용자 지정할 수 있습니다.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]데이터 타깃팅:** [!DNL Roku] 대상: [!DNL Roku] 장치 및 TV 신호, [!DNL The Roku Channel] (예: TV 장르 선호도, 스트리밍 TV 동작, 케이블 구독 상태) 및 [!DNL Roku] crm(고객 관계 관리) 시스템.

* **[!DNL Roku]컨텐츠 타깃팅:** 비공개 거래는 장르, 앱 적용, 시즌 및 텐트폴 이벤트, 내부 프로그램 등을 통해 앱을 타깃팅할 수 차단 목록에 추가하다 있습니다 [!DNL The Roku Channel] 전용.

## [!DNL Roku] 배치

DSP 캠페인에서, [만들기 [!DNL Roku]-특정 배치](/help/dsp/campaign-management/placements/placement-create.md) 배치 유형 사용 &quot;[!UICONTROL Connected TV (Roku)].&quot; 포함 [!DNL Roku] 배치 [!DNL Roku]- 정의된 목표를 가진 특정 패키지

각 [!DNL Roku] placement는 최소 하나 이상의 target을 사용해야 합니다. [!DNL Roku] 거래 또는 소스 DSP 고유 대상 일치 사용 방법 [!DNL Roku]에 대해 일치시킬 수 있는 하나 이상의 대상 세그먼트를 포함하십시오 [!DNL Roku] (옵트인) 결정적 데이터 세트.

### [!DNL Roku]-승인된 타사 추적 공급업체

[!DNL Roku] 배치에는 다음 공급업체의 타사 이벤트 픽셀 및 전환 픽셀이 포함될 수 있습니다.  [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], 및 [!DNL Research Now].

### 배치 전략별 우수 사례

다음은에 대한 권장 지침입니다 [!DNL Roku]- 특정 배치.

증분 도달 범위를 최대화하려면

* 에서 노출된 대상 억제 [!DNL Roku O&O] 을 사용하여 이미 도달한 대상을 제외함으로써 [!DNL The Roku Channel].

* 에서 노출된 대상 억제 [!DNL All Roku] 을 통해 이미 도달한 대상을 제외함으로써 [!DNL Roku] 플랫폼.

가장 빠른 설정의 경우:

* 에 대한 기존, 항상 켜져 있는 거래 Target [!DNL The Roku Channel] in [[!DNL On Demand] 인벤토리](/help/dsp/inventory/on-demand-inventory-subscribe.md) 빠르게 액세스 [!DNL Roku] 소유 및 운영 재고
* 에 대한 기존, 항상 켜져 있는 거래 Target [!DNL Roku Network] in [[!DNL On Demand] 인벤토리](/help/dsp/inventory/on-demand-inventory-subscribe.md) 규모를 빠르게 넓히다 [!DNL Roku] 플랫폼.

최대 배율:

* 사용자 지정 [!DNL Roku] 우선 순위 액세스 권한을 갖는 비공개 마켓플레이스 [!DNL Roku] 협상가로 공급하다.

>[!MORELIKETHIS]
>
>* [수동으로 거래 ID 상세내역 생성](/help/dsp/inventory/deal-id-create.md)
> * [가입 및 액세스 요청 대상 [!DNL On Demand] Premium 인벤토리 거래](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [배치 만들기](/help/dsp/campaign-management/placements/placement-create.md)


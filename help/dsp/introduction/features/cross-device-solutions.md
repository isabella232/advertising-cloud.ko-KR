---
title: 교차 장치 솔루션
description: 교차 장치 기능에 대해 자세히 알아보십시오.
feature: DSP Introduction
exl-id: 29f8ec41-35a6-4a29-a638-82a2929a8fe6
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---

# 교차 장치 솔루션

Advertising Cloud DSP과 통합 [!DNL LiveRamp] 및 [!DNL Adobe Device Co-op] 을(를) 사용하면 브랜드가 추적한 장치뿐만 아니라 사용자의 알려진 모든 장치로 대상을 확장할 수 있습니다. 또한 통합은 모든 장치에서 빈도 제한 및 속성 측정을 제공합니다.

지원되는 사람 기반 장치 그래프를 사용하는 경우 다음을 수행할 수 있습니다.

* 다양한 채널 및 장치에서 대상을 일치시켜 장치가 아닌 사람 및 가구에 광고를 전달합니다.
* 개별 사용자 간의 빈도를 파악하고 최대 가용량을 통해 광고 노출을 균형 있게 조정하십시오.
* 채널 또는 장치에서 대상을 노출하거나 전환하는 전략을 테스트합니다.

## 각 장치 그래프의 이점

* [!DNL Adobe Device Co-op]:
   * 참여하는 Adobe 광고주의 결정론적 및 확률론적 데이터의 옵트인 풀을 제공합니다
   * 데스크탑 및 모바일 웹 방문자가 제공하는 강력한 쿠키 ID 연결을 제공합니다
   * 미국 및 캐나다에서 주로 가져온 데이터를 포함합니다
   * 사용 요금이 없습니다

* [!DNL LiveRamp] 장치 그래프:
   * 오프라인 고객 데이터를 포함하여 결정론적 데이터 풀을 제공합니다.
   * 쿠키 ID와 모바일 장치 ID 간에 범위를 제공합니다
   * 주로 미국에서 온 데이터를 포함합니다
   * 빈도 제한 및 속성 측정에 대해 무료입니다
   * 확장 노출(를 사용해서만 전달되는 노출)에 대해 0.35CPM으로 가격이 책정되었습니다 [!DNL LiveRamp] 타깃팅된 대상 세그먼트 내에 있는 장치가 아닌 장치 그래프)

      요금은 당신의 계좌요율에 반영됩니다

## 사용자 기반 빈도 관리

사용자 기반 빈도 관리를 사용하면 실제 미디어 노출 제어를 위해 장치 수준이 아닌 개인 수준에서 빈도 상한을 지정할 수 있습니다.

### 사용자 기반 빈도 관리 활성화

* **캠페인:** 새 캠페인을 만들 때 [!UICONTROL Cross-Device Level] 설정 활성화 &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot;을 선택하고 장치 그래프를 선택합니다. 지정된 장치 그래프는 배치 수준에서 교차 장치 타깃팅과 캠페인, 패키지 및 배치 수준에서 사용자 기반 빈도 관리에 모두 사용됩니다. 주파수 캡은 사람의 알려진 모든 장치에 적용됩니다.

자세한 내용은 [캠페인 설정](/help/dsp/campaign-management/campaigns/campaign-settings.md).

캠페인을 저장한 후에는 캠페인을 변경할 수 없습니다 [!UICONTROL Cross Device Level] 설정

* **패키지:**  패키지 수준에서 추가 빈도 캡을 선택적으로 설정할 수 있습니다. DSP은 캠페인 계층에서 가장 엄격한 빈도 제한을 준수합니다.

* **배치:** 배치 레벨에서 추가 빈도 캡을 선택적으로 설정할 수 있습니다. DSP은 캠페인 계층에서 가장 엄격한 빈도 제한을 준수합니다.

## 사용자 기반 타겟팅

사용자 기반 타겟팅을 사용하면 데스크탑 및 모바일에서 고객을 찾을 수 있습니다.

### 사용자 기반 타겟팅 활성화

* **캠페인:** 새 캠페인을 만들 때 [!UICONTROL Cross-Device Level] 설정 활성화 &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot;을 선택하고 장치 그래프를 선택합니다. 지정된 장치 그래프는 배치 수준에서 교차 장치 타깃팅과 사용자 기반 빈도 관리에 모두 사용됩니다.

자세한 내용은 [캠페인 설정](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **배치:** 지정된 장치 그래프를 사용하는 캠페인에서 배치에 대한 대상 대상을 선택하면 [!UICONTROL Cross-Device Targeting] 옵션을 사용하면 지정된 세그먼트에 없는 장치라도 개인의 알려진 모든 장치(캠페인 설정에 지정된 장치 그래프에 따라)에 걸쳐 타깃팅을 확장할 수 있습니다.

### 사용자 기반 타깃팅에 대한 보고 설정

사용자 지정 보고서에 다음 지표를 포함할 수 있습니다.

* **노출 횟수:** (에서 [!UICONTROL Build Your Report] 섹션 [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) 장치 그래프(원래 대상 세그먼트 내에서 찾을 수 없음)를 활용하여 전달되는 증분 노출 횟수입니다. 이 지표는 타사 장치 그래프 사용과 관련된 적용 가능한 비용을 계산하는 데에도 사용됩니다.

   기간 동안 확장된 노출 횟수의 비용을 결정하려면 를 포함하는 사용자 지정 보고서를 실행하십시오 [!UICONTROL Extended Impressions] 열을 선택한 다음 총 확장 노출 수에 $0.00035($0.35/1000 노출 횟수)를 곱합니다.

   총 비용은 또한 [!UICONTROL Billable Other Net Spend] 열(아래) [!UICONTROL Metrics] > [!UICONTROL Spend]) 포함되어 있을 수 있습니다.

* **장치 그래프:** (에서 [!UICONTROL Build Your Report] 섹션 [!UICONTROL Dimensions] > [!UICONTROL Campaign]) 특정 캠페인, 패키지 또는 배치에 대해 선택한 장치 그래프입니다.

## 사용자 기반 속성 측정

*Advertising Cloud 전환 추적만 있는 광고주*

사용자 기반 속성을 사용하면 미디어 노출이 발생한 장치와 다른 장치에서 발생한 전환을 지정할 수 있습니다. 사이트에서 Advertising Cloud 변환 픽셀을 구현한 광고주를 위해 DSP, Advertising Cloud Search 및 Advertising Cloud Creative에서 사람 기반 속성 측정을 사용할 수 있습니다.

### 사용자 기반 속성 측정 활성화

교차 장치 속성 측정을 활성화하려면 [!DNL Adobe] 계정 팀입니다. 대상 [!DNL Adobe Device Co-op] 계정, 서명된 [!DNL Adobe Device Co-op] 계약 및 Experience Cloud [!DNL Organization ID] (이전에는 [!DNL IMS org ID]).

광고주 계정이 속성 측정에 장치 그래프를 사용하도록 구성되어 있는지 확인하려면:

1. 주 메뉴에서 **[!UICONTROL Settings]>[!UICONTROL Advertiser]**.
1. 광고주 행 위에 커서를 놓고 **[!UICONTROL Edit]**.
1. 에서 [!UICONTROL Integrations] 광고주 설정의 섹션을 보려면 [!UICONTROL Cross-Device Attribution] 설정이 활성 상태입니다.

   활성 통합의 경우 장치 그래프가 표시됩니다.

### 교차 장치 전환 속성에 대한 전환 보고서 설정

#### 전환 보고서 설정

속성 측정에 대해 장치 그래프가 활성화되면 [!UICONTROL Conversion] 보고서에는 [!UICONTROL Cross-Device Breakout] 설정 을 사용하면 다음을 포함하여 각 전환 지표에 대해 최대 3개의 개별 열을 포함할 수 있습니다.

* &lt;*전환*>[!UICONTROL (tp)]: 동일한 장치 전환과 장치 간 전환(해당하는 경우)을 모두 포함하는 총 전환(총 사람)을 포함합니다. 보고서에서 &quot;[!UICONTROL (tp)]전환 경로의 전환 지표 이름, 규칙 유형 및 전환 유형에 추가됩니다(예: &quot;Responses(le)(tl)(tp))).

* &lt;*전환*>[!UICONTROL (sd)]: (선택 사항) 전환 경로에서 단일 장치만 추적된 전환만 포함합니다. 보고서에서 &quot;[!UICONTROL (sd)]전환 경로의 전환 지표 이름, 규칙 유형 및 전환 유형에 추가됩니다(예: &quot;Response(le)(tl)(sd))).

* &lt;*전환*>[!UICONTROL (xd)]: (선택 사항) 전환 경로에서 두 개 이상의 장치가 추적된 전환만 포함합니다. 보고서에서 &quot;[!UICONTROL (xd)]전환 경로의 전환 지표 이름, 규칙 유형 및 전환 유형에 추가됩니다(예: &quot;응답(le)(tl)(xd))).

#### 전환 보고서를 해석하는 방법

교차 장치([!UICONTROL (xd)]/[!UICONTROL (tl)])에서 높낮이로, 평균보다 높은 교차 장치 전환을 유도하는 작업을 이해할 수 있습니다. 이를 통해 메시지 및 채널 투자를 사용자 행동에 맞추기 위해 광고 또는 타깃팅 전략을 알릴 수 있습니다.

* 패키지 - 가장 많은 총 전환을 유도하는 패키지와 높은 비율의 교차 장치 전환이 있는 패키지를 확인합니다. 따라서 초점을 맞춰야 하는 비용을 어디에 투입할 것인지 이해하는 데 도움이 됩니다.

* 배치 - 배치 성능과 속성을 비교합니다(예: 모바일 웹 광고가 데스크탑에서 전환을 유도할 수 있음). 속성에 대한 장치 그래프가 없으면 모바일 웹 게재가 데스크탑 변환에 미치는 영향을 누락할 수 있고, 사용자 대다수가 모바일 웹이 아닌 데스크탑에서 전환하는 경우 표시되지 않을 수 있습니다.

* 광고 - 전환율을 높이는 광고를 발견하고 웹 브라우저와 모바일 앱 환경 모두에서 값과 영향을 수량화합니다.

* 사이트 - 사이트를 수동으로 완전히 제외하는 대신 여러 사이트에서 최적화합니다. 웹 사이트에서 장치 간 전환을 유도하는 경우 이러한 동작이 발생하는 장치를 확인할 수 있습니다.

* 거래 - 교차 장치 전환을 제공하는 인벤토리 거래를 확인한 다음, 그러한 거래에 더 많은 장치와 채널을 포함하도록 타깃팅을 확장해야 하는지 여부를 결정함으로써 수동 최적화를 개선합니다.

>[!MORELIKETHIS]
>
>* [보고서 설정](/help/dsp/reports/report-settings.md)
>* [캠페인 설정](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [패키지 설정](/help/dsp/campaign-management/packages/package-settings.md)
>* [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md)


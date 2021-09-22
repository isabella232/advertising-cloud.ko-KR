---
title: 사용자 지정 목표
description: 최저 CPA 또는 가장 높은 ROAS에 맞게 최적화된 패키지에서 성공 이벤트를 정의하는 사용자 지정 목표에 대해 알아봅니다.
feature: DSP Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# 사용자 지정 목표

사용자 지정 목표는 광고주가 비즈니스 목표를 충족하는 데 필요한 성공 이벤트를 정의합니다. 최적화 목표 &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; 또는 &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot;를 사용하는 각 패키지에는 전체 최적화 목표를 달성하는 데 도움이 되는 사용자 지정 목표가 포함되어야 합니다. Advertising Cloud Search에서 사용자 지정 목표를 *목표*&#x200B;로 만들 수 있습니다.

![사용자 지정 목표](/help/dsp/assets/objective-goals.png)

각 사용자 지정 목표는 하나 이상의 지표 또는 *거래 속성* 과 이러한 거래 속성의 상대 가중치로 구성됩니다. 사용 가능한 트랜잭션 속성에는 Advertising Cloud 변환 픽셀을 사용하여 Adobe Analytics을 통해 추적된 모든 지표가 포함됩니다.

>[!NOTE]
>
>* [!DNL Analytics] Advertising Cloud 최적화에 차원 및 세그먼트를 사용할 수 없습니다.
>* DSP에서 Analytics 이벤트를 사용하려면 Adobe 계정 관리자와 함께 광고주 수준 통합을 구성합니다.
>* [!DNL Analytics] 사용자 지정 이벤트는 다음 이름 지정 규칙을 따릅니다.  `custom_event_[*event #*]_[*Analytics report suite ID*]`. 예: `custom_event_16_examplersid`


예를 들어 다음 세 가지 지표(거래 속성)가 캠페인 중 하나의 특정 패키지와 관련이 있다고 가정합니다. 20USD로 &quot;PDF 다운로드&quot;, &quot;이메일 등록&quot;(30USD) 및 &quot;주문 확인&quot;(40USD) 값) 고객 작업의 1회 통화 값에 따라 가중치를 제공하려는 경우 속성의 상대적 가중치는 1, 2 및 1.5가 됩니다.

사용자 지정 목표를 구성하는 방법에 대한 팁은 [사용자 지정 목표를 만드는 우수 사례](custom-goal-best-practices.md)를 참조하십시오.

[사용자 지정 목표](custom-goal-create.md)를 만들면 [Adobe Sensei을 사용하여 보고 및 알고리즘 최적화를 위해 패키지](/help/dsp/campaign-management/packages/package-settings.md)에 할당할 수 있습니다.

>[!MORELIKETHIS]
>
>* [사용자 지정 목표 만들기](custom-goal-create.md)
>* [사용자 지정 목표 구축에 대한 우수 사례](custom-goal-best-practices.md)
>* [최적화 목표 및 사용 방법](optimization-goals.md)
>* [패키지 설정](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP이 캠페인을 최적화하는 방법](optimization-how-dsp-optimizes-campaigns.md)


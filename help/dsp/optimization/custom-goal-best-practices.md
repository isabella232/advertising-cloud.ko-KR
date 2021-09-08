---
title: 사용자 지정 목표 구축에 대한 우수 사례
description: 성공 이벤트를 정의하기 위한 사용자 지정 목표를 작성하는 모범 사례를 알아봅니다.
feature: Optimization, Best Practices
exl-id: 54b16325-4b72-48a3-a2e0-4e342229211c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# 사용자 지정 목표 구축에 대한 우수 사례

## 단일 속성을 사용한 사용자 지정 목표

다음 예는 단일 속성(지표)을 타깃팅하는 목표를 구성하는 방법을 보여줍니다.

### 최적화 목표가 &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot;인 캠페인의 예

캠페인 목표가 매출([!UICONTROL Highest ROAS - Custom Goal])인 경우 사용자 지정 목표(목표)에는 가중치가 1인 &quot;[!UICONTROL Revenue]&quot; 속성이 포함됩니다.

![단일 속성을 사용하는 ROAS 사용자 지정 목표의 예](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> 1의 [!UICONTROL Property Weight]은(는) 추적되는 수입의 각 $1에 대해 1의 값과 같습니다.
>
> 예를 들어 가중치가 1인 $250 전환은 $250로 보고됩니다. 전환 지표에 0.5의 가중치가 지정된 경우, $250 전환이 Advertising Cloud에서 $125로 보고됩니다($250 전환 * 0.5 [!UICONTROL Property Weight] = $125).

### 최적화 목표가 &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot;인 캠페인의 예

캠페인 목표가 획득당 최소 비용(CPA)이고 하나의 성공 이벤트만 필요한 경우 해당 지표(다음 예에서 &quot;애플리케이션 제출&quot;)를 포함하게 됩니다. 가장 좋은 방법은 가중치를 1로 설정하는 것입니다.

![단일 속성을 사용한 CPA 사용자 지정 목표 예제](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> 하나의 [!UICONTROL Property Weight] 은 추적된 각 변환에 대해 1의 값과 같습니다.
>
> 예를 들어 10개의 애플리케이션 제출 전환이 추적되면 10개의 애플리케이션 제출 전환이 보고됩니다.  전환 지표에 0.5의 가중치가 지정된 경우 10개의 전환은 Advertising Cloud에서 5개로 보고됩니다(10개의 전환 * 0.5 [!UICONTROL Property Weight] = 5).

## 여러 속성을 사용한 사용자 지정 목표

사용자 지정 목표에 여러 속성을 사용하는 두 가지 시나리오가 있습니다.

* 캠페인 목표에는 여러 개의 성공 이벤트가 있습니다. 예를 들어 두 개 이상의 온사이트 작업을 위해 광고를 하고 있는 경우 모든 것이 CPA 목표에 귀속됩니다. 다음 예제 목표에는 세 개의 개별 속성(PDF 다운로드, 연락처 및 이메일 등록)이 포함되어 있으며 각 속성은 각 속성의 중요도가 같음을 [!DNL Adobe Sensei] 알고리즘에 알려줍니다. 비용이나 중요도가 다른 속성을 포함하는 경우 그에 따라 상대적 가중치를 조정할 수 있습니다.

   ![여러 속성이 있는 사용자 지정 목표 예](/help/dsp/assets/custom-goal-multiple-properties.png)

* 사용자 지정 목표에 있는 단일 속성은 최적화된 성능에 필요한 하루에 최소 10개의 전환을 달성하지 않습니다. 이는 최소 일별 패키지 지출 또는 제한된 자연어 전환 횟수로 인해 발생할 수 있습니다. 사용자 지정 목표에 추가 지원 속성을 추가하면 하루에 10개의 전환 임계값을 달성하는 데 도움이 될 수 있습니다. 10개의 지원 이벤트는 각 가중치가 1개(1) 미만인 경우에도 패키지가 10/일 임계값을 충족하는 데 도움이 될 수 있습니다. 하지만 그렇게 많은 이벤트를 추가할 필요는 없습니다.

   사용자 지정 목표에 지원 속성을 추가할 때 기본 성공 이벤트에 대한 상대적 중요도에 따라 가중치를 매기고 데이터 포인트의 양을 기억하십시오. 이렇게 하면 Adobe Sensei 알고리즘에서 여러 속성의 균형을 맞추고 목표를 위해 최적화할 수 있습니다.

   다음 예제 목표에는 각각 다른 가중치가 있는 세 개의 속성이 포함되어 있습니다. 애플리케이션 제출 = 1, 애플리케이션 시작 = 0.1, 광고주 랜딩 페이지 = 0.01. 즉, 각 애플리케이션 제출 전환의 값은 평균 10개의 애플리케이션 시작 전환 및 100개의 광고주 랜딩 페이지 전환과 동일합니다.

   ![여러 속성이 있는 사용자 지정 목표 예](/help/dsp/assets/custom-goal-multiple-properties2.png)

   대신, 응용 프로그램 제출과 동일하게 랜딩 페이지 방문 횟수를 가중처리하면 자연스럽게 더 높은 랜딩 페이지 방문 수가 목표를 압도하고 랜딩 페이지 방문 횟수로 왜곡할 수 있습니다.<!--reword-->

>[!MORELIKETHIS]
>
>* [사용자 지정 목표](custom-goal-about.md)
>* [사용자 지정 목표 만들기](custom-goal-create.md)
>* [최적화 목표 및 사용 방법](optimization-goals.md)
>* [패키지 설정](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP이 캠페인을 최적화하는 방법](optimization-how-dsp-optimizes-campaigns.md)


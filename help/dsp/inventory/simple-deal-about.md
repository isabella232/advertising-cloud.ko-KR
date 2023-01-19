---
title: 정보 [!UICONTROL Simple Ad Serving]
description: 알아보기 [!UICONTROL Simple Ad Serving] 은 이벤트 추적 픽셀을 사용합니다.
feature: DSP Simple Ad Serving
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# 정보 [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] 지정된 게시자와 전용 단일 배치를 사용하여 단일 광고 유형에 대해 보장되고 결정되지 않은 광고 전달 및 보고를 제공합니다. 사용 [!DNL Simple Ad Serving] 거래 ID를 통해 거래를 실행할 수 없는 경우. 모든 타겟팅, 예산 간격 및 최대 가용량, 빈도 제한은 게시자가 처리합니다. 이벤트 추적 픽셀을 통해 이러한 거래를 실행합니다.

사용 [!UICONTROL Simple Ad Serving], 각 광고는 게시자(사이트 서버)가 직접 제공하며, DSP은 게시자에게 전송할 이벤트 추적 픽셀을 제공하며, 게시자는 DSP 광고에 대한 픽셀과 트래픽을 구현해야 합니다. 인벤토리 유형에 따라 이벤트 픽셀이 노출, 클릭스루 및 비디오 재생 이벤트를 측정합니다.

다음 광고 유형을 사용할 수 있습니다.

* 데스크탑 표준 프리롤
* 태블릿 및 모바일 표준 프리롤
* 연결된 TV 표준 프리롤
* 디스플레이
* 오디오

을(를) 만들 수 있습니다 [!UICONTROL Simple Ad Serving] 거래 [!UICONTROL Inventory] > [!UICONTROL Deals] 보기. DSP에서는 하위 유형 &quot;[!DNL Simple ad serving]&quot;&quot;을 참조하십시오. 배치는 거래를 타겟팅하지만 추가 타겟팅, 예산 또는 빈도 캡핑을 허용하지 않습니다. 거래 이름, CPM, 노출 횟수 및 비행 날짜와 같은 일부 거래 설정만 편집할 수 있습니다.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] 배치는 계정의 사용 가능한 자금 또는 캠페인 및 패키지 예산을 준수하지 않습니다. 그러나, 지출은 추적되고 그러한 예산에 반영됩니다. CPM이 $0인 경우에도 이벤트 데이터가 항상 추적됩니다.

>[!MORELIKETHIS]
>
>* [만들기 [!UICONTROL Simple Ad Serving] 거래](simple-deal-create.md)
>* [편집 [!UICONTROL Simple Ad Serving] 거래 설정](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] 설정](simple-deal-settings.md)
>* [거래에 대한 세부 보고서 보기](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->

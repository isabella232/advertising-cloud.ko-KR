---
title: '[!UICONTROL CCPA Opt-out-of-Sale] 세그먼트 및 보고서 정보'
description: CCPA 판매 중지 요청에서 ID를 추적하기 위해 세그먼트를 만들고 ID의 보고서를 검색하는 방법에 대해 알아봅니다.
feature: CCPA, Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# [!UICONTROL CCPA Opt-out-of-Sale] 세그먼트 및 보고서 정보

[CCPA 판매 중지 세그먼트](ccpa-opt-out-segment-create.md)를 만들고 구현하여 CCPA(캘리포니아 소비자 개인 정보 보호법)에 따라 웹 사이트의 소비자 판매 중지 요청에서 사용자 ID를 추적할 수 있습니다. 사용자는 무한정 CCPA 판매 중지 세그먼트에 남아 있습니다.

세그먼트 픽셀 태그가 구현되면 Advertising Cloud은 광고주를 대신하여 ID 풀을 수집하기 시작합니다.

## 소비자 옵트아웃 보고서

Advertising Cloud은 고객이 계정에 대해 판매 중지 요청을 제출한 월별 ID에 대한 보고서를 생성합니다. 이 데이터는 CCPA 판매 중지 세그먼트를 사용하여 캡처된 요청과 Advertising Cloud DSP에서 만든 요청 및 Privacy Service API를 통해 작성된 모든 제출을 통합합니다.  보고서는 이전 월에 대한 각 달의 1일에 생성됩니다. 예를 들어 6월의 월별 사용자 목록은 7월 1일에 제공됩니다.

각 보고서는 GZIP 형식으로 압축된 탭으로 구분된 텍스트 파일로 사용할 수 있습니다. CCPA 판매 중지 세그먼트에 캡처된 사용자 ID는 세그먼트 및 광고주별로 식별됩니다.

[Advertising Cloud DSP 내에서 또는 Advertising Cloud [!DNL Trafficking API]를 사용하여 이전 3개월 내에 만든 월별 보고서](ccpa-opt-out-segment-report-retrieve.md)에 대한 링크를 검색할 수 있습니다. 각 링크는 7일 동안 유효하지만 고객이 하나를 검색하려고 할 때마다 새로 고침됩니다.

>[!MORELIKETHIS]
>
>* [캘리포니아 소비자 개인 정보 보호법을 위한 Adobe Advertising Cloud 지원: 소비자 옵트아웃 지원](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [세그먼트 만들기 및  [!UICONTROL CCPA Opt-Out-of-Sale] 구현](ccpa-opt-out-segment-create.md)
>* [소비자 판매 중지 보고서 검색](ccpa-opt-out-segment-report-retrieve.md)
>* [대상자 관리 기본 정보](audience-about.md)


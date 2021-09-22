---
title: CCPA 판매 중지 세그먼트 만들기 및 구현
description: 소비자 옵트아웃 요청에서 사용자 ID를 추적하는 세그먼트를 만들고 구현하는 방법을 알아봅니다.
feature: CCPA, DSP Segments
exl-id: aebe0c5b-382f-4e4a-b145-c32f32d216ca
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# CCPA 판매 중지 세그먼트 만들기 및 구현

CCPA(California Consumer Privacy Act)에 따라 웹 사이트의 소비자 판매 중지 요청에서 사용자 ID를 추적하는 세그먼트를 만들 수 있습니다. 사용자는 무한정 CCPA 판매 중지 세그먼트에 남아 있습니다.

세그먼트 픽셀 태그가 구현되면 Advertising Cloud은 광고주를 대신하여 ID 풀을 수집하기 시작합니다.

>[!NOTE]
>
>* Adobe Experience Platform Privacy Service API를 사용하여 CCPA 판매 중지 요청을 Advertising Cloud에 전달하는 방법에 대한 자세한 내용은 [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)을 참조하십시오.
>* CCPA 판매 중지 이벤트 추적과 관련이 없는 목적으로 웹 페이지를 방문하는 사용자와 데스크탑, 모바일 및 CTV 장치의 광고에 노출된 사용자를 추적하려면 [사용자 지정 세그먼트](/help/dsp/audiences/custom-segment-create.md)를 만드십시오.


1. 세그먼트를 만듭니다.

   1. 기본 메뉴에서 **대상 > 세그먼트**&#x200B;를 클릭합니다.

   1. 데이터 테이블 위에서 **[!UICONTROL Create]** 을 클릭합니다.

   1. 고유한 **[!UICONTROL Segment Name]** 을 입력합니다.

      권장 세그먼트 이름: &quot;&lt;*광고주 이름* - CCPA 판매 중지&quot;(예: &quot;Acme - CCPA 판매 중지&quot;)

   1. [!UICONTROL Segment Type]에 대해 **[!UICONTROL CCPA Opt-out of sale]**&#x200B;을 선택합니다.

   1. 클릭 **[!UICONTROL Save]**.

1. 픽셀 태그를 복사하여 세그먼트를 추적합니다.

   1. **[!UICONTROL Audiences]>[!UICONTROL Segments]**&#x200B;로 돌아갑니다.

   1. 세그먼트 행에서 새 세그먼트 위에 커서를 놓고 **[!UICONTROL Get pixel]** 을 클릭합니다.

   1. 이미지 픽셀(`<img src="https://rtd-tm.everesttech.net"`부터)을 복사하여 데스크탑 및 모바일 방문자의 사용자 ID를 웹 페이지로 수집합니다.

   1. 회사에서 CCPA 판매 중지 요청(예: 동의 관리 플랫폼 사용)을 추적하는 데 사용하는 메커니즘을 사용하여 배포를 위한 광고주 또는 웹 사이트 담당자에게 태그를 제공합니다.

      광고주의 IT 부서나 다른 그룹은 태그 배포를 예약하거나 알려주어야 할 수 있습니다.

      픽셀이 구현되면 Advertising Cloud은 광고주를 대신하여 ID 풀을 수집하기 시작합니다.

      구현 선택 및 로직은 광고주에게 달하지만 광고주가 픽셀을 실행하는 방법의 예는 다음과 같습니다.

      1. 소비자가 광고주의 홈페이지에 접속한다.
      1. 소비자는 광고주의 &quot;CCPA 판매 중지&quot; 버튼을 찾아 클릭합니다.
      1. 소비자에게는 광고주가 작동하는 서비스 공급자 목록이 표시됩니다.
      1. 소비자가 Adobe Advertising Cloud에 데이터 판매를 거부하도록 확인란을 선택합니다.

         이 작업은 픽셀을 트리거하여 지정된 &quot;[!UICONTROL CCPA Opt-out of sale]&quot; 세그먼트 내에서 소비자의 쿠키 ID를 수집합니다.

>[!MORELIKETHIS]
>
>* [캘리포니아 소비자 개인 정보 보호법을 위한 Adobe Advertising Cloud 지원: 소비자 옵트아웃 지원](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [세그먼트  [!UICONTROL CCPA Opt-out-of-Sale] 및 보고서 정보](ccpa-opt-out-about.md)
>* [소비자 판매 중지 보고서 검색](ccpa-opt-out-segment-report-retrieve.md)
>* [사용자 지정 세그먼트 만들기 및 구현](custom-segment-create.md)
>* [대상자 관리 기본 정보](audience-about.md)


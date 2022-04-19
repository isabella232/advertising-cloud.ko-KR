---
title: 추가 [!DNL Analytics for Advertising Cloud] 매크로 [!DNL Flashtalking] 광고 태그
description: 추가 이유 및 방법 알아보기 [!DNL Analytics for Advertising Cloud] 매크로 [!DNL Flashtalking] 광고 태그
feature: Integration with Adobe Analytics
source-git-commit: 915eea83b2dd246f0f512981efca7ac481cf0c6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# 추가 [!DNL Analytics for Advertising Cloud] 매크로 [!DNL Flashtalking] 광고 태그

*Advertising Cloud-Adobe Analytics 통합만 있는 광고주*

*Advertising Cloud DSP에만 적용 가능*

에서 광고 태그를 사용하는 경우 [!DNL Flashtalking] Advertising Cloud DSP 광고의 경우, Advertising Cloud용 Analytics 매개 변수를 랜딩 페이지 URL에 추가합니다. 매개 변수를 사용하면 Advertising Cloud에서 광고에 대한 클릭 데이터를 Adobe Analytics에 보낼 수 있습니다.

매크로 사용 [!DNL Flashtalking] 다음 유형의 디스플레이 및 비디오 광고 [!DNL Analytics for Advertising Cloud] 구현:

* **를 사용하는 광고주 [!DNL Adobe] [!DNL Analytics for Advertising Cloud] 웹 사이트에 구현된 JavaScript 코드**: 추가 매크로 없이 Advertising Cloud을 통해 구입하는 광고에서 Adobe Analytics에 몇 가지 클릭스루 데이터가 표시됩니다. 타사 쿠키를 지원하지 않아 JavaScript 코드를 통해 캡처되지 않은 브라우저에서 클릭스루 데이터를 캡처하려면 다음 섹션에 매크로를 추가합니다. [!DNL Flashtalking] 광고 태그입니다.

>[!NOTE]
>
>JavaScript 코드는 쿠키를 계속 사용할 수 있는 동안에만 클릭 추적을 위한 솔루션입니다. Advertising Cloud에서 쿠키를 중단하면 다음 매크로를 구현해야 합니다.

* **웹 사이트에서 [!DNL Analytics for Advertising Cloud] JavaScript 코드를 대신 [!DNL Analytics] 클릭스루 데이터만 위한 서버측 전달** (뷰스루 데이터 없음): 다음 매크로는 Advertising Cloud을 통해 구매하는 광고에서 시작되는 온사이트 클릭 활동을 보고하는 데 필요합니다.

## 광고 태그 표시

내 [!DNL Flashtalking] 광고 태그 설정에서 다음 매크로를 클릭스루 URL의 끝에 추가합니다 `Clicktag` 필드:

```html
?[ftqs:[AdobeAMO]]
```

예:  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

![예 [!DNL Flashtalking] 광고 태그 설정](/help/integrations/assets/macro-flashtalking-display-ad.png)

## 비디오 광고 태그

내 [!DNL Flashtalking] 광고 태그 설정에서 다음 매크로를 클릭스루 URL의 끝에 추가합니다 `Clicktag` 필드:

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

예:  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

![예 [!DNL Flashtalking] 광고 태그 설정](/help/integrations/assets/macro-flashtalking-video-ad.png)

>[!MORELIKETHIS]
>
>* [개요 [!DNL Analytics for Advertising Cloud]](overview.md)


<!-- >* [Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags](macros-google-campaign-manager.md) -->

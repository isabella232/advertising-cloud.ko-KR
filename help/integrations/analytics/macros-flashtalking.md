---
title: 추가 [!DNL Analytics for Advertising] 매크로 [!DNL Flashtalking] 광고 태그
description: 추가 이유 및 방법 알아보기 [!DNL Analytics for Advertising] 매크로 [!DNL Flashtalking] 광고 태그
feature: Integration with Adobe Analytics
exl-id: 4b060668-723c-4cd2-b70e-409501ec67de
source-git-commit: 04b57aec29e2d737bc33375614137543bead240c
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# 추가 [!DNL Analytics for Advertising] 매크로 [!DNL Flashtalking] 광고 태그

*Adobe Advertising-Adobe Analytics 통합 전용 광고주*

*Advertising DSP에만 적용 가능*

에서 광고 태그를 사용하는 경우 [!DNL Flashtalking] advertising DSP 광고의 경우, 랜딩 페이지 URL에 Analytics for Advertising 매개 변수를 추가합니다. 매개 변수 레코드 `s_kwcid` 및 `ef_id` 랜딩 페이지 URL에서 쿼리 문자열 매개 변수를 사용하므로 Adobe 광고에서 광고에 대한 클릭 데이터를 Adobe Analytics에 보낼 수 있습니다.

매크로 사용 [!DNL Flashtalking] 다음 유형의 디스플레이 및 비디오 광고 [!DNL Analytics for Advertising] 구현:

* **를 사용하는 광고주 [!DNL Adobe] [!DNL Analytics for Advertising] 웹 사이트에 구현된 JavaScript 코드**: JavaScript 코드가 이미 `s_kwcid` 및 `ef_id` 쿼리 문자열 매개 변수. 그러나 매크로를 사용하면 타사 쿠키가 지원되지 않을 때 클릭 기반 전환을 포함하도록 추적을 확장합니다. 가장 좋은 방법은 다음 섹션에 있는 매크로를 광고 태그에 추가하여 JavaScript 코드를 통해 캡처되지 않은 추가 클릭스루 데이터를 캡처하는 것입니다.

>[!NOTE]
>
>JavaScript 코드는 쿠키를 계속 사용할 수 있는 동안에만 클릭 추적을 위한 솔루션입니다. 쿠키가 중단되면 다음 매크로를 구현해야 합니다.

* **웹 사이트에서 [!DNL Analytics for Advertising] JavaScript 코드를 대신 [!DNL Analytics] 클릭스루 데이터만 위한 서버측 전달** (뷰스루 데이터 없음): 다음 매크로는 Adobe 광고를 통해 구입하는 광고에서 파생되는 온사이트 클릭 활동을 보고하는 데 필요합니다.

## 광고 태그 표시

내 [!DNL Flashtalking] 광고 태그 설정에서 다음 매크로를 클릭스루 URL의 끝에 추가합니다 `Clicktag` 필드:

```html
?[ftqs:[AdobeAMO]]
```

예:  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## 비디오 광고 태그

내 [!DNL Flashtalking] 광고 태그 설정에서 다음 매크로를 클릭스루 URL의 끝에 추가합니다 `Clicktag` 필드:

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

예:  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [개요 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe 광고 ID 사용 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [추가 [!DNL Analytics for Advertising] 매크로 [!DNL Google Campaign Manager 360] 광고 태그](/help/integrations/analytics/macros-google-campaign-manager.md)


---
title: 사용 [!DNL Last Event Service] JavaScript 라이브러리 [!DNL Web SDK]
description: 를 사용하여에서 전환하는 단계를 알아봅니다. [!DNL Analytics] [!DNL visitorAPI] 라이브러리 [!DNL Experience Platform] [!DNL Web SDK] 라이브러리 [!DNL Analytics for Advertising] 구현 을 참조하십시오.
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# 사용 [!DNL Last Event Service] Adobe Experience Platform을 사용한 JavaScript 라이브러리 [!DNL Web SDK]

*Adobe Advertising-Adobe Analytics 통합 전용 광고주*

조직에서 이전 Adobe Analytics을 사용하는 경우 `visitorAPI.js` 데이터 수집을 위한 라이브러리에서는 선택적으로 를 사용하여 전환할 수 있습니다 [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) 라이브러리(`alloy.js`). 여기에서 다음을 통해 다양한 Experience Cloud 서비스와 상호 작용할 수 있습니다. [!DNL Edge Network].

다음 [!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript 라이브러리는 있는 그대로 뷰스루 및 클릭스루 이벤트를 기록하고 보충 ID( )를 사용하여 연결된 전환과 결합합니다`SDID`). 다음 [!DNL Web SDK] 그러나 라이브러리는 [!DNL stitch ID]. 를 사용하려면 [!DNL Web SDK] 대상 [!DNL Analytics for Advertising]를 수정하려면 1)를 [!DNL Last Event Service] 태깅 합니다. [!DNL Web SDK] `sendEvent` 그에 따라 명령을 실행합니다.

## 1단계: 편집 [!DNL Last Event Service] 태그 지정 `[!DNL StitchID]`

에서 [!DNL Analytics for Advertising] [!DNL Last Event Service] 태그를 웹 페이지에서 사용하고 코드를 추가하여 다음을 생성합니다 `[!DNL StitchID]` 라이브러리에 번들로 제공되는 임의의 ID 생성기 사용.

**기존 태그:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**새 태그:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## 2단계: 사용 [!DNL Web SDK] 를 보내려면 [!DNL StitchID] 을 위한 XDM 데이터 [!DNL Analytics]

다음 속성을 [!DNL Web SDK] `sendEvent` 명령 보내기 [!DNL StitchID] to [!DNL Experience Edge] 로서의 [!DNL Experience Data Model] (XDM) 데이터 [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] 은 값을 `SDID`.

**추가할 속성:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**예:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [개요 [!DNL Analytics for Advertising]](overview.md)
>* [용 JavaScript 코드 [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)


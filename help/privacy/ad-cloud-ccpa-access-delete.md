---
title: '캘리포니아 소비자 개인 정보 보호법을 위한 Adobe Advertising Cloud 지원 : 소비자 데이터 액세스 및 삭제 지원'
description: 지원되는 데이터 요청 유형, 필수 설정 및 필드 값, 레거시 제품 ID를 사용한 API 액세스 요청 및 반환된 데이터 필드의 예에 대해 알아봅니다.
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
source-git-commit: 2e0395dc1e5aa52adc83c1aaea49793fd5555390
workflow-type: tm+mt
source-wordcount: '1090'
ht-degree: 0%

---

# 캘리포니아 소비자 개인 정보 보호법을 위한 Adobe Advertising Cloud 지원: 소비자 데이터 액세스 및 삭제 지원

*Adobe Advertising Cloud Search, Adobe Advertising Cloud Creative, Adobe Advertising Cloud DSP 및 Adobe의 경우[!DNL Media Optimizer DCO]*

>[!IMPORTANT]
>
>이 문서의 내용은 법률적인 조언이 아니며, 법률적인 조언을 대체하지 않습니다. 캘리포니아 소비자 개인 정보 보호법에 대한 법률 자문을 구하십시오.

CCPA(California Consumer Privacy Act)는 2020년 1월 1일부터 시행된 California의 새로운 개인 정보 보호법입니다. CCPA는 캘리포니아 주민에게 개인 정보에 대한 새로운 권리를 제공하고 캘리포니아에서 사업을 하는 특정 업체들에 데이터 보호 책임을 부과합니다. CCPA는 소비자에게 개인 정보를 액세스하고 삭제할 수 있는 권한과 제3자에게 &quot;개인 정보 판매&quot;의 자격이 되는 특정 활동을 거부할 수 있는 권한을 제공합니다.

기업은 Adobe Experience Cloud이 귀하를 대신하여 처리하고 저장하는 개인 데이터를 결정합니다.

Adobe Advertising Cloud은 서비스 제공업체로서, 개인 정보에 대한 액세스 및 삭제 요청 관리 및 개인 정보 판매 거부 요청 관리를 포함하여 Advertising Cloud 제품 및 서비스 사용에 적용되는 CPA에 따른 책임을 이행하도록 비즈니스를 지원합니다.

이 문서에서는 Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP(Demand Side Platform) 및 [!DNL Media Optimizer DCO] — 서비스 제공자로서 — Adobe을 사용하여 개인 정보에 액세스하고 삭제할 수 있는 소비자의 권한을 지원합니다 [!DNL Experience Platform Privacy Service API] 및 [!DNL Privacy Service UI].

Advertising Cloud DSP이 개인 정보 판매를 옵트아웃할 소비자 권한을 지원하는 방법에 대한 자세한 내용은 [캘리포니아 소비자 개인 정보 보호법을 위한 Adobe Advertising Cloud 지원: 소비자 옵트아웃 지원](/help/privacy/ad-cloud-ccpa-opt-out-of-sale.md).

CCPA를 위한 Adobe 개인 정보 서비스에 대한 자세한 내용은 [Adobe 개인 정보 보호 센터](https://www.adobe.com/privacy/ccpa.html).

## Advertising Cloud에 대해 지원되는 데이터 요청 유형

Adobe Experience Platform은 기업이 다음 작업을 완료할 수 있는 기능을 제공합니다.

* 내에서 소비자의 쿠키 수준 데이터 또는 장치 ID 수준 데이터(모바일 앱의 광고)에 액세스합니다 [!DNL Search], [!DNL Creative], [!DNL DSP], 또는 [!DNL DCO].
* 내에 저장된 쿠키 수준 데이터 삭제 [!DNL Search], [!DNL Creative], [!DNL DSP], 또는 [!DNL DCO] 브라우저를 사용하는 소비자의 경우 내에 저장된 ID 수준 데이터를 삭제하거나 [!DNL DSP] 를 사용하도록 선택할 수 있습니다.
* 하나 또는 모든 기존 요청의 상태를 확인합니다.

## Advertising Cloud에 대한 요청을 전송하기 위한 필수 설정

Advertising Cloud에서 소비자 개인 정보에 액세스하고 삭제를 요청하려면 다음을 수행해야 합니다.

1. JavaScript 라이브러리를 배포하여 고객의 쿠키를 검색하고 제거합니다. 같은 라이브러리 `AdobePrivacy.js`는 모든 Adobe Experience Cloud 솔루션에 사용됩니다.

   >[!IMPORTANT]
   >
   >일부 Experience Cloud 솔루션에 대한 요청에는 JavaScript 라이브러리가 필요하지 않지만 Advertising Cloud에 요청하려면 JavaScript 라이브러리가 필요합니다.

   고객이 회사의 개인 정보 포털과 같은 액세스 및 삭제 요청을 제출할 수 있는 웹 페이지에 라이브러리를 배포해야 합니다. 라이브러리는 Adobe 쿠키(네임스페이스 ID)를 검색하는 데 도움이 됩니다. `gsurferID`)를 사용하여 액세스 및 삭제 요청의 일부로 이러한 ID를 제출할 수 있습니다. [!DNL  Adobe Experience Platform Privacy Service API].

   고객이 개인 데이터를 삭제하도록 요청하면 라이브러리가 고객의 브라우저에서 고객의 쿠키도 삭제합니다.

   >[!NOTE]
   >
   >개인 데이터를 삭제하는 것은 옵트아웃과 다르므로, 대상 세그먼트로 최종 사용자의 타깃팅을 중지합니다. 그러나 소비자가 개인 데이터를 [!DNL Creative], [!DNL DSP], 또는 [!DNL DCO]또한 라이브러리는 세그먼트 타깃팅에서 고객을 옵트아웃하기 위해 Advertising Cloud에 요청을 보냅니다. 광고 문헌 [!DNL Search]에 대한 링크를 제공하는 것이 좋습니다 [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)에서는 대상 세그먼트 타깃팅을 옵트아웃하는 방법을 설명합니다.

1. Experience Cloud 조직 ID를 식별하고 Advertising Cloud 계정에 연결되어 있는지 확인합니다.

   Experience Cloud 조직 ID는 &quot;@AdobeOrg&quot;이 추가된 24자의 영숫자 문자열입니다. 대부분의 Experience Cloud 고객에게 조직 ID가 할당되었습니다. 마케팅 팀이나 내부 Adobe 시스템 관리자가 조직 ID를 모르거나 프로비저닝되었는지 확실하지 않은 경우 Adobe 고객 지원 센터(gdprsupport@adobe.com)에 문의하십시오. 를 사용하여 개인 정보 API에 요청을 제출하려면 조직 ID가 필요합니다. `imsOrgID` 네임스페이스.

   >[!IMPORTANT]
   >
   >조직의 Advertising Cloud 담당자에게 문의하여 다음을 포함한 모든 조직의 Advertising Cloud 계정을 확인합니다 [!DNL DSP] 계정 또는 광고주 [!DNL Search] 계정 및 [!DNL Creative] 또는 [!DNL DCO] 계정 — Experience Cloud 조직 ID에 연결되어 있습니다.

1. 다음 중 하나를 사용합니다 [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (자동화된 요청의 경우) 또는 [Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (임시 요청의 경우) 소비자를 대신하여 Advertising Cloud에 개인 정보에 대한 액세스 및 삭제 요청을 제출하고 기존 요청의 상태를 확인합니다.

   고객과 상호 작용하고 캠페인을 시작할 모바일 앱을 가진 광고주용 [!DNL DSP]를 다운로드하려면 Experience Cloud을 위한 개인 정보 보호 Mobile SDK를 다운로드해야 합니다. Mobile SDK를 사용하면 기업이 옵트아웃 상태 플래그를 설정하고 소비자의 장치 ID(네임스페이스 ID)를 검색할 수 있습니다. `deviceID`). 및 요청을 Privacy Service API에 제출합니다. 모바일 앱에는 SDK 버전 4.15.0 이상이 필요합니다.

   소비자 액세스 요청을 제출할 때 Privacy Service API는 지정된 쿠키 또는 장치 ID를 기반으로 소비자의 정보를 반환하며, 이를 소비자에게 반환해야 합니다.

   소비자 삭제 요청을 제출하면 쿠키 ID 또는 장치 ID와 쿠키와 연결된 모든 비용, 클릭 및 매출 데이터가 서버에서 삭제됩니다.

   >[!NOTE]
   비즈니스에 여러 Experience Cloud 조직 ID가 있는 경우, 각각에 대해 별도의 API 요청을 전송해야 합니다. 그러나 여러 Advertising Cloud 하위 솔루션([!DNL Search], [!DNL Creative], [!DNL DSP], 및 [!DNL DCO]). 하위 솔루션당 한 개의 계정을 사용하는 경우

이 모든 단계는 Advertising Cloud에서 지원을 받기 위해 필요합니다. Adobe Experience Platform Privacy Service을 사용하여 수행해야 하는 이러한 작업 및 기타 관련 작업과 필요한 항목을 찾을 수 있는 위치에 대한 자세한 내용은 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Advertising Cloud JSON 요청의 필수 필드 값

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Experience Cloud 조직 ID*>

&quot;users&quot;:

* `"key":` &lt;*일반적으로 고객의 이름*>

* `"action":` 둘 중 하나 `**access**` 또는 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (adcloud 쿠키 공간을 나타냅니다.)

   * `"value":` &lt;*다음에서 검색한 실제 고객의 쿠키 ID 값`AdobePrivacy.js`*>

* `"include": **adCloud**` (요청에 적용되는 Adobe 제품)

* `"regulation": **ccpa**` (요청에 적용되는 개인정보 보호 규정)

## AdobePrivacy.js에서 검색한 Advertising Cloud 사용자 ID를 사용하여 소비자가 제출한 요청의 예

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
}
```

## 액세스 요청을 위해 반환되는 데이터 필드

다음은 Advertising Cloud에 대한 개인 정보 액세스 응답의 예입니다.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```

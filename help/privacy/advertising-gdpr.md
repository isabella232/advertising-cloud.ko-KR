---
title: 개인 정보 보호 규정을 위한 Adobe 광고 지원
description: 지원되는 데이터 요청 유형, 필수 설정 및 필드 값, 레거시 제품 ID를 사용한 API 액세스 요청 및 반환된 데이터 필드의 예에 대해 알아봅니다
feature: GDPR
exl-id: 304d88d0-d63d-4b32-8d4d-c61ba2409adc
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# 개인 정보 보호 규정을 위한 Adobe 광고 지원

*대상 [!DNL Adobe Advertising Search]; Adobe 광고 DSP Adobe 광고 크리에이티브 및 Adobe Advertising DCO*

>[!IMPORTANT]
>
>이 문서의 내용은 법률적인 조언이 아니며, 법률적인 조언을 대체하지 않습니다. 개인 정보 보호 규정에 대한 법률 자문을 구하십시오.

2018년 5월 25일부터 적용되는 개인 정보 보호 규정(GDPR)은 유럽 연합(EU)의 국경 내의 모든 개인(데이터 주체)이 개인 데이터를 제어하고 국제 비즈니스에 대한 규제 환경을 단순화합니다. 이 법은 데이터 관리자의 비즈니스 위치에 상관없이 개인 데이터를 처리할 때 EU의 경계 내에서 개인 데이터를 수집하거나, 행동을 모니터링하거나, 개인 데이터를 수집하는 모든 기업(데이터 관리자)에 적용됩니다.

Adobe Experience Cloud은 고객을 대신하여 수신하여 보관하는 모든 개인 데이터에 대한 데이터 처리자의 역할을 합니다. 귀하는 데이터 제어자로서 Adobe Experience Cloud이 귀하를 대신하여 처리하고 저장하는 개인 데이터를 결정합니다.

이 문서에서는 [!DNL Advertising Search]; 광고 크리에이티브; Advertising DSP(Demand Side Platform); 및 [!DNL Advertising DCO] Adobe Experience Platform Privacy Service API 및 Privacy Service UI를 사용하여 데이터 주체의 GDPR 데이터 액세스 및 삭제 권한을 지원합니다.

GDPR의 비즈니스 의미에 대한 자세한 내용은 [GDPR 및 비즈니스](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Adobe 광고에 지원되는 데이터 요청 유형

Adobe Experience Platform은 기업이 다음 작업을 완료할 수 있는 기능을 제공합니다.

* 내에서 데이터 주체의 쿠키 수준 데이터 또는 장치 ID 수준 데이터(모바일 앱의 광고)에 액세스합니다 [!DNL Search], [!DNL Creative], [!DNL DSP], 또는 [!DNL DCO].
* 내에 저장된 쿠키 수준 데이터 삭제 [!DNL Search], [!DNL Creative], [!DNL DSP], 또는 [!DNL DCO] 브라우저를 사용하는 데이터 주체의 경우 내에 저장된 ID 수준 데이터를 삭제하거나 [!DNL DSP] 모바일 장치에서 앱을 사용하는 데이터 주제용.
* 하나 또는 모든 기존 요청의 상태를 확인합니다.

## Adobe 광고에 대한 요청을 전송하기 위한 필수 설정

Adobe 광고를 위한 데이터에 액세스하고 삭제를 요청하려면 다음을 수행해야 합니다.

1. JavaScript 라이브러리를 배포하여 데이터 주체 쿠키를 검색하고 제거합니다. 같은 라이브러리 `AdobePrivacy.js`는 모든 Adobe Experience Cloud 솔루션에 사용됩니다.

   >[!IMPORTANT]
   >
   >일부 Adobe Experience Cloud 솔루션에 대한 요청에는 JavaScript 라이브러리가 필요하지 않지만 Adobe 광고에 대한 요청에는 JavaScript 라이브러리가 필요합니다.

   데이터 주체가 회사의 개인 정보 포털과 같은 액세스 및 삭제 요청을 제출할 수 있는 웹 페이지에 라이브러리를 배포해야 합니다. 라이브러리는 Adobe 쿠키(네임스페이스 ID)를 검색하는 데 도움이 됩니다. `gsurferID`). Adobe Experience Platform Privacy Service API를 통해 액세스 및 삭제 요청의 일부로 이러한 ID를 제출할 수 있습니다.

   데이터 주체에서 개인 데이터 삭제를 요청하는 경우 라이브러리는 데이터 주체의 브라우저에서 데이터 주체의 쿠키도 삭제합니다.

   >[!NOTE]
   >
   >개인 데이터를 삭제하는 것은 옵트아웃과 다릅니다. 옵트아웃은 대상 세그먼트로 최종 사용자 타겟팅을 중지합니다. 그러나 데이터 주체에서 개인 데이터를 삭제하도록 요청하는 경우 [!DNL Creative], [!DNL DSP], 또는 [!DNL DCO]또한 라이브러리는 Adobe 타깃팅에서 데이터 주체를 옵트아웃하기 위해 Advertising에 요청을 보냅니다. 광고 문헌 [!DNL Search]를 설정하는 경우 데이터 주체에게 [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)에서는 대상 세그먼트 타깃팅을 옵트아웃하는 방법을 설명합니다.

1. Experience Cloud 조직 ID를 식별하고 Adobe 광고 계정에 연결되어 있는지 확인합니다.

   Experience Cloud 조직 ID는 &quot;@AdobeOrg&quot;이 추가된 24자의 영숫자 문자열입니다. 대부분의 Experience Cloud 고객에게 조직 ID가 할당되었습니다. 마케팅 팀이나 내부 Adobe 시스템 관리자가 조직 ID를 모르거나 프로비저닝되었는지 확실하지 않은 경우 Adobe 고객 지원 센터(gdprsupport@adobe.com)에 문의하십시오. 를 사용하여 개인 정보 API에 요청을 제출하려면 조직 ID가 필요합니다. `imsOrgID` 네임스페이스.

   >[!IMPORTANT]
   >
   >조직의 Adobe 광고 담당자에게 문의하여 다음을 포함한 모든 조직의 Adobe 광고 계정을 확인합니다 [!DNL DSP] 계정 또는 광고주 [!DNL Search] 계정 및 [!DNL Creative] 또는 [!DNL DCO] 계정 — Experience Cloud 조직 ID에 연결되어 있습니다.

1. 다음 중 하나를 사용합니다 [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (자동화된 요청의 경우) 또는 [Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (임시 요청의 경우) 데이터 주체를 대신하여 Advertising에 액세스 및 삭제 요청을 제출하고 기존 요청의 상태를 확인할 수 있습니다.

   모바일 앱을 보유한 광고주가 데이터 주체와 상호 작용하고 DSP에서 캠페인을 시작하는 경우 Experience Cloud용 Privacy-Ready Mobile SDK를 다운로드해야 합니다. Mobile SDK를 사용하여 데이터 제어자는 옵트아웃 상태 플래그를 설정하고 데이터 주체의 장치 ID(네임스페이스 ID)를 검색할 수 있습니다. deviceID)를 호출하고 요청을 Privacy Service API에 제출합니다. 모바일 앱에는 SDK 버전 4.15.0 이상이 필요합니다.

   데이터 주체의 액세스 요청을 제출할 때 Privacy Service API는 지정된 쿠키 또는 장치 ID를 기반으로 데이터 주체의 정보를 반환하며 이를 데이터 주체에게 반환해야 합니다.

   데이터 주체의 삭제 요청을 제출하면 쿠키 ID 또는 장치 ID와 쿠키와 연결된 모든 비용, 클릭 및 매출 데이터가 서버에서 삭제됩니다.

   >[!NOTE]
   회사에 여러 Experience Cloud 조직 ID가 있는 경우 각각에 대해 별도의 API 요청을 전송해야 합니다. 그러나 여러 Adobe 광고 하위 솔루션([!DNL Search], [!DNL Creative], [!DNL DSP], 및 [!DNL DCO]). 하위 솔루션당 한 개의 계정을 사용하는 경우

이러한 모든 단계는 Adobe 광고에 필요합니다. Adobe Experience Platform Privacy Service을 사용하여 수행해야 하는 이러한 작업 및 기타 관련 작업과 필요한 항목을 찾을 수 있는 위치에 대한 자세한 내용은 [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html).

## Adobe 광고 JSON 요청의 필수 필드 값

&quot;&quot;company context&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;*IMS 조직 ID 값*>

`"users":`

* `"key":` &lt;*일반적으로 데이터 주체의 이름입니다*>

* `"action":` 둘 중 하나 `**access**` 또는 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (이것은 [!DNL adcloud] cookie space)

   * `"value":` &lt;*검색된 실제 데이터 주체의 쿠키 ID 값`AdobePrivacy.js`*>

* `"include": **adCloud**` (요청에 적용되는 Adobe 제품)

* `"regulation": **gdpr**` (요청에 적용되는 개인정보 보호 규정)

## Adobe 광고 사용자 ID를 사용하여 데이터 주체가 제출한 요청의 예 `AdobePrivacy.js`

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
    "regulation":"gdpr"
}
}
```

## 액세스 요청을 위해 반환되는 데이터 필드

다음은 Adobe 광고에 대한 액세스 응답의 예입니다.

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

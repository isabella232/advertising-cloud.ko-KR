---
title: '캘리포니아 소비자 개인 정보 보호법을 위한 Adobe Advertising Cloud 지원 : 소비자 판매 중지 지원'
description: 소비자 판매 중지 요청 캡처에 대한 지원에 대해 알아봅니다.
feature: CCPA
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
source-git-commit: 2e0395dc1e5aa52adc83c1aaea49793fd5555390
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---

# 캘리포니아 소비자 개인 정보 보호법을 위한 Adobe Advertising Cloud 지원: 소비자 판매 거부 지원

*Adobe Advertising Cloud Demand Side Platform의 경우*

>[!IMPORTANT]
>
>이 문서의 내용은 법률적인 조언이 아니며, 법률적인 조언을 대체하지 않습니다. 캘리포니아 소비자 개인 정보 보호법에 대한 법률 자문을 구하십시오.

CCPA(California Consumer Privacy Act)는 2020년 1월 1일부터 시행된 California의 새로운 개인 정보 보호법입니다. CCPA는 캘리포니아 주민에게 개인 정보에 대한 새로운 권리를 제공하고 캘리포니아에서 사업을 하는 특정 업체들에 데이터 보호 책임을 부과합니다. CCPA는 소비자에게 개인 정보를 액세스하고 삭제할 수 있는 권한과 제3자에게 &quot;개인 정보 판매&quot;의 자격이 되는 특정 활동을 거부할 수 있는 권한을 제공합니다.

기업은 Adobe Experience Cloud이 귀하를 대신하여 처리하고 저장하는 개인 데이터를 결정합니다.

Adobe Advertising Cloud은 서비스 제공업체로서, 개인 정보에 액세스 및 삭제에 대한 소비자 요청 관리 및 개인 정보 판매를 거부하기 위한 소비자 요청 관리를 포함하여 Advertising Cloud 제품 및 서비스 사용에 적용되는 CPA에 따른 책임을 이행하도록 비즈니스를 지원합니다.

이 문서에서는 서비스 공급자인 DSP(Adobe Advertising Cloud Demand Side Platform)이 CCPA에 의해 정의된 각 용어가 &quot;개인 정보&quot; 판매&quot;에서 옵트아웃할 소비자 권한을 지원하는 방법에 대해 설명합니다. 여기에는 Advertising Cloud에 판매 중지 요청을 전달하는 방법 및 조직의 판매 중지 요청 보고서를 검색하는 방법에 대한 정보가 포함되어 있습니다.

Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP(Demand Side Platform) 및 Media Optimizer DCO가 소비자의 개인 정보 액세스 및 삭제 권한을 지원하는 방법에 대한 자세한 내용은 [캘리포니아 소비자 개인 정보 보호법을 위한 Adobe Advertising Cloud 지원: 소비자 데이터 액세스 및 삭제 지원](/help/privacy/ad-cloud-ccpa-access-delete.md).

CCPA를 위한 Adobe 개인 정보 서비스에 대한 자세한 내용은 [Adobe 개인 정보 보호 센터](https://www.adobe.com/privacy/ccpa.html).

## Advertising Cloud에 소비자 옵트아웃 요청 통신

다음 중 하나를 사용하여 소비자 판매 중지 요청을 전달할 수 있습니다.

* Advertising Cloud DSP에서 만든 CCPA 판매 중지 세그먼트
* Adobe Experience Platform Privacy Service API

### 방법 1: 를 사용하여 CCPA 판매 중지 요청 전달 [!UICONTROL CCPA Opt-Out-of-Sale] Advertising Cloud DSP의 세그먼트

>[!NOTE]
>
>사용자는 무한정 CCPA 판매 중지 세그먼트에 남아 있습니다.

1. Advertising Cloud DSP에서 광고주 계정에 로그인합니다. [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [CCPA 판매 중지 세그먼트를 만들고 세그먼트 픽셀을 구현하여 옵트아웃 요청을 캡처합니다](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### 방법 2: Adobe Experience Platform Privacy Service API를 사용하여 CCPA 판매 중지 요청 전달

*광고주가 Adobe Experience Cloud 조직 ID만 할당했습니다*

1. JavaScript 라이브러리를 배포하여 고객의 쿠키를 검색합니다. 같은 라이브러리 `AdobePrivacy.js`는 모든 Adobe Experience Cloud 솔루션에 사용됩니다.

   >[!IMPORTANT]
   >
   >일부 Adobe Experience Cloud 솔루션에 대한 요청에는 JavaScript 라이브러리가 필요하지 않지만 Advertising Cloud에 요청하려면 JavaScript 라이브러리가 필요합니다.

   고객이 회사의 개인 정보 포털과 같은 판매 중지 요청을 제출할 수 있는 웹 페이지에 라이브러리를 배포해야 합니다. 라이브러리는 Adobe 쿠키(네임스페이스 ID)를 검색하는 데 도움이 됩니다. `gsurferID`)를 사용하도록 이러한 id를 Adobe Experience Platform Privacy Service API를 통해 판매 중지 요청의 일부로 제출할 수 있습니다.

1. Experience Cloud 조직 ID를 식별하고 Advertising Cloud 계정에 연결되어 있는지 확인합니다.

   Experience Cloud 조직 ID는 &quot;@AdobeOrg&quot;이 추가된 24자의 영숫자 문자열입니다. 대부분의 Experience Cloud 고객에게 조직 ID가 할당되었습니다. 마케팅 팀이나 내부 Adobe 시스템 관리자가 조직 ID를 모르거나 프로비저닝되었는지 확실하지 않은 경우 Adobe 고객 지원 센터(gdprsupport@adobe.com)에 문의하십시오. 를 사용하여 개인 정보 API에 요청을 제출하려면 조직 ID가 필요합니다. `imsOrgID` 네임스페이스.

   >[!IMPORTANT]
   >
   >조직의 Advertising Cloud 담당자에게 문의하여 다음을 포함한 모든 조직의 Advertising Cloud 계정을 확인합니다 [!DNL DSP] 계정 또는 광고주 [!DNL Search] 계정 및 [!DNL Creative] 또는 [!DNL DCO] 계정 — Experience Cloud 조직 ID에 연결되어 있습니다.

1. Adobe Experience Platform Privacy Service API를 사용하여 다음을 수행할 수 있습니다 [판매 중지 요청 제출](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) 고객을 대신하여 Advertising Cloud에 전달하여 기존 요청의 상태를 확인합니다.

   판매 중지 요청의 예는 아래 부록을 참조하십시오.

   >[!NOTE]
   비즈니스에 여러 Experience Cloud 조직 ID가 있는 경우, 각각에 대해 별도의 API 요청을 전송해야 합니다. 그러나 여러 Advertising Cloud 하위 솔루션([!DNL Search], [!DNL Creative], [!DNL DSP], 및 [!DNL DCO]). 하위 솔루션당 한 개의 계정을 사용하는 경우

이 모든 단계는 Advertising Cloud에서 지원을 받기 위해 필요합니다. Adobe Experience Platform Privacy Service을 사용하여 수행해야 하는 이러한 작업 및 기타 관련 작업과 필요한 항목을 찾을 수 있는 위치에 대한 자세한 내용은 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## 판매 중지 요청을 제출한 소비자의 보고서 검색

Advertising Cloud은 고객이 계정에 대해 판매 중지 요청을 제출한 월별 ID에 대한 보고서를 생성합니다. 각 보고서는 GZIP 형식으로 압축된 탭으로 구분된 텍스트 파일로 사용할 수 있습니다. 이 데이터는 CCPA 판매 중지 세그먼트를 사용하여 캡처된 요청과 Advertising Cloud DSP에서 만들어진 요청과 Privacy Service API를 통해 작성된 모든 제출을 통합합니다. CCPA 판매 중지 세그먼트에 캡처된 사용자 ID는 세그먼트 및 광고주별로 식별됩니다. 보고서는 이전 월에 대한 각 달의 1일에 생성됩니다. 예를 들어 6월의 월별 사용자 목록은 7월 1일에 제공됩니다.

Advertising Cloud DSP 내에서 또는 Advertising Cloud을 사용하여 이전 3개월 내에 만든 월별 보고서에 대한 링크를 검색할 수 있습니다 [!DNL Trafficking API]. 각 링크는 7일 동안 유효하지만 고객이 하나를 검색하려고 할 때마다 새로 고침됩니다.

### 방법 1: Advertising Cloud DSP 내에서 소비자 판매 중지 보고서 검색

1. Advertising Cloud DSP에서 광고주 계정에 로그인합니다. [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [보고서 검색](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### 방법 2: Advertising Cloud을 사용하여 소비자 판매 중지 보고서 검색 [!DNL Trafficking API]

이 기능은 [!DNL Trafficking API]. 에 대한 설명서를 참조하십시오. [!DNL Trafficking API] 추가 정보.

조직에서 [!DNL Trafficking API] 하지만 더 많은 정보에 관심이 있다면 [!DNL Adobe] 계정 팀입니다.

## 부록: 예 [!UICONTROL CCPA Opt-Out-of-Sale] Privacy Service API 사용자 요청

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

위치:

* `"namespace": "AdCloud"` 는 `AdCloud` 쿠키 공간 및 해당 값은에서 검색된 고객의 쿠키 ID입니다. `AdobePrivacy.js`
* `"include": ["AdCloud"]` 요청이 Advertising Cloud에 적용됨을 나타냅니다

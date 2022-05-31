---
title: '내구성 ID 파트너에서 인증된 세그먼트 활성화 '
description: 내구성 ID 솔루션을 통해 인증된 대상을 활성화하는 방법에 대해 알아봅니다.
feature: DSP Audiences
source-git-commit: 155ab740084bebfba5fd992a23706129668fcc90
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 내구성 ID 파트너에서 인증된 세그먼트 활성화

*베타 기능*

Advertising Cloud DSP 내의 내구성 ID 솔루션을 통해 인증된 대상을 활성화하려면 세그먼트를 [!DNL RampIDs]: 입찰 가능한 환경에서 인식할 수 있습니다. 다음 방법 중 하나를 사용하여 이 작업을 수행할 수 있습니다.

* DSP과 [!DNL Adobe Real-Time Customer Data Profile (CDP)] 그리고 [!DNL Adobe-LiveRamp Retrieval API].

* 인증된 세그먼트를 [!DNL LiveRamp] [!DNL Connect] 대시보드 .

## Tasks

1. 다음 중 한 선택 사항에 대해서는 `adcloud-support@adobe.com` DSP에서 다음 설정을 활성화하면 DSP 캠페인에서 인증된 세그먼트를 한 번 타깃팅할 수 있습니다. [활성화 워크플로우의 모든 단계가 완료됨](source-about.md#workflow-sources):

   1. [!DNL LiveRamp] [!DNL RampID] 세그먼트 공유 전 캠페인 구성 [!DNL Real-Time CDP].

   1. 계정 수준 &quot;[!UICONTROL LiveRamp segments]&quot; 옵션을 선택합니다.

1. (사용자가 인증된 세그먼트를 [!DNL LiveRamp])에서 다음 단계를 완료하십시오. [!DNL LiveRamp] [!DNL Connect] 대시보드:

   1. 대상 타일 활성화 **[!DNL AAC API 1P Onboarding]**.

   1. 설정 [!DNL Identifier Settings] to **[!DNL Ramp ID]** 전용.

      ![식별자 설정](/help/dsp/assets/liveramp-tile-settings.png)

   1. (선택 사항) 쿠키 기반 식별자를 계속 수신하려면 두 번째 를 만듭니다 [!DNL AAC API 1P Onboarding] 대상이 &quot; 인 경우[!DNL Cookies],&quot; &quot;[!DNL IDFA],&quot; 및 &quot;[!DNL AAID]&quot;&quot;이(가) 선택되었습니다.

## 테스트 및 데이터 유효성 검사에 대한 우수 사례

* **Target [!DNL RampID]별도의 캠페인에서 기반 세그먼트 및 쿠키 기반 세그먼트 를 참조하십시오.**

   * Campaign 설정을 사용하면 한 식별자만 우선 순위를 지정할 수 있습니다.

   * 현재, [!DNL RampIDs] 온사이트 이벤트 중에 검색할 수 없습니다. 즉, 가장 낮은 CPA 및 ROAS와 같은 특정 사용자 지정 목표를 인증된 세그먼트를 사용할 수 없습니다. 성능 KPI가 제한적인 경우에만 쿠키 기반 세그먼트를 사용합니다.

* **두 위치에서 한 개의 배치를 만듭니다 [!DNL RampID] 및 쿠키 기반 캠페인.**

   * 공유된 세그먼트를 Target [!DNL LiveRamp] 표준 세그먼트 활성화 프로세스 사용.

   * Advertising Cloud 지원 팀과 협력하여 적절한 데이터 배포의 유효성을 검사합니다.

DSP 통합에 대해 자세히 알아보려면 [!DNL LiveRamp], 연락처 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Audience Sources에서 인증된 세그먼트 활성화 정보](source-about.md)
>* [자사 대상을 활성화할 대상 소스 만들기](source-create.md)
>* [대상 소스 설정](source-settings.md)
>* [Adobe Advertising Cloud DSP 연결](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [대상자 관리 기본 정보](/help/dsp/audiences/audience-about.md)


---
title: 자사 대상을 활성화할 대상 소스 만들기
description: 계정 또는 광고주 계정에 대상자를 가져오는 소스를 만드는 방법을 알아봅니다.
feature: DSP Audiences
source-git-commit: d1ebbd79b6ccf0249829feef134122f083060563
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# 자사 대상을 활성화할 대상 소스 만들기

*베타 기능*

<!-- Will this remain for admin users/Adobe account teams only? -->

DSP 계정 또는 광고주 계정으로 대상을 가져올 소스를 만듭니다. 현재 대상에서 대상을 가져올 수 있습니다. [a [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>에 대한 소스를 만든 후 [!DNL Real-Time CDP]를 활성화하려면 [!DNL Real-Time CDP] 내에서 Adobe Advertising Cloud DSP 대상을 통한 대상 [!DNL Real-Time CDP] 가져오기 시작합니다. 자세한 내용은 [활성화 워크플로우의 절차](source-about.md#workflow-sources).

1. 주 메뉴에서 **[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. 클릭 [!UICONTROL Add Source].

1. 에서 [!UICONTROL Select a Type] 메뉴에서 소스 유형을 선택합니다.

   *[!UICONTROL RT-CDP]*: 이 소스 유형, 대상 [a [!DNL Adobe Real-Time Customer Data Profile]](source-about.md)유일한 선택 사항입니다.

1. 을(를) 지정합니다. [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* 또는 *[!UICONTROL Account]*.

1. 나머지 항목을 입력합니다 [소스 설정](source-settings.md).

   의 사본을 유지합니다 [!UICONTROL Source Key] 생성된 . 나중에 값이 필요합니다.

1. 클릭 **[!UICONTROL Save]**.

1. Experience Platform에서 [!UICONTROL Source Key] DSP 소스 설정에서 생성되었습니다.

Advertising Cloud 대상 연결을 활성화하고 세그먼트를 선택하고 제어 권한에 액세스하는 방법에 대한 지침은 &quot;[Adobe Advertising Cloud DSP 연결](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [대상 소스 설정](source-settings.md)
>* [Audience Sources에서 인증된 세그먼트 활성화 정보](source-about.md)
>* [내구성 ID 파트너에서 인증된 세그먼트 활성화](source-durable-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP 연결](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [대상자 관리 기본 정보](/help/dsp/audiences/audience-about.md)


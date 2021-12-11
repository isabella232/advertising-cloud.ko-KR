---
title: 여러 타사 광고 만들기
description: 여러 타사 광고를 한 번에 만드는 방법을 알아봅니다.
feature: DSP Ads
exl-id: 83d35d27-1ab6-4fcf-877f-650a2dc6975a
source-git-commit: 19d6a2edf07eecf874537dd9d356737ed9156bd9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# 여러 타사 광고 만들기

타사 광고 서버에서 호스팅되는 크리에이티브 자산을 가리키는 태그를 업로드하여 한 번에 최대 500개의 타사 광고를 만들 수 있습니다. 광고에 대한 추적 픽셀을 포함할 수 있습니다.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

다음 중 하나를 업로드할 수 있습니다 [!DNL DoubleClick] 및 [!DNL Flashtalking] 제공된 템플릿을 사용하여 시트 또는 수동으로 채워진 파일에 태그를 지정합니다.

단일 타사 광고를 만들려면 다음을 참조하십시오 [광고 만들기](ad-create.md).

>[!TIP]
>
> HTTPS를 사용하여 안전하게 제공되는 타사 광고를 사용하는 것이 좋습니다. HTTPS를 사용하여 제공되는 URL은 &quot;https&quot;로 시작합니다.

1. 주 메뉴에서 **[!UICONTROL Campaigns]**.

1. 광고가 포함될 캠페인의 이름을 클릭합니다.

1. 데이터 테이블 위에서 **[!UICONTROL Create]**. 메뉴의 광고 유형 섹션에서 **[!UICONTROL Bulk upload ads]**.

1. 광고가 호스팅되는 광고 서버를 선택합니다. *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]*, 또는 *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] 및 [!DNL Flashtalking] 광고) 각 비디오 자산 및 각 디스플레이 자산에 사용할 태그 유형을 선택합니다. 사용 가능한 옵션은 광고 서버마다 다릅니다.

1. (광고를 제외한 모든 광고 서버의 광고 [!DNL DoubleClick] 및 [!DNL Flashtalking]) **[!UICONTROL Download this template]** 에서 템플릿을 다운로드하려면 다음을 수행하십시오. [!DNL Microsoft Excel] 광고 데이터로 채우고 로컬로 저장할 수 있는 XLSX(스프레드시트) 형식입니다. 필요한 열에는 다음이 포함됩니다 [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag], 및 [!UICONTROL Ad Types].

1. 클릭 **[!UICONTROL Upload]** 장치 또는 네트워크에서 .xlsx 또는 .xls 형식의 파일을 선택합니다.

   대상 [!DNL DoubleClick] 및 [!DNL Flashtalking] 광고, 광고 서버에서 편집되지 않은 태그 시트를 업로드합니다. 다른 광고 서버의 경우 3단계에서 다운로드한 템플릿을 사용합니다.

1. 업로드가 완료되면 을(를) 클릭합니다 **[!UICONTROL Start Building Ads]**.

1. 각 광고의 세부 정보와 상태를 검토합니다.

   1. 업로드된 태그의 유효성 검사를 기반으로 하는 각 광고의 상태를 검토합니다.
   1. (선택 사항) 각 광고에 대해 다음 중 하나를 수행합니다.
      * 광고를 미리 보려면 ![play](/help/dsp/assets/play.png) 광고 행에 아래에 그룹화됩니다.
      * 광고 세부 사항을 편집하려면 ![편집](/help/dsp/assets/edit.png)를 클릭하고, 세부 사항을 편집한 다음 를 클릭합니다. **저장**.
      * 광고를 제거하려면 **[!UICONTROL X]** 광고 행에 아래에 그룹화됩니다.

1. 클릭 **[!UICONTROL Create *N *광고]**.

1. 다음 중 하나를 수행합니다.

   * 클릭 **[!UICONTROL Done]**.

   * (광고가 거부된 경우) (선택 사항) 광고 레코드를 편집하고 검토를 위해 광고를 재실행하려면
      1. 광고 이름을 클릭합니다.
      1. 광고 설정을 편집합니다.
      1. 클릭 **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [광고 관리](ad-about.md)
>* [광고 만들기](ad-create.md)
>* [사용 가능한 광고 유형](ad-types.md)
>* [광고 사양](/help/dsp/assets/ad-specs.pdf)
>* [비디오: 타사 광고 태그를 대량 업로드하는 방법](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)


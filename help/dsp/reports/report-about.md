---
title: 사용자 지정 보고서 정보
description: 사용자 지정 보고서를 수동으로 만들거나 사전 구성된 보고서 템플릿을 사용하는 옵션에 대해 알아봅니다.
feature: DSP Custom Reports
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# 사용자 지정 보고서 정보

사용자 지정 보고서를 사용하면 캠페인 차원(예: 광고주, 배치, 사이트 또는 지역)과 가장 중요한 지표를 사용하여 보고서 데이터의 컨텐츠와 전달을 사용자 지정할 수 있습니다. 다음 중 하나를 수행할 수 있습니다.

* 세분화된 수준에서 캠페인 성과 보고서를 완전히 구성합니다.
* 사전 구성된 보고서 템플릿 중에서 선택하고 선택적으로 추가로 사용자 지정할 수 있습니다.

보고서를 한 번 생성하거나 지정된 시간대에서 매일, 주별 또는 월별 중에서 생성할 수 있도록 예약할 수 있습니다. 보고서가 생성되면 지정된 각 이메일 수신자에게 전달되거나 연결됩니다 [보고서 대상](/help/dsp/reports/report-destinations/report-destination-about.md) 다음 유형 중에서 선택합니다.

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP SSL(베타)

>[!NOTE]
>
>캠페인의 모든 수준(캠페인, 패키지, 배치 또는 광고)에서 주문형 데이터를 볼 수도 있습니다 [관련 캠페인 관리 보기 내에서](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## 사용 가능한 보고서 유형

* **[!UICONTROL Custom]:** 이 보고서는 대부분의 차원과 지표를 사용하여 고유한 사용자 지정 보고서를 만드는 데 사용할 수 있는 빈 템플릿입니다. [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], 및 [!UICONTROL Site] 보고서는 각 사용 사례에 대해 사전 선택된 열 및 차원과 함께 이 템플릿의 변형입니다.

* 사전 구성된 보고서 템플릿

   * **[!UICONTROL Billing]:** 이 보고서를 사용하여 캠페인별 미디어 과금을 위한 비용 지표와 같은 주요 청구 지표를 파악합니다.

      >[!NOTE]
      >
      >이 보고서에는 청구 세그먼트에 대한 데이터가 포함됩니다. 사용자 또는 장치가 여러 세그먼트에 속하는 노출에 제공되면 청구 가능한 세그먼트 하나가 노출에 반영됩니다.

   * **[!UICONTROL Conversion]:** 이 보고서를 사용하여 Adobe 광고 전환 추적을 사용하여 캡처한 전환 지표를 기반으로 캠페인이 어떻게 수행되는지 알아보십시오. 이 보고서에는 다중 터치 속성이 포함됩니다.

   * **[!UICONTROL Device]:** 이 미리 채워진 템플릿을 사용하여 장치 관련 차원별로 주요 지표를 볼 수 있습니다.

   * **[!UICONTROL Frequency (by Impression)]:** 이 보고서를 사용하여 고유 시청자에게 표시되는 노출 횟수(예: 한 노출 횟수, 2개의 노출 횟수, 3개의 노출 횟수 등을 본 고유 시청자 수)의 분포를 이해합니다. 데이터는 배치 또는 캠페인으로 사용할 수 있습니다.

      >[!NOTE]
      >
      >* 데이터는 2019년 3월 1일 이후에 사용할 수 있습니다.
      >* 빈도는 데이터 샘플링을 기반으로 합니다.
      >* 일부 인벤토리의 경우 게시자는 빈도 추적을 방지하는 장치 식별자를 전달하지 않습니다. 이 보고서에는 장치 식별자를 사용할 수 있는 노출만 포함됩니다.


   * **[!UICONTROL Frequency (by App/Site)]:** 이 보고서를 사용하여 앱 또는 사이트별로 도달한 고유 사용자의 수를 파악합니다. 특정 앱 또는 사이트(&quot;고유 사용자&quot;)만 통해 도달한 고유 사용자의 수를 확인할 수도 있습니다.

      >[!NOTE]
      >
      >* 데이터는 2018년 11월 15일 이후에 사용할 수 있습니다.
      >* 일부 개인 인벤토리의 경우 게시자는 빈도 추적을 방지하는 장치 식별자를 전달하지 않습니다.


   * **[!UICONTROL Geo]**: 이 미리 채워진 템플릿을 사용하여 지리적 차원별로 주요 지표를 볼 수 있습니다.

   * **[!UICONTROL Margin]:** 이 보고서를 사용하여 캠페인이나 배치별로 마진, 이익 및 기타 지출 지표와 같은 주요 지표를 볼 수 있습니다.

   * **[!UICONTROL Segment]:** 세그먼트별로 주요 지표를 보려면 이 미리 채워진 템플릿을 사용하십시오.

      >[!NOTE]
      >
      >* 이 보고서는 서로 다른 타깃팅된 세그먼트가 수행되는 방식을 보여주기 위한 것입니다. 세그먼트 멤버십 데이터를 사용합니다. 둘 이상의 타깃팅된 세그먼트에 속하는 개인 또는 장치에 노출이 제공되는 경우 이 보고서에는 각 세그먼트에 대해 한 개의 행이 포함됩니다. 이러한 이유로 이 보고서의 합계가 실제 게재와 일치하지 않을 수 있습니다.
      >* 세그먼트에 대한 전환 지표 및 사용자 지정 목표 데이터는 2019년 8월 2일 이후에 사용할 수 있습니다. 세그먼트에 대한 다른 모든 데이터는 2018년 6월 1일 이후에 사용할 수 있습니다.


   * **[!UICONTROL Site]:** 기본적으로 에는 표준 지표, 총 미디어 순 지출 및 사이트별 총 청구 가능한 순 지출 합계가 포함됩니다.

## 교차 계정 보고 {#cross-account-reporting}

여러 DSP 계정이 있는 모든 조직은 조직의 요구 사항에 따라 사용자 지정 보고서에서 교차 계정 데이터를 선택적으로 활성화할 수 있습니다. 예를 들어, 계정 A에게 계정 B의 데이터에 대한 액세스 권한을 제공하고 계정 B에게 계정 C(계정 A는 아님) 데이터에 대한 액세스 권한을 제공할 수 있습니다. 이 기능을 활성화하고 구성하려면 [!DNL Adobe] 계정 팀입니다.

조직에 대해 기능이 활성화되면 다음을 수행할 수 있습니다 [필터](report-settings.md) 계정별 다음 보고서 유형 중 하나:  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], 및 [!UICONTROL Conversion].

계정 설정은 [!UICONTROL Settings] > [!UICONTROL Account] a) 계정에 데이터를 사용할 수 있는 다른 계정과 b) 계정의 데이터에 액세스할 수 있는 다른 계정을 가리킵니다.

>[!MORELIKETHIS]
>
>* [사용자 지정 보고서 만들기](/help/dsp/reports/report-create.md)
>* [사용자 지정 보고서 설정](/help/dsp/reports/report-settings.md)
>* [플랫폼 내 보고서 정보](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [사용 가능한 보고서 열](/help/dsp/reports/report-columns.md)
>* [정보 [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)


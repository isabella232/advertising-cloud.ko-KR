---
title: 사용자 지정 보고서 설정
description: 사용자 지정 보고서 설정에 대한 설명을 참조하십시오.
feature: Custom Reports
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---


# 사용자 지정 보고서 설정

**[!UICONTROL Name]** 보고서 이름. 최대 길이는 180자입니다.

**[!UICONTROL Report Type]** 보고서 유형:  *[!UICONTROL Custom]* (사용 가능한 대부분의 선택 사항이 포함됨),  *[!UICONTROL Billing]*,  *[!UICONTROL Conversion]*,  *[!UICONTROL Device]*,  *[!UICONTROL Frequency (by Impression)]*,   *[!UICONTROL Frequency (by App/Site)]*,  *[!UICONTROL Geo]*,  *[!UICONTROL Margin]*,  *[!UICONTROL Media Performance]*,   *[!UICONTROL Segment]* 또는  *[!UICONTROL Site]*.

## [!UICONTROL Apply Filters] 섹션

**[!UICONTROL Timezone]:** 보고용 시간대입니다.

**[!UICONTROL Observe Daylight Savings Time]:** 보고된 시간에 일광 절약 시간을 고려합니다.

**\[날짜 범위\]:**  데이터를 생성할 날짜 범위입니다. 사용 가능한 일 수는 보고서 및 선택한 차원마다 다릅니다. 다음 중 하나를 선택합니다.

* **[!UICONTROL Previous N days]** : 오늘 전 특정 일 수에 대한 데이터를 포함합니다.

* **[!UICONTROL Custom]** : 특정 시작 날짜와 종료 날짜 사이의 데이터를 포함합니다. 이전 날짜까지 데이터를 보고하려면 **[!UICONTROL Present]** 을 선택합니다.

* **[!UICONTROL Last Calendar Month]:** 이전 달력 월의 데이터를 포함합니다.

**[!UICONTROL Add Filters]:**  (선택 사항) 차원이 보고서에 열로 포함되어 있는지 여부에 관계없이 데이터를 필터링할 수 있는 추가 차원입니다.  *[!UICONTROL Account]*,\*  *[!UICONTROL Advertiser]*,  *[!UICONTROL Campaign]*,  *[!UICONTROL Placement]*,  *[!UICONTROL Ad]*,  *[!UICONTROL Ad Type]*,  *[!UICONTROL Video]*,  *[!UICONTROL Video Duration]*,  *[!UICONTROL Country]* 및  *[!UICONTROL Package]*.

\* *[!UICONTROL Account]* 는 조직이 [교차 계정 보고](report-about.md#cross-account-reporting)에 대해 구성된 경우에만 다음 보고서 유형에 사용할 수 있습니다.  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] 및 [!UICONTROL Conversion]. 교차 계정 보고에 대한 자세한 내용은 Adobe 계정 관리자에게 문의하십시오.

필터를 하나 이상 적용하려면 다음을 수행하십시오.

* 차원을 선택하고 연산자(*같음* 또는 *다음과 같지 않음*)를 선택한 다음 해당 값을 선택합니다. 예를 들어 프리롤 광고에만 대한 데이터를 반환하려면 &quot;[!UICONTROL Ad Type equals Preroll]&quot;를 지정하십시오.
* (선택 사항) 필터에 추가 기준을 추가합니다.
* (선택 사항) 하나 이상의 기준이 있는 필터를 추가로 추가합니다.

## [!UICONTROL Build Your Report] 섹션

**[!UICONTROL Select To Add As Report Headers]**  : 보고서에 포함할 데이터 열 또는 헤더입니다. 열을 추가하려면 범주를 확장하고 열 이름 옆에 있는 확인란을 선택합니다. 사용할 수 없는 모든 지표는 비활성화됩니다. 사용 가능한 데이터 카테고리는 다음과 같습니다.

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] (광고주별로 정렬)
* [!UICONTROL Custom Goals] (광고주별로 정렬)

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 열 헤더의 순서입니다. 열을 드래그하여 놓아 순서를 사용자 지정할 수 있습니다.

## [!UICONTROL Multi-Touch Conversion Options] 섹션

**[!UICONTROL Format]:** 보고서를  *[!UICONTROL CSV]* (쉼표로 구분된 값) 또는  *[!UICONTROL Tab]* (탭으로 구분된 값) 형식으로 생성할지 여부.

**[!UICONTROL Report Headers]:** 열 헤더 *[!UICONTROL Include]* 의  *[!UICONTROL Do Not Include]* 여부입니다.

**[!UICONTROL Attribution Rule Settings]:**  ( [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo],  [!UICONTROL Segment] 및  [!UICONTROL Site]  [!UICONTROL Conversion Metrics]  또는  [!UICONTROL Custom Goals]  열이 있는 보고서. Advertising Cloud 전환 추적만 있는 광고주) 보고서 내에서 전환을 초래하는 일련의 이벤트에 전환 데이터를 속성 지정하는 방법입니다. 규칙 간의 차이점을 비교하려면 두 개 이상의 규칙을 선택할 수 있습니다.

>[!NOTE]
>
>전환 경로에는 광고주 노출 내에 있는 모든 노출 및 클릭 수를 포함하거나 Advertising Cloud Search에 구성된 클릭 전환 확인 기간이 포함됩니다. 전환 기여도 분석 중 노출 횟수에 대한 클릭 수가 기본 설정으로 지정됩니다. 전환 경로를 클릭하면 속성 규칙을 기반으로 전체 크레딧을 받습니다. 노출 횟수는 전환 경로에서 클릭 수가 추적되지 않은 경우에만 크레딧을 받습니다.

* *[!UICONTROL Last Event]* : 전환 경로에서 마지막 클릭 또는 노출에 대한 속성 전환.

* *[!UICONTROL Weight Last More]* : 전환 경로의 모든 이벤트에 대한 전환을 속성 지정하지만 마지막 이벤트에 가장 큰 가중치를 제공하고 이전 이벤트에 대해 순차적으로 가중치를 부여합니다.

* *[!UICONTROL Even Distribution]:* 전환 경로의 각 이벤트에 동일한 전환을 제공합니다.

* *[!UICONTROL Weight First More]* : 전환 경로의 모든 이벤트에 대한 전환을 속성 지정하지만 첫 번째 이벤트에 가장 큰 가중치를 제공하고 다음 이벤트에 대해 순차적으로 가중치를 부여합니다.

* *[!UICONTROL First Event]:* 변환 경로에서 첫 번째 클릭 또는 노출에 대한 속성 전환.

* *[!UICONTROL U-shaped]* : 전환 경로의 모든 이벤트에 대한 전환을 기여하지만 전환 경로 중간에 있는 이벤트에 대해 가중치가 지속적으로 감소하면서 첫 번째 및 마지막 이벤트에 가장 큰 가중치를 제공합니다.

* *[!UICONTROL Display Only]*  : 전환 경로에서 마지막 DSP 클릭 또는 노출에 대한 속성 전환. 여기에는 비디오 및 연결된 TV 광고가 포함되며 Advertising Cloud Search 광고의 클릭 수는 제외됩니다.

* *[!UICONTROL Social Only]:* 사용되지 않음

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising Cloud](). -->

**[!UICONTROL Paths as Columns]:**   (모든  [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo],  [!UICONTROL Segment]및  [!UICONTROL Site]  [!UICONTROL Conversion Metrics]  또는  [!UICONTROL Custom Goals]  열이 있는 보고서) 동일한 장치에서 이전 이벤트가 발생한 경우 보고할 전환 유형입니다. 최대 3가지 유형을 포함할 수 있습니다. 선택한 각 유형에 대해 각 전환 지표에 대해 별도의 열이 포함되며, 지정된 접미사([!UICONTROL (tl)], [!UICONTROL (ct)] 또는 [!UICONTROL (vt)])가 추가됩니다.

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]* : 클릭 수(클릭스루의 경우 CT)와 노출 수(뷰스루의 경우 VT)로 인한 전환을 포함합니다. 노출에 속하는 전환에는 지정된 뷰스루 가중치가 곱됩니다. 기본 뷰스루 가중치는 100%입니다. 즉, 노출에 속하는 전환은 클릭에 속하는 전환 값의 100%로 계산됩니다.

* *[!UICONTROL With Clicks (CT)]* : 클릭으로 인한 전환만 포함합니다.

* *[!UICONTROL Impressions Only (VT)]* : 전환 경로에서 클릭 수가 추적되지 않았으므로 노출에 기여한 전환만 포함합니다.

**[!UICONTROL Cross Device Level]:**   ( [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo],  [!UICONTROL Segment] 및  [!UICONTROL Site]  [!UICONTROL Conversion Metrics]  또는  [!UICONTROL Custom Goals]  열이 있는 보고서. 교차 장치 속성이 있는 광고주에만 적용 가능) 전환을 추적하는 수준입니다.  *[!UICONTROL People]* 또는  *[!UICONTROL Household]*.

[교차 장치 솔루션](/help/dsp/introduction/features/cross-device-solutions.md)에 대해 자세히 알아보십시오.

**[!UICONTROL Cross-Device Breakout]:**  ( [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo],  [!UICONTROL Segment] 및  [!UICONTROL Site]  [!UICONTROL Conversion Metrics]  또는  [!UICONTROL Custom Goals]  열이 있는 보고서. 교차 장치 속성이 있는 광고주에만 적용 가능) 보고서에 포함할 교차 장치 전환에 대한 세부 정보 수준입니다. 자세한 브레이크아웃을 원하는 경우 각 레벨을 별도의 열에 포함할 수 있습니다.

* *[!UICONTROL Total People (TP)]* : 동일한 장치 전환과 교차 장치 전환을 모두 포함하는 총 전환을 포함합니다(해당하는 경우). 보고서에서 &quot;[!UICONTROL (tp)]&quot;이 전환 지표 이름 및 규칙 유형에 추가됩니다.

* *[!UICONTROL Same Device (SD)]* : 전환 경로에서 단일 장치만 추적된 전환만 포함합니다. 보고서에서 &quot;[!UICONTROL (sd)]&quot;이 전환 지표 이름 및 규칙 유형에 추가됩니다.

* *[!UICONTROL Cross Device (XD)]* : 전환 경로에서 두 개 이상의 장치가 추적된 전환만 포함합니다. 보고서에서 &quot;[!UICONTROL (xd)]&quot;이 전환 지표 이름 및 규칙 유형에 추가됩니다.

**[!UICONTROL Conversion Reporting Based On]:**  전환 데이터를 보고하는 방법:

* *[!UICONTROL Conversion Timestamp]*  : (기본값) 전환은 전환 날짜와 연결됩니다.

* *[!UICONTROL Event Timestamp]:* 전환은 지정된 [!UICONTROL Attribution Rule Settings]에 의해 결정된 대로 노출 날짜나 전환을 일으킨 클릭에 따라 보고됩니다.

## [!UICONTROL Add Email Recipients] 섹션

**[!UICONTROL Email]:** 오류로 인해 보고서가 취소된 경우 완료된 보고서 또는 알림을 전송할 이메일 주소입니다. 여러 주소를 지정하려면 쉼표나 공백으로 구분합니다.

**[!UICONTROL Frequency]:** 보고서를 전송하는 빈도:  *[!UICONTROL Once]*,  *[!UICONTROL Daily]*,  *[!UICONTROL Weekly]*&#x200B;또는  *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] 섹션

**[!UICONTROL Send & Save]:** 보고서를 전송할 때:  *[!UICONTROL On Schedule]* 또는  *[!UICONTROL Run Now]*. 예약된 보고서는 계정의 시간대에 09:00까지 전달됩니다.

>[!NOTE]
>
>[언제든지 [!UICONTROL Reports] 보기에서 사용자 지정 보고서를 실행할 수 있습니다.](report-run-now.md)

>[!MORELIKETHIS]
>
>* [사용자 지정 보고서 정보](/help/dsp/reports/report-about.md)
>* [사용자 지정 보고서 만들기](/help/dsp/reports/report-create.md)
>* [사용자 지정 보고서 복제](/help/dsp/reports/report-copy.md)
>* [사용자 지정 보고서 편집](/help/dsp/reports/report-edit.md)
>* [사용자 지정 보고서 실행](/help/dsp/reports/report-run-now.md)
>* [사용자 지정 보고서 설정](/help/dsp/reports/report-settings.md)

* [사용 가능한 보고서 열](/help/dsp/reports/report-columns.md)

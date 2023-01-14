---
title: Advertising DSP의 광고 관리 정보
description: 광고 관리에 대해 알아봅니다.
feature: DSP Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---

# Advertising DSP의 광고 관리 정보

<!-- add "The Ads View (Dashboard?)" section -->

DSP은 다양한 광고 유형에 대한 타사 광고 서비스 태그(예: Google, Flashtalk 또는 Sizmek)를 통한 광고 전달을 지원하고 기본 디스플레이 광고에 대한 직접 자산 업로드를 지원합니다. 타사 태그를 개별적으로 또는 대량으로 업로드할 수 있습니다. 벌크 업로드는 파트너 태그 시트 또는 벌크 태그 템플릿을 사용합니다.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

광고가 설정되면, 캠페인의 게재 방법을 제어하는 타깃팅 매개 변수(예: 지역, 대상, 장치 및 인벤토리 타깃팅)가 포함된 각 광고를 게재해야 합니다. 단일 광고를 하나 또는 여러 배치에 첨부할 수 있습니다.

## 사용 가능한 광고 유형 {#ad-types}

다음 모든 광고 유형을 DSP에서 사용할 수 있습니다. 각 광고 유형에 대한 전체 사양은 [광고 사양](ad-specs.md).

* **오디오 광고(타사 전용)**: 오디오 광고는 디지털 게시자 사이트에서 컨텐츠 간에 재생되며 오디오 파일로 독립 실행형 또는 컴패니언 배너와 함께 실행할 수 있습니다. 오디오는 브랜드 인식을 유도하고 이동 중에도 사용자의 참여를 유도하는 데 가장 잘 사용됩니다. 오디오의 주요 성능 지표는 다음과 같습니다 [!UICONTROL Completion Rate] 및 [!UICONTROL Cost per Completion].

* **디스플레이 광고(타사 전용)**: 디스플레이 광고는 웹 브라우저나 앱에 표시되는 애니메이션 또는 정적 이미지입니다. 광고 단위를 클릭하면 사용자가 브랜드 된 사이트 또는 마이크로 사이트로 이동합니다. 디스플레이는 효율적인 CPM을 유도하고, 메시지 연결을 늘리고, 추가 브랜드 또는 제품 터치포인트를 추가하고, 사용자를 구매 단계로 유도하는 데 가장 잘 사용됩니다. 표시할 주요 성능 지표는 다음과 같습니다 [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions], 및 [!UICONTROL Cost per Conversion]. DSP에서는 다양한 디스플레이 배너 광고 크기를 지원합니다.

* **모바일 광고(타사 전용)**: 모바일 광고는 프리롤 비디오(VAST, MRAID) 또는 표준 디스플레이 포맷일 수 있습니다. 모바일 프리롤 비디오는 자동 재생 또는 클릭하여 재생할 수 있으며, 화면 간 뷰어에 도달하는 데 가장 잘 사용됩니다. Mobile Standard 디스플레이는 모바일 웹 브라우저 또는 앱에 표시되는 정적 이미지이며 디지털 비디오 구매를 보완하고 메시지 연결을 유도하며 추가 브랜딩 또는 제품 터치포인트를 추가하는 데 가장 잘 사용됩니다. 또한 모바일 광고는 전체 화면 대상 또는 모바일 삽입 광고 역할을 할 수 있으며, 이 광고는 모바일 대상에 대한 브랜드 인식을 개발하고 전환을 유도하는 데 가장 잘 사용되는 전체 화면, 영향이 높은 모바일 광고입니다.

* **기본 디스플레이 광고(자사 전용)**: 기본 광고는 표준 표시 형식으로 지원됩니다. 기본 광고에는 제목 및/또는 제목, 설명, 로고 및 이미지가 포함됩니다. 광고 요소를 결합하고 렌더링하여 게시자의 페이지 스타일에 맞게 렌더링하므로 광고가 게시자의 유기 콘텐츠와 혼합되어 더 높은 참여를 유도합니다. 기본 광고는 브랜드 인지도 및 시청자 친화적 광고로 고객 보기 및 참여율을 높이는 데 가장 잘 사용됩니다. 주요 성능 지표는 다음과 같습니다 [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions], 및 [!UICONTROL Cost Per Conversion].

* **프리롤 광고(타사 전용)**: 프리롤 광고(VAST 및 VPAID)는 프리미엄 비디오 컨텐츠 앞에 표시되며, 몰입감 있고 매력적인 뷰어 환경을 제공합니다. 프리롤 비디오는 대화형, 리치 미디어 기능, 오버레이, 롤오버 및 클릭유도자를 포함할 수 있습니다. 프리롤 비디오 광고의 주요 성능 지표는 다음과 같습니다 [!UICONTROL Video Completion Rate] 및 [!UICONTROL Viewability Rate].

* **연결된 TV 광고(타사 전용)**: 연결된 TV 광고는 프리미엄 TV 비디오 컨텐츠 전후에 표시됩니다. 연결된 모든 TV 인벤토리는 TV 장치에서 실행됩니다. 즉, 비디오가 건너뛸 수 없는 전체 화면 환경에서 자동으로 재생됩니다. 연결된 TV는 TV 광고에 가장 가까운 디지털 비디오 포맷이다. 연결된 TV의 주요 성능 지표는 다음과 같습니다 [!UICONTROL Completion Rate].

* **범용 비디오 광고(타사 전용)**: 범용 비디오 광고는 연결된 TV, 프리롤 및 모바일 프리롤 광고(VAST 및 VPAID)의 모든 기능을 하나로 결합하고 비디오 컨텐츠 전후에 표시됩니다. 범용 비디오 광고는 데스크탑, 모바일 및 연결된 TV 환경에서 비디오 인벤토리를 타깃팅할 때 사용할 수 있으므로 여러 비디오 광고를 만들 필요가 없습니다. 범용 비디오에 대한 주요 성능 지표는 다음과 같습니다 [!UICONTROL Completion Rate] 및 [!UICONTROL Viewability Rate].

## DSP Ad Approvals

광고를 만들 때 DSP에서 중요한 카테고리에 대해 검토하고, URL 기능을 클릭하고, 렌더링을 미리 봅니다.

처음에는 빨간색 점이 [!UICONTROL Status] 열. 검토 프로세스는 일반적으로 24-48시간이 소요됩니다. 그러나 끊어진 광고에는 48시간 이상 보류 중인 상태가 있을 수 있으므로 광고를 거부하기 전에 오류를 수정할 시간이 있습니다. 거부된 광고에는 거부에 대한 이유가 포함되어 있습니다.

DSP이 광고를 승인하면 상태 열에 녹색 점이 표시됩니다.

![승인 지표 [!UICONTROL Status] 열](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>DSP과 SSP가 모두 크리에이티브를 승인한 경우에만 광고가 제공됩니다. 각 SSP에는 자체 승인 요구 사항 및 프로세스가 있습니다.

>[!MORELIKETHIS]
>
>* [단일 광고 만들기](ad-create.md)
>* [여러 타사 광고 만들기](ad-create-multiple.md)
>* [광고 사양](ad-specs.md)


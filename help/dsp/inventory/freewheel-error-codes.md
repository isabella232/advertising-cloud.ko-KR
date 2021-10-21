---
title: 에 대한 오류 코드 [!DNL FreeWheel] 광고 제출
description: 광고 제출을 위해 반환되는 오류 코드를 참조합니다. [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: d2ad7d47d9cf13411fc831526a6fa4ff698b0a15
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 2%

---

# 에 대한 오류 코드 [!DNL FreeWheel] 광고 제출

실패한 광고 제출에 대한 오류 메시지는 Advertising Cloud DSP 또는 [!DNL FreeWheel]. 오류 메시지는 [!UICONTROL API Response] 열 [[!UICONTROL Freewheel Status] 대화 상자](freewheel-check-status.md).

## Advertising Cloud DSP 내부 오류

| 오류 메시지 | 설명 | 다음 단계 |
|--- |--- |--- |
| [!DNL 상태 응답 대기 중 [!DNL FreeWheel]] | [!DNL FreeWheel] 제출이 성공했거나 실패했다는 답변을 아직 받지 못했습니다. | 10분 후에 상태를 다시 확인합니다. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] 지정된 시계 번호가 없으면 UK 광고를 허용하지 않습니다. | 광고에 클럭 번호를 지정한 다음 광고를 다시 제출합니다. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | 광고를 제출하려고 할 때 트랜스코더가 광고 코드 변환을 완료하지 않았습니다. | 10분을 기다린 다음 광고를 다시 제출합니다. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | 제출된 거래는 프로그램 방식의 보장 거래로 설정되지 않았다. [!DNL FreeWheel] 보증 계약만 수락합니다. | 프로그램 방식으로 보장되는 거래로 거래 ID를 설정합니다. 광고가 자동으로 [!DNL FreeWheel] 거래 ID 워크플로우가 끝날 때 프로그래밍 방식으로 보장된 기본 배치를 저장하는 경우입니다. |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | 제출된 거래 ID가 없거나 Adobe 끝에서 활성 상태가 아닙니다. | 거래가 활성화 되었는지 확인한 다음 광고를 다시 제출합니다. |
| [!DNL \[public_id=]\&lt;deal>] 존재하지 않음 | 제출된 거래 ID가 [!DNL FreeWheel] 끝. | 다음 사항에 문의하십시오. [!DNL FreeWheel] 담당자 를 참조하십시오. |
| [!DNL Ad with identifier] \&lt;*광고 이름*\> [!DNL was not found.] | 제출된 광고 키가 없거나 Adobe 끝에서 활성 상태가 아닙니다. | 올바른 광고 키를 찾은 다음 광고를 다시 제출합니다. |
| [!DNL Pending Submission] | 제출이 아직 보류 중입니다. | 페이지를 새로 고칩니다. |

{style=&quot;table-layout:auto&quot;}

## FreeWheel API 오류

| 코드 | 의미 | 설명 | 다음 단계 |
|--- |--- |--- |--- |
| 401년 | 권한 없음 | 액세스 자격 증명이 잘못되었거나, 없거나, 잘못되었습니다. | 다음 사항에 문의하십시오. [!DNL Adobe] 계정 관리자. |
| 403년 | 금지됨 | 서버가 요청을 이해했지만 승인하지 않습니다. | 다음 사항에 문의하십시오. [!DNL Adobe] 계정 관리자. |
| 404년 | 없음 | 요청한 리소스를 사용할 수 없습니다. PUT 작업에서 크리에이티브 ID를 찾을 수 없으면 404가 반환됩니다. | 다음 사항에 문의하십시오. [!DNL Adobe] 계정 관리자. |
| 405년 | 메서드가 허용되지 않음 | 해당 리소스에서 지원하지 않는 요청 메서드를 사용하여 리소스를 요청했습니다(예: POST에서 데이터를 전송해야 하는 메서드에 GET 사용 또는 읽기 전용 리소스에 대한 PUT 사용). | 다음 사항에 문의하십시오. [!DNL Adobe] 계정 관리자. |
| 408년 | 요청 시간 초과 | 이 요청을 처리하는 동안 시간 제한이 발생했습니다. 시간 초과는 일반적으로 특정 리소스에 대한 단독 액세스 동시 요청에 의해 발생합니다. | 이 상태를 받으면 요청을 다시 제출합니다. 문제가 지속되면 [!DNL Adobe] 계정 관리자. |
| 422년 | 처리할 수 없는 엔터티 | 리소스가 잘못되었습니다. 이 오류는 요청 본문이 잘못되었거나 생성/업데이트된 리소스가 잘못된 경우(예: 거래 ID가 없는 경우) 발생합니다. 자세한 내용은 [FreeWheel API 422 오류](#freewheel-422-errors) 추가 정보. | 다음 사항에 문의하십시오. [!DNL Adobe] 계정 관리자. |
| 500년 | 내부 서버 오류 | API 시스템 오류입니다. | 다음 사항에 문의하십시오. [!DNL Adobe] 계정 관리자. |

{style=&quot;table-layout:auto&quot;}

## FreeWheel API 422 오류 {#freewheel-422-errors}

| 코드 | HTTP 코드 | 설명 |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422년 | 요청 데이터가 잘못된 json 형식입니다. 자세한 내용은 오류 메시지를 참조하십시오. |
| DATA_VALIDATION_FAILURE | 422년 | 요청 데이터에 필수 필드가 없거나 데이터 형식이 잘못되었습니다. 자세한 내용은 오류 메시지를 참조하십시오. |
| DATA_DEAL_INVALID | 422년 | 거래가 잘못 구성되었거나 존재하지 않습니다. 자세한 내용은 오류 메시지를 참조하십시오. |
| DATA_DEAL_GET_FAILURE | 422년 | 이 거래를 찾을 수 없거나 해당 구성에 문제가 있습니다. 자세한 내용은 오류 메시지를 참조하십시오. |
| DATA_CREATIVE_INGEST_FAILURE | 422년 | 광고 URL이 잘못되었습니다. 자세한 내용은 오류 메시지를 참조하십시오. |
| DATA_CREATIVE_LINK_FAILURE | 422년 | 광고 문안이 거래의 광고 단위 노드에 연결되어 있지 않았습니다. 자세한 내용은 오류 메시지를 참조하십시오. |
| DATA_CREATIVE_UPDATE_FAILURE | 422년 | 크리에이티브 내용은 업데이트되지 않았습니다. 자세한 내용은 오류 메시지를 참조하십시오. |
| DATA_DSP_GET_FAILURE | 422년 | DSP이 시스템 내에 없습니다. |
| DATA_CREATIVE_UNLINK_FAILURE | 422년 | 광고 단위가 광고 단위에 연결되지 않았습니다. |
| DATA_CREATIVE_DELETE_FAILURE | 422년 | 크리에이티브는 삭제되지 않았습니다. |
| DATA_CREATIVE_DETECTION_FAILURE | 422년 | URL이 검색되지 않았습니다. |
| DATA_ENTITY_NOT_FOUND | 422년 | 크리에이티브는 존재하지 않습니다. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [FreeWheel에서 프로그래밍 방식 보장 거래 설정 개요](/help/dsp/inventory/freewheel-overview.md)
>* [거래 ID 받은 편지함에서 거래 수락](deal-id-inbox-accept.md)
>* [FreeWheel에 프로그램 방식으로 보장되는 거래를 위한 광고 제출](/help/dsp/inventory/freewheel-submit.md)
>* [광고 상태 확인 [!DNL FreeWheel] 프로그램 방식의 보장 거래](/help/dsp/inventory/freewheel-check-status.md)


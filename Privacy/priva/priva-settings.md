---
title: Priva 설정 구성
f1.keywords:
- CSH
ms.author: chvukosw
author: chvukosw
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-priva-subject-rights-requests
- M365-priva-privacy-risk-management
search.appverid:
- MOE150
- MET150
description: Microsoft Priva의 전역 설정 옵션에 대해 자세히 알아보습니다.
ms.openlocfilehash: 9b59dcd875f248dd4a15be47d2f4383e8f656155
ms.sourcegitcommit: 1f3f2757f456628ec904bc3df985b00ffba8f892
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2022
ms.locfileid: "62542826"
---
# <a name="configure-priva-settings"></a>Priva 설정 구성

화면의 오른쪽 위 모서리에 있는 기어 아이콘을 선택하여 Microsoft Priva의 설정을 관리할 수 있습니다. 여기서 옵션을 사용하면 높은 수준의 기본 설정을 설정하고 주요 속성을 사용자 지정할 수 있습니다. 이 페이지에서는 기본 범주에 대한 설정 제공합니다.

## <a name="anonymization"></a>Anonymization

이 기능을 사용하면 개인 정보 보호 위험 관리 기능 내에서 특정 역할의 사용자에게 사용자 이름의Onymized 버전을 표시하는 데 사용할 수 있습니다. 중요한 데이터를 검토하는 동안 사용자의 ID를 마스킹할 수 있도록 식별 가능한 표시 이름을 일반 레이블로 대체합니다. 이 옵션은 주체 권한 요청 솔루션에는 적용되지 않습니다.

## <a name="user-notification-emails"></a>사용자 알림 전자 메일  

개인 정보 보호 위험 관리의 정책을 사용하면 사용자 환경에서 잠재적인 개인 정보 위험을 평가하기 위한 매개 변수를 설정할 수 있습니다. 정책 일치가 감지되면 개인 정보 보호 위험 관리는 취할 시정 조치에 대한 권장 사항과 개인 정보 보호 교육 링크가 있는 전자 메일을 사용자에게 보낼 수 있습니다. 이 설정 개인 정보 위험 관리의 전자 메일 알림 기능을 전체적으로 활성화 또는 비활성화할 수 있습니다. 전자 메일에서 알림 기능이 설정 모든 전자 메일이 사용하지 않도록 설정됩니다. 정책에 대한 자세한 내용은 [Create policies in Privacy Risk Management를 참조합니다](risk-management-policies.md).

## <a name="teams-collaboration"></a>Teams 공동 작업  

사용자 Microsoft Teams 권한 요청과 통합하여 이해 관계자와의 공동 작업을 향상합니다. 주체 권한 요청을 만들 때마다 연결된 팀이 Teams. 사용자는 요청의 공동 작업자 탭에서 팀에 추가할 수 있습니다. 주체 권한 요청에 대한 자세한 내용은 [Priva Subject Rights Requests에 대해 자세히를 참조합니다](subject-rights-requests.md).

## <a name="data-matching"></a>데이터 일치  

이 섹션에서는 데이터 주체의 특성을 설명하는 데이터 스마마를 업로드할 수 있습니다. 이렇게 하면 데이터 주체 환경 내에서 개인 데이터를 검색할 때 올바른 데이터 주체가 식별될 Microsoft 365 있습니다. Schemas 및 규칙 패키지는 XML 형식으로 만들어 업로드됩니다. 개인 **데이터 업로드에서** 제공된 SCHEMA와 일치하는 개인 데이터를 제출할 수도 있습니다. 직접 파일을 만들고 업로드하거나 Azure에서 개인 데이터를 업로드할 수 있습니다. 주체 권한 요청에 대한 자세한 내용은 [Priva Subject Rights Requests에 대해 자세히를 참조합니다](subject-rights-requests.md).

## <a name="data-retention-periods"></a>데이터 보존 기간

이 설정은 Priva Subject Rights Requests와 관련이 있습니다. 이를 통해 요청이 닫힌 후 수집된 데이터 및 보고서를 보존하려는 기간에 대한 기본 설정을 제어할 수 있습니다. 이 설정은 30일 또는 90일로 설정할 수 있으며 만든 모든 주체 권한 요청에 적용됩니다. 데이터 보존 기간이 조직의 정책 및 법적 의무를 준수하는지 확인하는 것이 좋습니다. 자세한 내용은 주체 권한 [요청에 대한 데이터 보존 설정에 대해 자세히 알아보아야 합니다](subject-rights-requests-reports.md#manage-data-retention).

## <a name="data-review-tags"></a>데이터 검토 태그

주체 권한 요청에서 검색된 파일을 표시하는 데 사용할 태그를 관리합니다. 이러한 태그를 사용하여 수동으로 삭제해야 할 수 있는 콘텐츠와 같이 추가 주의가 필요한 콘텐츠를 나타낼 수 있습니다. 이 설정 섹션에서는 사용자 지정 태그의 이름과 설명을 편집할 수 있습니다. 시스템에서 제공하는 기본 제공 태그에 대한 태그 설명을 편집할 수도 있습니다. 시스템 태그의 이름은 변경할 수 없습니다. 주체 권한 요청에 대한 자세한 내용은 주체 권한 요청에 대한 데이터 [검토를 참조합니다](subject-rights-requests-data-review.md#step-3-review-data).

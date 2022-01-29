---
title: Priva 주체 권한 요청에 대한 자세한 정보
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
search.appverid:
- MOE150
- MET150
description: Microsoft Priva의 주체 권한 요청 솔루션은 개인 데이터를 찾고 콘텐츠를 검토하고 보고서를 만드는 데 도움이 됩니다.
ms.openlocfilehash: 2aba05ded8940331cedf21fdf67861f5fe403dac
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/28/2022
ms.locfileid: "62249245"
---
# <a name="learn-about-priva-subject-rights-requests"></a>Priva 주체 권한 요청에 대한 자세한 정보

전 세계의 특정 개인 정보 보호 규정에 따라 개인 *(또는 데이터* 주체)은 회사가 수집한 개인 데이터를 검토하거나 관리하기 위한 요청을 할 수 있습니다. 이러한 요청을 DSRs(데이터 주체 요청), DSARS(데이터 주체 액세스 요청) 또는 소비자 권한 요청이라고도 합니다. 많은 양의 정보를 저장하는 기업의 경우 관련 데이터를 찾는 것이 큰 과제가 될 수 있습니다.

Microsoft Priva는 주체 권한 요청 솔루션을 통해 이러한 문의를 처리하는 데 도움이 될 수 있습니다. 또한 주제 데이터를 검색하고, 결과를 검토하고, 적절한 파일을 수집하고, 보고서를 생성하는 데 도움이 될 수 있는 워크플로, 자동화 및 공동 작업 기능을 제공합니다.

## <a name="how-priva-supports-subject-rights-request-fulfillment"></a>Priva가 주체 권한 요청 이행을 지원하는 방법

주체 권한 요청 주기는 조직에 대한 개인의 요청으로 시작됩니다. 일단 수신된 Priva의 기능을 사용하여 해당 데이터를 수집하고, 공동 작업하고, 검토하고, 보고서를 만들 수 있습니다. 그런 다음 데이터 주체에게 찾은 결과를 알리고 Priva 외부에서 요청을 이행하는 데 필요한 기타 작업(예: 데이터 지우기)을 수행할 수 있습니다. 워크플로를 관리하고 자동화하는 데 도움을 주기 위해 Priva의 통합된 통합 템플릿을 Power Automate 있습니다.

![주체 권한 요청에 대한 워크플로입니다.](../media/priva-srr-cycle.png)

### <a name="create-requests-and-collect-data"></a>요청 만들기 및 데이터 수집

Priva는 조직에서 저장하는 콘텐츠에서 데이터 주체와 관련된 데이터를 찾기 위한 강력한 검색 옵션을 Microsoft 365. 또한 이러한 요청에 대해 수집한 데이터 내에서 검토할 항목의 우선 순위를 지정하는 데 도움이 됩니다. Priva는 잠재적으로 기밀이 Microsoft Information Protection 수 있는 콘텐츠를 나타내며, 이러한 레이블로 항목에 플래그를 지정하는 민감도 레이블을 인식하고 있습니다. 또한 Priva는 여러 사용자 데이터가 포함될 수 있는 항목을 검색하고 플래그를 지정합니다. 여기서 데이터 주체에게 콘텐츠를 제공하기 전에 콘텐츠를 재배치해야 할 수 있습니다.

자세한 내용은 주체 권한 요청 [만들기를 참조합니다](subject-rights-requests-create.md).

### <a name="data-matching"></a>데이터 일치

데이터 일치를 사용하면 Priva를 사용하여 정확한 제공된 데이터 값에 따라 데이터 주체를 식별할 수 있습니다. 이 유형의 정보를 업로드하면 콘텐츠를 검색하는 정확도를 높일 수 있으며 주체 권한 요청을 만들 때 필드를 수동으로 제공해야 하는 필요성이 간소화됩니다. 또한 주체 권한 요청 내의 컨텍스트와 가장 많은 데이터 주체 콘텐츠가 있는 항목을 소개하는 개요 타일에 대한 컨텍스트를 제공합니다. 자세한 내용은 주체 권한 요청에 [대한 데이터 일치를 참조합니다](subject-rights-requests-data-match.md).

### <a name="review-data-and-collaborate-on-requests"></a>데이터 검토 및 요청 공동 작업

데이터가 수집된 후 결과를 평가하고, 보고서 및 내보내기에서 포함할 가장 관련성이 높은 항목을 선택하고, 필요한 모든 항목을 시정할 수 있습니다. 이는 주체 권한 요청 파이프라인 내의 팀 구성원 간에 공동으로 수행할 수 있습니다.

자세한 내용은 주체 권한 [요청에 대한 데이터 검토를 참조합니다](subject-rights-requests-data-review.md).

### <a name="fulfill-requests"></a>요청 이행

Priva는 보고서를 만들고 데이터 주체에게 다시 보낼 파일을 수집하는 도구를 제공합니다. 자세한 내용은 보고서 생성 및 [주체 권한 요청 이행을 참조합니다](subject-rights-requests-reports.md).

### <a name="automate-tasks"></a>작업 자동화

기본 제공 템플릿을 사용하여 Priva 내에서 워크플로 프로세스를 만들고 자동화할 Power Automate 있습니다. 이러한 템플릿은 ServiceNow에서 티켓을 작성하거나 일정 초대 설정과 같은 작업을 지원합니다. 자세한 내용은 주체 권한 요청에서 작업 [자동화를 참조합니다](subject-rights-requests-automate.md).

## <a name="legal-disclaimer"></a>법적 고지 조항

[Microsoft Priva 법적 고지 조항](priva-disclaimer.md)

---
title: Priva 주체 권한 요청에 대해 알아보기
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
description: Microsoft Priva의 주체 권한 요청 솔루션은 개인 데이터를 찾고 콘텐츠를 검토하고 보고서를 만드는 데 공동 작업하는 데 도움이 됩니다.
ms.openlocfilehash: 37ee3fc795559d216a7a8cd620cff2c3ca689c2b
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930629"
---
# <a name="learn-about-priva-subject-rights-requests"></a>Priva 주체 권한 요청에 대해 알아보기

전 세계의 특정 개인 정보 보호 규정에 따라 개인(또는 *데이터 주체)은* 회사가 수집한 자체에 대한 개인 데이터를 검토하거나 관리하도록 요청할 수 있습니다. 이러한 요청을 DSR(데이터 주체 요청), DSRS(데이터 주체 액세스 요청) 또는 소비자 권한 요청이라고도 합니다. 많은 양의 정보를 저장하는 회사의 경우 관련 데이터를 찾는 것이 매우 어려울 수 있습니다.

Microsoft Priva는 주체 권한 요청 솔루션을 통해 이러한 문의를 처리하는 데 도움이 될 수 있습니다. 주체 데이터를 검색하고, 결과를 검토하고, 적절한 파일을 수집하고, 보고서를 생성하는 데 도움이 되는 워크플로, 자동화 및 공동 작업 기능을 제공합니다.

## <a name="how-priva-supports-subject-rights-request-fulfillment"></a>Priva가 주체 권한 요청 이행을 지원하는 방법

주체 권한 요청 주기는 조직에 대한 개인의 요청으로 시작됩니다. 수신되면 Priva의 기능을 사용하여 해당 데이터를 수집하고, 공동 작업하고, 검토하고, 보고서를 만들 수 있습니다. 그런 다음, 데이터 주체에게 조사 결과를 알리고 Priva 외부에서 필요한 다른 작업을 수행하여 데이터 삭제와 같은 요청을 수행할 수 있습니다. 워크플로를 관리하고 자동화하는 데 도움이 되도록 통합된 Power Automate 템플릿을 사용할 수도 있습니다.

### <a name="create-requests-and-collect-data"></a>요청 만들기 및 데이터 수집

Priva는 조직에서 Microsoft 365 저장하는 콘텐츠에서 데이터 주체와 관련된 데이터를 찾기 위한 강력한 검색 옵션을 제공합니다. 또한 이러한 요청에 대해 수집하는 데이터 내에서 검토할 항목의 우선 순위를 지정하는 데 도움이 됩니다. Priva는 잠재적으로 기밀이며 특별 검토가 필요할 수 있는 콘텐츠를 나타내는 Microsoft Purview Information Protection 민감도 레이블을 알고 있으며 이러한 레이블이 있는 항목에 플래그를 지정합니다. 또한 Priva는 여러 사람의 데이터를 포함할 수 있는 항목을 검색하고 플래그를 지정할 수 있습니다. 여기서 데이터를 데이터 주체에 공급하기 전에 콘텐츠를 수정해야 할 수 있습니다.

자세한 내용은 [주체 권한 요청 만들기를](subject-rights-requests-create.md) 참조하세요.

### <a name="data-matching"></a>데이터 일치

데이터 일치를 사용하면 Priva가 정확히 제공된 데이터 값을 기반으로 데이터 주체를 식별할 수 있습니다. 이 형식의 정보를 업로드하면 콘텐츠 찾기의 정확도를 높일 수 있으며 주체 권한 요청을 만드는 동안 필드를 수동으로 제공해야 하는 필요성이 간소화됩니다. 또한 주체 권한 요청 및 가장 많은 데이터 주체 콘텐츠로 항목을 표시하는 개요 타일에 대한 컨텍스트를 제공합니다. 자세한 내용은 [주체 권한 요청에 대한 데이터 일치를 참조하세요](subject-rights-requests-data-match.md).

### <a name="review-data-and-collaborate-on-requests"></a>데이터 검토 및 요청에 대한 공동 작업

데이터를 수집한 후에는 결과를 평가하고 보고서 및 내보내기에서 포함할 가장 관련성이 큰 항목을 선택하고 필요한 수정 작업을 수행할 수 있습니다. 이 작업은 주체 권한 요청 파이프라인 내에서 팀 구성원 간에 공동으로 수행할 수 있습니다.

자세한 내용은 [주체 권한 요청에 대한 데이터 검토를](subject-rights-requests-data-review.md) 참조하세요.

### <a name="fulfill-requests"></a>요청 처리

Priva는 보고서를 만들고 데이터를 수집하여 데이터 주체로 다시 보낼 수 있는 도구를 제공합니다. 자세한 내용은 [보고서 생성 및 주체 권한 요청 수행을](subject-rights-requests-reports.md) 참조하세요.

### <a name="automate-tasks"></a>작업 자동화

기본 제공 Power Automate 템플릿을 사용하여 Priva 내에서 워크플로 프로세스를 만들고 자동화할 수 있습니다. 이러한 템플릿은 ServiceNow에서 티켓 제출 또는 일정 초대 설정과 같은 작업을 지원합니다. 자세한 내용은 [주체 권한 요청에서 작업 자동화를 참조하세요](subject-rights-requests-automate.md).

## <a name="legal-disclaimer"></a>법적 고지 사항

[Microsoft Priva 법적 고지 사항](priva-disclaimer.md)

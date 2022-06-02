---
title: Microsoft Graph API 및 Power Automate 통합
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
description: Microsoft Graph API 및 Power Automate 통합하여 Priva 주체 권한 요청 기능을 확장하는 방법을 알아봅니다.
ms.openlocfilehash: e4fcad2067ece3d1a6338e6d4891c59d91205a33
ms.sourcegitcommit: 9315064bf5bb9e889318e61ec5f082f36c815e1e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65851643"
---
# <a name="integrate-and-extend-through-microsoft-graph-api-and-power-automate"></a>Microsoft Graph API 및 Power Automate 통해 통합 및 확장

Microsoft Graph 주체 권한 요청 API를 사용하여 기존 비즈니스 프로세스 및 도구와 Priva 주체 권한 요청 통합할 수 있습니다. 일정 미리 알림 설정 및 ServiceNow에서 사례 만들기와 같은 작업에 기본 제공 Power Automate 흐름을 사용하여 주체 권한 요청의 자동화 기능을 확장할 수도 있습니다.

## <a name="microsoft-graph-subject-rights-requests-api"></a>Microsoft Graph 주체 권한 요청 API

Microsoft 365 주체 권한 요청 API는 기존 주체 권한 전략에 자동화를 도입하는 간단하면서도 강력한 방법을 제공합니다. 개인이 조직의 정보를 요청하는 경우 API를 통해 해당 요청에 대한 기준에 따라 Microsoft 365 내에서 해당 요청을 만들 수 있습니다. Microsoft 365 주체 권한 요청을 만들고, 진행 상황을 추적하고, 요청이 처리를 완료하고 콘텐츠를 검색할 준비가 되면 승인할 수 있습니다.

MICROSOFT API는 ISV, 솔루션의 Microsoft 365 수용하려는 파트너 및 해당 기간 업무 애플리케이션에서 API를 사용하려는 조직과 같이 솔루션을 확장하기 위해 누구나 사용할 수 있습니다.

[Microsoft Graph 주체 권한 요청 API 사용](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)에서 전체 설명서를 봅니다.

## <a name="power-automate-templates-for-subject-rights-requests"></a>주체 권한 요청에 대한 Power Automate 템플릿

Microsoft Power Automate 애플리케이션 및 서비스에서 작업을 자동화하는 워크플로 서비스입니다. 주체 권한 요청에는 사용자가 주체 권한 요청을 관리하는 데 도움이 되는 기본 제공 Power Automate 템플릿이 포함되어 있습니다. 사용자는 ServiceNow에서 티켓을 만들고 기한에 대한 일정 미리 알림을 추가하는 등의 프로세스에 대한 자동화 흐름을 설정할 수 있습니다. Power Automate 대한 자세한 내용은 [Power Automate 설명서를 참조하세요](/power-automate/getting-started).

주체 권한 요청 구독을 구매한 경우 권장되는 Power Automate 템플릿을 사용하기 위해 별도의 Power Automate 라이선스가 필요하지 않습니다. 이러한 템플릿은 조직을 지원하고 핵심 주체 권한 요청 시나리오를 포함하도록 사용자 지정할 수 있습니다. 그러나 이러한 템플릿에서 프리미엄 Power Automate 기능을 사용하거나 고유한 템플릿을 만들려면 추가 라이선스가 필요할 수 있습니다.

### <a name="available-templates"></a>사용 가능한 템플릿

- **ServiceNow에서 Priva 개인 정보 관리 사례에 대한 레코드 만들기**: 이 템플릿은 ServiceNow 솔루션을 사용하여 주체 권한 요청 사례를 추적하려는 조직을 위한 것입니다. ServiceNow에 연결할 계정을 포함한 ServiceNow 인스턴스 세부 정보를 입력하라는 메시지가 표시됩니다. 이 계정에는 ServiceNow에서 인시던트를 만들고 인시던트 세부 정보를 입력할 수 있는 기능이 있어야 합니다. 인스턴스에 연결되면 주체 권한 요청 관리자는 ServiceNow에서 사례에 대한 레코드를 만들 수 있으며 필요한 경우 템플릿이 선택한 필드에 채울 항목을 사용자 지정할 수 있습니다. 커넥터에 대한 자세한 내용은 [ServiceNow 커넥터 설명서를 참조하세요](/connectors/service-now/).

- **Priva 개인 정보 관리 사례에 대한 후속 조치를 위해 일정 미리 알림을 추가** 합니다. 이 템플릿은 주체 권한 요청에 대한 Outlook 일정에서 기한 미리 알림을 설정하는 데 사용됩니다. 이 도구는 요청의 이름 및 기한과 같은 요청의 속성에서 특정 세부 정보를 채웁습니다. 설명이 포함된 세부 정보를 추가하고, 받는 사람을 지정하고, 다른 고급 설정을 조정할 수 있습니다.

- **Priva 주체 권한 요청에 대한 태그로 파일 가져오기**: 이 템플릿을 사용하면 특정 태그가 지정된 주체 권한 요청에 대한 파일을 검색할 수 있습니다. 흐름을 편집하여 사용자 지정 작업을 수행하거나 내부 프로세스 또는 도구에 사용할 반환된 파일 목록을 볼 수 있습니다.

### <a name="create-a-new-power-automate-flow-from-a-template"></a>템플릿에서 새 Power Automate 흐름 만들기

1. [Microsoft Purview 규정 준수 포털](https://compliance.microsoft.com/) 왼쪽 탐색 영역에서 **Priva 주체 권한 요청** 선택합니다.

2. 작업하려는 주체 권한 요청을 찾아 목록에서 선택하여 세부 정보 페이지를 엽니다.

3. 오른쪽 위 모서리에서 **자동화** 를 선택한 다음 **Power Automate 흐름 관리를** 선택하여 흐름 플라이아웃 창을 엽니다.

4. **새로** 만들기를 선택하고 사용 가능한 옵션에서 사용할 템플릿을 선택합니다. 여기에서 프롬프트에 따라 흐름 빌드를 완료하는 단계를 사용자 지정하고 추가합니다. 옵션은 사용하는 템플릿에 따라 달라집니다(아래 템플릿 형식 참조).

5. 작업을 마치면 **저장** 을 선택합니다.

템플릿의 인스턴스를 저장한 후 흐름 인스턴스에 올바른 컨텍스트와 ID가 있도록 요청의 세부 정보 페이지에서 실행해야 합니다. 요청을 열고 **, 자동화** 메뉴로 돌아가서 템플릿을 선택하고, **흐름 실행을** 선택합니다. **흐름 실행 작업 참조** 를 선택하여 과거 활동을 볼 수 있습니다.

### <a name="share-a-power-automate-flow"></a>Power Automate 흐름 공유

Power Automate 흐름을 공유하면 다른 소유자를 추가할 수 있으며 흐름을 편집, 업데이트 및 삭제할 수 있습니다. 모든 소유자는 실행 기록에 액세스하고 다른 소유자를 추가하거나 제거할 수 있습니다. 

흐름을 공유하려면 작업하려는 주체 권한 요청을 열고 **자동화** 를 선택한 다음 **Power Automate 흐름 관리를** 선택합니다. 이 창에서 기존 흐름을 선택한 다음 **공유** 옵션을 사용하여 사용자 또는 그룹을 추가할 수 있습니다.

이 창에서는 Power Automate 흐름에서 사용되는 서비스에 대한 포함된 연결을 관리하는 옵션도 제공합니다. 이러한 설정을 변경하면 흐름을 실행하는 기능에 영향을 줄 수 있습니다.

### <a name="edit-or-delete-power-automate-flow"></a>Power Automate 흐름 편집 또는 삭제

Power Automate 흐름의 세부 정보를 조정하려면 요청 세부 정보 페이지의 오른쪽 위 모서리에서 **자동화** 를 선택한 다음, **Power Automate 흐름 관리를** 선택합니다.

**Power Automate 흐름** 창에서 편집할 흐름을 선택하고 명령 모음에서 **편집** 을 선택하여 단계를 편집하거나 추가합니다. 완료되면 **저장** 을 선택합니다.

흐름을 삭제하려면 **Power Automate 흐름** 창의 목록에서 흐름을 선택하고 명령 모음에서 **삭제** 를 선택합니다. 흐름은 모든 소유자에 대해 제거되고 모든 사용자에 대해 제거됩니다. 이전 흐름 인스턴스는 데이터 손실을 방지하기 위해 계속 실행됩니다. 삭제가 최종되기 전에 확인하라는 메시지가 표시됩니다.

## <a name="legal-disclaimer"></a>법적 고지 사항

[Microsoft Priva 법적 고지 사항](priva-disclaimer.md)

---
title: '주체 권한 요청에서 작업 자동화 '
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
description: Microsoft Power Automate 사용하여 Priva에서 주체 권한 요청에 대한 필수 작업을 자동화하는 방법을 알아봅니다.
ms.openlocfilehash: ec9edde16b60c2326ca899e587dfe5dc7a1e32f5
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930499"
---
# <a name="automate-tasks-in-subject-rights-requests"></a>주체 권한 요청에서 작업 자동화 

Microsoft Power Automate 애플리케이션 및 서비스에서 작업을 자동화하는 워크플로 서비스입니다. Microsoft Priva 주체 권한 요청에 Power Automate 흐름을 사용하도록 설정하면 ServiceNow에서 티켓을 만들거나 기한에 대한 일정 미리 알림을 추가하는 등 사례 및 사용자에 대한 중요한 작업을 자동화할 수 있습니다. Power Automate 대한 자세한 내용은 [설명서 사이트를](/power-automate/getting-started) 방문하세요.

주체 권한 요청 구독이 있는 고객은 Priva에 권장되는 Power Automate 템플릿을 사용하기 위해 다른 Power Automate 라이선스가 필요하지 않습니다. 이러한 템플릿은 조직을 지원하고 핵심 주체 권한 요청 시나리오를 포함하도록 사용자 지정할 수 있습니다. 이러한 템플릿에서 프리미엄 Power Automate 기능을 사용하거나, Microsoft 365 규정 준수 커넥터를 사용하여 사용자 지정 템플릿을 만들거나, Microsoft 365 다른 규정 준수 영역에 Power Automate 템플릿을 사용하도록 선택하는 경우 더 많은 Power Automate 라이선스가 필요할 수 있습니다.

## <a name="create-a-new-power-automate-flow-from-a-template"></a>템플릿에서 새 Power Automate 흐름 만들기

1. [Microsoft Purview 규정 준수 포털](https://compliance.microsoft.com/)에서 탐색의 Priva 섹션으로 이동하여 **Priva 주체 권한 요청을** 선택합니다.
1. 목록에서 작업하려는 주체 권한 요청을 열고 **자동화**, **Power Automate 흐름 관리를** 차례로 선택합니다. 그러면 흐름 플라이아웃 창이 열립니다.
1. **새** 옵션을 사용하고 사용 가능한 옵션에서 사용할 템플릿을 선택합니다. 여기에서 마법사의 프롬프트에 따라 설정을 완료합니다. 옵션은 템플릿 유형에 따라 달라집니다.

템플릿의 인스턴스를 저장한 후 흐름 인스턴스에 올바른 컨텍스트 및 ID가 있도록 주체 권한 요청의 세부 정보 페이지에서 실행해야 합니다. 요청을 열고 **, 자동화** 메뉴로 돌아가서 템플릿을 선택하고, **흐름 실행을** 선택합니다. **흐름 실행 작업 참조** 를 선택하여 과거 활동을 볼 수 있습니다.

### <a name="power-automate-templates-in-priva"></a>Priva에서 템플릿 Power Automate

- **ServiceNow에서 개인 정보 관리 사례에 대한 레코드 만들기**: 이 템플릿은 ServiceNow 솔루션을 사용하여 주체 권한 요청 사례를 추적하려는 조직을 위한 것입니다. ServiceNow에 연결할 계정을 포함하는 ServiceNow 인스턴스 세부 정보를 입력하라는 메시지가 표시됩니다. 이 계정에는 ServiceNow에서 인시던트를 만들고 인시던트 세부 정보를 입력할 수 있는 기능이 있어야 합니다. 인스턴스에 연결되면 주체 권한 요청 관리자는 ServiceNow에서 사례에 대한 레코드를 만들 수 있으며 필요한 경우 템플릿이 선택한 필드에 채울 항목을 사용자 지정할 수 있습니다. 커넥터에 대한 자세한 내용은 [ServiceNow 커넥터 참조 페이지를 참조하세요](/connectors/service-now/).
- **일정 미리 알림 만들기**: 이 템플릿은 주체 권한 요청에 대한 Outlook 일정에서 기한 미리 알림을 설정하는 데 사용됩니다. 이 도구는 요청의 이름 및 기한과 같은 요청의 속성에서 특정 세부 정보를 채웁습니다. 설명이 포함된 세부 정보를 추가하고, 받는 사람을 지정하고, 다른 고급 설정을 조정할 수 있습니다.
- **주체 권한 요청에 대한 태그로 파일 가져오기**: 이 템플릿을 사용하면 특정 태그가 지정된 주체 권한 요청에 대한 파일을 검색할 수 있습니다. 흐름을 편집하여 사용자 지정 작업을 수행하거나 내부 프로세스 또는 도구에 활용할 반환된 파일 목록을 볼 수 있습니다.

## <a name="share-a-power-automate-flow"></a>Power Automate 흐름 공유

Power Automate 흐름을 공유하면 다른 소유자를 추가하고 흐름을 편집, 업데이트 및 삭제할 수 있습니다. 모든 소유자는 실행 기록에 액세스하고 다른 소유자를 추가하거나 제거할 수도 있습니다. 흐름을 공유하려면 작업하려는 주체 권한 요청을 열고 **자동화** 를 선택한 다음 **Power Automate 흐름 관리를** 선택합니다. 이 창에서 기존 흐름을 선택한 다음 공유 옵션을 사용하여 사용자 또는 그룹을 추가할 수 있습니다.

이 창에서는 Power Automate 흐름에서 사용되는 서비스에 대한 포함된 연결을 관리하는 옵션도 제공합니다. 이러한 설정을 변경하면 흐름을 실행하는 기능에 영향을 줄 수 있습니다.

## <a name="edit-or-delete-power-automate-flow"></a>Power Automate 흐름 편집 또는 삭제

Power Automate 흐름의 세부 정보를 조정하려면 주체 권한 요청을 열고 **자동화** 를 선택하고 **Power Automate 흐름 관리를** 선택합니다. 이 창에서 기존 흐름을 선택하여 세부 정보를 볼 수 있습니다. 모든 섹션에서 편집을 사용하여 속성을 변경한 다음 저장합니다.

흐름을 완전히 제거하려면 **삭제** 옵션을 사용합니다. 모든 소유자에 대한 흐름을 제거하고 모든 사용자에 대해 제거합니다. 이전 흐름 인스턴스는 데이터 손실을 방지하기 위해 계속 실행됩니다. 삭제가 최종되기 전에 선택 사항을 확인할 수 있습니다.

## <a name="legal-disclaimer"></a>법적 고지 사항

[Microsoft Priva 법적 고지 사항](priva-disclaimer.md)

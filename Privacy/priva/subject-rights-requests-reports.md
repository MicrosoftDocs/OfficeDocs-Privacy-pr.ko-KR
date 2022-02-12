---
title: 보고서 생성 및 주체 권한 요청 수행
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
description: 주체 권한 요청에 대해 Microsoft Priva에서 만든 데이터 패키지를 관리하고 데이터 주체에 대한 요청을 이행하는 방법을 학습합니다.
ms.openlocfilehash: 9931422434414146601ede959af910caf1befcc1
ms.sourcegitcommit: 1f3f2757f456628ec904bc3df985b00ffba8f892
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2022
ms.locfileid: "62542836"
---
# <a name="generate-reports-and-fulfill-a-subject-rights-request"></a>보고서 생성 및 주체 권한 요청 수행

Microsoft Priva에서 주체 권한 요청에 대한 데이터 검토를 완료한 후 이행 요청으로 이동할 수 있습니다. Priva는 보고서를 만들고 데이터 검토 프로세스 중에 **포함** 으로 표시된 파일을 수집합니다. 이러한 데이터 패키지에서 선택한 파일을 데이터 주체에게 제출하여 요청을 완료할 수 있습니다. 또한 Priva는 Microsoft 365 권한 요청 API를 활용하여 자동화 기능을 도입할 수 있습니다.

## <a name="prepare-final-reports-for-the-data-subject"></a>데이터 주체에 대한 최종 보고서 준비

주체 권한 요청 데이터 패키지는 zip 파일로 생성됩니다. 이 패키지를 생성하는 데 최대 30분이 걸릴 수 있습니다. 준비가 되면 주체 권한 요청 페이지에서 주체 권한 요청을 열고 보고서 탭을 열고 다운로드를 찾  은 다음 zip 파일을 여십시오.

데이터 패키지에는 여러 파일이 포함되어 있습니다. Azure 폴더 외부의 파일은 참조를 위해 제공하며 주로 관리자가 사용해야 합니다. 데이터 주체의 주요 자료는 Azure 폴더에 **포함되어** 있습니다.

이 폴더의 내용을 신중하게 검토하고 데이터 주체에 필요한 파일만 제출하는 것이 좋습니다. 대응을 평가하여 해당 법률의 요구 사항을 충족하는지 확인합니다.

### <a name="azure-folder-contents"></a>Azure 폴더 내용

이 폴더를 연 다음 파일 파일을 **AEDExport.zip** 니다. 내용에는 다음이 포함됩니다.

- **Extracted_text_files 폴더** 에는 기본 파일(지원되는 경우)에서 추출된 텍스트가 포함되어 있습니다.
- **NativeFiles 폴더** 에는 기본 파일 형식의 **모든 포함** 항목이 포함됩니다.
- Redacted files are in the **NativeFiles** folder and have theuffix "_burn.pdf".
- 내보낼 파일의 이름을 고유 식별자를 사용하여 개인 데이터를 보호합니다. 를 사용하여 고유한 이름을 원본 파일 이름으로 상호 참조할 **수** Export_load_file.csv. 원래 파일 이름에는 중요한 정보가 포함되어 있을 수 있기 때문에 해당 정보에 적용되는 정책을 따라야 합니다.

zip 파일의 내용을 검토한 후 필요한 경우 수정하여 최종 패키지에 포함하지 않는 콘텐츠를 제거합니다. 완료되면 데이터 주체에게 안전하게 전송합니다.

## <a name="integrate-with-partner-solutions"></a>파트너 솔루션과 통합

기본 주체 권한 요청 API를 활용하여 Priva 주체 권한 요청 솔루션을 기존 비즈니스 프로세스 및 도구와 Microsoft 365 수 있습니다. 이를 통해 주체 권한 전략에 자동화를 도입할 수 있는 간단한 방법도 제공합니다.

데이터 주체가 조직에서 정보를 요청할 때 API를 활용하여 해당 요청에 대한 사용자 지정 기준에 Microsoft 365 내에서 해당 요청을 만들 수 있습니다. Microsoft 365 주체 권한 요청을 만들고, 해당 스테이지를 통해 요청의 진행 상황을 추적하고, 요청이 처리를 완료하고 콘텐츠를 검색할 준비가 된 경우 이를 인정할 수 있습니다. 당사의 API는 ISV, 파트너가 솔루션에서 솔루션을 수용할 수 Microsoft 365 또는 조직이 해당 비즈니스 응용 프로그램과 함께 사용할 수 있도록 하는 등 솔루션을 보다 쉽게 사용할 수 있도록 하는 데 사용할 수 있습니다.

자세한 내용은 [Microsoft Graph 권한 요청 API 사용을 참조합니다](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview).

## <a name="manage-data-retention"></a>데이터 보존 관리

이 도구를 통해 생성된 보고서 및 Azure에 저장된 주석이 있는 파일과 같은 관련 데이터는 지정된 기간 동안 저장됩니다. 데이터 보존 기간은 **Priva 설정** 정의되어 있으며 모든 주체 권한 요청에 적용됩니다. 데이터 보존 기간을 보거나 변경하기 위해 아래 단계를 따르세요.

1. Priva Subject Rights Requests의 어디에서나 설정 오른쪽 **위** 모서리에 있는 톱니바(기어 아이콘)를 선택합니다.
2. 왼쪽 **탐색에서 데이터** 보존 기간을 선택합니다.
3. 드롭다운 메뉴를 사용하여 보존 기간으로 30일 또는 90일을 선택합니다.

선택한 데이터 보존 기간이 조직의 정책 및 법적 의무를 준수하는지 확인해야 합니다.

## <a name="legal-disclaimer"></a>법적 고지 조항

[Microsoft Priva 법적 고지 조항](priva-disclaimer.md)

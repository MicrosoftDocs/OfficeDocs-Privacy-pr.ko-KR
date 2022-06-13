---
title: 주체 권한 요청의 데이터 예측 및 검색
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
description: 데이터를 검색하는 방법 및 Microsoft Priva 주체 권한 요청 검색 설정을 수정하는 방법을 이해합니다.
ms.openlocfilehash: 9d35a7f37861d7d3ecc5d1bac7db92c75939b4c3
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046748"
---
# <a name="data-estimate-and-retrieval"></a>데이터 예측 및 검색

**이 문서에서는** 주체 권한 요청의 데이터 추정 및 데이터 검색 단계를 이해합니다. 요청의 검색 쿼리를 보고 편집하여 검색을 구체화하는 방법을 알아봅니다.

## <a name="data-estimate"></a>데이터 예상
요청을 만들면 Priva 즉시 Microsoft 365 환경 내의 콘텐츠에서 데이터 주체와 일치하는 항목을 찾기 시작합니다. 기준과 일치하는 것으로 생각되는 모든 항목을 식별하면 요청 **개요 페이지의** **데이터 예상 요약** 카드에 추정치가 표시됩니다. 검색 범위 내의 데이터 양은 예상을 완료하는 데 걸리는 시간에 영향을  미칩니다.

요청은 데이터 **검색** 의 다음 단계로 자동으로 이동되며, 모든 콘텐츠 항목이 함께 수집되어 관련자가 데이터 검토에 대해 공동 작업을 수행할 수 있습니다. 경우에 따라 검색으로 이동하기 전에 데이터 예상을 일시 중지하고 계속하기 전에 수행할 다음 단계를 알려 줍니다.

### <a name="pause-in-data-estimate"></a>데이터 예측에서 일시 중지

**데이터 예상** 단계에서 요청이 일시 중지되는 두 가지 이유가 있습니다.

1. 요청을 처음 만들 때 먼저 견적을 받도록 선택할 수 있습니다. 자세한 내용은 [요청 만들기](subject-rights-requests-create.md#create-a-request) 의 5단계를 참조하세요.

2. 검토할 많은 수의 항목(10K 항목 이상)을 반환하도록 예상된 경우 워크플로가 일시 중지됩니다. 이 시점에서 결과를 미리 보고 [검색 쿼리를 편집](subject-rights-requests-create.md#refining-your-search) 할지 또는 식별된 항목을 계속 검색할지 결정할 수 있습니다.

**데이터 예측** 에서 요청이 일시 중지되면 요청 세부 정보 페이지에 항목 수, 볼륨, 위치 및 **검색 쿼리 세부 정보를 볼** 수 있는 링크에 대한 요약 정보가 포함된 카드가 표시됩니다.

![데이터 예측 카드입니다.](../media/priva-srr-data-estimate.png)

## <a name="view-and-edit-search-queries"></a>검색 쿼리 보기 및 편집

요청의 검색에 대한 자세한 정보를 보려면 **데이터 예상 요약** 카드에서 **검색 쿼리 세부 정보 보기를** 선택합니다. 쿼리를 요약하고 발견된 내용에 대한 자세한 내용을 표시하는 플라이아웃 창이 열립니다. 여기에서 다음 옵션을 사용할 수 있습니다.

- **미리 보기 결과를** 선택하여 현재 검색 설정에서 반환될 콘텐츠 형식의 미리 보기를 가져옵니다.
- **검색 쿼리 편집** 을 선택하여 검색 설정을 변경합니다.

**검색 쿼리 편집** 을 선택하면 데이터 주체를 식별하거나 조건을 변경하고 검색에서 처리할 위치를 조정하는 속성을 변경하거나 추가하는 단계별 프로세스를 진행하게 됩니다. [검색 구체화](subject-rights-requests-create.md#refining-your-search)의 지침에 따라 자세한 정보를 확인합니다. 새 검색 쿼리의 최종 버전을 검토한 다음 **저장** 을 선택하여 검색을 다시 시작할 수 있습니다.

새 예상치가 생성되고 요청 상태가 **데이터 예상** 으로 돌아갑니다. 새 검색을 완료하는 데 최대 60분이 걸릴 수 있습니다. 완료되면 요청의 세부 정보 페이지에 업데이트된 결과가 표시됩니다.

계속 진행할 준비가 되면 화면 오른쪽 위에 있는 **데이터 검색** 을 선택하여 데이터 검색 단계로 이동합니다.

## <a name="retrieve-data"></a>데이터 검색

데이터 검색 단계는 데이터 주체의 개인 데이터를 포함하는 모든 파일, 이메일, 채팅, 이미지 및 기타 콘텐츠 항목을 검색하는 경우입니다. 항목은 검토를 위해 Azure Blob Storage 컨테이너에 함께 배치됩니다. 데이터 검색은 데이터 볼륨에 따라 몇 분 또는 훨씬 더 오래 걸릴 수 있습니다.

이 단계가 완료되면 요청이 검토 **데이터의** 다음 단계로 자동으로 이동합니다.

## <a name="next-steps"></a>다음 단계

[주체 권한 요청에 대한 검토 데이터를](subject-rights-requests-data-review.md) 방문하여 주요 작업에 대해 알아보고 **데이터 검토** 단계를 위해 관련자와 공동 작업합니다.

## <a name="legal-disclaimer"></a>법적 고지 사항

[Microsoft Priva 법적 고지 사항](priva-disclaimer.md)
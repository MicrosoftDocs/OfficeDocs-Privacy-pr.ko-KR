---
title: 주체 권한 요청에 대한 데이터 일치
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
description: 데이터 주체에 대한 추가 정보를 Microsoft Priva에 업로드하는 방법을 알아봅니다.
ms.openlocfilehash: 90ee0e8e21d25954c11113992cbb7ece847c85ab
ms.sourcegitcommit: 6b88d22d0250cbb9a4ba1f71665f29cb67939851
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2022
ms.locfileid: "65059742"
---
# <a name="data-matching-for-subject-rights-requests"></a>주체 권한 요청에 대한 데이터 일치

데이터 일치를 통해 조직은 Microsoft Priva가 정확히 제공된 데이터 값을 기반으로 데이터 주체를 식별할 수 있도록 할 수 있습니다. 이렇게 하면 내부 담당자와 상호 작용하는 외부 사용자 모두에 대해 이러한 데이터 값에 해당하는 데이터 주체 콘텐츠를 찾는 정확도를 높일 수 있습니다. 또한 주체 권한 요청 생성 중에 필드를 수동으로 제공해야 하는 필요성이 간소화되고 주체 권한 요청 내에서 컨텍스트를 제공하고 항목에 가장 많은 데이터 주체 콘텐츠를 표시하는 개요 타일에 대한 컨텍스트를 제공합니다. 해당 보기에 대한 자세한 내용은 [Priva에서 개인 데이터 찾기 및 시각화를](priva-data-profile.md#items-with-the-most-data-subject-content) 참조하세요.

데이터 일치 기능을 사용하려면 개인 정보 관리 역할 그룹의 구성원이어야 합니다. [Microsoft Purview 규정 준수 포털](https://compliance.microsoft.com/)의 Priva 내에서 위쪽 탐색에서 **설정** 선택한 다음 **데이터 일치** 를 선택합니다. 여기에서 개인 데이터 스키마를 정의하고 아래와 같이 개인 데이터 업로드를 제공해야 합니다. 항목을 추가할 수 있으며 추가한 항목을 삭제할 수 있지만 항목을 수정할 수는 없습니다.

## <a name="prepare-for-data-import"></a>데이터 가져오기 준비

스키마를 정의하거나 데이터를 업로드하기 전에 데이터 주체 정보의 원본을 식별해야 합니다. 필요한 파일 형식은 Microsoft Excel 같은 애플리케이션에서 읽을 수 있는 .csv. 열 머리글이 첫 번째 행에 표시되도록 이 내보내기를 구조화합니다. 이러한 헤더에는 개인 데이터 스키마에 대한 특성의 이름이 포함되어야 합니다. 각 필드의 데이터 형식을 확인합니다. 데이터에 쉼표가 포함된 경우 이러한 값을 큰따옴표로 묶어 별도의 필드로 구문 분석하지 않도록 합니다.

## <a name="define-the-personal-data-schema"></a>개인 데이터 스키마 정의

데이터 일치를 설정하는 첫 번째 단계는 데이터 주체의 특성을 설명하는 개인 데이터 스키마를 정의하는 것입니다. 데이터 일치 설정 영역의 첫 번째 탭에 이 스키마를 업로드합니다. 필요한 파일에는 **개인 데이터 스키마** XML 파일 및 **규칙 패키지** XML 파일이 포함 됩니다.

### <a name="personal-data-schema-xml"></a>개인 데이터 스키마 XML

개인 데이터 스키마 파일은 예상되는 열 이름을 정의하는 XML 파일입니다.

- 이 스키마 파일 이름을 *pdm.xml*.
- 아래 예제와 같이 필드 이름 태그를 사용하여 각 열 이름을 정의합니다.
- 검색 가능 = "true"를 사용하여 최대 5개의 필드를 검색할 수 있습니다. 하나 이상의 필드 이름을 검색할 수 있어야 합니다. 샘플 구문: `\<Field name="" searchable=""/>`.
- 개인 데이터 스키마에는 DataStore 태그 섹션이 있습니다. 네 개의 필수 필드를 필드 이름(primaryKeyField, upnField, firstNameField, lastNameField)에 매핑해야 합니다.

예를 들어 다음 XML 파일은 5개의 필드(PatientID, MRN, SSN, 전화 및 DOB)를 사용하여 샘플 스키마를 정의합니다. primaryKeyField는 PatientID에 매핑되고, upnField는 MRN에 매핑되고, firstNameField는 FirstName에 매핑되고, lastNameField는 LastName에 매핑됩니다.

(여기에 있는 예제를 복사, 수정 및 사용할 수 있습니다.)

 ```xml
<PdmSchema xmlns="http://schemas.microsoft.com/office/2020/pdm">
      <DataStore name="Patientrecords" description="Schema for patient records" version="1" primaryKeyField="PatientID" upnField="MRN" firstNameField="FirstName" lastNameField="LastName">
            <Field name="PatientID" searchable="true"/>
            <Field name="MRN" searchable="true" />
            <Field name="FirstName" />
            <Field name="LastName" />
            <Field name="SSN" searchable="true" />
            <Field name="Phone" searchable="true" />
            <Field name="DOB" searchable="true" />
            <Field name="Gender" />
            <Field name="Address" />
      </DataStore>
</PdmSchema>
 ```

### <a name="rule-package-xml"></a>규칙 패키지 XML

규칙 패키지를 설정할 때 위에서 만든 개인 데이터 스키마 파일인 pdm.xml 올바르게 참조해야 합니다. 다음 샘플 규칙 패키지 XML에서 데이터 일치 중요 형식을 만들려면 다음 필드를 사용자 지정해야 합니다.

- **RulePack ID** &  **PrivacyMatch ID**: New-GUID를 사용하여 GUID를 생성합니다.
- **데이터 저장소**: 이 필드는 사용할 개인 데이터 일치 조회 데이터 저장소를 지정합니다. 구성된 개인 데이터 스키마의 정의된 DataStore 이름을 제공합니다.
- **idMatch**: 이 필드는 개인 데이터 일치의 기본 요소를 가리킵니다.
  - **일치**: 정확한 조회에 사용할 필드를 지정합니다. 개인 데이터 스키마에서 검색 가능한 필드 이름을 제공합니다.
  - **분류**: 이 필드는 개인 데이터 일치 조회를 트리거하는 중요한 형식 일치를 지정합니다. 기존 기본 제공 이름이나 GUID 또는 사용자 지정 중요 유형 정보를 제공할 수 있습니다. 성능 문제가 발생하지 않도록 개인 데이터 일치에서 사용자 지정 중요한 정보 유형을 분류 요소로 사용하는 경우 많은 콘텐츠(예: "숫자" 또는 "5자 단어")와 일치하는 사용자 지정 중요한 정보 유형을 사용하지 마세요. 지원 키워드를 추가하거나 사용자 지정 분류 중요한 정보 유형의 정의에 서식을 포함하는 것이 좋습니다.
- **일치**: 이 필드는 idMatch 근접에서 발견된 추가 증거를 가리킵니다.
  - **일치**: DataStore의 개인 데이터 스키마에 필드 이름을 입력합니다.
- **리소스**: 이 섹션에서는 여러 로캘의 중요한 형식에 대한 이름과 설명을 지정합니다.
  - **idRef**: ExactMatch ID에 대한 GUID를 제공합니다.
  - **이름 & 설명**: 필요에 따라 사용자 지정합니다.

아래 규칙 패키지 XML 예제에서는 개인 데이터 스키마 XML을 만드는 이전 단계의 pdm.xml 예제 파일을 참조합니다.

- **Datastore**: dataStore 이름은 앞에서 만든 스키마 파일인 dataStore = "PatientRecords"를 참조합니다.
- **idMatch**: idMatch 값은 이전에 만든 pdm.xml 파일에 나열된 검색 가능한 필드를 참조합니다. idMatch matches = "SSN".
  - **분류**: 분류 값은 기존 또는 사용자 지정 중요한 정보 유형인 분류 = "미국 SSN(사회 보장 번호)"을 참조합니다. (이 경우 미국 주민 등록 번호의 기존의 중요한 정보 유형을 사용합니다.)

다음 예제 코드와 같이 XML 형식(유니코드 인코딩 사용)으로 규칙 패키지를 만듭니다. 이 예제를 복사, 수정 및 사용할 수 있습니다.

 ```xml
<RulePackage xmlns="http://schemas.microsoft.com/office/2020/pdm">
  <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b21">
    <Version build="0" major="2" minor="0" revision="0" />
    <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
    <Details defaultLangCode="en-us">
      <LocalizedDetails langcode="en-us">
        <PublisherName>IP DLP</PublisherName>
        <Name>Health Care PDM Rulepack</Name>
        <Description>This rule package contains the Personal Data Match sensitive type for health care sensitive types.</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  <Rules>
    <PrivacyMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB381" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="6">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </PrivacyMatch>
    <LocalizedStrings>
      <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB381">
        <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
        <Description default="true" langcode="en-us">PDM Sensitive type for detecting Patient SSN.</Description>
      </Resource>
    </LocalizedStrings>
  </Rules>
</RulePackage>
 ```

## <a name="sensitive-info-types"></a>중요한 정보 유형

데이터 일치를 설정하는 두 번째 단계는 PDM(개인 데이터 일치)에 대한 고유한 중요한 정보 유형을 만드는 것입니다. [중요한 정보 유형(SIT)](/microsoft-365/compliance/sensitive-information-type-learn-about)은 사회 보장 또는 신용 카드 번호와 같은 중요한 정보를 검색하는 패턴 기반 분류자입니다. PDM 중요한 정보 유형을 설정하면 제네릭 값이 아닌 정확한 데이터 값을 사용하여 일치 항목을 검색할 수 있습니다. 이 단계를 시작하려면 **PDM 중요한 정보 유형 만들기** 를 선택하여 만들기 마법사를 시작합니다.

## <a name="upload-personal-data"></a>개인 데이터 업로드

개인 데이터 스키마 및 중요한 정보 유형을 정의한 후 세 번째 단계는 개인 데이터를 업로드하는 것입니다. **개인 데이터 업로드** 탭으로 이동하여 **추가** 를 선택하고 첫 번째 단계에서 정의한 개인 스키마를 선택한 다음, 개인 데이터가 포함된 파일을 업로드합니다.

로컬 파일을 선택하거나 개인 데이터 파일이 포함된 기존 Microsoft Azure Storage 위치에 SAS URL을 제공하여 이 개인 데이터를 업로드할 수 있습니다.
만든 스키마를 준수하는 이 프로세스의 첫 번째 단계로 파일을 준비한 경우 업로드에 해당 파일을 사용할 수 있습니다.

## <a name="legal-disclaimer"></a>법적 고지 사항

[Microsoft Priva 법적 고지 사항](priva-disclaimer.md)

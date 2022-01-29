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
description: 데이터 주체에 대한 추가 정보를 Microsoft Priva에 업로드하는 방법을 학습합니다.
ms.openlocfilehash: 1339962a1c4dba18a1d0b21d8a2cebb17ad0f91a
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/28/2022
ms.locfileid: "62249198"
---
# <a name="data-matching-for-subject-rights-requests"></a>주체 권한 요청에 대한 데이터 일치

데이터 일치를 통해 조직은 Microsoft Priva를 사용하여 정확한 제공된 데이터 값에 따라 데이터 주체를 식별할 수 있습니다. 이렇게 하여 내부 직원 및 상호 작용하는 외부 사용자 모두에 대해 해당 데이터 값에 해당하는 데이터 주체 콘텐츠를 검색하는 정확도를 높일 수 있습니다. 또한 주체 권한 요청을 생성하는 동안 필드를 수동으로 제공해야 하는 필요성을 간소화하고 주체 권한 요청 내의 컨텍스트와 가장 많은 데이터 주체 콘텐츠가 있는 항목을 소개하는 개요 타일에 대한 컨텍스트를 제공합니다. 보기에 대한 자세한 내용은 Priva에서 개인 데이터 [찾기 및 시각화를 참조합니다](priva-data-profile.md#items-with-the-most-data-subject-content).

데이터 일치 기능을 사용하려면 개인 정보 관리 역할 그룹의 구성원이 되어야 합니다. 원본의 Priva에서 Microsoft 365 규정 준수 센터 [](https://compliance.microsoft.com/)위쪽 설정 다음 데이터 일치를  **선택합니다**. 여기에서는 아래와 같이 개인 데이터chema를 정의하고 개인 데이터 업로드를 제공해야 합니다. 항목을 추가할 수 있으며 UI를 통해 추가한 항목을 삭제할 수 있습니다. 그러나 현재 UI에서 현재 있는 항목을 수정할 수는 없습니다.

## <a name="prepare-for-data-import"></a>데이터 가져오기 준비

데이터를 업로드하거나 해당 데이터를 정의하기 전에 데이터 주체 정보의 원본을 식별해야 합니다. 필수 파일 형식은 .csv 응용 프로그램에서 읽을 수 있는 Microsoft Excel. 열 머리줄이 첫 번째 행에 나타나게 이 내보내기 구조를 구성합니다. 이러한 헤더에는 개인 데이터 스마의 특성 이름이 포함되어야 합니다. 각 필드의 데이터 형식을 검사합니다. 데이터 중 하나에 콤보가 포함되어 있는 경우 이러한 값을 작은 따옴표로 하여 별도의 필드로 구문 분석되지 않도록 합니다.

## <a name="define-the-personal-data-schema"></a>개인 데이터Chema 정의

개인 데이터 schema는 데이터 주체의 특성을 설명합니다. 업로드 설정 영역의 첫 번째 탭에서 이 schema를 선택합니다. 필요한 파일에는 개인 **데이터 schema** XML 파일과 규칙 **패키지** XML 파일이 포함됩니다.

### <a name="personal-data-schema-xml"></a>개인 데이터 schema XML

개인 데이터chema 파일은 예상되는 열 이름을 정의하는 XML 파일입니다.

- 이 schema 파일의 이름을 에 *pdm.xml*.
- 아래 예제와 같은 필드 이름 태그를 사용하여 각 열 이름을 정의합니다.
- 검색할 수 있는 필드에 대해 최대 5개의 필드까지 검색 가능 = "true"를 사용할 수 있습니다. 하나 이상의 필드 이름을 검색할 수 있어야 합니다. 샘플 구문: `\<Field name="" searchable=""/>`.
- 개인 데이터 schema에는 DataStore 태그 섹션이 있습니다. primaryKeyField, upnField, firstNameField, lastNameField의 네 가지 필수 필드를 필드 이름에 매핑해야 합니다.

예를 들어 다음 XML 파일은 PatientID, MRN, SSN, 전화 및 DOB 필드가 검색 가능으로 지정된 샘플 전화 정의합니다. primaryKeyField는 PatientID에 매핑하고, upnField는 MRN에 매핑하고, firstNameField는 FirstName에 매핑하고, lastNameField는 LastName에 매핑됩니다.

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

규칙 패키지를 설정할 때 위에서 만든 개인 데이터 스마마 파일을 올바르게 참조해야 합니다. pdm.xml. 다음 샘플 규칙 패키지 XML에서 데이터 일치 중요한 유형을 만들 수 있도록 다음 필드를 사용자 지정해야 합니다.

- **RulePack id** &  **PrivacyMatch id**: New-GUID를 사용하여 GUID를 생성합니다.
- **데이터 저장소**: 이 필드는 사용할 개인 데이터 일치 보기 데이터 저장소를 지정합니다. 구성된 개인 데이터 schema의 정의된 DataStore 이름을 제공합니다.
- **idMatch**: 이 필드는 개인 데이터 일치의 기본 요소를 포인트로 합니다.
  - **일치**: 정확한 Lookup에 사용할 필드를 지정합니다. 개인 데이터 schema에서 검색 가능한 필드 이름을 제공합니다.
  - **분류**: 이 필드는 개인 데이터 일치를 트리거하는 중요한 유형 일치를 지정합니다. 기존 기본 제공 이름이나 GUID 또는 사용자 지정 중요 유형 정보를 제공할 수 있습니다. 성능 문제가 발생하지 않도록 개인 데이터 일치에서 분류 요소로 사용자 지정 중요한 정보 유형을 사용하는 경우 콘텐츠의 많은 비율(예: "숫자" 또는 "5문자 단어")과 일치하는 사용자 지정 중요한 정보 유형을 사용하지 않도록 합니다. 지원 키워드를 추가하거나 사용자 지정 분류 중요한 정보 유형 정의에 서식을 포함하는 것이 좋습니다.
- **일치**: 이 필드는 idMatch의 근접성에서 발견된 추가 증거를 포인트로 합니다.
  - **일치**: DataStore의 개인 데이터 Schema에 필드 이름을 입력합니다.
- **리소스**: 이 섹션에서는 여러 로 지역의 중요한 유형에 대한 이름과 설명을 지정합니다.
  - **idRef**: ExactMatch ID의 GUID를 제공 합니다.
  - **이름 & 설명**: 필요에 따라 사용자 지정합니다.

아래 규칙 패키지 XML 예제에서는 개인 데이터 pdm.xml XML을 만드는 이전 단계의 예제 파일을 참조합니다.

- **Datastore**: dataStore 이름은 앞에서 만든 스마마 파일을 참조합니다. dataStore = "PatientRecords".
- **idMatch: idMatch** 값은 앞에서 만든 pdm.xml 파일에 나열된 검색 가능한 필드를 참조합니다. idMatch 일치 = "SSN".
  - **분류**: 분류 값은 기존 또는 사용자 지정 중요한 정보 유형인 분류 = "미국 SSN(사회 보장 번호)"을 참조합니다. (이 경우 미국 주민 등록 번호의 기존의 중요한 정보 유형을 사용합니다.)

다음 예제 코드와 같이 유니코드 인코딩을 사용하여 XML 형식으로 규칙 패키지를 만들 수 있습니다. 이 예제를 복사, 수정 및 사용할 수 있습니다.

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

## <a name="upload-personal-data"></a>업로드 데이터 저장
개인 데이터chema를 정의한 후 데이터 일치 설정 페이지의 두 번째  탭에서 개인 데이터 업로드를 수행할 수 있습니다. 추가를 **선택하면** 첫 번째 단계에서 정의한 개인 스마마를 선택한 다음 개인 데이터가 포함된 파일을 업로드합니다.

로컬 파일을 선택하거나 개인 데이터 파일이 포함된 기존 Microsoft Azure Storage 위치에 SAS URL을 제공하여 이 개인 데이터를 업로드할 수 있습니다.
이 프로세스에서 만든 Schema를 준수하는 파일을 첫 번째 단계로 준비한 경우 해당 파일을 업로드에 사용할 수 있습니다.

## <a name="legal-disclaimer"></a>법적 고지 조항

[Microsoft Priva 법적 고지 조항](priva-disclaimer.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
ms.openlocfilehash: 11c6c1073f53ba4a4b93fdae02ae6f6eb22e0f04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325507"
---
# <span data-ttu-id="5faeb-101">Get-AzRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="5faeb-101">Get-AzRegulatoryComplianceControl</span></span>

## <span data-ttu-id="5faeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5faeb-102">SYNOPSIS</span></span>
<span data-ttu-id="5faeb-103">Mevzuat uyumluluk denetimlerini alır</span><span class="sxs-lookup"><span data-stu-id="5faeb-103">Gets regulatory compliance controls</span></span>

## <span data-ttu-id="5faeb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5faeb-104">SYNTAX</span></span>

### <span data-ttu-id="5faeb-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5faeb-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplianceControl [-Name <String>] -StandardName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5faeb-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="5faeb-106">ResourceId</span></span>
```
Get-AzRegulatoryComplianceControl -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5faeb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5faeb-107">DESCRIPTION</span></span>
<span data-ttu-id="5faeb-108">Spcific denetim ayrıntılarını edinin veya belirli mevzuat uyumluluk standartı altındaki tüm denetimleri listeleyin.</span><span class="sxs-lookup"><span data-stu-id="5faeb-108">Get a spcific control details or list all the controls under specific regulatory compliance standard.</span></span>

## <span data-ttu-id="5faeb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5faeb-109">EXAMPLES</span></span>

### <span data-ttu-id="5faeb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5faeb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.1
Name               : A1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Current processing capacity and usage are maintained, monitored, and evaluated to manage capacity
                     demand and to enable the implementation of additional capacity to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.2
Name               : A1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Environmental protections, software, data backup processes, and recovery infrastructure are
                     designed, developed, implemented, operated, maintained, and monitored to meet availability
                     commitments and requirements.
State              : Passed
PassedAssessments  : 3
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.3
Name               : A1.3
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Recovery plan procedures supporting system recovery are tested to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.1
Name               : C1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information is protected during the system design, development, testing,
                     implementation, and change processes in accordance with confidentiality commitments and
                     requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0
```

<span data-ttu-id="5faeb-111">Belirli bir mevzuat standardı altındaki tüm denetimleri alın.</span><span class="sxs-lookup"><span data-stu-id="5faeb-111">Get all controls under specific regulatory standard.</span></span>

### <span data-ttu-id="5faeb-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5faeb-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP" -Name "C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="5faeb-113">Denetim kimliğine göre belirli denetim ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="5faeb-113">Get specific control details according to control id.</span></span>

### <span data-ttu-id="5faeb-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="5faeb-114">Example 3</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="5faeb-115">Kaynak kimliğine göre belirli denetim ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="5faeb-115">Get specific control details according to resource id.</span></span>

## <span data-ttu-id="5faeb-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5faeb-116">PARAMETERS</span></span>

### <span data-ttu-id="5faeb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5faeb-117">-DefaultProfile</span></span>
<span data-ttu-id="5faeb-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5faeb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5faeb-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5faeb-119">-Name</span></span>
<span data-ttu-id="5faeb-120">Denetim kimliği.</span><span class="sxs-lookup"><span data-stu-id="5faeb-120">Control Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5faeb-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5faeb-121">-ResourceId</span></span>
<span data-ttu-id="5faeb-122">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5faeb-122">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5faeb-123">-StandardName</span><span class="sxs-lookup"><span data-stu-id="5faeb-123">-StandardName</span></span>
<span data-ttu-id="5faeb-124">Standart ad.</span><span class="sxs-lookup"><span data-stu-id="5faeb-124">Standard Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5faeb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5faeb-125">CommonParameters</span></span>
<span data-ttu-id="5faeb-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5faeb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5faeb-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5faeb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5faeb-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5faeb-128">INPUTS</span></span>

### <span data-ttu-id="5faeb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5faeb-129">System.String</span></span>

## <span data-ttu-id="5faeb-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5faeb-130">OUTPUTS</span></span>

### <span data-ttu-id="5faeb-131">Microsoft. Azure. Commands. securitcenter. modeller. Re</span><span class="sxs-lookup"><span data-stu-id="5faeb-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span></span>

## <span data-ttu-id="5faeb-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5faeb-132">NOTES</span></span>

## <span data-ttu-id="5faeb-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5faeb-133">RELATED LINKS</span></span>

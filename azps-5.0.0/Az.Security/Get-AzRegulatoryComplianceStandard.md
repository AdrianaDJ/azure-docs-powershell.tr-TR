---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279466"
---
# <span data-ttu-id="ec60e-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="ec60e-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="ec60e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec60e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec60e-103">Retoey uyumluluk standartlarını alır</span><span class="sxs-lookup"><span data-stu-id="ec60e-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="ec60e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec60e-104">SYNTAX</span></span>

### <span data-ttu-id="ec60e-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec60e-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec60e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="ec60e-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec60e-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="ec60e-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec60e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec60e-108">DESCRIPTION</span></span>
<span data-ttu-id="ec60e-109">Spcific mevzuat uyumluluk Satandard ayrıntılarını edinin veya belirli bir aboneliğin altındaki tüm mevzuat uyumluluk standartlarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="ec60e-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="ec60e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec60e-110">EXAMPLES</span></span>

### <span data-ttu-id="ec60e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ec60e-111">Example 1</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/Azure-CIS-1.1.0
Name                : Azure-CIS-1.1.0
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 20
FailedControls      : 4
SkippedControls     : 0
UnsupportedControls : 87

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/ISO-27001
Name                : ISO-27001
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 9
FailedControls      : 10
SkippedControls     : 2
UnsupportedControls : 93

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/PCI-DSS-3.2.1
Name                : PCI-DSS-3.2.1
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 13
FailedControls      : 32
SkippedControls     : 0
UnsupportedControls : 187

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="ec60e-112">Bir aboneliğin altındaki tüm mevzuat uyumluluk standartlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="ec60e-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="ec60e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ec60e-113">Example 2</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -Name "SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="ec60e-114">Standart ad uyarınca belirli bir mevzuat uyumluluk standardının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="ec60e-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="ec60e-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ec60e-115">Example 3</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplianceStandards/SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="ec60e-116">Kaynak kimliği 'ne göre belirli bir mevzuat uyumluluk standardının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="ec60e-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="ec60e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec60e-117">PARAMETERS</span></span>

### <span data-ttu-id="ec60e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec60e-118">-DefaultProfile</span></span>
<span data-ttu-id="ec60e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec60e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec60e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec60e-120">-Name</span></span>
<span data-ttu-id="ec60e-121">Standart ad.</span><span class="sxs-lookup"><span data-stu-id="ec60e-121">Standard name.</span></span>

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

### <span data-ttu-id="ec60e-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ec60e-122">-ResourceId</span></span>
<span data-ttu-id="ec60e-123">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ec60e-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="ec60e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec60e-124">CommonParameters</span></span>
<span data-ttu-id="ec60e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec60e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec60e-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ec60e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec60e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec60e-127">INPUTS</span></span>

### <span data-ttu-id="ec60e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ec60e-128">System.String</span></span>

## <span data-ttu-id="ec60e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec60e-129">OUTPUTS</span></span>

### <span data-ttu-id="ec60e-130">Microsoft. Azure. Commands. securitcenter. modeller. Re</span><span class="sxs-lookup"><span data-stu-id="ec60e-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="ec60e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec60e-131">NOTES</span></span>

## <span data-ttu-id="ec60e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec60e-132">RELATED LINKS</span></span>

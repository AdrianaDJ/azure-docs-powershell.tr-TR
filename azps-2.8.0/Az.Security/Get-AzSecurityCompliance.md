---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityCompliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityCompliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityCompliance.md
ms.openlocfilehash: 03ebb186dcfa781b6136e7824cd1006faad68805
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933268"
---
# <span data-ttu-id="a3b9a-101">Get-AzSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="a3b9a-101">Get-AzSecurityCompliance</span></span>

## <span data-ttu-id="a3b9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b9a-103">Zaman içinde bir aboneliğin güvenlik uyumluluğunu alma</span><span class="sxs-lookup"><span data-stu-id="a3b9a-103">Get the security compliance of a subscription over time</span></span>

## <span data-ttu-id="a3b9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3b9a-104">SYNTAX</span></span>

### <span data-ttu-id="a3b9a-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3b9a-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityCompliance [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3b9a-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a3b9a-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityCompliance -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3b9a-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a3b9a-107">ResourceId</span></span>
```
Get-AzSecurityCompliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3b9a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3b9a-108">DESCRIPTION</span></span>
<span data-ttu-id="a3b9a-109">Bu abonelikteki geçerli sağlıklı ve güvenli olmayan kaynaklar oranına dayanan bir aboneliğin güvenlik uyumluluğunu alır.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-109">Gets the security compliance of a subscription based on the current healthy and non secured resources ratio on this subscription.</span></span>
<span data-ttu-id="a3b9a-110">Güvenlik uyumluluğu her gün hesaplanır ve geçmiş kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-110">The security compliance is calculated every day and the history is saved.</span></span>

## <span data-ttu-id="a3b9a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3b9a-111">EXAMPLES</span></span>

### <span data-ttu-id="a3b9a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a3b9a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityCompliance


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-19Z
Name                       : 2018-08-19Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 19/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-18Z
Name                       : 2018-08-18Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 18/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-17Z
Name                       : 2018-08-17Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 17/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-16Z
Name                       : 2018-08-16Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 16/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-15Z
Name                       : 2018-08-15Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 15/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-14Z
Name                       : 2018-08-14Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 14/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-13Z
Name                       : 2018-08-13Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 13/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-12Z
Name                       : 2018-08-12Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 12/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-11Z
Name                       : 2018-08-11Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 11/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-10Z
Name                       : 2018-08-10Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 10/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-09Z
Name                       : 2018-08-09Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 09/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-08Z
Name                       : 2018-08-08Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 08/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-07Z
Name                       : 2018-08-07Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 07/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="a3b9a-113">Aboneliğin güvenlik uyumluluğunu son 14 gün boyunca alır</span><span class="sxs-lookup"><span data-stu-id="a3b9a-113">Gets the security compliance of a subscription for the last 14 days</span></span>

### <span data-ttu-id="a3b9a-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a3b9a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityCompliance -Name "2018-08-20Z"


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="a3b9a-115">Aboneliğin güvenlik uyumluluğunu belirli bir tarihte alır</span><span class="sxs-lookup"><span data-stu-id="a3b9a-115">Gets the security compliance of a subscription on a specific date</span></span>

## <span data-ttu-id="a3b9a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3b9a-116">PARAMETERS</span></span>

### <span data-ttu-id="a3b9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b9a-117">-DefaultProfile</span></span>
<span data-ttu-id="a3b9a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3b9a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3b9a-119">-Name</span></span>
<span data-ttu-id="a3b9a-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-120">Resource name.</span></span>

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

### <span data-ttu-id="a3b9a-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a3b9a-121">-ResourceId</span></span>
<span data-ttu-id="a3b9a-122">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-122">Resource ID.</span></span>

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

### <span data-ttu-id="a3b9a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b9a-123">CommonParameters</span></span>
<span data-ttu-id="a3b9a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b9a-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3b9a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b9a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3b9a-126">INPUTS</span></span>

### <span data-ttu-id="a3b9a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a3b9a-127">System.String</span></span>

## <span data-ttu-id="a3b9a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3b9a-128">OUTPUTS</span></span>

### <span data-ttu-id="a3b9a-129">Microsoft. Azure. Commands. Security. model.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-129">Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityCompliance</span></span>

## <span data-ttu-id="a3b9a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3b9a-130">NOTES</span></span>

## <span data-ttu-id="a3b9a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3b9a-131">RELATED LINKS</span></span>
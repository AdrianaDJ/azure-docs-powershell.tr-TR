---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: c287fd6aafcfe63a26c5f1dfd01503adb741428d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109139"
---
# <span data-ttu-id="b639d-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="b639d-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="b639d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b639d-102">SYNOPSIS</span></span>
<span data-ttu-id="b639d-103">Bir öğretici Hizmetler hesabı için güncel kullanımları edinin.</span><span class="sxs-lookup"><span data-stu-id="b639d-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="b639d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b639d-104">SYNTAX</span></span>

### <span data-ttu-id="b639d-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b639d-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b639d-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="b639d-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b639d-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b639d-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b639d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b639d-108">DESCRIPTION</span></span>
<span data-ttu-id="b639d-109">**Get-Azlıveiveservicesaccountusage** cmdlet 'i, bir öğretici hizmet hesabı için güncel kullanımları alır.</span><span class="sxs-lookup"><span data-stu-id="b639d-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="b639d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b639d-110">EXAMPLES</span></span>

### <span data-ttu-id="b639d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b639d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="b639d-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b639d-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="b639d-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b639d-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="b639d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b639d-114">PARAMETERS</span></span>

### <span data-ttu-id="b639d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b639d-115">-DefaultProfile</span></span>
<span data-ttu-id="b639d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b639d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b639d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b639d-117">-InputObject</span></span>
<span data-ttu-id="b639d-118">Öğretici hizmetler hesap nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b639d-118">Cognitive Services Account Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b639d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b639d-119">-Name</span></span>
<span data-ttu-id="b639d-120">Öğretici hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="b639d-120">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b639d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b639d-121">-ResourceGroupName</span></span>
<span data-ttu-id="b639d-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b639d-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b639d-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b639d-123">-ResourceId</span></span>
<span data-ttu-id="b639d-124">Öğretici Hizmetler hesabı kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b639d-124">Cognitive Services Account Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b639d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b639d-125">CommonParameters</span></span>
<span data-ttu-id="b639d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b639d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b639d-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b639d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b639d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b639d-128">INPUTS</span></span>

### <span data-ttu-id="b639d-129">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="b639d-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="b639d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b639d-130">System.String</span></span>

## <span data-ttu-id="b639d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b639d-131">OUTPUTS</span></span>

### <span data-ttu-id="b639d-132">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesusage</span><span class="sxs-lookup"><span data-stu-id="b639d-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="b639d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b639d-133">NOTES</span></span>

## <span data-ttu-id="b639d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b639d-134">RELATED LINKS</span></span>

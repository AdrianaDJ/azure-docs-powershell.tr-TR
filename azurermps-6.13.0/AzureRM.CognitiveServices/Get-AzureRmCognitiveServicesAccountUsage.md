---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
ms.openlocfilehash: 1cdfaa6b57a0bcf6d50e0e3a77f80c1a5c069069
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587270"
---
# <span data-ttu-id="c14a9-101">Get-AzureRmCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="c14a9-101">Get-AzureRmCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="c14a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c14a9-102">SYNOPSIS</span></span>
<span data-ttu-id="c14a9-103">Bir öğretici Hizmetler hesabı için güncel kullanımları edinin.</span><span class="sxs-lookup"><span data-stu-id="c14a9-103">Get current usages for a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c14a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c14a9-104">SYNTAX</span></span>

### <span data-ttu-id="c14a9-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c14a9-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c14a9-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="c14a9-106">InputObjectParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c14a9-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c14a9-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c14a9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c14a9-108">DESCRIPTION</span></span>
<span data-ttu-id="c14a9-109">**Get-Azurermöğretici Iveservicesaccountusage** cmdlet 'i, bir öğretici sitif Hizmetler hesabı için güncel kullanımları alır.</span><span class="sxs-lookup"><span data-stu-id="c14a9-109">The **Get-AzureRmCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="c14a9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c14a9-110">EXAMPLES</span></span>

### <span data-ttu-id="c14a9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c14a9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="c14a9-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c14a9-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="c14a9-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c14a9-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="c14a9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c14a9-114">PARAMETERS</span></span>

### <span data-ttu-id="c14a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14a9-115">-DefaultProfile</span></span>
<span data-ttu-id="c14a9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c14a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14a9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c14a9-117">-InputObject</span></span>
<span data-ttu-id="c14a9-118">Öğretici hizmetler hesap nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c14a9-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="c14a9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c14a9-119">-Name</span></span>
<span data-ttu-id="c14a9-120">Öğretici hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="c14a9-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="c14a9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c14a9-121">-ResourceGroupName</span></span>
<span data-ttu-id="c14a9-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c14a9-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c14a9-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c14a9-123">-ResourceId</span></span>
<span data-ttu-id="c14a9-124">Öğretici Hizmetler hesabı kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c14a9-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="c14a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14a9-125">CommonParameters</span></span>
<span data-ttu-id="c14a9-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c14a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14a9-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c14a9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14a9-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c14a9-128">INPUTS</span></span>

### <span data-ttu-id="c14a9-129">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="c14a9-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>
<span data-ttu-id="c14a9-130">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c14a9-130">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c14a9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c14a9-131">System.String</span></span>

## <span data-ttu-id="c14a9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c14a9-132">OUTPUTS</span></span>

### <span data-ttu-id="c14a9-133">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesusage</span><span class="sxs-lookup"><span data-stu-id="c14a9-133">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="c14a9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c14a9-134">NOTES</span></span>

## <span data-ttu-id="c14a9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c14a9-135">RELATED LINKS</span></span>

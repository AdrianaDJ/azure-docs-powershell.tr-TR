---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
ms.openlocfilehash: a549e6c94ae43c8c1cc267448552565f932aa63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586813"
---
# <span data-ttu-id="662dd-101">Get-AzureRmCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="662dd-101">Get-AzureRmCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="662dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="662dd-102">SYNOPSIS</span></span>
<span data-ttu-id="662dd-103">Bir öğretici Hizmetler hesabı için güncel kullanımları edinin.</span><span class="sxs-lookup"><span data-stu-id="662dd-103">Get current usages for a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="662dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="662dd-104">SYNTAX</span></span>

### <span data-ttu-id="662dd-105">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="662dd-105">InputObjectParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="662dd-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="662dd-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="662dd-107">ResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="662dd-107">ResourceNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="662dd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="662dd-108">DESCRIPTION</span></span>
<span data-ttu-id="662dd-109">**Get-Azurermöğretici Iveservicesaccountusage** cmdlet 'i, bir öğretici sitif Hizmetler hesabı için güncel kullanımları alır.</span><span class="sxs-lookup"><span data-stu-id="662dd-109">The **Get-AzureRmCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="662dd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="662dd-110">EXAMPLES</span></span>

### <span data-ttu-id="662dd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="662dd-111">Example 1</span></span>
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

### <span data-ttu-id="662dd-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="662dd-112">Example 2</span></span>
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

### <span data-ttu-id="662dd-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="662dd-113">Example 3</span></span>
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

## <span data-ttu-id="662dd-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="662dd-114">PARAMETERS</span></span>

### <span data-ttu-id="662dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662dd-115">-DefaultProfile</span></span>
<span data-ttu-id="662dd-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="662dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="662dd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="662dd-117">-InputObject</span></span>
<span data-ttu-id="662dd-118">Öğretici hizmetler hesap nesnesi.</span><span class="sxs-lookup"><span data-stu-id="662dd-118">Cognitive Services Account Object.</span></span>
```yaml
Type: PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="662dd-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="662dd-119">-Name</span></span>
<span data-ttu-id="662dd-120">Öğretici hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="662dd-120">Cognitive Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="662dd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="662dd-121">-ResourceGroupName</span></span>
<span data-ttu-id="662dd-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="662dd-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="662dd-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="662dd-123">-ResourceId</span></span>
<span data-ttu-id="662dd-124">Öğretici Hizmetler hesabı kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="662dd-124">Cognitive Services Account Resource ID.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="662dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="662dd-125">CommonParameters</span></span>
<span data-ttu-id="662dd-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="662dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="662dd-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="662dd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="662dd-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="662dd-128">INPUTS</span></span>

### <span data-ttu-id="662dd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="662dd-129">System.String</span></span>

## <span data-ttu-id="662dd-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="662dd-130">OUTPUTS</span></span>

### <span data-ttu-id="662dd-131">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesusage</span><span class="sxs-lookup"><span data-stu-id="662dd-131">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="662dd-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="662dd-132">NOTES</span></span>

## <span data-ttu-id="662dd-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="662dd-133">RELATED LINKS</span></span>

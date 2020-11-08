---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274958"
---
# <span data-ttu-id="ff933-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="ff933-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="ff933-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff933-102">SYNOPSIS</span></span>
<span data-ttu-id="ff933-103">Kural altyapısı yapılandırmalarını alın.</span><span class="sxs-lookup"><span data-stu-id="ff933-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="ff933-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff933-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff933-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff933-105">DESCRIPTION</span></span>
<span data-ttu-id="ff933-106">**Get-AzFrontDoorRulesEngine** cmdlet 'i belirli bir kural altyapısı yapılandırmasını alır veya ön kapılarla ilişkilendirilmiş tüm kural altyapısı yapılandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="ff933-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="ff933-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff933-107">EXAMPLES</span></span>

### <span data-ttu-id="ff933-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ff933-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="ff933-109">Belirli kural altyapısı yapılandırmasını edinin.</span><span class="sxs-lookup"><span data-stu-id="ff933-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="ff933-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ff933-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="ff933-111">Tüm kural altyapısı yapılandırmalarını ön kapıda edinin.</span><span class="sxs-lookup"><span data-stu-id="ff933-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="ff933-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ff933-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="ff933-113">Varolmayan bir kural altyapısı alınırken beklenen çıktı.</span><span class="sxs-lookup"><span data-stu-id="ff933-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="ff933-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff933-114">PARAMETERS</span></span>

### <span data-ttu-id="ff933-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff933-115">-DefaultProfile</span></span>
<span data-ttu-id="ff933-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff933-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff933-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ff933-117">-FrontDoorName</span></span>
<span data-ttu-id="ff933-118">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="ff933-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff933-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="ff933-119">-Name</span></span>
<span data-ttu-id="ff933-120">Kural altyapısı adı.</span><span class="sxs-lookup"><span data-stu-id="ff933-120">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff933-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff933-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff933-122">Ön kapıda oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ff933-122">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff933-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff933-123">CommonParameters</span></span>
<span data-ttu-id="ff933-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff933-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff933-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ff933-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff933-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff933-126">INPUTS</span></span>

### <span data-ttu-id="ff933-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ff933-127">None</span></span>

## <span data-ttu-id="ff933-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff933-128">OUTPUTS</span></span>

### <span data-ttu-id="ff933-129">Microsoft. Azure. Commands. Frontkapısı. modeller. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="ff933-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="ff933-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff933-130">NOTES</span></span>

## <span data-ttu-id="ff933-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff933-131">RELATED LINKS</span></span>

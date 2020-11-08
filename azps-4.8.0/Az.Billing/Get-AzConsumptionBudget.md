---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: dfca3033b5061116882eb68eb18fa2ff3ddd0c53
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268066"
---
# <span data-ttu-id="1fb29-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="1fb29-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="1fb29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fb29-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb29-103">Bir abonelikteki veya kaynak grubundaki bütçelerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="1fb29-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="1fb29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fb29-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="1fb29-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fb29-105">DESCRIPTION</span></span>
<span data-ttu-id="1fb29-106">Get-AzConsumptionBudget cmdlet 'i, bir abonelikteki veya kaynak grubundaki bütçelerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="1fb29-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="1fb29-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fb29-107">EXAMPLES</span></span>

### <span data-ttu-id="1fb29-108">Örnek 1: abonelik düzeyindeki bütçelerin listesini alma</span><span class="sxs-lookup"><span data-stu-id="1fb29-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="1fb29-109">Örnek 2: Kaynak Grup düzeyindeki bütçelerin listesini alma</span><span class="sxs-lookup"><span data-stu-id="1fb29-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="1fb29-110">Örnek 3: abonelik düzeyinde bütçe adıyla bir bütçe edinme</span><span class="sxs-lookup"><span data-stu-id="1fb29-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="1fb29-111">Örnek 4: kaynak grup düzeyinde bütçe adıyla bir bütçe edinme</span><span class="sxs-lookup"><span data-stu-id="1fb29-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="1fb29-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fb29-112">PARAMETERS</span></span>

### <span data-ttu-id="1fb29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb29-113">-DefaultProfile</span></span>
<span data-ttu-id="1fb29-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1fb29-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb29-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="1fb29-115">-Name</span></span>
<span data-ttu-id="1fb29-116">Bütçenin adı.</span><span class="sxs-lookup"><span data-stu-id="1fb29-116">Name of a budget.</span></span>

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

### <span data-ttu-id="1fb29-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb29-117">-ResourceGroupName</span></span>
<span data-ttu-id="1fb29-118">Bütçenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="1fb29-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="1fb29-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb29-119">CommonParameters</span></span>
<span data-ttu-id="1fb29-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fb29-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb29-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb29-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb29-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fb29-122">INPUTS</span></span>

### <span data-ttu-id="1fb29-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1fb29-123">None</span></span>

## <span data-ttu-id="1fb29-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fb29-124">OUTPUTS</span></span>

### <span data-ttu-id="1fb29-125">Microsoft. Azure. Commands. tüketim. modeller. Psbütçe</span><span class="sxs-lookup"><span data-stu-id="1fb29-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="1fb29-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fb29-126">NOTES</span></span>

## <span data-ttu-id="1fb29-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fb29-127">RELATED LINKS</span></span>

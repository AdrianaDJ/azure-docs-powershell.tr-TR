---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: 1c34c4a6e7d9621d1afc0cf06d841eceb2b34cb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753151"
---
# <span data-ttu-id="67e6d-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="67e6d-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="67e6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="67e6d-103">Bir abonelikteki veya kaynak grubundaki bütçelerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="67e6d-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="67e6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67e6d-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="67e6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67e6d-105">DESCRIPTION</span></span>
<span data-ttu-id="67e6d-106">Get-AzConsumptionBudget cmdlet 'i, bir abonelikteki veya kaynak grubundaki bütçelerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="67e6d-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="67e6d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67e6d-107">EXAMPLES</span></span>

### <span data-ttu-id="67e6d-108">Örnek 1: abonelik düzeyindeki bütçelerin listesini alma</span><span class="sxs-lookup"><span data-stu-id="67e6d-108">Example 1: Get a list of budgets at subscription level</span></span>
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

### <span data-ttu-id="67e6d-109">Örnek 2: Kaynak Grup düzeyindeki bütçelerin listesini alma</span><span class="sxs-lookup"><span data-stu-id="67e6d-109">Example 2: Get a list of budgets at resource group level</span></span>
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

### <span data-ttu-id="67e6d-110">Örnek 3: abonelik düzeyinde bütçe adıyla bir bütçe edinme</span><span class="sxs-lookup"><span data-stu-id="67e6d-110">Example 3: Get a budget with the budget name at subscription level</span></span>
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

### <span data-ttu-id="67e6d-111">Örnek 4: kaynak grup düzeyinde bütçe adıyla bir bütçe edinme</span><span class="sxs-lookup"><span data-stu-id="67e6d-111">Example 4: Get a budget with the budget name at resource group level</span></span>
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

## <span data-ttu-id="67e6d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67e6d-112">PARAMETERS</span></span>

### <span data-ttu-id="67e6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e6d-113">-DefaultProfile</span></span>
<span data-ttu-id="67e6d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67e6d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67e6d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="67e6d-115">-Name</span></span>
<span data-ttu-id="67e6d-116">Bütçenin adı.</span><span class="sxs-lookup"><span data-stu-id="67e6d-116">Name of a budget.</span></span>

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

### <span data-ttu-id="67e6d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e6d-117">-ResourceGroupName</span></span>
<span data-ttu-id="67e6d-118">Bütçenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="67e6d-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="67e6d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e6d-119">CommonParameters</span></span>
<span data-ttu-id="67e6d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67e6d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e6d-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e6d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e6d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67e6d-122">INPUTS</span></span>

### <span data-ttu-id="67e6d-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="67e6d-123">None</span></span>

## <span data-ttu-id="67e6d-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67e6d-124">OUTPUTS</span></span>

### <span data-ttu-id="67e6d-125">Microsoft. Azure. Commands. tüketim. modeller. Psbütçe</span><span class="sxs-lookup"><span data-stu-id="67e6d-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="67e6d-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67e6d-126">NOTES</span></span>

## <span data-ttu-id="67e6d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67e6d-127">RELATED LINKS</span></span>
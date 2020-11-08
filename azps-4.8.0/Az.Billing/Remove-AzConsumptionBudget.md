---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108490"
---
# <span data-ttu-id="dbfa7-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="dbfa7-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="dbfa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbfa7-102">SYNOPSIS</span></span>
<span data-ttu-id="dbfa7-103">Bir abonelikteki veya bir kaynak grubundaki bütçeyi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="dbfa7-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="dbfa7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbfa7-104">SYNTAX</span></span>

### <span data-ttu-id="dbfa7-105">Abonelik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dbfa7-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbfa7-106">Yöneltil</span><span class="sxs-lookup"><span data-stu-id="dbfa7-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbfa7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbfa7-107">DESCRIPTION</span></span>
<span data-ttu-id="dbfa7-108">Remove-AzConsumptionBudget cmdlet 'i bir abonelikteki veya kaynak grubundaki bütçeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dbfa7-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="dbfa7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbfa7-109">EXAMPLES</span></span>

### <span data-ttu-id="dbfa7-110">Örnek 1: abonelik düzeyindeki bütçe adı ile bütçeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="dbfa7-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="dbfa7-111">Örnek 2: kaynak grup düzeyinde bütçe adıyla bir bütçeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="dbfa7-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="dbfa7-112">Örnek 3: abonelik düzeyindeki boruları aracılığıyla bütçeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="dbfa7-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="dbfa7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbfa7-113">PARAMETERS</span></span>

### <span data-ttu-id="dbfa7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbfa7-114">-DefaultProfile</span></span>
<span data-ttu-id="dbfa7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dbfa7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbfa7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbfa7-116">-InputObject</span></span>
<span data-ttu-id="dbfa7-117">Bütçe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dbfa7-117">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbfa7-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="dbfa7-118">-Name</span></span>
<span data-ttu-id="dbfa7-119">Bütçenin adı.</span><span class="sxs-lookup"><span data-stu-id="dbfa7-119">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfa7-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dbfa7-120">-PassThru</span></span>
<span data-ttu-id="dbfa7-121">Bütçe başarıyla kaldırılmışsa cmdlet doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="dbfa7-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfa7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbfa7-122">-ResourceGroupName</span></span>
<span data-ttu-id="dbfa7-123">Bütçenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="dbfa7-123">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfa7-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="dbfa7-124">-Confirm</span></span>
<span data-ttu-id="dbfa7-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dbfa7-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfa7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbfa7-126">-WhatIf</span></span>
<span data-ttu-id="dbfa7-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dbfa7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbfa7-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dbfa7-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfa7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbfa7-129">CommonParameters</span></span>
<span data-ttu-id="dbfa7-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbfa7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbfa7-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbfa7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbfa7-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbfa7-132">INPUTS</span></span>

### <span data-ttu-id="dbfa7-133">Microsoft. Azure. Commands. tüketim. modeller. Psbütçe</span><span class="sxs-lookup"><span data-stu-id="dbfa7-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="dbfa7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbfa7-134">OUTPUTS</span></span>

### <span data-ttu-id="dbfa7-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dbfa7-135">System.Boolean</span></span>

## <span data-ttu-id="dbfa7-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbfa7-136">NOTES</span></span>

## <span data-ttu-id="dbfa7-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbfa7-137">RELATED LINKS</span></span>

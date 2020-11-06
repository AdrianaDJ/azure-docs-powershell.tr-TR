---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/remove-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
ms.openlocfilehash: b14afecc7f31f878b4ce1598f8b135265ff72249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593284"
---
# <span data-ttu-id="edfee-101">Remove-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="edfee-101">Remove-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="edfee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edfee-102">SYNOPSIS</span></span>
<span data-ttu-id="edfee-103">Bir abonelikteki veya bir kaynak grubundaki bütçeyi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="edfee-103">Remove a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edfee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edfee-104">SYNTAX</span></span>

### <span data-ttu-id="edfee-105">Abonelik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="edfee-105">Subscription (Default)</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edfee-106">Yöneltil</span><span class="sxs-lookup"><span data-stu-id="edfee-106">Piping</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edfee-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="edfee-107">DESCRIPTION</span></span>
<span data-ttu-id="edfee-108">Remove-AzureRmConsumptionBudget cmdlet 'i bir abonelikteki veya kaynak grubundaki bütçeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="edfee-108">The Remove-AzureRmConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="edfee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edfee-109">EXAMPLES</span></span>

### <span data-ttu-id="edfee-110">Örnek 1: abonelik düzeyindeki bütçe adı ile bütçeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="edfee-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="edfee-111">Örnek 2: kaynak grup düzeyinde bütçe adıyla bir bütçeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="edfee-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="edfee-112">Örnek 3: abonelik düzeyindeki boruları aracılığıyla bütçeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="edfee-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget | Remove-AzureRmConsumptionBudget -PassThru
True
```

## <span data-ttu-id="edfee-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edfee-113">PARAMETERS</span></span>

### <span data-ttu-id="edfee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edfee-114">-DefaultProfile</span></span>
<span data-ttu-id="edfee-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edfee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edfee-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edfee-116">-InputObject</span></span>
<span data-ttu-id="edfee-117">Bütçe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="edfee-117">Budget object.</span></span>

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

### <span data-ttu-id="edfee-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="edfee-118">-Name</span></span>
<span data-ttu-id="edfee-119">Bütçenin adı.</span><span class="sxs-lookup"><span data-stu-id="edfee-119">Name of a budget.</span></span>

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

### <span data-ttu-id="edfee-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="edfee-120">-PassThru</span></span>
<span data-ttu-id="edfee-121">Bütçe başarıyla kaldırılmışsa cmdlet doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="edfee-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="edfee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edfee-122">-ResourceGroupName</span></span>
<span data-ttu-id="edfee-123">Bütçenin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="edfee-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="edfee-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="edfee-124">-Confirm</span></span>
<span data-ttu-id="edfee-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edfee-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edfee-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edfee-126">-WhatIf</span></span>
<span data-ttu-id="edfee-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edfee-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edfee-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edfee-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edfee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfee-129">CommonParameters</span></span>
<span data-ttu-id="edfee-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edfee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfee-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edfee-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfee-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edfee-132">INPUTS</span></span>

### <span data-ttu-id="edfee-133">Microsoft. Azure. Commands. tüketim. modeller. Psbütçe</span><span class="sxs-lookup"><span data-stu-id="edfee-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="edfee-134">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="edfee-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="edfee-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edfee-135">OUTPUTS</span></span>

### <span data-ttu-id="edfee-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="edfee-136">System.Boolean</span></span>

## <span data-ttu-id="edfee-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edfee-137">NOTES</span></span>

## <span data-ttu-id="edfee-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edfee-138">RELATED LINKS</span></span>

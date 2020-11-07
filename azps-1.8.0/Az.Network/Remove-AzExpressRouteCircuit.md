---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: a4672e459a692ce8c0c19b35bf68240d979e75ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760183"
---
# <span data-ttu-id="71887-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71887-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="71887-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71887-102">SYNOPSIS</span></span>
<span data-ttu-id="71887-103">ExpressRoute devresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="71887-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="71887-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71887-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71887-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="71887-105">DESCRIPTION</span></span>
<span data-ttu-id="71887-106">**Remove-Azexpressroutedevresi** cmdlet 'ı bir ExpressRoute devresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="71887-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="71887-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71887-107">EXAMPLES</span></span>

### <span data-ttu-id="71887-108">Örnek 1: ExpressRoute devresini silme</span><span class="sxs-lookup"><span data-stu-id="71887-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="71887-109">Örnek 2: ardışık düzeni kullanarak ExpressRoute devresini silme</span><span class="sxs-lookup"><span data-stu-id="71887-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="71887-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71887-110">PARAMETERS</span></span>

### <span data-ttu-id="71887-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="71887-111">-AsJob</span></span>
<span data-ttu-id="71887-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="71887-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71887-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71887-113">-DefaultProfile</span></span>
<span data-ttu-id="71887-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71887-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71887-115">-Force</span><span class="sxs-lookup"><span data-stu-id="71887-115">-Force</span></span>
<span data-ttu-id="71887-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="71887-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71887-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="71887-117">-Name</span></span>
<span data-ttu-id="71887-118">Kaldırılacak ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="71887-118">The name of the ExpressRoute circuit to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71887-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="71887-119">-PassThru</span></span>
<span data-ttu-id="71887-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="71887-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="71887-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="71887-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71887-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71887-122">-ResourceGroupName</span></span>
<span data-ttu-id="71887-123">Bu ExpressRoute devresi 'in ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71887-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71887-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="71887-124">-Confirm</span></span>
<span data-ttu-id="71887-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="71887-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71887-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71887-126">-WhatIf</span></span>
<span data-ttu-id="71887-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="71887-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71887-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="71887-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71887-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71887-129">CommonParameters</span></span>
<span data-ttu-id="71887-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71887-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71887-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71887-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71887-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71887-132">INPUTS</span></span>

### <span data-ttu-id="71887-133">System. String</span><span class="sxs-lookup"><span data-stu-id="71887-133">System.String</span></span>

## <span data-ttu-id="71887-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71887-134">OUTPUTS</span></span>

### <span data-ttu-id="71887-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71887-135">System.Boolean</span></span>

## <span data-ttu-id="71887-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71887-136">NOTES</span></span>

## <span data-ttu-id="71887-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71887-137">RELATED LINKS</span></span>

[<span data-ttu-id="71887-138">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="71887-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="71887-139">Taşıma-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="71887-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="71887-140">Yeni-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="71887-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="71887-141">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="71887-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
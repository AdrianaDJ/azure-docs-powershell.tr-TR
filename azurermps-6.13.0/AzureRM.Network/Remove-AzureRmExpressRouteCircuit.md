---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e38cdc9a7f0b34fa5e7769192fa5fcb0ad342de1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592286"
---
# <span data-ttu-id="71cba-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71cba-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="71cba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71cba-102">SYNOPSIS</span></span>
<span data-ttu-id="71cba-103">ExpressRoute devresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="71cba-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71cba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71cba-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71cba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="71cba-105">DESCRIPTION</span></span>
<span data-ttu-id="71cba-106">**Remove-Azurermexpressroutedevresi** bir ExpressRoute devresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="71cba-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="71cba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71cba-107">EXAMPLES</span></span>

### <span data-ttu-id="71cba-108">Örnek 1: ExpressRoute devresini silme</span><span class="sxs-lookup"><span data-stu-id="71cba-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="71cba-109">Örnek 2: ardışık düzeni kullanarak ExpressRoute devresini silme</span><span class="sxs-lookup"><span data-stu-id="71cba-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="71cba-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71cba-110">PARAMETERS</span></span>

### <span data-ttu-id="71cba-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="71cba-111">-AsJob</span></span>
<span data-ttu-id="71cba-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="71cba-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71cba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cba-113">-DefaultProfile</span></span>
<span data-ttu-id="71cba-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71cba-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71cba-115">-Force</span><span class="sxs-lookup"><span data-stu-id="71cba-115">-Force</span></span>
<span data-ttu-id="71cba-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="71cba-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71cba-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="71cba-117">-Name</span></span>
<span data-ttu-id="71cba-118">Kaldırılacak ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="71cba-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="71cba-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="71cba-119">-PassThru</span></span>
<span data-ttu-id="71cba-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="71cba-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="71cba-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="71cba-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71cba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71cba-122">-ResourceGroupName</span></span>
<span data-ttu-id="71cba-123">Bu ExpressRoute devresi 'in ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cba-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="71cba-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="71cba-124">-Confirm</span></span>
<span data-ttu-id="71cba-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="71cba-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71cba-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71cba-126">-WhatIf</span></span>
<span data-ttu-id="71cba-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="71cba-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71cba-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="71cba-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71cba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cba-129">CommonParameters</span></span>
<span data-ttu-id="71cba-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71cba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cba-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71cba-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cba-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71cba-132">INPUTS</span></span>

### <span data-ttu-id="71cba-133">System. String</span><span class="sxs-lookup"><span data-stu-id="71cba-133">System.String</span></span>

## <span data-ttu-id="71cba-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71cba-134">OUTPUTS</span></span>

### <span data-ttu-id="71cba-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71cba-135">System.Boolean</span></span>

## <span data-ttu-id="71cba-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71cba-136">NOTES</span></span>

## <span data-ttu-id="71cba-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71cba-137">RELATED LINKS</span></span>

[<span data-ttu-id="71cba-138">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="71cba-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="71cba-139">Taşı-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="71cba-139">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="71cba-140">New-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="71cba-140">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="71cba-141">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="71cba-141">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

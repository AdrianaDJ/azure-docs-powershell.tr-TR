---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: dd47e858132dbe77556d82ce234d41bc2c990f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590728"
---
# <span data-ttu-id="d04ef-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d04ef-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="d04ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d04ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d04ef-103">ExpressRoute devresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d04ef-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d04ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d04ef-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d04ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d04ef-105">DESCRIPTION</span></span>
<span data-ttu-id="d04ef-106">**Remove-Azurermexpressroutedevresi** bir ExpressRoute devresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d04ef-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d04ef-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d04ef-107">EXAMPLES</span></span>

### <span data-ttu-id="d04ef-108">Örnek 1: ExpressRoute devresini silme</span><span class="sxs-lookup"><span data-stu-id="d04ef-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="d04ef-109">Örnek 2: ardışık düzeni kullanarak ExpressRoute devresini silme</span><span class="sxs-lookup"><span data-stu-id="d04ef-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="d04ef-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d04ef-110">PARAMETERS</span></span>

### <span data-ttu-id="d04ef-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d04ef-111">-Force</span></span>
<span data-ttu-id="d04ef-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d04ef-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d04ef-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d04ef-113">-Name</span></span>
<span data-ttu-id="d04ef-114">Kaldırılacak ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="d04ef-114">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="d04ef-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d04ef-115">-PassThru</span></span>
<span data-ttu-id="d04ef-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d04ef-116">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="d04ef-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d04ef-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d04ef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d04ef-118">-ResourceGroupName</span></span>
<span data-ttu-id="d04ef-119">Bu ExpressRoute devresi 'in ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d04ef-119">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="d04ef-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="d04ef-120">-Confirm</span></span>
<span data-ttu-id="d04ef-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d04ef-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d04ef-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d04ef-122">-WhatIf</span></span>
<span data-ttu-id="d04ef-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d04ef-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d04ef-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d04ef-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d04ef-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04ef-125">-DefaultProfile</span></span>
<span data-ttu-id="d04ef-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d04ef-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d04ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04ef-127">CommonParameters</span></span>
<span data-ttu-id="d04ef-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d04ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04ef-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d04ef-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04ef-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d04ef-130">INPUTS</span></span>

## <span data-ttu-id="d04ef-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d04ef-131">OUTPUTS</span></span>

## <span data-ttu-id="d04ef-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d04ef-132">NOTES</span></span>

## <span data-ttu-id="d04ef-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d04ef-133">RELATED LINKS</span></span>

[<span data-ttu-id="d04ef-134">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d04ef-134">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d04ef-135">Taşı-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d04ef-135">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d04ef-136">New-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d04ef-136">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d04ef-137">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d04ef-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

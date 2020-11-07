---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 0ade3324e842735cab33ed6d6a40b5279cf8391e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931952"
---
# <span data-ttu-id="06b94-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="06b94-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="06b94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06b94-102">SYNOPSIS</span></span>
<span data-ttu-id="06b94-103">Bir ExpressRoute devresini klasik dağıtım modelinden Kaynak Yöneticisi dağıtım modeline götürür.</span><span class="sxs-lookup"><span data-stu-id="06b94-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="06b94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06b94-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06b94-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06b94-105">DESCRIPTION</span></span>
<span data-ttu-id="06b94-106">**Taşıma-Azexpressroutedevresi** cmdlet 'i, bir ExpressRoute devresini klasik dağıtım modelinden Kaynak Yöneticisi dağıtım modeline taşır.</span><span class="sxs-lookup"><span data-stu-id="06b94-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="06b94-107">Taşıma sonrasında ExpressRoute devresi, Kaynak Yöneticisi dağıtım modelinde oluşturulan diğer ExpressRoute devresi gibi çalışır ve çalışır.</span><span class="sxs-lookup"><span data-stu-id="06b94-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="06b94-108">Devre, sanal ağ ve VPN ağ geçitleri bu işlemden taşınmaz.</span><span class="sxs-lookup"><span data-stu-id="06b94-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="06b94-109">Bu kaynakların taşıma sonrasında yeniden yapılandırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="06b94-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="06b94-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06b94-110">EXAMPLES</span></span>

### <span data-ttu-id="06b94-111">Örnek 1: ExpressRoute devresini Kaynak Yöneticisi dağıtım modeline taşıma</span><span class="sxs-lookup"><span data-stu-id="06b94-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="06b94-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06b94-112">PARAMETERS</span></span>

### <span data-ttu-id="06b94-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="06b94-113">-AsJob</span></span>
<span data-ttu-id="06b94-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="06b94-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06b94-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b94-115">-DefaultProfile</span></span>
<span data-ttu-id="06b94-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06b94-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06b94-117">-Force</span><span class="sxs-lookup"><span data-stu-id="06b94-117">-Force</span></span>
<span data-ttu-id="06b94-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="06b94-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06b94-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="06b94-119">-Location</span></span>
<span data-ttu-id="06b94-120">ExpressRoute devresi bulunan Azure konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="06b94-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="06b94-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="06b94-121">-Name</span></span>
<span data-ttu-id="06b94-122">Taşınacak ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="06b94-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="06b94-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b94-123">-ResourceGroupName</span></span>
<span data-ttu-id="06b94-124">Taşınan ExpressRoute devresini içerecek kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="06b94-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="06b94-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="06b94-125">-ServiceKey</span></span>
<span data-ttu-id="06b94-126">Klasik dağıtım modelinde ExpressRoute devresi tarafından kullanılan hizmet anahtarı.</span><span class="sxs-lookup"><span data-stu-id="06b94-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="06b94-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="06b94-127">-Tag</span></span>
<span data-ttu-id="06b94-128">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="06b94-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="06b94-129">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="06b94-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06b94-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="06b94-130">-Confirm</span></span>
<span data-ttu-id="06b94-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="06b94-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b94-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b94-132">-WhatIf</span></span>
<span data-ttu-id="06b94-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06b94-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b94-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="06b94-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b94-135">CommonParameters</span></span>
<span data-ttu-id="06b94-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06b94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b94-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06b94-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b94-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06b94-138">INPUTS</span></span>

### <span data-ttu-id="06b94-139">System. String</span><span class="sxs-lookup"><span data-stu-id="06b94-139">System.String</span></span>

### <span data-ttu-id="06b94-140">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="06b94-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="06b94-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06b94-141">OUTPUTS</span></span>

### <span data-ttu-id="06b94-142">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="06b94-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="06b94-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06b94-143">NOTES</span></span>

## <span data-ttu-id="06b94-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06b94-144">RELATED LINKS</span></span>

[<span data-ttu-id="06b94-145">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="06b94-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="06b94-146">Yeni-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="06b94-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="06b94-147">Remove-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="06b94-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="06b94-148">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="06b94-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
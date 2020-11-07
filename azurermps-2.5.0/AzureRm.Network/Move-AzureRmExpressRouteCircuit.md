---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: bd4d51c03d26a1fb99b04c8b5245850512c2c940
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939305"
---
# <span data-ttu-id="531e7-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="531e7-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="531e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="531e7-102">SYNOPSIS</span></span>
<span data-ttu-id="531e7-103">Bir ExpressRoute devresini klasik dağıtım modelinden Kaynak Yöneticisi dağıtım modeline götürür.</span><span class="sxs-lookup"><span data-stu-id="531e7-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="531e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="531e7-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="531e7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="531e7-105">DESCRIPTION</span></span>
<span data-ttu-id="531e7-106">**Taşıma-Azurermexpressroutedevresi** cmdlet 'i, bir ExpressRoute devresini klasik dağıtım modelinden Kaynak Yöneticisi dağıtım modeline taşır.</span><span class="sxs-lookup"><span data-stu-id="531e7-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="531e7-107">Taşıma sonrasında ExpressRoute devresi, Kaynak Yöneticisi dağıtım modelinde oluşturulan diğer ExpressRoute devresi gibi çalışır ve çalışır.</span><span class="sxs-lookup"><span data-stu-id="531e7-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="531e7-108">Devre, sanal ağ ve VPN ağ geçitleri bu işlemden taşınmaz.</span><span class="sxs-lookup"><span data-stu-id="531e7-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="531e7-109">Bu kaynakların taşıma sonrasında yeniden yapılandırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="531e7-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="531e7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="531e7-110">EXAMPLES</span></span>

### <span data-ttu-id="531e7-111">Örnek 1: ExpressRoute devresini Kaynak Yöneticisi dağıtım modeline taşıma</span><span class="sxs-lookup"><span data-stu-id="531e7-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="531e7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="531e7-112">PARAMETERS</span></span>

### <span data-ttu-id="531e7-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="531e7-113">-AsJob</span></span>
<span data-ttu-id="531e7-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="531e7-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531e7-115">-DefaultProfile</span></span>
<span data-ttu-id="531e7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="531e7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="531e7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="531e7-117">-Force</span></span>
<span data-ttu-id="531e7-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="531e7-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531e7-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="531e7-119">-Location</span></span>
<span data-ttu-id="531e7-120">ExpressRoute devresi bulunan Azure konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="531e7-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="531e7-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="531e7-121">-Name</span></span>
<span data-ttu-id="531e7-122">Taşınacak ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="531e7-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="531e7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="531e7-123">-ResourceGroupName</span></span>
<span data-ttu-id="531e7-124">Taşınan ExpressRoute devresini içerecek kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="531e7-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="531e7-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="531e7-125">-ServiceKey</span></span>
<span data-ttu-id="531e7-126">Klasik dağıtım modelinde ExpressRoute devresi tarafından kullanılan hizmet anahtarı.</span><span class="sxs-lookup"><span data-stu-id="531e7-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="531e7-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="531e7-127">-Tag</span></span>
<span data-ttu-id="531e7-128">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="531e7-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="531e7-129">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="531e7-129">For example:</span></span>

<span data-ttu-id="531e7-130">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="531e7-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="531e7-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="531e7-131">-Confirm</span></span>
<span data-ttu-id="531e7-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="531e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531e7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="531e7-133">-WhatIf</span></span>
<span data-ttu-id="531e7-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="531e7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="531e7-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="531e7-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531e7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531e7-136">CommonParameters</span></span>
<span data-ttu-id="531e7-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="531e7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531e7-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="531e7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531e7-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="531e7-139">INPUTS</span></span>

## <span data-ttu-id="531e7-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="531e7-140">OUTPUTS</span></span>

### <span data-ttu-id="531e7-141">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="531e7-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="531e7-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="531e7-142">NOTES</span></span>

## <span data-ttu-id="531e7-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="531e7-143">RELATED LINKS</span></span>

[<span data-ttu-id="531e7-144">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="531e7-144">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="531e7-145">New-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="531e7-145">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="531e7-146">Remove-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="531e7-146">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="531e7-147">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="531e7-147">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)

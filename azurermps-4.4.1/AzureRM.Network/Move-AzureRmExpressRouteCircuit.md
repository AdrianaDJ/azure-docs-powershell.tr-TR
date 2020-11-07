---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e4d167f98f837434018e04da91a31973acb45c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592180"
---
# <span data-ttu-id="3df3d-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3df3d-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="3df3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3df3d-102">SYNOPSIS</span></span>
<span data-ttu-id="3df3d-103">Bir ExpressRoute devresini klasik dağıtım modelinden Kaynak Yöneticisi dağıtım modeline götürür.</span><span class="sxs-lookup"><span data-stu-id="3df3d-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3df3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3df3d-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3df3d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3df3d-105">DESCRIPTION</span></span>
<span data-ttu-id="3df3d-106">**Taşıma-Azurermexpressroutedevresi** cmdlet 'i, bir ExpressRoute devresini klasik dağıtım modelinden Kaynak Yöneticisi dağıtım modeline taşır.</span><span class="sxs-lookup"><span data-stu-id="3df3d-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="3df3d-107">Taşıma sonrasında ExpressRoute devresi, Kaynak Yöneticisi dağıtım modelinde oluşturulan diğer ExpressRoute devresi gibi çalışır ve çalışır.</span><span class="sxs-lookup"><span data-stu-id="3df3d-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="3df3d-108">Devre, sanal ağ ve VPN ağ geçitleri bu işlemden taşınmaz.</span><span class="sxs-lookup"><span data-stu-id="3df3d-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="3df3d-109">Bu kaynakların taşıma sonrasında yeniden yapılandırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3df3d-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="3df3d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3df3d-110">EXAMPLES</span></span>

### <span data-ttu-id="3df3d-111">Örnek 1: ExpressRoute devresini Kaynak Yöneticisi dağıtım modeline taşıma</span><span class="sxs-lookup"><span data-stu-id="3df3d-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="3df3d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3df3d-112">PARAMETERS</span></span>

### <span data-ttu-id="3df3d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3df3d-113">-Force</span></span>
<span data-ttu-id="3df3d-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3df3d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3df3d-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="3df3d-115">-Location</span></span>
<span data-ttu-id="3df3d-116">ExpressRoute devresi bulunan Azure konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="3df3d-116">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="3df3d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3df3d-117">-Name</span></span>
<span data-ttu-id="3df3d-118">Taşınacak ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="3df3d-118">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="3df3d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df3d-119">-ResourceGroupName</span></span>
<span data-ttu-id="3df3d-120">Taşınan ExpressRoute devresini içerecek kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3df3d-120">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="3df3d-121">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="3df3d-121">-ServiceKey</span></span>
<span data-ttu-id="3df3d-122">Klasik dağıtım modelinde ExpressRoute devresi tarafından kullanılan hizmet anahtarı.</span><span class="sxs-lookup"><span data-stu-id="3df3d-122">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="3df3d-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3df3d-123">-Tag</span></span>
<span data-ttu-id="3df3d-124">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="3df3d-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3df3d-125">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="3df3d-125">For example:</span></span>

<span data-ttu-id="3df3d-126">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="3df3d-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3df3d-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="3df3d-127">-Confirm</span></span>
<span data-ttu-id="3df3d-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3df3d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df3d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df3d-129">-WhatIf</span></span>
<span data-ttu-id="3df3d-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3df3d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3df3d-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3df3d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3df3d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df3d-132">-DefaultProfile</span></span>
<span data-ttu-id="3df3d-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3df3d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3df3d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df3d-134">CommonParameters</span></span>
<span data-ttu-id="3df3d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3df3d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df3d-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3df3d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df3d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3df3d-137">INPUTS</span></span>

## <span data-ttu-id="3df3d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3df3d-138">OUTPUTS</span></span>

### <span data-ttu-id="3df3d-139">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="3df3d-139">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3df3d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3df3d-140">NOTES</span></span>

## <span data-ttu-id="3df3d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3df3d-141">RELATED LINKS</span></span>

[<span data-ttu-id="3df3d-142">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="3df3d-142">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3df3d-143">New-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="3df3d-143">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3df3d-144">Remove-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="3df3d-144">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3df3d-145">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="3df3d-145">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
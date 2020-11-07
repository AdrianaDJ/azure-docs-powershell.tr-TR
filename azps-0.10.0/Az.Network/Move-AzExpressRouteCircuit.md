---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: ffa10dca752adaeebbdd6fbf92a6a16b094a3085
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935445"
---
# <span data-ttu-id="f992a-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f992a-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="f992a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f992a-102">SYNOPSIS</span></span>
<span data-ttu-id="f992a-103">Bir ExpressRoute devresini klasik dağıtım modelinden Kaynak Yöneticisi dağıtım modeline götürür.</span><span class="sxs-lookup"><span data-stu-id="f992a-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="f992a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f992a-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f992a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f992a-105">DESCRIPTION</span></span>
<span data-ttu-id="f992a-106">**Taşıma-Azexpressroutedevresi** cmdlet 'i, bir ExpressRoute devresini klasik dağıtım modelinden Kaynak Yöneticisi dağıtım modeline taşır.</span><span class="sxs-lookup"><span data-stu-id="f992a-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="f992a-107">Taşıma sonrasında ExpressRoute devresi, Kaynak Yöneticisi dağıtım modelinde oluşturulan diğer ExpressRoute devresi gibi çalışır ve çalışır.</span><span class="sxs-lookup"><span data-stu-id="f992a-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="f992a-108">Devre, sanal ağ ve VPN ağ geçitleri bu işlemden taşınmaz.</span><span class="sxs-lookup"><span data-stu-id="f992a-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="f992a-109">Bu kaynakların taşıma sonrasında yeniden yapılandırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f992a-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="f992a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f992a-110">EXAMPLES</span></span>

### <span data-ttu-id="f992a-111">Örnek 1: ExpressRoute devresini Kaynak Yöneticisi dağıtım modeline taşıma</span><span class="sxs-lookup"><span data-stu-id="f992a-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="f992a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f992a-112">PARAMETERS</span></span>

### <span data-ttu-id="f992a-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="f992a-113">-AsJob</span></span>
<span data-ttu-id="f992a-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f992a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f992a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f992a-115">-DefaultProfile</span></span>
<span data-ttu-id="f992a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f992a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f992a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f992a-117">-Force</span></span>
<span data-ttu-id="f992a-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f992a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f992a-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="f992a-119">-Location</span></span>
<span data-ttu-id="f992a-120">ExpressRoute devresi bulunan Azure konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="f992a-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="f992a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="f992a-121">-Name</span></span>
<span data-ttu-id="f992a-122">Taşınacak ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="f992a-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="f992a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f992a-123">-ResourceGroupName</span></span>
<span data-ttu-id="f992a-124">Taşınan ExpressRoute devresini içerecek kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f992a-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="f992a-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="f992a-125">-ServiceKey</span></span>
<span data-ttu-id="f992a-126">Klasik dağıtım modelinde ExpressRoute devresi tarafından kullanılan hizmet anahtarı.</span><span class="sxs-lookup"><span data-stu-id="f992a-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="f992a-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f992a-127">-Tag</span></span>
<span data-ttu-id="f992a-128">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="f992a-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f992a-129">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="f992a-129">For example:</span></span>

<span data-ttu-id="f992a-130">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="f992a-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f992a-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="f992a-131">-Confirm</span></span>
<span data-ttu-id="f992a-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f992a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f992a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f992a-133">-WhatIf</span></span>
<span data-ttu-id="f992a-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f992a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f992a-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f992a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f992a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f992a-136">CommonParameters</span></span>
<span data-ttu-id="f992a-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f992a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f992a-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f992a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f992a-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f992a-139">INPUTS</span></span>

## <span data-ttu-id="f992a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f992a-140">OUTPUTS</span></span>

### <span data-ttu-id="f992a-141">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="f992a-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f992a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f992a-142">NOTES</span></span>

## <span data-ttu-id="f992a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f992a-143">RELATED LINKS</span></span>

[<span data-ttu-id="f992a-144">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="f992a-144">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f992a-145">Yeni-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="f992a-145">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="f992a-146">Remove-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="f992a-146">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="f992a-147">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="f992a-147">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)

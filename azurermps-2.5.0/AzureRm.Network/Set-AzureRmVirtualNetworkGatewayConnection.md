---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: bb098e23f6e55cc28fcae02b7094a953c5179308
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939688"
---
# <span data-ttu-id="34b87-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="34b87-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="34b87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34b87-102">SYNOPSIS</span></span>
<span data-ttu-id="34b87-103">Sanal ağ geçidi bağlantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="34b87-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34b87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34b87-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34b87-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34b87-105">DESCRIPTION</span></span>
<span data-ttu-id="34b87-106">**Set-AzureRmVirtualNetworkGatewayConnection** cmdlet 'i sanal ağ geçidi bağlantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="34b87-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="34b87-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34b87-107">EXAMPLES</span></span>

### <span data-ttu-id="34b87-108">2</span><span class="sxs-lookup"><span data-stu-id="34b87-108">1:</span></span>
```

```

## <span data-ttu-id="34b87-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34b87-109">PARAMETERS</span></span>

### <span data-ttu-id="34b87-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="34b87-110">-AsJob</span></span>
<span data-ttu-id="34b87-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="34b87-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34b87-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b87-112">-DefaultProfile</span></span>
<span data-ttu-id="34b87-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34b87-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34b87-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="34b87-114">-EnableBgp</span></span>
<span data-ttu-id="34b87-115">S2S VPN tüneli üzerinden BGP oturumunun kullanılıp kullanılmayacağını</span><span class="sxs-lookup"><span data-stu-id="34b87-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b87-116">-Force</span><span class="sxs-lookup"><span data-stu-id="34b87-116">-Force</span></span>
<span data-ttu-id="34b87-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="34b87-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34b87-118">-Ipsecpolicies</span><span class="sxs-lookup"><span data-stu-id="34b87-118">-IpsecPolicies</span></span>
<span data-ttu-id="34b87-119">IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="34b87-119">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b87-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="34b87-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="34b87-121">S2S bağlantısı için ilkeye dayalı trafik seçicileri kullanılıp kullanılmayacağını</span><span class="sxs-lookup"><span data-stu-id="34b87-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b87-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="34b87-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="34b87-123">Bu cmdlet 'in sanal ağ geçidi bağlantısını değiştirmek için kullandığı PSVirtualNetworkGatewayConnection nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34b87-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34b87-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="34b87-124">-Confirm</span></span>
<span data-ttu-id="34b87-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34b87-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34b87-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34b87-126">-WhatIf</span></span>
<span data-ttu-id="34b87-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34b87-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34b87-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34b87-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34b87-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b87-129">CommonParameters</span></span>
<span data-ttu-id="34b87-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34b87-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b87-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b87-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b87-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34b87-132">INPUTS</span></span>

### <span data-ttu-id="34b87-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="34b87-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="34b87-134">' VirtualNetworkGatewayConnection ' parametresi ardışık düzenin ' PSVirtualNetworkGatewayConnection ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="34b87-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="34b87-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34b87-135">OUTPUTS</span></span>

### <span data-ttu-id="34b87-136">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="34b87-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="34b87-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34b87-137">NOTES</span></span>

## <span data-ttu-id="34b87-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34b87-138">RELATED LINKS</span></span>

[<span data-ttu-id="34b87-139">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="34b87-139">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="34b87-140">Yeni-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="34b87-140">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="34b87-141">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="34b87-141">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)



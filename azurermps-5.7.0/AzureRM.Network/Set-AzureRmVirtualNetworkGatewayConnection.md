---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 218ef3115a4bc8325bc4dda37ae0a5e5820afae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588871"
---
# <span data-ttu-id="e38a7-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e38a7-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e38a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e38a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e38a7-103">Sanal ağ geçidi bağlantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="e38a7-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e38a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e38a7-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e38a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e38a7-105">DESCRIPTION</span></span>
<span data-ttu-id="e38a7-106">**Set-AzureRmVirtualNetworkGatewayConnection** cmdlet 'i sanal ağ geçidi bağlantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="e38a7-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="e38a7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e38a7-107">EXAMPLES</span></span>

## <span data-ttu-id="e38a7-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e38a7-108">PARAMETERS</span></span>

### <span data-ttu-id="e38a7-109">-Iş</span><span class="sxs-lookup"><span data-stu-id="e38a7-109">-AsJob</span></span>
<span data-ttu-id="e38a7-110">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e38a7-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e38a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38a7-111">-DefaultProfile</span></span>
<span data-ttu-id="e38a7-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e38a7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e38a7-113">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="e38a7-113">-EnableBgp</span></span>
<span data-ttu-id="e38a7-114">S2S VPN tüneli üzerinden BGP oturumunun kullanılıp kullanılmayacağını</span><span class="sxs-lookup"><span data-stu-id="e38a7-114">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="e38a7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e38a7-115">-Force</span></span>
<span data-ttu-id="e38a7-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e38a7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e38a7-117">-Ipsecpolicies</span><span class="sxs-lookup"><span data-stu-id="e38a7-117">-IpsecPolicies</span></span>
<span data-ttu-id="e38a7-118">IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="e38a7-118">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="e38a7-119">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="e38a7-119">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="e38a7-120">S2S bağlantısı için ilkeye dayalı trafik seçicileri kullanılıp kullanılmayacağını</span><span class="sxs-lookup"><span data-stu-id="e38a7-120">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="e38a7-121">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e38a7-121">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="e38a7-122">Bu cmdlet 'in sanal ağ geçidi bağlantısını değiştirmek için kullandığı PSVirtualNetworkGatewayConnection nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e38a7-122">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="e38a7-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e38a7-123">-Confirm</span></span>
<span data-ttu-id="e38a7-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e38a7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e38a7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e38a7-125">-WhatIf</span></span>
<span data-ttu-id="e38a7-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e38a7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e38a7-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e38a7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e38a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38a7-128">CommonParameters</span></span>
<span data-ttu-id="e38a7-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e38a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38a7-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e38a7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38a7-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e38a7-131">INPUTS</span></span>

### <span data-ttu-id="e38a7-132">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e38a7-132">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="e38a7-133">' VirtualNetworkGatewayConnection ' parametresi ardışık düzenin ' PSVirtualNetworkGatewayConnection ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e38a7-133">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="e38a7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e38a7-134">OUTPUTS</span></span>

### <span data-ttu-id="e38a7-135">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e38a7-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e38a7-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e38a7-136">NOTES</span></span>

## <span data-ttu-id="e38a7-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e38a7-137">RELATED LINKS</span></span>

[<span data-ttu-id="e38a7-138">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e38a7-138">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e38a7-139">Yeni-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e38a7-139">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e38a7-140">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e38a7-140">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)



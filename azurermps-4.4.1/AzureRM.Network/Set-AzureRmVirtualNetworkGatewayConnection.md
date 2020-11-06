---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5885f98d66e6226273215dcde856f5fc50d0bd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589216"
---
# <span data-ttu-id="14a5f-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="14a5f-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="14a5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="14a5f-103">Sanal ağ geçidi bağlantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="14a5f-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14a5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14a5f-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14a5f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14a5f-105">DESCRIPTION</span></span>
<span data-ttu-id="14a5f-106">**Set-AzureRmVirtualNetworkGatewayConnection** cmdlet 'i sanal ağ geçidi bağlantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="14a5f-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="14a5f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14a5f-107">EXAMPLES</span></span>

## <span data-ttu-id="14a5f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14a5f-108">PARAMETERS</span></span>

### <span data-ttu-id="14a5f-109">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="14a5f-109">-EnableBgp</span></span>
<span data-ttu-id="14a5f-110">S2S VPN tüneli üzerinden BGP oturumunun kullanılıp kullanılmayacağını</span><span class="sxs-lookup"><span data-stu-id="14a5f-110">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14a5f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="14a5f-111">-Force</span></span>
<span data-ttu-id="14a5f-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="14a5f-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="14a5f-113">-Ipsecpolicies</span><span class="sxs-lookup"><span data-stu-id="14a5f-113">-IpsecPolicies</span></span>
<span data-ttu-id="14a5f-114">IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="14a5f-114">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="14a5f-115">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="14a5f-115">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="14a5f-116">S2S bağlantısı için ilkeye dayalı trafik seçicileri kullanılıp kullanılmayacağını</span><span class="sxs-lookup"><span data-stu-id="14a5f-116">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a5f-117">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="14a5f-117">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="14a5f-118">Bu cmdlet 'in sanal ağ geçidi bağlantısını değiştirmek için kullandığı PSVirtualNetworkGatewayConnection nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="14a5f-118">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14a5f-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="14a5f-119">-Confirm</span></span>
<span data-ttu-id="14a5f-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="14a5f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a5f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a5f-121">-WhatIf</span></span>
<span data-ttu-id="14a5f-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="14a5f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a5f-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="14a5f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14a5f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a5f-124">-DefaultProfile</span></span>
<span data-ttu-id="14a5f-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14a5f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14a5f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a5f-126">CommonParameters</span></span>
<span data-ttu-id="14a5f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14a5f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a5f-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a5f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a5f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14a5f-129">INPUTS</span></span>

### <span data-ttu-id="14a5f-130">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="14a5f-130">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="14a5f-131">' VirtualNetworkGatewayConnection ' parametresi ardışık düzenin ' PSVirtualNetworkGatewayConnection ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="14a5f-131">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="14a5f-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14a5f-132">OUTPUTS</span></span>

### <span data-ttu-id="14a5f-133">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="14a5f-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="14a5f-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14a5f-134">NOTES</span></span>

## <span data-ttu-id="14a5f-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14a5f-135">RELATED LINKS</span></span>

[<span data-ttu-id="14a5f-136">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="14a5f-136">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="14a5f-137">Yeni-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="14a5f-137">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="14a5f-138">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="14a5f-138">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)



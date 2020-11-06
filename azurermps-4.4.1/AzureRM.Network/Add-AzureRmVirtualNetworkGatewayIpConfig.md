---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 08dc5728e13423fdd9e05c5d5b5d843b963c4aa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593075"
---
# <span data-ttu-id="7f258-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7f258-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="7f258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f258-102">SYNOPSIS</span></span>
<span data-ttu-id="7f258-103">Sanal ağ geçidine IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="7f258-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f258-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f258-104">SYNTAX</span></span>

### <span data-ttu-id="7f258-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="7f258-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f258-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7f258-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f258-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f258-107">DESCRIPTION</span></span>
<span data-ttu-id="7f258-108">**Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet 'i sanal ağ GEÇIDINE bir IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="7f258-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="7f258-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f258-109">EXAMPLES</span></span>

## <span data-ttu-id="7f258-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f258-110">PARAMETERS</span></span>

### <span data-ttu-id="7f258-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f258-111">-Name</span></span>
<span data-ttu-id="7f258-112">Eklenecek ağ geçidi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f258-112">Specifies the name of the gateway IP configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f258-113">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="7f258-113">-PrivateIpAddress</span></span>
<span data-ttu-id="7f258-114">Özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f258-114">Specifies the private IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f258-115">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7f258-115">-PublicIpAddress</span></span>
<span data-ttu-id="7f258-116">Genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f258-116">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f258-117">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="7f258-117">-PublicIpAddressId</span></span>
<span data-ttu-id="7f258-118">Genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f258-118">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f258-119">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="7f258-119">-Subnet</span></span>
<span data-ttu-id="7f258-120">**Pssubnet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f258-120">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f258-121">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7f258-121">-SubnetId</span></span>
<span data-ttu-id="7f258-122">Alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f258-122">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f258-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7f258-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="7f258-124">**Psvirtualnetworkgateway** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f258-124">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="7f258-125">Bu cmdlet belirttiğiniz **Psvirtualnetworkgateway** nesnesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7f258-125">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="7f258-126">**Psvirtualnetworkgateway** nesnesini almak için Get-AzureRmVirtualNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f258-126">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f258-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f258-127">-Confirm</span></span>
<span data-ttu-id="7f258-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f258-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f258-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f258-129">-WhatIf</span></span>
<span data-ttu-id="7f258-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f258-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f258-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f258-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f258-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f258-132">-DefaultProfile</span></span>
<span data-ttu-id="7f258-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f258-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f258-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f258-134">CommonParameters</span></span>
<span data-ttu-id="7f258-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f258-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f258-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f258-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f258-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f258-137">INPUTS</span></span>

### <span data-ttu-id="7f258-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7f258-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="7f258-139">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7f258-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="7f258-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f258-140">OUTPUTS</span></span>

### <span data-ttu-id="7f258-141">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7f258-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7f258-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f258-142">NOTES</span></span>

## <span data-ttu-id="7f258-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f258-143">RELATED LINKS</span></span>

[<span data-ttu-id="7f258-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7f258-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7f258-145">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7f258-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="7f258-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7f258-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)



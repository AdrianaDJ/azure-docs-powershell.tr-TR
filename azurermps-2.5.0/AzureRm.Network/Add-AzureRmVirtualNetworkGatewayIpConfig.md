---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 340baa4b7a7d0afaf0e0523cb8c2f14f8270bf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940115"
---
# <span data-ttu-id="72bfa-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="72bfa-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="72bfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="72bfa-103">Sanal ağ geçidine IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="72bfa-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72bfa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72bfa-104">SYNTAX</span></span>

### <span data-ttu-id="72bfa-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="72bfa-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72bfa-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="72bfa-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72bfa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="72bfa-107">DESCRIPTION</span></span>
<span data-ttu-id="72bfa-108">**Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet 'i sanal ağ GEÇIDINE bir IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="72bfa-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="72bfa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72bfa-109">EXAMPLES</span></span>

### <span data-ttu-id="72bfa-110">2</span><span class="sxs-lookup"><span data-stu-id="72bfa-110">1:</span></span>
```

```

## <span data-ttu-id="72bfa-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72bfa-111">PARAMETERS</span></span>

### <span data-ttu-id="72bfa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72bfa-112">-DefaultProfile</span></span>
<span data-ttu-id="72bfa-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72bfa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72bfa-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="72bfa-114">-Name</span></span>
<span data-ttu-id="72bfa-115">Eklenecek ağ geçidi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72bfa-115">Specifies the name of the gateway IP configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bfa-116">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="72bfa-116">-PrivateIpAddress</span></span>
<span data-ttu-id="72bfa-117">Özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72bfa-117">Specifies the private IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bfa-118">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="72bfa-118">-PublicIpAddress</span></span>
<span data-ttu-id="72bfa-119">Genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72bfa-119">Specifies the public IP address.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bfa-120">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="72bfa-120">-PublicIpAddressId</span></span>
<span data-ttu-id="72bfa-121">Genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="72bfa-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bfa-122">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="72bfa-122">-Subnet</span></span>
<span data-ttu-id="72bfa-123">**Pssubnet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72bfa-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bfa-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="72bfa-124">-SubnetId</span></span>
<span data-ttu-id="72bfa-125">Alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="72bfa-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bfa-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72bfa-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="72bfa-127">**Psvirtualnetworkgateway** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72bfa-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="72bfa-128">Bu cmdlet belirttiğiniz **Psvirtualnetworkgateway** nesnesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="72bfa-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="72bfa-129">**Psvirtualnetworkgateway** nesnesini almak için Get-AzureRmVirtualNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72bfa-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72bfa-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="72bfa-130">-Confirm</span></span>
<span data-ttu-id="72bfa-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72bfa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72bfa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72bfa-132">-WhatIf</span></span>
<span data-ttu-id="72bfa-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72bfa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72bfa-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72bfa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72bfa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72bfa-135">CommonParameters</span></span>
<span data-ttu-id="72bfa-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72bfa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72bfa-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72bfa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72bfa-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72bfa-138">INPUTS</span></span>

### <span data-ttu-id="72bfa-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72bfa-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="72bfa-140">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="72bfa-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="72bfa-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72bfa-141">OUTPUTS</span></span>

### <span data-ttu-id="72bfa-142">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72bfa-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="72bfa-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72bfa-143">NOTES</span></span>

## <span data-ttu-id="72bfa-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72bfa-144">RELATED LINKS</span></span>

[<span data-ttu-id="72bfa-145">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72bfa-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="72bfa-146">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="72bfa-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="72bfa-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="72bfa-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)



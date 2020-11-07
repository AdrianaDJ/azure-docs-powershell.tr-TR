---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 31790ead292c9146aa73f41c56e79f3bdf51c715
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935621"
---
# <span data-ttu-id="4dd5f-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="4dd5f-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="4dd5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dd5f-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd5f-103">Sanal ağ geçidine IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="4dd5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4dd5f-104">SYNTAX</span></span>

### <span data-ttu-id="4dd5f-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4dd5f-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd5f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4dd5f-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd5f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4dd5f-107">DESCRIPTION</span></span>
<span data-ttu-id="4dd5f-108">**Add-AzVirtualNetworkGatewayIpConfig** cmdlet 'i sanal ağ GEÇIDINE bir IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="4dd5f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4dd5f-109">EXAMPLES</span></span>

### <span data-ttu-id="4dd5f-110">2</span><span class="sxs-lookup"><span data-stu-id="4dd5f-110">1:</span></span>
```

```

## <span data-ttu-id="4dd5f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4dd5f-111">PARAMETERS</span></span>

### <span data-ttu-id="4dd5f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd5f-112">-DefaultProfile</span></span>
<span data-ttu-id="4dd5f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dd5f-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="4dd5f-114">-Name</span></span>
<span data-ttu-id="4dd5f-115">Eklenecek ağ geçidi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="4dd5f-116">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="4dd5f-116">-PrivateIpAddress</span></span>
<span data-ttu-id="4dd5f-117">Özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="4dd5f-118">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="4dd5f-118">-PublicIpAddress</span></span>
<span data-ttu-id="4dd5f-119">Genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="4dd5f-120">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="4dd5f-120">-PublicIpAddressId</span></span>
<span data-ttu-id="4dd5f-121">Genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="4dd5f-122">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="4dd5f-122">-Subnet</span></span>
<span data-ttu-id="4dd5f-123">**Pssubnet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="4dd5f-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4dd5f-124">-SubnetId</span></span>
<span data-ttu-id="4dd5f-125">Alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="4dd5f-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4dd5f-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="4dd5f-127">**Psvirtualnetworkgateway** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="4dd5f-128">Bu cmdlet belirttiğiniz **Psvirtualnetworkgateway** nesnesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="4dd5f-129">**Psvirtualnetworkgateway** nesnesini almak için Get-AzVirtualNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="4dd5f-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="4dd5f-130">-Confirm</span></span>
<span data-ttu-id="4dd5f-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dd5f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd5f-132">-WhatIf</span></span>
<span data-ttu-id="4dd5f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dd5f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dd5f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd5f-135">CommonParameters</span></span>
<span data-ttu-id="4dd5f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4dd5f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd5f-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd5f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd5f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4dd5f-138">INPUTS</span></span>

### <span data-ttu-id="4dd5f-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4dd5f-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="4dd5f-140">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4dd5f-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="4dd5f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4dd5f-141">OUTPUTS</span></span>

### <span data-ttu-id="4dd5f-142">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4dd5f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="4dd5f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4dd5f-143">NOTES</span></span>

## <span data-ttu-id="4dd5f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4dd5f-144">RELATED LINKS</span></span>

[<span data-ttu-id="4dd5f-145">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4dd5f-145">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="4dd5f-146">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="4dd5f-146">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="4dd5f-147">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="4dd5f-147">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)



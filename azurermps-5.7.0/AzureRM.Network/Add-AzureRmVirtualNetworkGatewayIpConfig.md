---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 4b157dfd7e7ac47a8161c9f36f9b52bbaaa61869
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588191"
---
# <span data-ttu-id="2725e-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="2725e-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="2725e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2725e-102">SYNOPSIS</span></span>
<span data-ttu-id="2725e-103">Sanal ağ geçidine IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="2725e-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2725e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2725e-104">SYNTAX</span></span>

### <span data-ttu-id="2725e-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="2725e-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2725e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2725e-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2725e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2725e-107">DESCRIPTION</span></span>
<span data-ttu-id="2725e-108">**Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet 'i sanal ağ GEÇIDINE bir IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="2725e-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="2725e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2725e-109">EXAMPLES</span></span>

## <span data-ttu-id="2725e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2725e-110">PARAMETERS</span></span>

### <span data-ttu-id="2725e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2725e-111">-DefaultProfile</span></span>
<span data-ttu-id="2725e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2725e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2725e-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2725e-113">-Name</span></span>
<span data-ttu-id="2725e-114">Eklenecek ağ geçidi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2725e-114">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="2725e-115">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="2725e-115">-PrivateIpAddress</span></span>
<span data-ttu-id="2725e-116">Özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2725e-116">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="2725e-117">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="2725e-117">-PublicIpAddress</span></span>
<span data-ttu-id="2725e-118">Genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2725e-118">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="2725e-119">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="2725e-119">-PublicIpAddressId</span></span>
<span data-ttu-id="2725e-120">Genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2725e-120">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="2725e-121">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="2725e-121">-Subnet</span></span>
<span data-ttu-id="2725e-122">**Pssubnet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2725e-122">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="2725e-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2725e-123">-SubnetId</span></span>
<span data-ttu-id="2725e-124">Alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2725e-124">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="2725e-125">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2725e-125">-VirtualNetworkGateway</span></span>
<span data-ttu-id="2725e-126">**Psvirtualnetworkgateway** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2725e-126">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="2725e-127">Bu cmdlet belirttiğiniz **Psvirtualnetworkgateway** nesnesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2725e-127">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="2725e-128">**Psvirtualnetworkgateway** nesnesini almak için Get-AzureRmVirtualNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2725e-128">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="2725e-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="2725e-129">-Confirm</span></span>
<span data-ttu-id="2725e-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2725e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2725e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2725e-131">-WhatIf</span></span>
<span data-ttu-id="2725e-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2725e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2725e-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2725e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2725e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2725e-134">CommonParameters</span></span>
<span data-ttu-id="2725e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2725e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2725e-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2725e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2725e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2725e-137">INPUTS</span></span>

### <span data-ttu-id="2725e-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2725e-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="2725e-139">' VirtualNetworkGateway ' parametresi ardışık düzenin ' PSVirtualNetworkGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2725e-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="2725e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2725e-140">OUTPUTS</span></span>

### <span data-ttu-id="2725e-141">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2725e-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2725e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2725e-142">NOTES</span></span>

## <span data-ttu-id="2725e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2725e-143">RELATED LINKS</span></span>

[<span data-ttu-id="2725e-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2725e-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2725e-145">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="2725e-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="2725e-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="2725e-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)



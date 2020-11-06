---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: b88fff9775665f5b20f403d46f11bba89dc61220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589425"
---
# <span data-ttu-id="9cb95-101">Remove-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="9cb95-101">Remove-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="9cb95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cb95-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb95-103">Sanal ağ geçidi kaynağında VPN özel IPSec ilkesi kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9cb95-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cb95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cb95-104">SYNTAX</span></span>

### <span data-ttu-id="9cb95-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9cb95-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb95-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9cb95-106">ByFactoryObject</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb95-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="9cb95-107">ByResourceId</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb95-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cb95-108">DESCRIPTION</span></span>
<span data-ttu-id="9cb95-109">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="9cb95-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="9cb95-110">**Remove-Azurermvpnclientıpsecparameter** cmdlet 'ı sanal ağ geçidinde ayarlanan VPN özel IPSec parametrelerini kaldırır, bu da sanal ağ ağ geçidiniz üzerinde, virtualnetworkgateway adına ve kaynak grubu ADıNA dayanan VPN ağ geçidinde varsayılan VPN IPSec ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9cb95-110">The **Remove-AzureRmVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="9cb95-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cb95-111">EXAMPLES</span></span>

### <span data-ttu-id="9cb95-112">1: sanal ağ ağ geçidinde ayarlanan VPN IPSec parametrelerini siler</span><span class="sxs-lookup"><span data-stu-id="9cb95-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="9cb95-113">Sanal ağ geçidinde "myRG" kaynak grubunda "myGateway" adıyla ayarlanmış VPN özel IPSec parametrelerini siler.</span><span class="sxs-lookup"><span data-stu-id="9cb95-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="9cb95-114">Bu komut, kaldırmanın başarılı olup olmadığını gösteren bool nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="9cb95-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="9cb95-115">Not: Bu, sanal ağ geçidinde varsayılan VPN IPSec ilkesini ayarlamaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="9cb95-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="9cb95-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cb95-116">PARAMETERS</span></span>

### <span data-ttu-id="9cb95-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb95-117">-DefaultProfile</span></span>
<span data-ttu-id="9cb95-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cb95-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb95-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cb95-119">-InputObject</span></span>
<span data-ttu-id="9cb95-120">Sanal ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="9cb95-120">The virtual network gateaway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb95-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb95-121">-ResourceGroupName</span></span>
<span data-ttu-id="9cb95-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9cb95-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb95-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9cb95-123">-ResourceId</span></span>
<span data-ttu-id="9cb95-124">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="9cb95-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb95-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9cb95-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9cb95-126">Sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="9cb95-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb95-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="9cb95-127">-Confirm</span></span>
<span data-ttu-id="9cb95-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9cb95-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb95-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb95-129">-WhatIf</span></span>
<span data-ttu-id="9cb95-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cb95-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb95-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9cb95-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb95-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb95-132">CommonParameters</span></span>
<span data-ttu-id="9cb95-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cb95-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb95-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cb95-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb95-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cb95-135">INPUTS</span></span>

### <span data-ttu-id="9cb95-136">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9cb95-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="9cb95-137">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9cb95-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9cb95-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9cb95-138">System.String</span></span>

## <span data-ttu-id="9cb95-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cb95-139">OUTPUTS</span></span>

### <span data-ttu-id="9cb95-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9cb95-140">System.Boolean</span></span>

## <span data-ttu-id="9cb95-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cb95-141">NOTES</span></span>

## <span data-ttu-id="9cb95-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cb95-142">RELATED LINKS</span></span>

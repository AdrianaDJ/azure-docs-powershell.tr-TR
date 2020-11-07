---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: fcf908f0c67a81ad9ff82eec3aad82f14ac6d1f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917999"
---
# <span data-ttu-id="03b72-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="03b72-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="03b72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03b72-102">SYNOPSIS</span></span>
<span data-ttu-id="03b72-103">Sanal ağ geçidi kaynağında VPN özel IPSec ilkesi kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="03b72-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="03b72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03b72-104">SYNTAX</span></span>

### <span data-ttu-id="03b72-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="03b72-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b72-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="03b72-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b72-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="03b72-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03b72-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="03b72-108">DESCRIPTION</span></span>
<span data-ttu-id="03b72-109">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="03b72-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="03b72-110">**Remove-Azvpnclientıpsecparameter** cmdlet 'ı, sanal ağ geçidinde ayarlanan VPN özel IPSec parametrelerini kaldırır, bu da VPN ağ geçidinde varsayılan VPN IPSec Ilkesini VirtualNetworkGateway adına ve kaynak grubu adına dayalı olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="03b72-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="03b72-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03b72-111">EXAMPLES</span></span>

### <span data-ttu-id="03b72-112">1: sanal ağ ağ geçidinde ayarlanan VPN IPSec parametrelerini siler</span><span class="sxs-lookup"><span data-stu-id="03b72-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="03b72-113">Sanal ağ geçidinde "myRG" kaynak grubunda "myGateway" adıyla ayarlanmış VPN özel IPSec parametrelerini siler.</span><span class="sxs-lookup"><span data-stu-id="03b72-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="03b72-114">Bu komut, kaldırmanın başarılı olup olmadığını gösteren bool nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="03b72-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="03b72-115">Not: Bu, sanal ağ geçidinde varsayılan VPN IPSec ilkesini ayarlamaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="03b72-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="03b72-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03b72-116">PARAMETERS</span></span>

### <span data-ttu-id="03b72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b72-117">-DefaultProfile</span></span>
<span data-ttu-id="03b72-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03b72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b72-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03b72-119">-InputObject</span></span>
<span data-ttu-id="03b72-120">Sanal ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="03b72-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="03b72-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b72-121">-ResourceGroupName</span></span>
<span data-ttu-id="03b72-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="03b72-122">The resource group name.</span></span>

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

### <span data-ttu-id="03b72-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="03b72-123">-ResourceId</span></span>
<span data-ttu-id="03b72-124">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="03b72-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="03b72-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="03b72-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="03b72-126">Sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="03b72-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="03b72-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="03b72-127">-Confirm</span></span>
<span data-ttu-id="03b72-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03b72-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03b72-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03b72-129">-WhatIf</span></span>
<span data-ttu-id="03b72-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03b72-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03b72-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03b72-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03b72-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b72-132">CommonParameters</span></span>
<span data-ttu-id="03b72-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03b72-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b72-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03b72-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b72-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03b72-135">INPUTS</span></span>

### <span data-ttu-id="03b72-136">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="03b72-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="03b72-137">System. String</span><span class="sxs-lookup"><span data-stu-id="03b72-137">System.String</span></span>

## <span data-ttu-id="03b72-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03b72-138">OUTPUTS</span></span>

### <span data-ttu-id="03b72-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03b72-139">System.Boolean</span></span>

## <span data-ttu-id="03b72-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03b72-140">NOTES</span></span>

## <span data-ttu-id="03b72-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03b72-141">RELATED LINKS</span></span>

[<span data-ttu-id="03b72-142">Get-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="03b72-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="03b72-143">Yeni-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="03b72-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="03b72-144">Set-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="03b72-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)

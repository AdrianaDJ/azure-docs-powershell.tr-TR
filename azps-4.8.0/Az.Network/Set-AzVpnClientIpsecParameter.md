---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108819"
---
# <span data-ttu-id="4fd38-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="4fd38-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="4fd38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fd38-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd38-103">Mevcut sanal ağ geçidi için VPN IPSec parametrelerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4fd38-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="4fd38-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4fd38-104">SYNTAX</span></span>

### <span data-ttu-id="4fd38-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4fd38-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd38-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4fd38-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd38-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="4fd38-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fd38-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4fd38-108">DESCRIPTION</span></span>
<span data-ttu-id="4fd38-109">**Set-Azvpnclientıpsecparameter** cmdlet 'i, mevcut sanal ağ ağ geçidi için VPN IPSec parametrelerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4fd38-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="4fd38-110">Sanal ağ geçidi oluşturulduğunda, ağ geçidinde varsayılan VPN IPSec ilkeleri kümesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4fd38-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="4fd38-111">Bu durumda, site kullanıcısı, VPN ağ geçidine bağlanmak için belirli özel IPSec ilkesini kullanmak istiyor, kullanıcının önce VPN ağ geçidinde IPSec ilkesini ayarlamış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4fd38-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="4fd38-112">**Set-Azvpnclientıpsecparameter** , bunu yapmanın bir yolunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="4fd38-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="4fd38-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4fd38-113">EXAMPLES</span></span>

### <span data-ttu-id="4fd38-114">Örnek 1: varolan sanal ağ ağ geçidine özel VPN IPSec ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4fd38-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="4fd38-115">Bu örnekte, özel VPN IPSec ilkesi, ContosoResourceGroup adlı kaynak grubundan ContosoVirtualGateway adlı varolan sanal ağ ağ geçidine göre ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4fd38-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="4fd38-116">New-AzVpnClientIpsecParameter cmdlet, geçen bir veya tüm parametre değerlerini geçen Kullanıcı adına geçirilen VPN IPSec parametreleri nesnesini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4fd38-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="4fd38-117">Bu oluşturulmuş Vpnclientıpsecparameters nesnesi, yukarıdaki örnekte gösterildiği gibi sanal ağ geçidinde belirtilen VPN IPSec özel ilkesini ayarlamak için Set-AzVpnClientIpsecParameter komutuna geçirilir.</span><span class="sxs-lookup"><span data-stu-id="4fd38-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="4fd38-118">Bu komut, parametre ayarlama işlevinin gösterildiği Vpnclientıpsecparameters nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4fd38-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="4fd38-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4fd38-119">PARAMETERS</span></span>

### <span data-ttu-id="4fd38-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd38-120">-DefaultProfile</span></span>
<span data-ttu-id="4fd38-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4fd38-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd38-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fd38-122">-InputObject</span></span>
<span data-ttu-id="4fd38-123">Sanal ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="4fd38-123">The virtual network gateway object</span></span>

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

### <span data-ttu-id="4fd38-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd38-124">-ResourceGroupName</span></span>
<span data-ttu-id="4fd38-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4fd38-125">The resource group name.</span></span>

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

### <span data-ttu-id="4fd38-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4fd38-126">-ResourceId</span></span>
<span data-ttu-id="4fd38-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="4fd38-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4fd38-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="4fd38-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="4fd38-129">Sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="4fd38-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="4fd38-130">-Vpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="4fd38-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="4fd38-131">VPN istemcisi IPSec parametreleri.</span><span class="sxs-lookup"><span data-stu-id="4fd38-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="4fd38-132">Bu parametre değeri PS komut satırı: New-Azvpnclientıpsecparameter kullanılarak oluşturulabilir</span><span class="sxs-lookup"><span data-stu-id="4fd38-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd38-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="4fd38-133">-Confirm</span></span>
<span data-ttu-id="4fd38-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4fd38-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fd38-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fd38-135">-WhatIf</span></span>
<span data-ttu-id="4fd38-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4fd38-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fd38-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4fd38-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fd38-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd38-138">CommonParameters</span></span>
<span data-ttu-id="4fd38-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4fd38-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd38-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd38-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd38-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4fd38-141">INPUTS</span></span>

### <span data-ttu-id="4fd38-142">Microsoft. Azure. Commands. Network. model. Psvpnclientıpsecparameters</span><span class="sxs-lookup"><span data-stu-id="4fd38-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="4fd38-143">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4fd38-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="4fd38-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4fd38-144">System.String</span></span>

## <span data-ttu-id="4fd38-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4fd38-145">OUTPUTS</span></span>

### <span data-ttu-id="4fd38-146">Microsoft. Azure. Commands. Network. model. Psvpnclientıpsecparameters</span><span class="sxs-lookup"><span data-stu-id="4fd38-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="4fd38-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4fd38-147">NOTES</span></span>

## <span data-ttu-id="4fd38-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4fd38-148">RELATED LINKS</span></span>

[<span data-ttu-id="4fd38-149">Get-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="4fd38-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="4fd38-150">Yeni-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="4fd38-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="4fd38-151">Remove-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="4fd38-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

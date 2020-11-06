---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 38dcfdb1188a810b0f154dfed31f8a1ef3206247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591344"
---
# <span data-ttu-id="ed11b-101">Set-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ed11b-101">Set-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="ed11b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed11b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed11b-103">Mevcut sanal ağ geçidi için VPN IPSec parametrelerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ed11b-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed11b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed11b-104">SYNTAX</span></span>

### <span data-ttu-id="ed11b-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed11b-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed11b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ed11b-106">ByFactoryObject</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed11b-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="ed11b-107">ByResourceId</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed11b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed11b-108">DESCRIPTION</span></span>
<span data-ttu-id="ed11b-109">**Set-Azurermvpnclientıpsecparameter** cmdlet 'i, mevcut sanal ağ ağ geçidi için VPN IPSec parametrelerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ed11b-109">The **Set-AzureRmVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="ed11b-110">Sanal ağ geçidi oluşturulduğunda, ağ geçidinde varsayılan VPN IPSec ilkeleri kümesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ed11b-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="ed11b-111">Bu durumda, site kullanıcısı, VPN ağ geçidine bağlanmak için belirli özel IPSec ilkesini kullanmak istiyor, kullanıcının önce VPN ağ geçidinde IPSec ilkesini ayarlamış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ed11b-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="ed11b-112">**Set-Azurermvpnclientıpsecparameter** , bunu yapmanın bir yolunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="ed11b-112">**Set-AzureRmVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="ed11b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed11b-113">EXAMPLES</span></span>

### <span data-ttu-id="ed11b-114">Örnek 1: varolan sanal ağ ağ geçidine özel VPN IPSec ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ed11b-114">Example 1 : Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="ed11b-115">Bu örnekte, özel VPN IPSec ilkesi, ContosoResourceGroup adlı kaynak grubundan ContosoVirtualGateway adlı varolan sanal ağ ağ geçidine göre ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ed11b-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="ed11b-116">New-AzureRmVpnClientIpsecParameter cmdlet, geçen bir veya tüm parametre değerlerini geçen Kullanıcı adına geçirilen VPN IPSec parametreleri nesnesini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ed11b-116">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="ed11b-117">Bu oluşturulmuş Vpnclientıpsecparameters nesnesi, yukarıdaki örnekte gösterildiği gibi sanal ağ geçidinde belirtilen VPN IPSec özel ilkesini ayarlamak için Set-AzureRmVpnClientIpsecParameter komutuna geçirilir.</span><span class="sxs-lookup"><span data-stu-id="ed11b-117">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="ed11b-118">Bu komut, parametre ayarlama işlevinin gösterildiği Vpnclientıpsecparameters nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ed11b-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="ed11b-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed11b-119">PARAMETERS</span></span>

### <span data-ttu-id="ed11b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed11b-120">-DefaultProfile</span></span>
<span data-ttu-id="ed11b-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed11b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed11b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed11b-122">-InputObject</span></span>
<span data-ttu-id="ed11b-123">Sanal ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="ed11b-123">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="ed11b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed11b-124">-ResourceGroupName</span></span>
<span data-ttu-id="ed11b-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ed11b-125">The resource group name.</span></span>

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

### <span data-ttu-id="ed11b-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ed11b-126">-ResourceId</span></span>
<span data-ttu-id="ed11b-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ed11b-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ed11b-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ed11b-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ed11b-129">Sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="ed11b-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="ed11b-130">-Vpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="ed11b-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="ed11b-131">VPN istemcisi IPSec parametreleri.</span><span class="sxs-lookup"><span data-stu-id="ed11b-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="ed11b-132">Bu parametre değeri PS komut ver: New-Azurermvpnclientıpsecparameter kullanılarak oluşturulabilir</span><span class="sxs-lookup"><span data-stu-id="ed11b-132">This parameter value can be constructed using PS command let:New-AzureRmVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="ed11b-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed11b-133">-Confirm</span></span>
<span data-ttu-id="ed11b-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed11b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed11b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed11b-135">-WhatIf</span></span>
<span data-ttu-id="ed11b-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed11b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed11b-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed11b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed11b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed11b-138">CommonParameters</span></span>
<span data-ttu-id="ed11b-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed11b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed11b-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed11b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed11b-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed11b-141">INPUTS</span></span>

### <span data-ttu-id="ed11b-142">Microsoft. Azure. Commands. Network. model. Psvpnclientıpsecparameters</span><span class="sxs-lookup"><span data-stu-id="ed11b-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>
<span data-ttu-id="ed11b-143">Parametreler: Vpnclientıpsecparameter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ed11b-143">Parameters: VpnClientIPsecParameter (ByValue)</span></span>

### <span data-ttu-id="ed11b-144">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed11b-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="ed11b-145">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ed11b-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ed11b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ed11b-146">System.String</span></span>

## <span data-ttu-id="ed11b-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed11b-147">OUTPUTS</span></span>

### <span data-ttu-id="ed11b-148">Microsoft. Azure. Commands. Network. model. Psvpnclientıpsecparameters</span><span class="sxs-lookup"><span data-stu-id="ed11b-148">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="ed11b-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed11b-149">NOTES</span></span>

## <span data-ttu-id="ed11b-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed11b-150">RELATED LINKS</span></span>

[<span data-ttu-id="ed11b-151">Yeni-Azurermvpnclientıpsecparameters</span><span class="sxs-lookup"><span data-stu-id="ed11b-151">New-AzureRmVpnClientIpsecParameters</span></span>](./New-AzureRmVpnClientIpsecParameters.md)

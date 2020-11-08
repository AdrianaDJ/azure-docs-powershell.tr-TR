---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 6d16703b7f0492bb2c37291e135cb1b9c836a572
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097252"
---
# <span data-ttu-id="0d7e7-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0d7e7-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="0d7e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7e7-103">Site bağlantısı noktası için VirtualHub altında yeni bir P2SVpnGateway oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="0d7e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d7e7-104">SYNTAX</span></span>

### <span data-ttu-id="0d7e7-105">ByVirtualHubNameByVpnServerConfigurationObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0d7e7-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d7e7-106">Byvirtualhubnamebyvpnserverconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="0d7e7-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d7e7-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="0d7e7-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d7e7-108">Byvirtualhubobjectbyvpnserverconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="0d7e7-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d7e7-109">Byvirtualhubresourceıdbyvpnserverconfigurationnesnesi</span><span class="sxs-lookup"><span data-stu-id="0d7e7-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d7e7-110">Byvirtualhubresourceıdbyvpnserverconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="0d7e7-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d7e7-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d7e7-111">DESCRIPTION</span></span>
<span data-ttu-id="0d7e7-112">**New-AzP2sVpnGateway** cmdlet 'i, site Istemcilerinden Azure virtualwan 'a noktadan site bağlanabilirliğinin üzerine gelmek Için virtualhub 'ın altında yeni bir P2SVpnGateway oluşturmanıza imkan verir.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-112">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="0d7e7-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d7e7-113">EXAMPLES</span></span>

### <span data-ttu-id="0d7e7-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0d7e7-114">Example 1</span></span>
```powershell
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="0d7e7-115">**New-AzP2sVpnGateway** cmdlet 'i, site bağlantısının üzerine gelmek Için virtualhub altında yeni bir P2SVpnGateway oluşturmanıza imkan verir.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-115">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="0d7e7-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d7e7-116">PARAMETERS</span></span>

### <span data-ttu-id="0d7e7-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="0d7e7-117">-AsJob</span></span>
<span data-ttu-id="0d7e7-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0d7e7-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d7e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7e7-119">-DefaultProfile</span></span>
<span data-ttu-id="0d7e7-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d7e7-121">-Name</span></span>
<span data-ttu-id="0d7e7-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d7e7-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d7e7-124">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-124">The resource name.</span></span>

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

### <span data-ttu-id="0d7e7-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0d7e7-125">-Tag</span></span>
<span data-ttu-id="0d7e7-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-127">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="0d7e7-127">-VirtualHub</span></span>
<span data-ttu-id="0d7e7-128">Bu P2SVpnGateway 'in ilişkilendirildiği VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-128">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-129">-Virtualhubıd</span><span class="sxs-lookup"><span data-stu-id="0d7e7-129">-VirtualHubId</span></span>
<span data-ttu-id="0d7e7-130">Bu P2SVpnGateway ile ilişkilendirilmesi gerektiği VirtualHub kimliği.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-130">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-131">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="0d7e7-131">-VirtualHubName</span></span>
<span data-ttu-id="0d7e7-132">Bu P2SVpnGateway ile ilişkilendirilmesi gerektiği VirtualHub kimliği.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-132">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-133">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="0d7e7-133">-VpnClientAddressPool</span></span>
<span data-ttu-id="0d7e7-134">Bu P2SVpnGateway P2SConnectionConfiguration için VpnClient AddressPool P2S.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-134">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-135">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="0d7e7-135">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="0d7e7-136">Bu P2SVpnGateway için ölçek birimi.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-136">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-137">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d7e7-137">-VpnServerConfiguration</span></span>
<span data-ttu-id="0d7e7-138">Bu P2SVpnGateway 'e eklenecek VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-138">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-139">-Vpnserverconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="0d7e7-139">-VpnServerConfigurationId</span></span>
<span data-ttu-id="0d7e7-140">Bu P2SVpnGateway 'in eklendiği VPN sunucusu yapılandırma nesnesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-140">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d7e7-141">-Confirm</span></span>
<span data-ttu-id="0d7e7-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d7e7-143">-WhatIf</span></span>
<span data-ttu-id="0d7e7-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d7e7-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7e7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7e7-146">CommonParameters</span></span>
<span data-ttu-id="0d7e7-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d7e7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7e7-148">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d7e7-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7e7-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d7e7-149">INPUTS</span></span>

### <span data-ttu-id="0d7e7-150">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0d7e7-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="0d7e7-151">System. String Microsoft. Azure. Commands. Network. modeller. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d7e7-151">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="0d7e7-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d7e7-152">OUTPUTS</span></span>

### <span data-ttu-id="0d7e7-153">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0d7e7-153">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="0d7e7-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d7e7-154">NOTES</span></span>

## <span data-ttu-id="0d7e7-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d7e7-155">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 39fb3223b1a80b831874bbd833d6d0c97aace53f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937328"
---
# <span data-ttu-id="69faf-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="69faf-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="69faf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69faf-102">SYNOPSIS</span></span>
<span data-ttu-id="69faf-103">VirtualHub 'ın altında, site bağlantısının üzerine gelin mevcut bir P2SVpnGateway 'i güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="69faf-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="69faf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69faf-104">SYNTAX</span></span>

### <span data-ttu-id="69faf-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="69faf-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69faf-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="69faf-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69faf-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="69faf-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69faf-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="69faf-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69faf-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="69faf-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69faf-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="69faf-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69faf-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="69faf-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69faf-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="69faf-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69faf-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="69faf-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69faf-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="69faf-114">DESCRIPTION</span></span>
<span data-ttu-id="69faf-115">**Update-AzP2sVpnGateway** cmdlet 'ı, virtualhub altındaki mevcut bir P2SVpnGateway yeni VpnClientAddressPool veya yeni VpnServerConfiguration veya VpnGatewayScaleUnit değişimi ile güncelleştirmenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="69faf-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="69faf-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69faf-116">EXAMPLES</span></span>

### <span data-ttu-id="69faf-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="69faf-117">Example 1</span></span>
```powershell
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1 
PS C:\> $vpnClientAddressSpaces[0] = "101.10.0.0/16"
PS C:\> Update-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VpnClientAddressPool $vpnClientAddressSpaces                                    

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/NilamdWestUsVirtualH
                                 ub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/NilamdWe
                                 stUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "101.10.0.0/16"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"d7debc2f-ccbb-4f00-bddc-42c99b52fda3\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="69faf-118">**Update-AzP2sVpnGateway** cmdlet 'ı, virtualhub altındaki mevcut bir P2SVpnGateway yeni VpnClientAddressPool ile güncelleştirmenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="69faf-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="69faf-119">Site istemcisi bu P2SVpnGateway ile bağlantı kurduğunda, bu VpnClientAddressPool 'un IP adresinden biri bu istemciye tahsis olur.</span><span class="sxs-lookup"><span data-stu-id="69faf-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

## <span data-ttu-id="69faf-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69faf-120">PARAMETERS</span></span>

### <span data-ttu-id="69faf-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="69faf-121">-AsJob</span></span>
<span data-ttu-id="69faf-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="69faf-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69faf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69faf-123">-DefaultProfile</span></span>
<span data-ttu-id="69faf-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69faf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69faf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69faf-125">-InputObject</span></span>
<span data-ttu-id="69faf-126">Değiştirilecek P2S VPN ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="69faf-126">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69faf-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="69faf-127">-Name</span></span>
<span data-ttu-id="69faf-128">P2S VPN ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="69faf-128">The P2S vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases: ResourceName, P2SVpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69faf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69faf-129">-ResourceGroupName</span></span>
<span data-ttu-id="69faf-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="69faf-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69faf-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="69faf-131">-ResourceId</span></span>
<span data-ttu-id="69faf-132">Değiştirilecek P2SVpnGateway Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="69faf-132">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69faf-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="69faf-133">-Tag</span></span>
<span data-ttu-id="69faf-134">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="69faf-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="69faf-135">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="69faf-135">-VpnClientAddressPool</span></span>
<span data-ttu-id="69faf-136">Bu P2SVpnGateway P2SConnectionConfiguration için VpnClient AddressPool P2S.</span><span class="sxs-lookup"><span data-stu-id="69faf-136">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69faf-137">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="69faf-137">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="69faf-138">Bu P2SVpnGateway için ölçek birimi.</span><span class="sxs-lookup"><span data-stu-id="69faf-138">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69faf-139">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="69faf-139">-VpnServerConfiguration</span></span>
<span data-ttu-id="69faf-140">Bu P2SVpnGateway 'e eklenecek VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="69faf-140">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69faf-141">-Vpnserverconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="69faf-141">-VpnServerConfigurationId</span></span>
<span data-ttu-id="69faf-142">Bu P2SVpnGateway 'in eklendiği VPN sunucusu yapılandırma nesnesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="69faf-142">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationResourceId, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69faf-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="69faf-143">-Confirm</span></span>
<span data-ttu-id="69faf-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69faf-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69faf-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69faf-145">-WhatIf</span></span>
<span data-ttu-id="69faf-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69faf-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69faf-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69faf-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69faf-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69faf-148">CommonParameters</span></span>
<span data-ttu-id="69faf-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69faf-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69faf-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69faf-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69faf-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69faf-151">INPUTS</span></span>

### <span data-ttu-id="69faf-152">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="69faf-152">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="69faf-153">System. String Microsoft. Azure. Commands. Network. modeller. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="69faf-153">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="69faf-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69faf-154">OUTPUTS</span></span>

### <span data-ttu-id="69faf-155">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="69faf-155">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="69faf-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69faf-156">NOTES</span></span>

## <span data-ttu-id="69faf-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69faf-157">RELATED LINKS</span></span>

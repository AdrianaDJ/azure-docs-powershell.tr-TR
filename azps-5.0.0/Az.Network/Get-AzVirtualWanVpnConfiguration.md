---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
ms.openlocfilehash: 6e67f192cab1d1183d8c8cfd1a38f6c398311bf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276897"
---
# <span data-ttu-id="34aed-101">Get-AzVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="34aed-101">Get-AzVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="34aed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34aed-102">SYNOPSIS</span></span>
<span data-ttu-id="34aed-103">VpnConnections aracılığıyla bu WAN 'a bağlı VpnSites alt kümesinin VPN yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="34aed-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="34aed-104">Üretilen VPN yapılandırmasını, müşterinin belirttiği bir depolama blob 'una yükler.</span><span class="sxs-lookup"><span data-stu-id="34aed-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="34aed-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34aed-105">SYNTAX</span></span>

### <span data-ttu-id="34aed-106">Byvirtualwannamebyvpnsitenesnesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34aed-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34aed-107">Byvirtualwannamebyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="34aed-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34aed-108">Byvirtualwanobjectbyvpnsitenesnesi</span><span class="sxs-lookup"><span data-stu-id="34aed-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34aed-109">Byvirtualwanobjectbyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="34aed-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34aed-110">Byvirtualwanresourceıdbyvpnsitenesnesi</span><span class="sxs-lookup"><span data-stu-id="34aed-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34aed-111">Byvirtualwanresourceıdbyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="34aed-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34aed-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="34aed-112">DESCRIPTION</span></span>
<span data-ttu-id="34aed-113">VpnConnections aracılığıyla bu WAN 'a bağlı VpnSites alt kümesinin VPN yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="34aed-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="34aed-114">Üretilen VPN yapılandırmasını, müşterinin belirttiği bir depolama blob 'una yükler.</span><span class="sxs-lookup"><span data-stu-id="34aed-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="34aed-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34aed-115">EXAMPLES</span></span>

### <span data-ttu-id="34aed-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="34aed-116">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="34aed-117">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34aed-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="34aed-118">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34aed-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="34aed-119">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="34aed-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="34aed-120">Ardından, yapılandırma bu komutbu komutu kullanarak indirilir.</span><span class="sxs-lookup"><span data-stu-id="34aed-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="34aed-121">Komutlarıbaşarılı olursa, indirme yapılandırması SignedSasUrl tarafından gösterilen blob 'a yazılır.</span><span class="sxs-lookup"><span data-stu-id="34aed-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="34aed-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34aed-122">PARAMETERS</span></span>

### <span data-ttu-id="34aed-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34aed-123">-DefaultProfile</span></span>
<span data-ttu-id="34aed-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34aed-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34aed-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34aed-125">-InputObject</span></span>
<span data-ttu-id="34aed-126">Değiştirilecek VPN sitesi nesnesi</span><span class="sxs-lookup"><span data-stu-id="34aed-126">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteObject, ByVirtualWanObjectByVpnSiteResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34aed-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="34aed-127">-Name</span></span>
<span data-ttu-id="34aed-128">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="34aed-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aed-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34aed-129">-ResourceGroupName</span></span>
<span data-ttu-id="34aed-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="34aed-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aed-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="34aed-131">-ResourceId</span></span>
<span data-ttu-id="34aed-132">Sanal WAN için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="34aed-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34aed-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="34aed-133">-StorageSasUrl</span></span>
<span data-ttu-id="34aed-134">Yapılandırmanın oluşturulacağı depolama konumunun SAS URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="34aed-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="34aed-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="34aed-135">-VpnSite</span></span>
<span data-ttu-id="34aed-136">Yapılandırma oluşturmak için VpnSite kaynak kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="34aed-136">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite[]
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanObjectByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aed-137">-Vpnsitekimliği</span><span class="sxs-lookup"><span data-stu-id="34aed-137">-VpnSiteId</span></span>
<span data-ttu-id="34aed-138">Yapılandırma oluşturmak için VpnSite kaynak kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="34aed-138">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVirtualWanNameByVpnSiteResourceId, ByVirtualWanObjectByVpnSiteResourceId, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aed-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="34aed-139">-Confirm</span></span>
<span data-ttu-id="34aed-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34aed-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34aed-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34aed-141">-WhatIf</span></span>
<span data-ttu-id="34aed-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34aed-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34aed-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34aed-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34aed-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34aed-144">CommonParameters</span></span>
<span data-ttu-id="34aed-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34aed-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34aed-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34aed-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34aed-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34aed-147">INPUTS</span></span>

### <span data-ttu-id="34aed-148">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="34aed-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="34aed-149">System. String</span><span class="sxs-lookup"><span data-stu-id="34aed-149">System.String</span></span>

## <span data-ttu-id="34aed-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34aed-150">OUTPUTS</span></span>

### <span data-ttu-id="34aed-151">Microsoft. Azure. Commands. Network. model. Psvirtualwanvpnsitesyapılandırması</span><span class="sxs-lookup"><span data-stu-id="34aed-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="34aed-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34aed-152">NOTES</span></span>

## <span data-ttu-id="34aed-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34aed-153">RELATED LINKS</span></span>

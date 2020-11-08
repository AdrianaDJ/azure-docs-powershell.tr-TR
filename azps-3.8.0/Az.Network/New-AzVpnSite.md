---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: a459ec99852d83dcba05a3a594ee2ae4378c318c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096495"
---
# <span data-ttu-id="0c6c0-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="0c6c0-101">New-AzVpnSite</span></span>

## <span data-ttu-id="0c6c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6c0-103">Yeni bir Azure VpnSite kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="0c6c0-104">Bu, Cortex sanal hub ile S2S bağlantısı için Azure 'a yüklenen müşteri dallarının RM temsilidir.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="0c6c0-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c6c0-105">SYNTAX</span></span>

### <span data-ttu-id="0c6c0-106">Byvirtualwannamebyvpnsiteıpaddress (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c6c0-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c6c0-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="0c6c0-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c6c0-108">Byvirtualwanobjectbyvpnsiteıpaddress</span><span class="sxs-lookup"><span data-stu-id="0c6c0-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c6c0-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="0c6c0-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c6c0-110">Byvirtualwanresourceıdbyvpnsiteıpaddress</span><span class="sxs-lookup"><span data-stu-id="0c6c0-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c6c0-111">Byvirtualwanresourceıdbyvpnsitelinkobject</span><span class="sxs-lookup"><span data-stu-id="0c6c0-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c6c0-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c6c0-112">DESCRIPTION</span></span>
<span data-ttu-id="0c6c0-113">Yeni bir Azure VpnSite kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="0c6c0-114">Bu, Cortex sanal hub ile S2S bağlantısı için Azure 'a yüklenen müşteri dallarının RM temsilidir.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="0c6c0-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c6c0-115">EXAMPLES</span></span>

### <span data-ttu-id="0c6c0-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c6c0-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "nonlinkSite"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "nonlinkSite" -Name myVirtualWAN -Location "East US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "nonlinkSite" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : nonlinkSite
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="0c6c0-117">Yukarıdaki, Azure 'daki "nonlinkSite" kaynak grubunda bir kaynak grubu, Doğu ABD 'de sanal WAN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="0c6c0-118">Ardından bir müşteri dalının temsil etmesi ve sanal WAN 'a bağlandığı bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="0c6c0-119">Bu dal ve New-AzVpnConnection komutunu kullanan bir VpnGateway ile bir IPSec bağlantısı oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="0c6c0-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0c6c0-120">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "multilink"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName multilink -Name myVirtualWAN -Location "East US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "multilink" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)
```

<span data-ttu-id="0c6c0-121">Yukarıdaki, Azure 'daki "Multilink" kaynak grubunda Doğu ABD 'de 1 VpnSiteLinks 'e sahip bir kaynak grubu, sanal WAN ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

## <span data-ttu-id="0c6c0-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c6c0-122">PARAMETERS</span></span>

### <span data-ttu-id="0c6c0-123">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="0c6c0-123">-AddressSpace</span></span>
<span data-ttu-id="0c6c0-124">Sanal ağın adres önekleri.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-124">The address prefixes of the virtual network.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="0c6c0-125">-AsJob</span></span>
<span data-ttu-id="0c6c0-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0c6c0-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-127">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="0c6c0-127">-BgpAsn</span></span>
<span data-ttu-id="0c6c0-128">Bu VpnSite için BGP ASN.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-128">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-129">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="0c6c0-129">-BgpPeeringAddress</span></span>
<span data-ttu-id="0c6c0-130">Bu VpnSite için BGP eşleme adresi.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-130">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-131">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="0c6c0-131">-BgpPeeringWeight</span></span>
<span data-ttu-id="0c6c0-132">Bu VpnSite için BGP eşleme ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-132">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6c0-133">-DefaultProfile</span></span>
<span data-ttu-id="0c6c0-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c6c0-135">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="0c6c0-135">-DeviceModel</span></span>
<span data-ttu-id="0c6c0-136">Uzak VPN aygıtının aygıt modeli.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-136">The device model of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-137">-Devicevençi</span><span class="sxs-lookup"><span data-stu-id="0c6c0-137">-DeviceVendor</span></span>
<span data-ttu-id="0c6c0-138">Uzak VPN aygıtının cihaz satıcısı.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-138">The device vendor of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-139">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="0c6c0-139">-IpAddress</span></span>
<span data-ttu-id="0c6c0-140">Bu VpnSite için IPAddress.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-140">The IPAddress for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-141">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="0c6c0-141">-LinkSpeedInMbps</span></span>
<span data-ttu-id="0c6c0-142">Uzak VPN aygıtının aygıt modeli.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-142">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-143">-Konum</span><span class="sxs-lookup"><span data-stu-id="0c6c0-143">-Location</span></span>
<span data-ttu-id="0c6c0-144">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-144">The resource location.</span></span>

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

### <span data-ttu-id="0c6c0-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c6c0-145">-Name</span></span>
<span data-ttu-id="0c6c0-146">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-146">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6c0-147">-ResourceGroupName</span></span>
<span data-ttu-id="0c6c0-148">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-148">The resource name.</span></span>

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

### <span data-ttu-id="0c6c0-149">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0c6c0-149">-Tag</span></span>
<span data-ttu-id="0c6c0-150">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-150">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-151">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="0c6c0-151">-VirtualWan</span></span>
<span data-ttu-id="0c6c0-152">Bu Vpnsitesinin bağlı olduğu VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-152">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-153">-Virtualwanıd</span><span class="sxs-lookup"><span data-stu-id="0c6c0-153">-VirtualWanId</span></span>
<span data-ttu-id="0c6c0-154">Bu Vpnsitesinin bağlı olduğu RESOURCEID Virtualan.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-154">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-155">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="0c6c0-155">-VirtualWanName</span></span>
<span data-ttu-id="0c6c0-156">Bu Vpnsitesinin bağlı olması gerektiği VirtualWan adı.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-156">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-157">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6c0-157">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="0c6c0-158">Bu Vpnsitesinin bağlı olduğu VirtualWan 'ın kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-158">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-159">-Vpnsite</span><span class="sxs-lookup"><span data-stu-id="0c6c0-159">-VpnSiteLink</span></span>
<span data-ttu-id="0c6c0-160">Bu VpnSite 'in sahip olduğu VpnSiteLinks listesi.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-160">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: ByVirtualWanNameByVpnSiteLinkObject, ByVirtualWanObjectByVpnSiteLinkObject, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c0-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c6c0-161">-Confirm</span></span>
<span data-ttu-id="0c6c0-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c6c0-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c6c0-163">-WhatIf</span></span>
<span data-ttu-id="0c6c0-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c6c0-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c6c0-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6c0-166">CommonParameters</span></span>
<span data-ttu-id="0c6c0-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6c0-168">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0c6c0-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6c0-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c6c0-169">INPUTS</span></span>

### <span data-ttu-id="0c6c0-170">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0c6c0-170">None</span></span>

## <span data-ttu-id="0c6c0-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c6c0-171">OUTPUTS</span></span>

### <span data-ttu-id="0c6c0-172">Microsoft. Azure. Commands. Network. modeller. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="0c6c0-172">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="0c6c0-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c6c0-173">NOTES</span></span>

## <span data-ttu-id="0c6c0-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c6c0-174">RELATED LINKS</span></span>

[<span data-ttu-id="0c6c0-175">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="0c6c0-175">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="0c6c0-176">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="0c6c0-176">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="0c6c0-177">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="0c6c0-177">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)

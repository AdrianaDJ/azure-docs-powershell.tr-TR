---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325876"
---
# <span data-ttu-id="f0290-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f0290-101">New-AzVpnSite</span></span>

## <span data-ttu-id="f0290-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0290-102">SYNOPSIS</span></span>
<span data-ttu-id="f0290-103">Yeni bir Azure VpnSite kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0290-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="f0290-104">Bu, Cortex sanal hub ile S2S bağlantısı için Azure 'a yüklenen müşteri dallarının RM temsilidir.</span><span class="sxs-lookup"><span data-stu-id="f0290-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="f0290-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0290-105">SYNTAX</span></span>

### <span data-ttu-id="f0290-106">Byvirtualwannamebyvpnsiteıpaddress (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0290-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0290-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="f0290-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0290-108">Byvirtualwanobjectbyvpnsiteıpaddress</span><span class="sxs-lookup"><span data-stu-id="f0290-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0290-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="f0290-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0290-110">Byvirtualwanresourceıdbyvpnsiteıpaddress</span><span class="sxs-lookup"><span data-stu-id="f0290-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0290-111">Byvirtualwanresourceıdbyvpnsitelinkobject</span><span class="sxs-lookup"><span data-stu-id="f0290-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0290-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0290-112">DESCRIPTION</span></span>
<span data-ttu-id="f0290-113">Yeni bir Azure VpnSite kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0290-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="f0290-114">Bu, Cortex sanal hub ile S2S bağlantısı için Azure 'a yüklenen müşteri dallarının RM temsilidir.</span><span class="sxs-lookup"><span data-stu-id="f0290-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="f0290-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0290-115">EXAMPLES</span></span>

### <span data-ttu-id="f0290-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f0290-116">Example 1</span></span>

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

<span data-ttu-id="f0290-117">Yukarıdaki, Azure 'daki "nonlinkSite" kaynak grubunda bir kaynak grubu, Doğu ABD 'de sanal WAN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0290-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="f0290-118">Ardından bir müşteri dalının temsil etmesi ve sanal WAN 'a bağlandığı bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0290-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="f0290-119">Bu dal ve New-AzVpnConnection komutunu kullanan bir VpnGateway ile bir IPSec bağlantısı oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="f0290-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="f0290-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f0290-120">Example 2</span></span>
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

<span data-ttu-id="f0290-121">Yukarıdaki, Azure 'daki "Multilink" kaynak grubunda Doğu ABD 'de 1 VpnSiteLinks 'e sahip bir kaynak grubu, sanal WAN ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0290-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="f0290-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="f0290-122">Example 3</span></span>

<span data-ttu-id="f0290-123">Yeni bir Azure VpnSite kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0290-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="f0290-124">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="f0290-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="f0290-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0290-125">PARAMETERS</span></span>

### <span data-ttu-id="f0290-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="f0290-126">-AddressSpace</span></span>
<span data-ttu-id="f0290-127">Sanal ağın adres önekleri.</span><span class="sxs-lookup"><span data-stu-id="f0290-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="f0290-128">-Iş</span><span class="sxs-lookup"><span data-stu-id="f0290-128">-AsJob</span></span>
<span data-ttu-id="f0290-129">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f0290-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0290-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="f0290-130">-BgpAsn</span></span>
<span data-ttu-id="f0290-131">Bu VpnSite için BGP ASN.</span><span class="sxs-lookup"><span data-stu-id="f0290-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="f0290-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="f0290-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="f0290-133">Bu VpnSite için BGP eşleme adresi.</span><span class="sxs-lookup"><span data-stu-id="f0290-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="f0290-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="f0290-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="f0290-135">Bu VpnSite için BGP eşleme ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="f0290-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="f0290-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0290-136">-DefaultProfile</span></span>
<span data-ttu-id="f0290-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0290-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0290-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="f0290-138">-DeviceModel</span></span>
<span data-ttu-id="f0290-139">Uzak VPN aygıtının aygıt modeli.</span><span class="sxs-lookup"><span data-stu-id="f0290-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="f0290-140">-Devicevençi</span><span class="sxs-lookup"><span data-stu-id="f0290-140">-DeviceVendor</span></span>
<span data-ttu-id="f0290-141">Uzak VPN aygıtının cihaz satıcısı.</span><span class="sxs-lookup"><span data-stu-id="f0290-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="f0290-142">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="f0290-142">-IpAddress</span></span>
<span data-ttu-id="f0290-143">Bu VpnSite için IPAddress.</span><span class="sxs-lookup"><span data-stu-id="f0290-143">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="f0290-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="f0290-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="f0290-145">Uzak VPN aygıtının aygıt modeli.</span><span class="sxs-lookup"><span data-stu-id="f0290-145">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="f0290-146">-Konum</span><span class="sxs-lookup"><span data-stu-id="f0290-146">-Location</span></span>
<span data-ttu-id="f0290-147">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="f0290-147">The resource location.</span></span>

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

### <span data-ttu-id="f0290-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0290-148">-Name</span></span>
<span data-ttu-id="f0290-149">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f0290-149">The resource name.</span></span>

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

### <span data-ttu-id="f0290-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="f0290-150">-O365Policy</span></span>
<span data-ttu-id="f0290-151">Bu VpnSite için Office 365 trafiği ayırıcı ilkesi.</span><span class="sxs-lookup"><span data-stu-id="f0290-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0290-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0290-152">-ResourceGroupName</span></span>
<span data-ttu-id="f0290-153">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f0290-153">The resource name.</span></span>

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

### <span data-ttu-id="f0290-154">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f0290-154">-Tag</span></span>
<span data-ttu-id="f0290-155">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="f0290-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f0290-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="f0290-156">-VirtualWan</span></span>
<span data-ttu-id="f0290-157">Bu Vpnsitesinin bağlı olduğu VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f0290-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="f0290-158">-Virtualwanıd</span><span class="sxs-lookup"><span data-stu-id="f0290-158">-VirtualWanId</span></span>
<span data-ttu-id="f0290-159">Bu Vpnsitesinin bağlı olduğu RESOURCEID Virtualan.</span><span class="sxs-lookup"><span data-stu-id="f0290-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="f0290-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="f0290-160">-VirtualWanName</span></span>
<span data-ttu-id="f0290-161">Bu Vpnsitesinin bağlı olması gerektiği VirtualWan adı.</span><span class="sxs-lookup"><span data-stu-id="f0290-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="f0290-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0290-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="f0290-163">Bu Vpnsitesinin bağlı olduğu VirtualWan 'ın kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f0290-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="f0290-164">-Vpnsite</span><span class="sxs-lookup"><span data-stu-id="f0290-164">-VpnSiteLink</span></span>
<span data-ttu-id="f0290-165">Bu VpnSite 'in sahip olduğu VpnSiteLinks listesi.</span><span class="sxs-lookup"><span data-stu-id="f0290-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="f0290-166">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0290-166">-Confirm</span></span>
<span data-ttu-id="f0290-167">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0290-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0290-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0290-168">-WhatIf</span></span>
<span data-ttu-id="f0290-169">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0290-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0290-170">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0290-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0290-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0290-171">CommonParameters</span></span>
<span data-ttu-id="f0290-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0290-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0290-173">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f0290-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0290-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0290-174">INPUTS</span></span>

### <span data-ttu-id="f0290-175">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f0290-175">None</span></span>

## <span data-ttu-id="f0290-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0290-176">OUTPUTS</span></span>

### <span data-ttu-id="f0290-177">Microsoft. Azure. Commands. Network. modeller. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="f0290-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="f0290-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0290-178">NOTES</span></span>

## <span data-ttu-id="f0290-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0290-179">RELATED LINKS</span></span>

[<span data-ttu-id="f0290-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f0290-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="f0290-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f0290-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="f0290-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f0290-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: 239a09435c7410ef948503d7f4b31cd60943ce59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932683"
---
# <span data-ttu-id="e7ad2-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e7ad2-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="e7ad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ad2-103">VPN sitesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-103">Updates a VPN site.</span></span>

## <span data-ttu-id="e7ad2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7ad2-104">SYNTAX</span></span>

### <span data-ttu-id="e7ad2-105">ByVpnSiteNameNoVirtualWanUpdate (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7ad2-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7ad2-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="e7ad2-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7ad2-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ad2-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ad2-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="e7ad2-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ad2-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="e7ad2-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7ad2-110">Byvpnsiteobjectbyvirtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="e7ad2-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ad2-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="e7ad2-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ad2-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="e7ad2-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7ad2-113">Byvpnsiteresourceıdbyvirtualwanname</span><span class="sxs-lookup"><span data-stu-id="e7ad2-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7ad2-114">Byvpnsiteresourceıdbyvirtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="e7ad2-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7ad2-115">Byvpnsiteresourceıdbyvirtualwanobject</span><span class="sxs-lookup"><span data-stu-id="e7ad2-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ad2-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="e7ad2-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7ad2-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7ad2-117">DESCRIPTION</span></span>
<span data-ttu-id="e7ad2-118">**Update-AzVpnSite** cmdlet 'ı bir VPN sitesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="e7ad2-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7ad2-119">EXAMPLES</span></span>

### <span data-ttu-id="e7ad2-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7ad2-120">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 2.3.4.5
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="e7ad2-121">Yukarıdaki, Azure 'daki "testRG" kaynak grubundaki Batı</span><span class="sxs-lookup"><span data-stu-id="e7ad2-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="e7ad2-122">Ardından bir müşteri dalının temsil etmesi ve sanal WAN 'a bağlandığı bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="e7ad2-123">Site oluşturulduktan sonra, Set-AzVpnSite komutunu kullanarak sitenin IPAddress 'i güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="e7ad2-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7ad2-124">PARAMETERS</span></span>

### <span data-ttu-id="e7ad2-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="e7ad2-125">-AddressSpace</span></span>
<span data-ttu-id="e7ad2-126">Sanal ağın adres önekleri.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="e7ad2-127">Bu veya AddressSpaceObject kullanın ancak ikisini birden kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="e7ad2-128">-Iş</span><span class="sxs-lookup"><span data-stu-id="e7ad2-128">-AsJob</span></span>
<span data-ttu-id="e7ad2-129">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e7ad2-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7ad2-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="e7ad2-130">-BgpAsn</span></span>
<span data-ttu-id="e7ad2-131">Bu VpnSite için BGP ASN.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e7ad2-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="e7ad2-133">Bu VpnSite için BGP eşleme adresi.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="e7ad2-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="e7ad2-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="e7ad2-135">Bu VpnSite için BGP eşleme ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ad2-136">-DefaultProfile</span></span>
<span data-ttu-id="e7ad2-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7ad2-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="e7ad2-138">-DeviceModel</span></span>
<span data-ttu-id="e7ad2-139">Uzak VPN aygıtının aygıt modeli.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="e7ad2-140">-Devicevençi</span><span class="sxs-lookup"><span data-stu-id="e7ad2-140">-DeviceVendor</span></span>
<span data-ttu-id="e7ad2-141">Uzak VPN aygıtının cihaz satıcısı.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="e7ad2-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7ad2-142">-InputObject</span></span>
<span data-ttu-id="e7ad2-143">Değiştirilecek VPN sitesi nesnesi</span><span class="sxs-lookup"><span data-stu-id="e7ad2-143">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObjectByVirtualWanName, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteObjectNoVirtualWanUpdate
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-144">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="e7ad2-144">-IpAddress</span></span>
<span data-ttu-id="e7ad2-145">Yerel ağ geçidinin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="e7ad2-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="e7ad2-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="e7ad2-147">Uzak VPN aygıtının aygıt modeli.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-147">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7ad2-148">-Name</span></span>
<span data-ttu-id="e7ad2-149">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7ad2-150">-ResourceGroupName</span></span>
<span data-ttu-id="e7ad2-151">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-151">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e7ad2-152">-ResourceId</span></span>
<span data-ttu-id="e7ad2-153">VPN sitesinin Azure Resource ID 'si.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-153">The Azure resource ID for the vpn site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceIdByVirtualWanName, ByVpnSiteResourceIdByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanObject, ByVpnSiteResourceIdNoVirtualWanUpdate
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-154">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e7ad2-154">-Tag</span></span>
<span data-ttu-id="e7ad2-155">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e7ad2-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="e7ad2-156">-VirtualWan</span></span>
<span data-ttu-id="e7ad2-157">Bu Vpnsitesinin bağlı olduğu VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVpnSiteNameByVirtualWanObject, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteResourceIdByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-158">-Virtualwanıd</span><span class="sxs-lookup"><span data-stu-id="e7ad2-158">-VirtualWanId</span></span>
<span data-ttu-id="e7ad2-159">Bu Vpnsitesinin bağlı olduğu RESOURCEID Virtualan.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="e7ad2-160">-VirtualWanName</span></span>
<span data-ttu-id="e7ad2-161">Bu Vpnsitesinin bağlı olması gerektiği VirtualWan adı.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7ad2-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="e7ad2-163">Bu Vpnsitesinin bağlı olduğu VirtualWan 'ın kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-164">-Vpnsite</span><span class="sxs-lookup"><span data-stu-id="e7ad2-164">-VpnSiteLink</span></span>
<span data-ttu-id="e7ad2-165">Bu VpnSite 'in sahip olduğu VpnSiteLinks listesi.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-166">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7ad2-166">-Confirm</span></span>
<span data-ttu-id="e7ad2-167">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7ad2-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7ad2-168">-WhatIf</span></span>
<span data-ttu-id="e7ad2-169">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7ad2-170">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7ad2-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ad2-171">CommonParameters</span></span>
<span data-ttu-id="e7ad2-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ad2-173">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-173">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ad2-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7ad2-174">INPUTS</span></span>

### <span data-ttu-id="e7ad2-175">Microsoft. Azure. Commands. Network. modeller. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="e7ad2-175">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="e7ad2-176">System. String</span><span class="sxs-lookup"><span data-stu-id="e7ad2-176">System.String</span></span>

## <span data-ttu-id="e7ad2-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7ad2-177">OUTPUTS</span></span>

### <span data-ttu-id="e7ad2-178">Microsoft. Azure. Commands. Network. modeller. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="e7ad2-178">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="e7ad2-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7ad2-179">NOTES</span></span>

## <span data-ttu-id="e7ad2-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7ad2-180">RELATED LINKS</span></span>

[<span data-ttu-id="e7ad2-181">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e7ad2-181">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="e7ad2-182">Yeni-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e7ad2-182">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="e7ad2-183">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e7ad2-183">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

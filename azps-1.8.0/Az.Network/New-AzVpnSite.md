---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 980b84fd1b23cb7e4b034dee485b785b96893f11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760237"
---
# <span data-ttu-id="8501f-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8501f-101">New-AzVpnSite</span></span>

## <span data-ttu-id="8501f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8501f-102">SYNOPSIS</span></span>
<span data-ttu-id="8501f-103">Yeni bir Azure VpnSite kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8501f-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="8501f-104">Bu, Cortex sanal hub ile S2S bağlantısı için Azure 'a yüklenen müşteri dallarının RM temsilidir.</span><span class="sxs-lookup"><span data-stu-id="8501f-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="8501f-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8501f-105">SYNTAX</span></span>

### <span data-ttu-id="8501f-106">ByVirtualWanName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8501f-106">ByVirtualWanName (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8501f-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="8501f-107">ByVirtualWanObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8501f-108">İ Virtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="8501f-108">ByVirtualWanResourceId</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8501f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="8501f-109">DESCRIPTION</span></span>
<span data-ttu-id="8501f-110">Yeni bir Azure VpnSite kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8501f-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="8501f-111">Bu, Cortex sanal hub ile S2S bağlantısı için Azure 'a yüklenen müşteri dallarının RM temsilidir.</span><span class="sxs-lookup"><span data-stu-id="8501f-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="8501f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8501f-112">EXAMPLES</span></span>

### <span data-ttu-id="8501f-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8501f-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="8501f-114">Yukarıdaki, Azure 'daki "testRG" kaynak grubundaki Batı</span><span class="sxs-lookup"><span data-stu-id="8501f-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="8501f-115">Ardından bir müşteri dalının temsil etmesi ve sanal WAN 'a bağlandığı bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8501f-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="8501f-116">Bu dal ve New-AzVpnConnection komutunu kullanan bir VpnGateway ile bir IPSec bağlantısı oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="8501f-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="8501f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8501f-117">PARAMETERS</span></span>

### <span data-ttu-id="8501f-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="8501f-118">-AddressSpace</span></span>
<span data-ttu-id="8501f-119">Sanal ağın adres önekleri.</span><span class="sxs-lookup"><span data-stu-id="8501f-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="8501f-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="8501f-120">-AsJob</span></span>
<span data-ttu-id="8501f-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8501f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8501f-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="8501f-122">-BgpAsn</span></span>
<span data-ttu-id="8501f-123">Bu VpnSite için BGP ASN.</span><span class="sxs-lookup"><span data-stu-id="8501f-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="8501f-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="8501f-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="8501f-125">Bu VpnSite için BGP eşleme adresi.</span><span class="sxs-lookup"><span data-stu-id="8501f-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="8501f-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="8501f-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="8501f-127">Bu VpnSite için BGP eşleme ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="8501f-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="8501f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8501f-128">-DefaultProfile</span></span>
<span data-ttu-id="8501f-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8501f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8501f-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="8501f-130">-DeviceModel</span></span>
<span data-ttu-id="8501f-131">Uzak VPN aygıtının aygıt modeli.</span><span class="sxs-lookup"><span data-stu-id="8501f-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="8501f-132">-Devicevençi</span><span class="sxs-lookup"><span data-stu-id="8501f-132">-DeviceVendor</span></span>
<span data-ttu-id="8501f-133">Uzak VPN aygıtının cihaz satıcısı.</span><span class="sxs-lookup"><span data-stu-id="8501f-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="8501f-134">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="8501f-134">-IpAddress</span></span>
<span data-ttu-id="8501f-135">Bu VpnSite için IPAddress.</span><span class="sxs-lookup"><span data-stu-id="8501f-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="8501f-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="8501f-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="8501f-137">Uzak VPN aygıtının aygıt modeli.</span><span class="sxs-lookup"><span data-stu-id="8501f-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="8501f-138">-Konum</span><span class="sxs-lookup"><span data-stu-id="8501f-138">-Location</span></span>
<span data-ttu-id="8501f-139">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="8501f-139">The resource location.</span></span>

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

### <span data-ttu-id="8501f-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="8501f-140">-Name</span></span>
<span data-ttu-id="8501f-141">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8501f-141">The resource name.</span></span>

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

### <span data-ttu-id="8501f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8501f-142">-ResourceGroupName</span></span>
<span data-ttu-id="8501f-143">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8501f-143">The resource name.</span></span>

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

### <span data-ttu-id="8501f-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8501f-144">-Tag</span></span>
<span data-ttu-id="8501f-145">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="8501f-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8501f-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="8501f-146">-VirtualWan</span></span>
<span data-ttu-id="8501f-147">Bu Vpnsitesinin bağlı olduğu VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="8501f-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8501f-148">-Virtualwanıd</span><span class="sxs-lookup"><span data-stu-id="8501f-148">-VirtualWanId</span></span>
<span data-ttu-id="8501f-149">Bu Vpnsitesinin bağlı olduğu RESOURCEID Virtualan.</span><span class="sxs-lookup"><span data-stu-id="8501f-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8501f-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="8501f-150">-VirtualWanName</span></span>
<span data-ttu-id="8501f-151">Bu Vpnsitesinin bağlı olması gerektiği VirtualWan adı.</span><span class="sxs-lookup"><span data-stu-id="8501f-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8501f-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8501f-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="8501f-153">Bu Vpnsitesinin bağlı olduğu VirtualWan 'ın kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8501f-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8501f-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="8501f-154">-Confirm</span></span>
<span data-ttu-id="8501f-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8501f-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8501f-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8501f-156">-WhatIf</span></span>
<span data-ttu-id="8501f-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8501f-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8501f-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8501f-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8501f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8501f-159">CommonParameters</span></span>
<span data-ttu-id="8501f-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8501f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8501f-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8501f-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8501f-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8501f-162">INPUTS</span></span>

### <span data-ttu-id="8501f-163">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8501f-163">None</span></span>

## <span data-ttu-id="8501f-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8501f-164">OUTPUTS</span></span>

### <span data-ttu-id="8501f-165">Microsoft. Azure. Commands. Network. modeller. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="8501f-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="8501f-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8501f-166">NOTES</span></span>

## <span data-ttu-id="8501f-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8501f-167">RELATED LINKS</span></span>

[<span data-ttu-id="8501f-168">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8501f-168">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="8501f-169">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8501f-169">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="8501f-170">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="8501f-170">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)

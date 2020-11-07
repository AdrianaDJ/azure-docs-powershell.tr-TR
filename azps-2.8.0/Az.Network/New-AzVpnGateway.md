---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 08915aaf72fbab91d8173480f4e608ebdbaa28ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918144"
---
# <span data-ttu-id="e1395-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e1395-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="e1395-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1395-102">SYNOPSIS</span></span>
<span data-ttu-id="e1395-103">Ölçeklenebilir bir VPN ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1395-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="e1395-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1395-104">SYNTAX</span></span>

### <span data-ttu-id="e1395-105">ByVirtualHubName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e1395-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1395-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e1395-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1395-107">Byvirtualhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="e1395-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1395-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1395-108">DESCRIPTION</span></span>

<span data-ttu-id="e1395-109">New-AzVpnGateway ölçeklenebilir bir VPN ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1395-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="e1395-110">Bu, VirtualHub içindeki site bağlantılarına site için tanımlanmış yazılımdır.</span><span class="sxs-lookup"><span data-stu-id="e1395-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="e1395-111">Bu ağ geçidi, bu veya Set-AzVpnGateway cmdlet 'inde belirtilen ölçek birimine göre yeniden boyutlandırır ve ölçekler.</span><span class="sxs-lookup"><span data-stu-id="e1395-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="e1395-112">Bir bağlantı, VPNSite olarak bilinen bir daldan/siteden ölçeklenebilir ağ geçidine ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e1395-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="e1395-113">Her bağlantı 2 Active-Active tünelden oluşur.</span><span class="sxs-lookup"><span data-stu-id="e1395-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="e1395-114">VpnGateway, başvurulan VirtualHub ile aynı konumda olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1395-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="e1395-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1395-115">EXAMPLES</span></span>

### <span data-ttu-id="e1395-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e1395-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="e1395-117">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda bir kaynak grubu, sanal WAN, sanal ağ, Batı ABD 'deki sanal hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1395-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e1395-118">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e1395-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="e1395-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1395-119">PARAMETERS</span></span>

### <span data-ttu-id="e1395-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="e1395-120">-AsJob</span></span>
<span data-ttu-id="e1395-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e1395-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1395-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1395-122">-DefaultProfile</span></span>
<span data-ttu-id="e1395-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1395-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1395-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e1395-124">-Name</span></span>
<span data-ttu-id="e1395-125">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e1395-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1395-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1395-126">-ResourceGroupName</span></span>
<span data-ttu-id="e1395-127">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e1395-127">The resource name.</span></span>

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

### <span data-ttu-id="e1395-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e1395-128">-Tag</span></span>
<span data-ttu-id="e1395-129">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="e1395-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e1395-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="e1395-130">-VirtualHub</span></span>
<span data-ttu-id="e1395-131">Bu VpnGateway 'in VirtualHub 'ı ile ilişkilendirilmesi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e1395-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1395-132">-Virtualhubıd</span><span class="sxs-lookup"><span data-stu-id="e1395-132">-VirtualHubId</span></span>
<span data-ttu-id="e1395-133">Bu VpnGateway 'in ilişkilendirildiği VirtualHub kimliği.</span><span class="sxs-lookup"><span data-stu-id="e1395-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1395-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="e1395-134">-VirtualHubName</span></span>
<span data-ttu-id="e1395-135">Bu VpnGateway 'in ilişkilendirildiği VirtualHub kimliği.</span><span class="sxs-lookup"><span data-stu-id="e1395-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1395-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e1395-136">-VpnConnection</span></span>
<span data-ttu-id="e1395-137">Bu VpnGateway 'in sahip olduğu VpnConnections listesi.</span><span class="sxs-lookup"><span data-stu-id="e1395-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1395-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e1395-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="e1395-139">Bu VpnGateway 'in ölçek birimi.</span><span class="sxs-lookup"><span data-stu-id="e1395-139">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1395-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="e1395-140">-Confirm</span></span>
<span data-ttu-id="e1395-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e1395-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1395-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1395-142">-WhatIf</span></span>
<span data-ttu-id="e1395-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1395-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1395-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e1395-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1395-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1395-145">CommonParameters</span></span>
<span data-ttu-id="e1395-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1395-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1395-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1395-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1395-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1395-148">INPUTS</span></span>

### <span data-ttu-id="e1395-149">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e1395-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="e1395-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e1395-150">System.String</span></span>

## <span data-ttu-id="e1395-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1395-151">OUTPUTS</span></span>

### <span data-ttu-id="e1395-152">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e1395-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="e1395-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1395-153">NOTES</span></span>

## <span data-ttu-id="e1395-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1395-154">RELATED LINKS</span></span>

[<span data-ttu-id="e1395-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e1395-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="e1395-156">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e1395-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="e1395-157">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e1395-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)

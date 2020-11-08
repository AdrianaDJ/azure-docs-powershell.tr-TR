---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 8db43fc826086235a51f32e67a8f787a3ac5792d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097249"
---
# <span data-ttu-id="feb7f-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="feb7f-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="feb7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feb7f-102">SYNOPSIS</span></span>
<span data-ttu-id="feb7f-103">Ölçeklenebilir bir VPN ağ geçidi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="feb7f-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="feb7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="feb7f-104">SYNTAX</span></span>

### <span data-ttu-id="feb7f-105">ByVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="feb7f-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb7f-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="feb7f-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb7f-107">Byvpngatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="feb7f-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="feb7f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="feb7f-108">DESCRIPTION</span></span>
<span data-ttu-id="feb7f-109">**Update-AzVpnGateway** cmdlet 'i ÖLÇEKLENEBILIR bir VPN ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="feb7f-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="feb7f-110">Azure VPN ağ geçidi, VirtualHub içindeki site bağlantılarına site için tanımlanmış bir yazılımdır.</span><span class="sxs-lookup"><span data-stu-id="feb7f-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="feb7f-111">Bu ağ geçidi, Kullanıcı tarafından belirtilen ölçek birimine göre yeniden boyutlandırır ve ölçekler.</span><span class="sxs-lookup"><span data-stu-id="feb7f-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="feb7f-112">VPN sitesi olarak bilinen bir daldan/siteden ölçeklenebilir ağ geçidine bağlantı oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="feb7f-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="feb7f-113">Her bağlantı 2 Active-Active tünelden oluşur</span><span class="sxs-lookup"><span data-stu-id="feb7f-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="feb7f-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="feb7f-114">EXAMPLES</span></span>

### <span data-ttu-id="feb7f-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="feb7f-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="feb7f-116">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda bir kaynak grubu, sanal WAN, sanal ağ, Batı ABD 'deki sanal hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="feb7f-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="feb7f-117">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="feb7f-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="feb7f-118">Ağ Geçidi oluşturulduktan sonra, ağ geçidini 3 ölçekli birimlere güncellemek için Set-AzVpnGateway kullanır.</span><span class="sxs-lookup"><span data-stu-id="feb7f-118">After the gateway has been created, it uses Set-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="feb7f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="feb7f-119">PARAMETERS</span></span>

### <span data-ttu-id="feb7f-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="feb7f-120">-AsJob</span></span>
<span data-ttu-id="feb7f-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="feb7f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="feb7f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb7f-122">-DefaultProfile</span></span>
<span data-ttu-id="feb7f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="feb7f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feb7f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feb7f-124">-InputObject</span></span>
<span data-ttu-id="feb7f-125">Değiştirilecek VPN ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="feb7f-125">The vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="feb7f-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="feb7f-126">-Name</span></span>
<span data-ttu-id="feb7f-127">Sanal WAN adı.</span><span class="sxs-lookup"><span data-stu-id="feb7f-127">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb7f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb7f-128">-ResourceGroupName</span></span>
<span data-ttu-id="feb7f-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="feb7f-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb7f-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="feb7f-130">-ResourceId</span></span>
<span data-ttu-id="feb7f-131">Değiştirilecek Vpnağ geçidinin Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="feb7f-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb7f-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="feb7f-132">-Tag</span></span>
<span data-ttu-id="feb7f-133">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="feb7f-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="feb7f-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="feb7f-134">-VpnConnection</span></span>
<span data-ttu-id="feb7f-135">Bu VpnGateway 'in sahip olduğu VpnConnections listesi.</span><span class="sxs-lookup"><span data-stu-id="feb7f-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="feb7f-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="feb7f-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="feb7f-137">Bu VpnGateway 'in ölçek birimi.</span><span class="sxs-lookup"><span data-stu-id="feb7f-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="feb7f-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="feb7f-138">-Confirm</span></span>
<span data-ttu-id="feb7f-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="feb7f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feb7f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feb7f-140">-WhatIf</span></span>
<span data-ttu-id="feb7f-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="feb7f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feb7f-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="feb7f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feb7f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb7f-143">CommonParameters</span></span>
<span data-ttu-id="feb7f-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="feb7f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb7f-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feb7f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb7f-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="feb7f-146">INPUTS</span></span>

### <span data-ttu-id="feb7f-147">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="feb7f-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="feb7f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="feb7f-148">System.String</span></span>

## <span data-ttu-id="feb7f-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="feb7f-149">OUTPUTS</span></span>

### <span data-ttu-id="feb7f-150">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="feb7f-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="feb7f-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="feb7f-151">NOTES</span></span>

## <span data-ttu-id="feb7f-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="feb7f-152">RELATED LINKS</span></span>

[<span data-ttu-id="feb7f-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="feb7f-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="feb7f-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="feb7f-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="feb7f-155">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="feb7f-155">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

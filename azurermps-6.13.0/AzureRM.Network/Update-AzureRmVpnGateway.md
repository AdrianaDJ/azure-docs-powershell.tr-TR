---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
ms.openlocfilehash: 00730f6e252373eebbbbc476fdd889b2eeb39e12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762912"
---
# <span data-ttu-id="ed0b4-101">Update-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ed0b4-101">Update-AzureRmVpnGateway</span></span>

## <span data-ttu-id="ed0b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed0b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0b4-103">Update-AzureRmVpnGateway uygun hedef durumuna ölçeklenebilir bir VPN ağ geçidi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-103">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed0b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed0b4-104">SYNTAX</span></span>

### <span data-ttu-id="ed0b4-105">ByVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed0b4-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed0b4-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ed0b4-106">ByVpnGatewayObject</span></span>
```
Update-AzureRmVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed0b4-107">Byvpngatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="ed0b4-107">ByVpnGatewayResourceId</span></span>
```
Update-AzureRmVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed0b4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed0b4-108">DESCRIPTION</span></span>
<span data-ttu-id="ed0b4-109">Update-AzureRmVpnGateway uygun hedef durumuna ölçeklenebilir bir VPN ağ geçidi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-109">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span> <span data-ttu-id="ed0b4-110">AzureRmVpnGateway, VirtualHub içindeki site bağlantılarına site için tanımlanmış bir yazılımdır.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-110">An AzureRmVpnGateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="ed0b4-111">Bu ağ geçidi, Kullanıcı tarafından belirtilen ölçek birimine göre yeniden boyutlandırır ve ölçekler.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="ed0b4-112">Bağlantı, VPNSite olarak bilinen bir daldan/siteden ölçeklenebilir ağ geçidine yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-112">A connection can be set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="ed0b4-113">Her bağlantı 2 Active-Active tünelden oluşur</span><span class="sxs-lookup"><span data-stu-id="ed0b4-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="ed0b4-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed0b4-114">EXAMPLES</span></span>

### <span data-ttu-id="ed0b4-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed0b4-115">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

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

<span data-ttu-id="ed0b4-116">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda bir kaynak grubu, sanal WAN, sanal ağ, Batı ABD 'deki sanal hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ed0b4-117">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="ed0b4-118">Ağ Geçidi oluşturulduktan sonra, ağ geçidini 3 ölçekli birimlere güncellemek için Set-AzureRmVpnGateway kullanır.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-118">After the gateway has been created, it uses Set-AzureRmVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="ed0b4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed0b4-119">PARAMETERS</span></span>

### <span data-ttu-id="ed0b4-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="ed0b4-120">-AsJob</span></span>
<span data-ttu-id="ed0b4-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ed0b4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed0b4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0b4-122">-DefaultProfile</span></span>
<span data-ttu-id="ed0b4-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed0b4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed0b4-124">-InputObject</span></span>
<span data-ttu-id="ed0b4-125">Değiştirilecek VPN ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="ed0b4-125">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="ed0b4-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed0b4-126">-Name</span></span>
<span data-ttu-id="ed0b4-127">Sanal WAN adı.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-127">The virtual wan name.</span></span>

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

### <span data-ttu-id="ed0b4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed0b4-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed0b4-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-129">The resource group name.</span></span>

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

### <span data-ttu-id="ed0b4-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ed0b4-130">-ResourceId</span></span>
<span data-ttu-id="ed0b4-131">Değiştirilecek Vpnağ geçidinin Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="ed0b4-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ed0b4-132">-Tag</span></span>
<span data-ttu-id="ed0b4-133">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ed0b4-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ed0b4-134">-VpnConnection</span></span>
<span data-ttu-id="ed0b4-135">Bu VpnGateway 'in sahip olduğu VpnConnections listesi.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="ed0b4-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="ed0b4-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="ed0b4-137">Bu VpnGateway 'in ölçek birimi.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="ed0b4-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed0b4-138">-Confirm</span></span>
<span data-ttu-id="ed0b4-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed0b4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed0b4-140">-WhatIf</span></span>
<span data-ttu-id="ed0b4-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed0b4-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed0b4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0b4-143">CommonParameters</span></span>
<span data-ttu-id="ed0b4-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed0b4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0b4-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed0b4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0b4-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed0b4-146">INPUTS</span></span>

### <span data-ttu-id="ed0b4-147">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ed0b4-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="ed0b4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ed0b4-148">System.String</span></span>

## <span data-ttu-id="ed0b4-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed0b4-149">OUTPUTS</span></span>

### <span data-ttu-id="ed0b4-150">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ed0b4-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="ed0b4-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed0b4-151">NOTES</span></span>

## <span data-ttu-id="ed0b4-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed0b4-152">RELATED LINKS</span></span>

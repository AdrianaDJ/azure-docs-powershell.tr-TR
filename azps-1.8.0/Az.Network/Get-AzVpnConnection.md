---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: f8fa769e02241c58108621a10c19fa9536da0e82
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760446"
---
# <span data-ttu-id="15178-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="15178-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="15178-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15178-102">SYNOPSIS</span></span>
<span data-ttu-id="15178-103">VPN bağlantısını adıyla alır veya bir VpnGateway 'e bağlı tüm VPN bağlantılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="15178-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="15178-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15178-104">SYNTAX</span></span>

### <span data-ttu-id="15178-105">ByVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="15178-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15178-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="15178-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15178-107">Byvpngatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="15178-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15178-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="15178-108">DESCRIPTION</span></span>
<span data-ttu-id="15178-109">VPN bağlantısını adıyla alır veya bir VpnGateway 'e bağlı tüm VPN bağlantılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="15178-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="15178-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15178-110">EXAMPLES</span></span>

### <span data-ttu-id="15178-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="15178-111">Example 1</span></span>

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
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="15178-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15178-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="15178-113">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="15178-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="15178-114">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="15178-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="15178-115">Ardından bağlantı adını kullanarak bağlantıyı alır.</span><span class="sxs-lookup"><span data-stu-id="15178-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="15178-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="15178-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
```

<span data-ttu-id="15178-117">Bu cmdlet, "test" ile başlayan tüm bağlantıları alır.</span><span class="sxs-lookup"><span data-stu-id="15178-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="15178-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15178-118">PARAMETERS</span></span>

### <span data-ttu-id="15178-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15178-119">-DefaultProfile</span></span>
<span data-ttu-id="15178-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15178-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15178-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="15178-121">-Name</span></span>
<span data-ttu-id="15178-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="15178-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="15178-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="15178-123">-ParentObject</span></span>
<span data-ttu-id="15178-124">Bu bağlantı için üst VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="15178-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15178-125">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="15178-125">-ParentResourceId</span></span>
<span data-ttu-id="15178-126">Bu bağlantı için üst VpnGateway 'in kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="15178-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15178-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="15178-127">-ParentResourceName</span></span>
<span data-ttu-id="15178-128">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="15178-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15178-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15178-129">-ResourceGroupName</span></span>
<span data-ttu-id="15178-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="15178-130">The resource group name.</span></span>

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

### <span data-ttu-id="15178-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15178-131">CommonParameters</span></span>
<span data-ttu-id="15178-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15178-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15178-133">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15178-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15178-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15178-134">INPUTS</span></span>

### <span data-ttu-id="15178-135">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="15178-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="15178-136">System. String</span><span class="sxs-lookup"><span data-stu-id="15178-136">System.String</span></span>

## <span data-ttu-id="15178-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15178-137">OUTPUTS</span></span>

### <span data-ttu-id="15178-138">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="15178-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="15178-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15178-139">NOTES</span></span>

## <span data-ttu-id="15178-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15178-140">RELATED LINKS</span></span>

[<span data-ttu-id="15178-141">Yeni-Azvpnbağlantısı</span><span class="sxs-lookup"><span data-stu-id="15178-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="15178-142">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="15178-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="15178-143">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="15178-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
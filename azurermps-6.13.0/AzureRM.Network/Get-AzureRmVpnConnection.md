---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnConnection.md
ms.openlocfilehash: 7f4ba2cf4a57eedea41eccb8d5846129a80414d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589478"
---
# <span data-ttu-id="f699b-101">Get-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f699b-101">Get-AzureRmVpnConnection</span></span>

## <span data-ttu-id="f699b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f699b-102">SYNOPSIS</span></span>
<span data-ttu-id="f699b-103">VPN bağlantısını adıyla alır veya bir VpnGateway 'e bağlı tüm VPN bağlantılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="f699b-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f699b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f699b-104">SYNTAX</span></span>

### <span data-ttu-id="f699b-105">ByVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f699b-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f699b-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="f699b-106">ByVpnGatewayObject</span></span>
```
Get-AzureRmVpnConnection -ParentObject <PSVpnGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f699b-107">Byvpngatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="f699b-107">ByVpnGatewayResourceId</span></span>
```
Get-AzureRmVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f699b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f699b-108">DESCRIPTION</span></span>
<span data-ttu-id="f699b-109">VPN bağlantısını adıyla alır veya bir VpnGateway 'e bağlı tüm VPN bağlantılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="f699b-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="f699b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f699b-110">EXAMPLES</span></span>

### <span data-ttu-id="f699b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f699b-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

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
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="f699b-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f699b-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="f699b-113">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f699b-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="f699b-114">Ağ Geçidi oluşturulduktan sonra, New-AzureRmVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="f699b-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="f699b-115">Ardından bağlantı adını kullanarak bağlantıyı alır.</span><span class="sxs-lookup"><span data-stu-id="f699b-115">Then it gets the connection using the connection name.</span></span>

## <span data-ttu-id="f699b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f699b-116">PARAMETERS</span></span>

### <span data-ttu-id="f699b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f699b-117">-DefaultProfile</span></span>
<span data-ttu-id="f699b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f699b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f699b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="f699b-119">-Name</span></span>
<span data-ttu-id="f699b-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f699b-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f699b-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f699b-121">-ParentObject</span></span>
<span data-ttu-id="f699b-122">Bu bağlantı için üst VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f699b-122">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="f699b-123">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="f699b-123">-ParentResourceId</span></span>
<span data-ttu-id="f699b-124">Bu bağlantı için üst VpnGateway 'in kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f699b-124">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="f699b-125">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f699b-125">-ParentResourceName</span></span>
<span data-ttu-id="f699b-126">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f699b-126">The parent resource name.</span></span>

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

### <span data-ttu-id="f699b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f699b-127">-ResourceGroupName</span></span>
<span data-ttu-id="f699b-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f699b-128">The resource group name.</span></span>

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

### <span data-ttu-id="f699b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f699b-129">CommonParameters</span></span>
<span data-ttu-id="f699b-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f699b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f699b-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f699b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f699b-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f699b-132">INPUTS</span></span>

### <span data-ttu-id="f699b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f699b-133">System.String</span></span>

## <span data-ttu-id="f699b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f699b-134">OUTPUTS</span></span>

### <span data-ttu-id="f699b-135">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f699b-135">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="f699b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f699b-136">NOTES</span></span>

## <span data-ttu-id="f699b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f699b-137">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095842"
---
# <span data-ttu-id="3c986-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="3c986-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="3c986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c986-102">SYNOPSIS</span></span>
<span data-ttu-id="3c986-103">P2SVpnGateway adresinden site bağlantılarının sistem durumu bilgilerine sahip olan geçerli bir işaret alır.</span><span class="sxs-lookup"><span data-stu-id="3c986-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="3c986-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c986-104">SYNTAX</span></span>

### <span data-ttu-id="3c986-105">ByP2SVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3c986-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c986-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="3c986-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c986-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="3c986-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c986-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c986-108">DESCRIPTION</span></span>
<span data-ttu-id="3c986-109">**Get-AzP2sVpnGatewayConnectionHealth** cmdlet 'i P2SVpnGateway 'dan site bağlantılarına işaret eden geçerli toplu durumu almanızı olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="3c986-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="3c986-110">Toplu sağlık P2SVpnGateway 'e bağlı olan site istemcilerinin, P2SVpnGateway ve ayrılan IP adresleri aracılığıyla site istemcilerine bağlı noktaya giden toplam bayt ve çıkış baytlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c986-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="3c986-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c986-111">EXAMPLES</span></span>

### <span data-ttu-id="3c986-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3c986-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayConnectionHealth -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : { 
                  "VpnClientConnectionsCount": 2,
                      "AllocatedIpAddresses": { "192.168.2.1", "192.168.2.2" },
                      "TotalIngressBytesTransferred": 100,
                      "TotalEgressBytesTransferred": 200
                 }
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="3c986-113">**Get-AzP2sVpnGatewayConnectionHealth** cmdlet 'i P2SVpnGateway 'dan site bağlantılarına işaret eden geçerli toplu durumu almanızı olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="3c986-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="3c986-114">Yukarıdaki komut çıkış durumunun, P2SVpnGateway 'e bağlı olan site istemcilerinin 2 olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c986-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="3c986-115">P2SVpnGateway aracılığıyla aktarılan toplam gelen ve çıkış baytları, sırasıyla 100 ve 200.</span><span class="sxs-lookup"><span data-stu-id="3c986-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="3c986-116">Site istemcilerine bağlı bağlantı noktası için ayrılan IP adresleri "192.168.2.1", "192.168.2.2" dir.</span><span class="sxs-lookup"><span data-stu-id="3c986-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="3c986-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c986-117">PARAMETERS</span></span>

### <span data-ttu-id="3c986-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c986-118">-DefaultProfile</span></span>
<span data-ttu-id="3c986-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c986-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c986-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c986-120">-InputObject</span></span>
<span data-ttu-id="3c986-121">Değiştirilecek P2S VPN ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="3c986-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c986-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c986-122">-Name</span></span>
<span data-ttu-id="3c986-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="3c986-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c986-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c986-124">-ResourceGroupName</span></span>
<span data-ttu-id="3c986-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3c986-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c986-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3c986-126">-ResourceId</span></span>
<span data-ttu-id="3c986-127">Değiştirilecek P2SVpnGateway Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3c986-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c986-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c986-128">CommonParameters</span></span>
<span data-ttu-id="3c986-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c986-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c986-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c986-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c986-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c986-131">INPUTS</span></span>

### <span data-ttu-id="3c986-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3c986-132">System.String</span></span>
<span data-ttu-id="3c986-133">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3c986-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="3c986-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c986-134">OUTPUTS</span></span>

### <span data-ttu-id="3c986-135">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3c986-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="3c986-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c986-136">NOTES</span></span>

## <span data-ttu-id="3c986-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c986-137">RELATED LINKS</span></span>
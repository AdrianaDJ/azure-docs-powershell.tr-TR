---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 83d91b7761200813e2973dfe4a76067e92f9bf42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932734"
---
# <span data-ttu-id="77dee-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77dee-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="77dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77dee-102">SYNOPSIS</span></span>
<span data-ttu-id="77dee-103">Sanal ağ geçidi bağlantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="77dee-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="77dee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="77dee-104">SYNTAX</span></span>

### <span data-ttu-id="77dee-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="77dee-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecPolTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77dee-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="77dee-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecPolTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] 
 -Tag <Hashtable> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77dee-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="77dee-107">DESCRIPTION</span></span>
<span data-ttu-id="77dee-108">**Set-AzVirtualNetworkGatewayConnection** cmdlet 'i sanal ağ geçidi bağlantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="77dee-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="77dee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="77dee-109">EXAMPLES</span></span>

### <span data-ttu-id="77dee-110">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="77dee-110">Example 1:</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

### <span data-ttu-id="77dee-111">Örnek 2: var olan VirtualNetworkGatewayConnection 'a etiket ekleme/güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="77dee-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
                          Name          Value
                          ============  ============
                          testtagValue  SomeKeyValue
                          testtagKey    SomeTagKey
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

## <span data-ttu-id="77dee-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="77dee-112">PARAMETERS</span></span>

### <span data-ttu-id="77dee-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="77dee-113">-AsJob</span></span>
<span data-ttu-id="77dee-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="77dee-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77dee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77dee-115">-DefaultProfile</span></span>
<span data-ttu-id="77dee-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="77dee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77dee-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="77dee-117">-EnableBgp</span></span>
<span data-ttu-id="77dee-118">S2S VPN tüneli üzerinden BGP oturumunun kullanılıp kullanılmayacağını</span><span class="sxs-lookup"><span data-stu-id="77dee-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77dee-119">-Force</span><span class="sxs-lookup"><span data-stu-id="77dee-119">-Force</span></span>
<span data-ttu-id="77dee-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="77dee-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77dee-121">-Ipsecpolicies</span><span class="sxs-lookup"><span data-stu-id="77dee-121">-IpsecPolicies</span></span>
<span data-ttu-id="77dee-122">IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="77dee-122">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77dee-123">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="77dee-123">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="77dee-124">Trafik seçici ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="77dee-124">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77dee-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="77dee-125">-Tag</span></span>
<span data-ttu-id="77dee-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="77dee-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dee-127">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="77dee-127">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="77dee-128">S2S bağlantısı için ilkeye dayalı trafik seçicileri kullanılıp kullanılmayacağını</span><span class="sxs-lookup"><span data-stu-id="77dee-128">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dee-129">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77dee-129">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="77dee-130">Bu cmdlet 'in sanal ağ geçidi bağlantısını değiştirmek için kullandığı PSVirtualNetworkGatewayConnection nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="77dee-130">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77dee-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="77dee-131">-Confirm</span></span>
<span data-ttu-id="77dee-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="77dee-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dee-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77dee-133">-WhatIf</span></span>
<span data-ttu-id="77dee-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="77dee-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77dee-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="77dee-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dee-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77dee-136">CommonParameters</span></span>
<span data-ttu-id="77dee-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="77dee-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77dee-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77dee-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77dee-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="77dee-139">INPUTS</span></span>

### <span data-ttu-id="77dee-140">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77dee-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="77dee-141">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="77dee-141">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="77dee-142">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="77dee-142">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="77dee-143">Microsoft. Azure. Commands. Network. modeller. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="77dee-143">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="77dee-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="77dee-144">OUTPUTS</span></span>

### <span data-ttu-id="77dee-145">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77dee-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="77dee-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="77dee-146">NOTES</span></span>

## <span data-ttu-id="77dee-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="77dee-147">RELATED LINKS</span></span>

[<span data-ttu-id="77dee-148">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77dee-148">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="77dee-149">Yeni-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77dee-149">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="77dee-150">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77dee-150">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)



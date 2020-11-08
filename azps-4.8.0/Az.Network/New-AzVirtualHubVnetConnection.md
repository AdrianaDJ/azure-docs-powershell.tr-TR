---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e9156887f328242f8c4896dc707a1814f58f2869
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274361"
---
# <span data-ttu-id="45958-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="45958-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="45958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45958-102">SYNOPSIS</span></span>
<span data-ttu-id="45958-103">New-AzVirtualHubVnetConnection cmdlet 'i, Azure sanal hub 'a sanal bir ağı eşuygulayan bir HubVirtualNetworkConnection kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45958-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="45958-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45958-104">SYNTAX</span></span>

### <span data-ttu-id="45958-105">ByVirtualHubNameByRemoteVirtualNetworkObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="45958-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45958-106">Byvirtualhubnamebyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="45958-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45958-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="45958-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45958-108">Byvirtualhubobjectbyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="45958-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45958-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="45958-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45958-110">Byvirtualhubresourceıdbyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="45958-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45958-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="45958-111">DESCRIPTION</span></span>
<span data-ttu-id="45958-112">New-AzVirtualHubVnetConnection cmdlet 'i, Azure sanal hub 'a sanal bir ağı eşuygulayan bir HubVirtualNetworkConnection kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45958-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="45958-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45958-113">EXAMPLES</span></span>

### <span data-ttu-id="45958-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="45958-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="45958-115">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45958-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="45958-116">Bundan sonra sanal ağı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="45958-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="45958-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="45958-117">Example 2</span></span>

<span data-ttu-id="45958-118">New-AzVirtualHubVnetConnection cmdlet 'i, Azure sanal hub 'a sanal bir ağı eşuygulayan bir HubVirtualNetworkConnection kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45958-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="45958-119">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="45958-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```

## <span data-ttu-id="45958-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45958-120">PARAMETERS</span></span>

### <span data-ttu-id="45958-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="45958-121">-AsJob</span></span>
<span data-ttu-id="45958-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="45958-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45958-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45958-123">-DefaultProfile</span></span>
<span data-ttu-id="45958-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45958-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45958-125">-Enableınternetgüvenlik</span><span class="sxs-lookup"><span data-stu-id="45958-125">-EnableInternetSecurity</span></span>
<span data-ttu-id="45958-126">Bu bağlantı için İnternet güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="45958-126">Enable internet security for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45958-127">-Enableınternetsecurityflag</span><span class="sxs-lookup"><span data-stu-id="45958-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="45958-128">Bu bağlantı için İnternet güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="45958-128">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="45958-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="45958-129">-Name</span></span>
<span data-ttu-id="45958-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="45958-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45958-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="45958-131">-ParentObject</span></span>
<span data-ttu-id="45958-132">Üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="45958-132">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45958-133">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="45958-133">-ParentResourceId</span></span>
<span data-ttu-id="45958-134">Üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="45958-134">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45958-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="45958-135">-ParentResourceName</span></span>
<span data-ttu-id="45958-136">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="45958-136">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45958-137">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="45958-137">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="45958-138">Bu hub sanal ağ bağlantısının bağlı olduğu uzaktaki sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="45958-138">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45958-139">-Remotevirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="45958-139">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="45958-140">Bu hub sanal ağ bağlantısının bağlı olduğu uzaktaki sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="45958-140">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45958-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45958-141">-ResourceGroupName</span></span>
<span data-ttu-id="45958-142">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="45958-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45958-143">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="45958-143">-RoutingConfiguration</span></span>
<span data-ttu-id="45958-144">Bu bağlantı için Yönlendirme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="45958-144">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45958-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="45958-145">-Confirm</span></span>
<span data-ttu-id="45958-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="45958-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45958-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45958-147">-WhatIf</span></span>
<span data-ttu-id="45958-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="45958-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45958-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="45958-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45958-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45958-150">CommonParameters</span></span>
<span data-ttu-id="45958-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45958-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45958-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="45958-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45958-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45958-153">INPUTS</span></span>

### <span data-ttu-id="45958-154">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="45958-154">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="45958-155">System. String</span><span class="sxs-lookup"><span data-stu-id="45958-155">System.String</span></span>

## <span data-ttu-id="45958-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45958-156">OUTPUTS</span></span>

### <span data-ttu-id="45958-157">Microsoft. Azure. Commands. Network. model. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="45958-157">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="45958-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45958-158">NOTES</span></span>

## <span data-ttu-id="45958-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45958-159">RELATED LINKS</span></span>

[<span data-ttu-id="45958-160">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="45958-160">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="45958-161">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="45958-161">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="45958-162">Yeni-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="45958-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)

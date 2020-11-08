---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 0c07686b59f89bfee656701e14a7c938f49eeb86
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274305"
---
# <span data-ttu-id="cb89d-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cb89d-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="cb89d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb89d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb89d-103">Mevcut bir HubVirtualNetworkConnection öğesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cb89d-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="cb89d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb89d-104">SYNTAX</span></span>

### <span data-ttu-id="cb89d-105">ByHubVirtualNetworkConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cb89d-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb89d-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="cb89d-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb89d-107">Byhubvirtualnetworkconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="cb89d-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb89d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb89d-108">DESCRIPTION</span></span>
<span data-ttu-id="cb89d-109">Mevcut bir HubVirtualNetworkConnection öğesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cb89d-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="cb89d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb89d-110">EXAMPLES</span></span>

### <span data-ttu-id="cb89d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cb89d-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
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

<span data-ttu-id="cb89d-112">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb89d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="cb89d-113">Sanal hub 'ı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="cb89d-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="cb89d-114">Bu sanal ağ bağlantısı daha sonra İnternet güvenliğini etkinleştirecek şekilde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="cb89d-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="cb89d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb89d-115">PARAMETERS</span></span>

### <span data-ttu-id="cb89d-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="cb89d-116">-AsJob</span></span>
<span data-ttu-id="cb89d-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cb89d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb89d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb89d-118">-DefaultProfile</span></span>
<span data-ttu-id="cb89d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb89d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb89d-120">-Enableınternetgüvenlik</span><span class="sxs-lookup"><span data-stu-id="cb89d-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="cb89d-121">Bu bağlantı için İnternet güvenliğini etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="cb89d-121">Enable internet security for this connection.</span></span>

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

### <span data-ttu-id="cb89d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb89d-122">-InputObject</span></span>
<span data-ttu-id="cb89d-123">Değiştirilecek hubvirtualnetworkconnection kaynağı.</span><span class="sxs-lookup"><span data-stu-id="cb89d-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb89d-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb89d-124">-Name</span></span>
<span data-ttu-id="cb89d-125">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cb89d-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb89d-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="cb89d-126">-ParentResourceName</span></span>
<span data-ttu-id="cb89d-127">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cb89d-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb89d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb89d-128">-ResourceGroupName</span></span>
<span data-ttu-id="cb89d-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cb89d-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb89d-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cb89d-130">-ResourceId</span></span>
<span data-ttu-id="cb89d-131">Değiştirilecek hubvirtualnetworkconnection kaynağının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="cb89d-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb89d-132">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb89d-132">-RoutingConfiguration</span></span>
<span data-ttu-id="cb89d-133">Bu bağlantı için Yönlendirme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="cb89d-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="cb89d-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="cb89d-134">-Confirm</span></span>
<span data-ttu-id="cb89d-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cb89d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb89d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb89d-136">-WhatIf</span></span>
<span data-ttu-id="cb89d-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb89d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb89d-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cb89d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb89d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb89d-139">CommonParameters</span></span>
<span data-ttu-id="cb89d-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb89d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb89d-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb89d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb89d-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb89d-142">INPUTS</span></span>

### <span data-ttu-id="cb89d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cb89d-143">System.String</span></span>

### <span data-ttu-id="cb89d-144">Microsoft. Azure. Commands. Network. model. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="cb89d-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="cb89d-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb89d-145">OUTPUTS</span></span>

### <span data-ttu-id="cb89d-146">Microsoft. Azure. Commands. Network. model. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="cb89d-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="cb89d-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb89d-147">NOTES</span></span>

## <span data-ttu-id="cb89d-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb89d-148">RELATED LINKS</span></span>

[<span data-ttu-id="cb89d-149">Yeni-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb89d-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)

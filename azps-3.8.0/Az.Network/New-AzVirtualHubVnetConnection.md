---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 3be41be3c62b0676ea10e9fe7c9d89927c4de757
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098715"
---
# <span data-ttu-id="780ac-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="780ac-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="780ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="780ac-102">SYNOPSIS</span></span>
<span data-ttu-id="780ac-103">New-AzVirtualHubVnetConnection cmdlet 'i, Azure sanal hub 'a sanal bir ağı eşuygulayan bir HubVirtualNetworkConnection kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="780ac-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="780ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="780ac-104">SYNTAX</span></span>

### <span data-ttu-id="780ac-105">ByVirtualHubNameByRemoteVirtualNetworkObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="780ac-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="780ac-106">Byvirtualhubnamebyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="780ac-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="780ac-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="780ac-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="780ac-108">Byvirtualhubobjectbyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="780ac-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="780ac-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="780ac-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="780ac-110">Byvirtualhubresourceıdbyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="780ac-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="780ac-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="780ac-111">DESCRIPTION</span></span>
<span data-ttu-id="780ac-112">New-AzVirtualHubVnetConnection cmdlet 'i, Azure sanal hub 'a sanal bir ağı eşuygulayan bir HubVirtualNetworkConnection kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="780ac-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="780ac-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="780ac-113">EXAMPLES</span></span>

### <span data-ttu-id="780ac-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="780ac-114">Example 1</span></span>

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
```

<span data-ttu-id="780ac-115">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="780ac-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="780ac-116">Bundan sonra sanal ağı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="780ac-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="780ac-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="780ac-117">PARAMETERS</span></span>

### <span data-ttu-id="780ac-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="780ac-118">-AsJob</span></span>
<span data-ttu-id="780ac-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="780ac-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="780ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780ac-120">-DefaultProfile</span></span>
<span data-ttu-id="780ac-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="780ac-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="780ac-122">-Enableınternetgüvenlik</span><span class="sxs-lookup"><span data-stu-id="780ac-122">-EnableInternetSecurity</span></span>
<span data-ttu-id="780ac-123">Bu bağlantı için İnternet güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="780ac-123">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="780ac-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="780ac-124">-Name</span></span>
<span data-ttu-id="780ac-125">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="780ac-125">The resource name.</span></span>

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

### <span data-ttu-id="780ac-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="780ac-126">-ParentObject</span></span>
<span data-ttu-id="780ac-127">Üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="780ac-127">The parent resource.</span></span>

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

### <span data-ttu-id="780ac-128">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="780ac-128">-ParentResourceId</span></span>
<span data-ttu-id="780ac-129">Üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="780ac-129">The parent resource.</span></span>

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

### <span data-ttu-id="780ac-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="780ac-130">-ParentResourceName</span></span>
<span data-ttu-id="780ac-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="780ac-131">The resource group name.</span></span>

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

### <span data-ttu-id="780ac-132">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="780ac-132">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="780ac-133">Bu hub sanal ağ bağlantısının bağlı olduğu uzaktaki sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="780ac-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="780ac-134">-Remotevirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="780ac-134">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="780ac-135">Bu hub sanal ağ bağlantısının bağlı olduğu uzaktaki sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="780ac-135">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="780ac-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="780ac-136">-ResourceGroupName</span></span>
<span data-ttu-id="780ac-137">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="780ac-137">The resource group name.</span></span>

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

### <span data-ttu-id="780ac-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="780ac-138">-Confirm</span></span>
<span data-ttu-id="780ac-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="780ac-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="780ac-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="780ac-140">-WhatIf</span></span>
<span data-ttu-id="780ac-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="780ac-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="780ac-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="780ac-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="780ac-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780ac-143">CommonParameters</span></span>
<span data-ttu-id="780ac-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="780ac-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780ac-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="780ac-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780ac-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="780ac-146">INPUTS</span></span>

### <span data-ttu-id="780ac-147">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="780ac-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="780ac-148">System. String</span><span class="sxs-lookup"><span data-stu-id="780ac-148">System.String</span></span>

## <span data-ttu-id="780ac-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="780ac-149">OUTPUTS</span></span>

### <span data-ttu-id="780ac-150">Microsoft. Azure. Commands. Network. model. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="780ac-150">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="780ac-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="780ac-151">NOTES</span></span>

## <span data-ttu-id="780ac-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="780ac-152">RELATED LINKS</span></span>

[<span data-ttu-id="780ac-153">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="780ac-153">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="780ac-154">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="780ac-154">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 6805d6671d0335599dc95f206ddb8482867734fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763148"
---
# <span data-ttu-id="3641f-101">New-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3641f-101">New-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="3641f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3641f-102">SYNOPSIS</span></span>
<span data-ttu-id="3641f-103">New-AzureRmVirtualHubVnetConnection cmdlet 'i, Azure sanal hub 'a sanal bir ağı eşuygulayan bir HubVirtualNetworkConnection kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3641f-103">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3641f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3641f-104">SYNTAX</span></span>

### <span data-ttu-id="3641f-105">ByVirtualHubNameByRemoteVirtualNetworkObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3641f-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3641f-106">Byvirtualhubnamebyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="3641f-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3641f-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="3641f-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3641f-108">Byvirtualhubobjectbyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="3641f-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3641f-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="3641f-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3641f-110">Byvirtualhubresourceıdbyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="3641f-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3641f-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="3641f-111">DESCRIPTION</span></span>
<span data-ttu-id="3641f-112">New-AzureRmVirtualHubVnetConnection cmdlet 'i, Azure sanal hub 'a sanal bir ağı eşuygulayan bir HubVirtualNetworkConnection kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3641f-112">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="3641f-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3641f-113">EXAMPLES</span></span>

### <span data-ttu-id="3641f-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3641f-114">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="3641f-115">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3641f-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="3641f-116">Bundan sonra sanal ağı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="3641f-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="3641f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3641f-117">PARAMETERS</span></span>

### <span data-ttu-id="3641f-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="3641f-118">-AsJob</span></span>
<span data-ttu-id="3641f-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3641f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3641f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3641f-120">-DefaultProfile</span></span>
<span data-ttu-id="3641f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3641f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3641f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="3641f-122">-Name</span></span>
<span data-ttu-id="3641f-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="3641f-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3641f-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3641f-124">-ParentObject</span></span>
<span data-ttu-id="3641f-125">Üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="3641f-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3641f-126">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="3641f-126">-ParentResourceId</span></span>
<span data-ttu-id="3641f-127">Üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="3641f-127">The parent resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3641f-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="3641f-128">-ParentResourceName</span></span>
<span data-ttu-id="3641f-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3641f-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3641f-130">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3641f-130">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="3641f-131">Bu hub sanal ağ bağlantısının bağlı olduğu uzaktaki sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="3641f-131">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3641f-132">-Remotevirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="3641f-132">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="3641f-133">Bu hub sanal ağ bağlantısının bağlı olduğu uzaktaki sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="3641f-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3641f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3641f-134">-ResourceGroupName</span></span>
<span data-ttu-id="3641f-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3641f-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3641f-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="3641f-136">-Confirm</span></span>
<span data-ttu-id="3641f-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3641f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3641f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3641f-138">-WhatIf</span></span>
<span data-ttu-id="3641f-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3641f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3641f-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3641f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3641f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3641f-141">CommonParameters</span></span>
<span data-ttu-id="3641f-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3641f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3641f-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3641f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3641f-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3641f-144">INPUTS</span></span>

### <span data-ttu-id="3641f-145">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3641f-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="3641f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3641f-146">System.String</span></span>

## <span data-ttu-id="3641f-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3641f-147">OUTPUTS</span></span>

### <span data-ttu-id="3641f-148">Microsoft. Azure. Commands. Network. model. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="3641f-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="3641f-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3641f-149">NOTES</span></span>

## <span data-ttu-id="3641f-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3641f-150">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 79bf22b5da9426ccb895b42faaeb4b01036828aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760489"
---
# <span data-ttu-id="e353e-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e353e-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="e353e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e353e-102">SYNOPSIS</span></span>
<span data-ttu-id="e353e-103">Sanal bir hub 'da sanal ağ bağlantısını alır veya sanal bir hub 'daki tüm sanal ağ bağlantılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="e353e-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="e353e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e353e-104">SYNTAX</span></span>

### <span data-ttu-id="e353e-105">ByVirtualHubName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e353e-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e353e-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e353e-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e353e-107">Byvirtualhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="e353e-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e353e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e353e-108">DESCRIPTION</span></span>
<span data-ttu-id="e353e-109">Sanal bir hub 'da sanal ağ bağlantısını alır veya sanal bir hub 'daki tüm sanal ağ bağlantılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="e353e-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="e353e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e353e-110">EXAMPLES</span></span>

### <span data-ttu-id="e353e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e353e-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="e353e-112">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e353e-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e353e-113">Bundan sonra sanal ağı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="e353e-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="e353e-114">Hub sanal ağ bağlantısı oluşturulduktan sonra, kaynak grup adını, hub adını ve bağlantı adını kullanarak hub sanal ağ bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="e353e-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="e353e-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e353e-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="e353e-116">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e353e-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e353e-117">Bundan sonra sanal ağı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="e353e-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="e353e-118">Hub sanal ağ bağlantısı oluşturulduktan sonra, kaynak grup adını ve hub adını kullanarak tüm Hub sanal ağ bağlantılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="e353e-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="e353e-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e353e-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="e353e-120">Bu cmdlet, kaynak grup adını ve hub adını kullanarak "test" ile başlayan tüm Hub sanal ağ bağlantılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="e353e-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="e353e-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e353e-121">PARAMETERS</span></span>

### <span data-ttu-id="e353e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e353e-122">-DefaultProfile</span></span>
<span data-ttu-id="e353e-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e353e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e353e-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e353e-124">-Name</span></span>
<span data-ttu-id="e353e-125">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e353e-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="e353e-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e353e-126">-ParentObject</span></span>
<span data-ttu-id="e353e-127">Üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="e353e-127">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e353e-128">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="e353e-128">-ParentResourceId</span></span>
<span data-ttu-id="e353e-129">Üst kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e353e-129">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e353e-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e353e-130">-ParentResourceName</span></span>
<span data-ttu-id="e353e-131">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e353e-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e353e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e353e-132">-ResourceGroupName</span></span>
<span data-ttu-id="e353e-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e353e-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e353e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e353e-134">CommonParameters</span></span>
<span data-ttu-id="e353e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e353e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e353e-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e353e-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e353e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e353e-137">INPUTS</span></span>

### <span data-ttu-id="e353e-138">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e353e-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="e353e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e353e-139">System.String</span></span>

## <span data-ttu-id="e353e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e353e-140">OUTPUTS</span></span>

### <span data-ttu-id="e353e-141">Microsoft. Azure. Commands. Network. model. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="e353e-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="e353e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e353e-142">NOTES</span></span>

## <span data-ttu-id="e353e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e353e-143">RELATED LINKS</span></span>

[<span data-ttu-id="e353e-144">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e353e-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="e353e-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e353e-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

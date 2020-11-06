---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 8aeb992b08e2749168ef3da2db6c264158c6a9ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588475"
---
# <span data-ttu-id="f4ebe-101">Get-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f4ebe-101">Get-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="f4ebe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ebe-103">Sanal bir hub 'da sanal ağ bağlantısını alır veya sanal bir hub 'daki tüm sanal ağ bağlantılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4ebe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4ebe-104">SYNTAX</span></span>

### <span data-ttu-id="f4ebe-105">ByVirtualHubName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4ebe-105">ByVirtualHubName (Default)</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4ebe-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="f4ebe-106">ByVirtualHubObject</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4ebe-107">Byvirtualhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="f4ebe-107">ByVirtualHubResourceId</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4ebe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4ebe-108">DESCRIPTION</span></span>
<span data-ttu-id="f4ebe-109">Sanal bir hub 'da sanal ağ bağlantısını alır veya sanal bir hub 'daki tüm sanal ağ bağlantılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="f4ebe-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4ebe-110">EXAMPLES</span></span>

### <span data-ttu-id="f4ebe-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4ebe-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="f4ebe-112">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f4ebe-113">Bundan sonra sanal ağı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="f4ebe-114">Hub sanal ağ bağlantısı oluşturulduktan sonra, kaynak grup adını, hub adını ve bağlantı adını kullanarak hub sanal ağ bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="f4ebe-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f4ebe-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="f4ebe-116">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f4ebe-117">Bundan sonra sanal ağı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="f4ebe-118">Hub sanal ağ bağlantısı oluşturulduktan sonra, kaynak grup adını ve hub adını kullanarak tüm Hub sanal ağ bağlantılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

## <span data-ttu-id="f4ebe-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4ebe-119">PARAMETERS</span></span>

### <span data-ttu-id="f4ebe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ebe-120">-DefaultProfile</span></span>
<span data-ttu-id="f4ebe-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4ebe-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4ebe-122">-Name</span></span>
<span data-ttu-id="f4ebe-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ebe-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f4ebe-124">-ParentObject</span></span>
<span data-ttu-id="f4ebe-125">Üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-125">The parent resource.</span></span>

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

### <span data-ttu-id="f4ebe-126">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="f4ebe-126">-ParentResourceId</span></span>
<span data-ttu-id="f4ebe-127">Üst kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-127">The parent resource id.</span></span>

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

### <span data-ttu-id="f4ebe-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f4ebe-128">-ParentResourceName</span></span>
<span data-ttu-id="f4ebe-129">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-129">The parent resource name.</span></span>

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

### <span data-ttu-id="f4ebe-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ebe-130">-ResourceGroupName</span></span>
<span data-ttu-id="f4ebe-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-131">The resource group name.</span></span>

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

### <span data-ttu-id="f4ebe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ebe-132">CommonParameters</span></span>
<span data-ttu-id="f4ebe-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4ebe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ebe-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ebe-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ebe-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4ebe-135">INPUTS</span></span>

### <span data-ttu-id="f4ebe-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f4ebe-136">None</span></span>

## <span data-ttu-id="f4ebe-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4ebe-137">OUTPUTS</span></span>

### <span data-ttu-id="f4ebe-138">Microsoft. Azure. Commands. Network. model. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="f4ebe-138">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="f4ebe-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4ebe-139">NOTES</span></span>

## <span data-ttu-id="f4ebe-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4ebe-140">RELATED LINKS</span></span>

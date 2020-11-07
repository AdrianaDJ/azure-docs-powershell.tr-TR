---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e3ba40bf4527571ed6b3396a9208a9a0931a7be7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938451"
---
# <span data-ttu-id="f36a9-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f36a9-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="f36a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f36a9-102">SYNOPSIS</span></span>
<span data-ttu-id="f36a9-103">Mevcut bir HubVirtualNetworkConnection öğesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f36a9-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="f36a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f36a9-104">SYNTAX</span></span>

### <span data-ttu-id="f36a9-105">ByHubVirtualNetworkConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f36a9-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f36a9-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f36a9-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f36a9-107">Byhubvirtualnetworkconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="f36a9-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> -EnableInternetSecurity <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f36a9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f36a9-108">DESCRIPTION</span></span>
<span data-ttu-id="f36a9-109">Mevcut bir HubVirtualNetworkConnection öğesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f36a9-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="f36a9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f36a9-110">EXAMPLES</span></span>

### <span data-ttu-id="f36a9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f36a9-111">Example 1</span></span>
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
```

<span data-ttu-id="f36a9-112">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f36a9-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f36a9-113">Sanal hub 'ı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="f36a9-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="f36a9-114">Bu sanal ağ bağlantısı daha sonra İnternet güvenliğini etkinleştirecek şekilde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f36a9-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="f36a9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f36a9-115">PARAMETERS</span></span>

### <span data-ttu-id="f36a9-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="f36a9-116">-AsJob</span></span>
<span data-ttu-id="f36a9-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f36a9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f36a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36a9-118">-DefaultProfile</span></span>
<span data-ttu-id="f36a9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f36a9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f36a9-120">-Enableınternetgüvenlik</span><span class="sxs-lookup"><span data-stu-id="f36a9-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="f36a9-121">Bu bağlantı için İnternet güvenliğini etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="f36a9-121">Enable internet security for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36a9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f36a9-122">-InputObject</span></span>
<span data-ttu-id="f36a9-123">Değiştirilecek hubvirtualnetworkconnection kaynağı.</span><span class="sxs-lookup"><span data-stu-id="f36a9-123">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="f36a9-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f36a9-124">-Name</span></span>
<span data-ttu-id="f36a9-125">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f36a9-125">The resource name.</span></span>

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

### <span data-ttu-id="f36a9-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f36a9-126">-ParentResourceName</span></span>
<span data-ttu-id="f36a9-127">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f36a9-127">The parent resource name.</span></span>

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

### <span data-ttu-id="f36a9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36a9-128">-ResourceGroupName</span></span>
<span data-ttu-id="f36a9-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f36a9-129">The resource group name.</span></span>

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

### <span data-ttu-id="f36a9-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f36a9-130">-ResourceId</span></span>
<span data-ttu-id="f36a9-131">Değiştirilecek hubvirtualnetworkconnection kaynağının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f36a9-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="f36a9-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="f36a9-132">-Confirm</span></span>
<span data-ttu-id="f36a9-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f36a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f36a9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f36a9-134">-WhatIf</span></span>
<span data-ttu-id="f36a9-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f36a9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f36a9-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f36a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f36a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36a9-137">CommonParameters</span></span>
<span data-ttu-id="f36a9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f36a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f36a9-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f36a9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36a9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f36a9-140">INPUTS</span></span>

### <span data-ttu-id="f36a9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f36a9-141">System.String</span></span>

### <span data-ttu-id="f36a9-142">Microsoft. Azure. Commands. Network. model. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="f36a9-142">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="f36a9-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f36a9-143">OUTPUTS</span></span>

### <span data-ttu-id="f36a9-144">Microsoft. Azure. Commands. Network. model. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="f36a9-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="f36a9-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f36a9-145">NOTES</span></span>

## <span data-ttu-id="f36a9-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f36a9-146">RELATED LINKS</span></span>
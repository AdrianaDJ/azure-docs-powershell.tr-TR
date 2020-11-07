---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 3a7c48803f18bf73f75e721296757e37ff89d44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762107"
---
# <span data-ttu-id="0f7db-101">Remove-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0f7db-101">Remove-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="0f7db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f7db-102">SYNOPSIS</span></span>
<span data-ttu-id="0f7db-103">Remove-AzureRmVirtualHubVnetConnection cmdlet 'i, uzak VNET 'i hub VNET 'e eşaktaran bir Azure sanal ağ bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0f7db-103">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f7db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f7db-104">SYNTAX</span></span>

### <span data-ttu-id="0f7db-105">ByHubVirtualNetworkConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f7db-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f7db-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="0f7db-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzureRmVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f7db-107">Byhubvirtualnetworkconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="0f7db-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f7db-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f7db-108">DESCRIPTION</span></span>
<span data-ttu-id="0f7db-109">Remove-AzureRmVirtualHubVnetConnection cmdlet 'i, uzak VNET 'i hub VNET 'e eşaktaran bir Azure sanal ağ bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0f7db-109">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="0f7db-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f7db-110">EXAMPLES</span></span>

### <span data-ttu-id="0f7db-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0f7db-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="0f7db-112">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f7db-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="0f7db-113">Bundan sonra sanal ağı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="0f7db-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="0f7db-114">Hub sanal ağ bağlantısı oluşturulduktan sonra, kaynak grup adını, hub adını ve bağlantı adını kullanarak hub sanal ağ bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0f7db-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="0f7db-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0f7db-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzureRmHubVnetConnection
```

<span data-ttu-id="0f7db-116">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f7db-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="0f7db-117">Bundan sonra sanal ağı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="0f7db-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="0f7db-118">Hub sanal ağ bağlantısı oluşturulduktan sonra, Get-AzureRmHubVirtualNetworkConnection 'dan alınan çıktıda PowerShell boruları kullanarak hub sanal ağ bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0f7db-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzureRmHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="0f7db-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f7db-119">PARAMETERS</span></span>

### <span data-ttu-id="0f7db-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="0f7db-120">-AsJob</span></span>
<span data-ttu-id="0f7db-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0f7db-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f7db-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f7db-122">-DefaultProfile</span></span>
<span data-ttu-id="0f7db-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f7db-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f7db-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0f7db-124">-Force</span></span>
<span data-ttu-id="0f7db-125">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="0f7db-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0f7db-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f7db-126">-InputObject</span></span>
<span data-ttu-id="0f7db-127">Değiştirilecek hubvirtualnetworkconnection kaynağı.</span><span class="sxs-lookup"><span data-stu-id="0f7db-127">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f7db-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f7db-128">-Name</span></span>
<span data-ttu-id="0f7db-129">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="0f7db-129">The resource name.</span></span>

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

### <span data-ttu-id="0f7db-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="0f7db-130">-ParentResourceName</span></span>
<span data-ttu-id="0f7db-131">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="0f7db-131">The parent resource name.</span></span>

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

### <span data-ttu-id="0f7db-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0f7db-132">-PassThru</span></span>
<span data-ttu-id="0f7db-133">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f7db-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f7db-134">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0f7db-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f7db-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f7db-135">-ResourceGroupName</span></span>
<span data-ttu-id="0f7db-136">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0f7db-136">The resource group name.</span></span>

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

### <span data-ttu-id="0f7db-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0f7db-137">-ResourceId</span></span>
<span data-ttu-id="0f7db-138">Değiştirilecek hubvirtualnetworkconnection kaynağının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0f7db-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="0f7db-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f7db-139">-Confirm</span></span>
<span data-ttu-id="0f7db-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f7db-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f7db-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f7db-141">-WhatIf</span></span>
<span data-ttu-id="0f7db-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f7db-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f7db-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0f7db-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f7db-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f7db-144">CommonParameters</span></span>
<span data-ttu-id="0f7db-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f7db-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f7db-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f7db-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f7db-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f7db-147">INPUTS</span></span>

### <span data-ttu-id="0f7db-148">Microsoft. Azure. Commands. Network. model. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="0f7db-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="0f7db-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0f7db-149">System.String</span></span>

## <span data-ttu-id="0f7db-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f7db-150">OUTPUTS</span></span>

### <span data-ttu-id="0f7db-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f7db-151">System.Boolean</span></span>

## <span data-ttu-id="0f7db-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f7db-152">NOTES</span></span>

## <span data-ttu-id="0f7db-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f7db-153">RELATED LINKS</span></span>

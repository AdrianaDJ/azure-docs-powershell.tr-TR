---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: d005ef841828dc1fe37915c4a7b0d28ad93e3b44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265981"
---
# <span data-ttu-id="1e784-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e784-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="1e784-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e784-102">SYNOPSIS</span></span>
<span data-ttu-id="1e784-103">Azure VirtualHub kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1e784-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="1e784-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e784-104">SYNTAX</span></span>

### <span data-ttu-id="1e784-105">ByVirtualWanObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e784-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e784-106">İ Virtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="1e784-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e784-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e784-107">DESCRIPTION</span></span>
<span data-ttu-id="1e784-108">Azure VirtualHub kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1e784-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="1e784-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e784-109">EXAMPLES</span></span>

### <span data-ttu-id="1e784-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e784-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="1e784-111">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1e784-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="1e784-112">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1e784-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="1e784-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1e784-113">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="1e784-114">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1e784-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="1e784-115">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1e784-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="1e784-116">Bu örnek, örnek 1 ' e benzer, ancak sanal hub 'ı oluşturmak için gereken sanal WAN 'ya başvuruda bulunmak için kaynak kimliği kullanır.</span><span class="sxs-lookup"><span data-stu-id="1e784-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="1e784-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1e784-117">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="1e784-118">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1e784-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="1e784-119">Sanal hub 'da "10.0.1.0/24" adres alanı ve bir yol tablosu eklenmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1e784-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="1e784-120">Bu örnek, örnek 2 ' ye benzer, ancak aynı zamanda bir yol tablosunu sanal hub 'a iliştirir.</span><span class="sxs-lookup"><span data-stu-id="1e784-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="1e784-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e784-121">PARAMETERS</span></span>

### <span data-ttu-id="1e784-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1e784-122">-AddressPrefix</span></span>
<span data-ttu-id="1e784-123">Bu sanal hub için adres alanı dizesi.</span><span class="sxs-lookup"><span data-stu-id="1e784-123">The address space string for this virtual hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e784-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="1e784-124">-AsJob</span></span>
<span data-ttu-id="1e784-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1e784-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e784-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e784-126">-DefaultProfile</span></span>
<span data-ttu-id="1e784-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e784-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e784-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1e784-128">-HubVnetConnection</span></span>
<span data-ttu-id="1e784-129">Bu sanal hub ile ilişkilendirilmiş hub sanal ağ bağlantıları.</span><span class="sxs-lookup"><span data-stu-id="1e784-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e784-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="1e784-130">-Location</span></span>
<span data-ttu-id="1e784-131">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="1e784-131">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e784-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e784-132">-Name</span></span>
<span data-ttu-id="1e784-133">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="1e784-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e784-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e784-134">-ResourceGroupName</span></span>
<span data-ttu-id="1e784-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1e784-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e784-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1e784-136">-RouteTable</span></span>
<span data-ttu-id="1e784-137">Bu sanal hub ile ilişkili yol tablosu.</span><span class="sxs-lookup"><span data-stu-id="1e784-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e784-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="1e784-138">-Sku</span></span>
<span data-ttu-id="1e784-139">Sanal hub 'ın SKU 'su.</span><span class="sxs-lookup"><span data-stu-id="1e784-139">The sku of the Virtual Hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e784-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1e784-140">-Tag</span></span>
<span data-ttu-id="1e784-141">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="1e784-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e784-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="1e784-142">-VirtualWan</span></span>
<span data-ttu-id="1e784-143">Bu hub 'ın bağlandığı sanal WAN nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1e784-143">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e784-144">-Virtualwanıd</span><span class="sxs-lookup"><span data-stu-id="1e784-144">-VirtualWanId</span></span>
<span data-ttu-id="1e784-145">Bu hub 'ın bağlandığı sanal WAN nesnesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="1e784-145">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e784-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e784-146">-Confirm</span></span>
<span data-ttu-id="1e784-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e784-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e784-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e784-148">-WhatIf</span></span>
<span data-ttu-id="1e784-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e784-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e784-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e784-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e784-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e784-151">CommonParameters</span></span>
<span data-ttu-id="1e784-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e784-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e784-153">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1e784-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e784-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e784-154">INPUTS</span></span>

### <span data-ttu-id="1e784-155">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1e784-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="1e784-156">System. String</span><span class="sxs-lookup"><span data-stu-id="1e784-156">System.String</span></span>

## <span data-ttu-id="1e784-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e784-157">OUTPUTS</span></span>

### <span data-ttu-id="1e784-158">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e784-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="1e784-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e784-159">NOTES</span></span>

## <span data-ttu-id="1e784-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e784-160">RELATED LINKS</span></span>

[<span data-ttu-id="1e784-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e784-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="1e784-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e784-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="1e784-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1e784-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)

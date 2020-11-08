---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: a07df2c6330757bf9e5b4f211429f6e2918fea39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266977"
---
# <span data-ttu-id="89605-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="89605-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="89605-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89605-102">SYNOPSIS</span></span>
<span data-ttu-id="89605-103">Sanal bir hub 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="89605-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="89605-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89605-104">SYNTAX</span></span>

### <span data-ttu-id="89605-105">ByVirtualHubName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89605-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89605-106">Byvirtualhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="89605-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89605-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="89605-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89605-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="89605-108">DESCRIPTION</span></span>
<span data-ttu-id="89605-109">**Update-AzVirtualHub** cmdlet 'i sanal bir hub 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="89605-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="89605-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89605-110">EXAMPLES</span></span>

### <span data-ttu-id="89605-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="89605-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="89605-112">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="89605-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="89605-113">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="89605-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="89605-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="89605-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="89605-115">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="89605-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="89605-116">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="89605-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="89605-117">Bu örnek, örnek 1 ' e benzer, ancak aynı zamanda bir yol tablosunu sanal hub 'a ekler.</span><span class="sxs-lookup"><span data-stu-id="89605-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="89605-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89605-118">PARAMETERS</span></span>

### <span data-ttu-id="89605-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="89605-119">-AddressPrefix</span></span>
<span data-ttu-id="89605-120">Bu sanal hub için adres alanı dizesi.</span><span class="sxs-lookup"><span data-stu-id="89605-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="89605-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="89605-121">-AsJob</span></span>
<span data-ttu-id="89605-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="89605-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89605-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89605-123">-DefaultProfile</span></span>
<span data-ttu-id="89605-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89605-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89605-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="89605-125">-HubVnetConnection</span></span>
<span data-ttu-id="89605-126">Bu sanal hub ile ilişkilendirilmiş hub sanal ağ bağlantıları.</span><span class="sxs-lookup"><span data-stu-id="89605-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="89605-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89605-127">-InputObject</span></span>
<span data-ttu-id="89605-128">Değiştirilecek sanal hub nesnesi.</span><span class="sxs-lookup"><span data-stu-id="89605-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89605-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="89605-129">-Name</span></span>
<span data-ttu-id="89605-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="89605-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89605-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89605-131">-ResourceGroupName</span></span>
<span data-ttu-id="89605-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="89605-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89605-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="89605-133">-ResourceId</span></span>
<span data-ttu-id="89605-134">Değiştirilecek sanal hub 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="89605-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89605-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="89605-135">-RouteTable</span></span>
<span data-ttu-id="89605-136">Bu sanal hub ile ilişkili yol tablosu.</span><span class="sxs-lookup"><span data-stu-id="89605-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="89605-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="89605-137">-Sku</span></span>
<span data-ttu-id="89605-138">Sanal hub 'ın SKU 'su.</span><span class="sxs-lookup"><span data-stu-id="89605-138">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="89605-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="89605-139">-Tag</span></span>
<span data-ttu-id="89605-140">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="89605-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="89605-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="89605-141">-Confirm</span></span>
<span data-ttu-id="89605-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89605-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89605-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89605-143">-WhatIf</span></span>
<span data-ttu-id="89605-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89605-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89605-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89605-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89605-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89605-146">CommonParameters</span></span>
<span data-ttu-id="89605-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89605-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89605-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="89605-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89605-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89605-149">INPUTS</span></span>

### <span data-ttu-id="89605-150">System. String</span><span class="sxs-lookup"><span data-stu-id="89605-150">System.String</span></span>

### <span data-ttu-id="89605-151">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="89605-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="89605-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89605-152">OUTPUTS</span></span>

### <span data-ttu-id="89605-153">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="89605-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="89605-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89605-154">NOTES</span></span>

## <span data-ttu-id="89605-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89605-155">RELATED LINKS</span></span>

[<span data-ttu-id="89605-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="89605-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="89605-157">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="89605-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="89605-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="89605-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

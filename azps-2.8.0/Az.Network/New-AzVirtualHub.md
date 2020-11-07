---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: 8527b383dd5469d1a9bc34b7916a1e28b3f673f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918187"
---
# <span data-ttu-id="1dc70-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1dc70-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="1dc70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dc70-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc70-103">Azure VirtualHub kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1dc70-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="1dc70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1dc70-104">SYNTAX</span></span>

### <span data-ttu-id="1dc70-105">ByVirtualWanObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1dc70-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc70-106">İ Virtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="1dc70-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc70-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dc70-107">DESCRIPTION</span></span>
<span data-ttu-id="1dc70-108">Azure VirtualHub kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1dc70-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="1dc70-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1dc70-109">EXAMPLES</span></span>

### <span data-ttu-id="1dc70-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1dc70-110">Example 1</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="1dc70-111">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1dc70-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="1dc70-112">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1dc70-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="1dc70-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1dc70-113">Example 2</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="1dc70-114">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1dc70-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="1dc70-115">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1dc70-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="1dc70-116">Bu örnek, örnek 1 ' e benzer, ancak sanal hub 'ı oluşturmak için gereken sanal WAN 'ya başvuruda bulunmak için kaynak kimliği kullanır.</span><span class="sxs-lookup"><span data-stu-id="1dc70-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="1dc70-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1dc70-117">Example 3</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="1dc70-118">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1dc70-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="1dc70-119">Sanal hub 'da "10.0.1.0/24" adres alanı ve bir yol tablosu eklenmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1dc70-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="1dc70-120">Bu örnek, örnek 2 ' ye benzer, ancak aynı zamanda bir yol tablosunu sanal hub 'a iliştirir.</span><span class="sxs-lookup"><span data-stu-id="1dc70-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="1dc70-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1dc70-121">PARAMETERS</span></span>

### <span data-ttu-id="1dc70-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1dc70-122">-AddressPrefix</span></span>
<span data-ttu-id="1dc70-123">Bu sanal hub için adres alanı dizesi.</span><span class="sxs-lookup"><span data-stu-id="1dc70-123">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc70-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="1dc70-124">-AsJob</span></span>
<span data-ttu-id="1dc70-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1dc70-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dc70-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc70-126">-DefaultProfile</span></span>
<span data-ttu-id="1dc70-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1dc70-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dc70-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1dc70-128">-HubVnetConnection</span></span>
<span data-ttu-id="1dc70-129">Bu sanal hub ile ilişkilendirilmiş hub sanal ağ bağlantıları.</span><span class="sxs-lookup"><span data-stu-id="1dc70-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc70-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="1dc70-130">-Location</span></span>
<span data-ttu-id="1dc70-131">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="1dc70-131">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc70-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="1dc70-132">-Name</span></span>
<span data-ttu-id="1dc70-133">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="1dc70-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc70-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc70-134">-ResourceGroupName</span></span>
<span data-ttu-id="1dc70-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1dc70-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc70-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1dc70-136">-RouteTable</span></span>
<span data-ttu-id="1dc70-137">Bu sanal hub ile ilişkili yol tablosu.</span><span class="sxs-lookup"><span data-stu-id="1dc70-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc70-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1dc70-138">-Tag</span></span>
<span data-ttu-id="1dc70-139">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="1dc70-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc70-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="1dc70-140">-VirtualWan</span></span>
<span data-ttu-id="1dc70-141">Bu hub 'ın bağlandığı sanal WAN nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1dc70-141">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc70-142">-Virtualwanıd</span><span class="sxs-lookup"><span data-stu-id="1dc70-142">-VirtualWanId</span></span>
<span data-ttu-id="1dc70-143">Bu hub 'ın bağlandığı sanal WAN nesnesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="1dc70-143">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc70-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="1dc70-144">-Confirm</span></span>
<span data-ttu-id="1dc70-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1dc70-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc70-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc70-146">-WhatIf</span></span>
<span data-ttu-id="1dc70-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1dc70-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc70-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1dc70-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc70-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc70-149">CommonParameters</span></span>
<span data-ttu-id="1dc70-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1dc70-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc70-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc70-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc70-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1dc70-152">INPUTS</span></span>

### <span data-ttu-id="1dc70-153">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1dc70-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="1dc70-154">System. String</span><span class="sxs-lookup"><span data-stu-id="1dc70-154">System.String</span></span>

## <span data-ttu-id="1dc70-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1dc70-155">OUTPUTS</span></span>

### <span data-ttu-id="1dc70-156">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1dc70-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="1dc70-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1dc70-157">NOTES</span></span>

## <span data-ttu-id="1dc70-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1dc70-158">RELATED LINKS</span></span>

[<span data-ttu-id="1dc70-159">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1dc70-159">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="1dc70-160">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1dc70-160">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="1dc70-161">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1dc70-161">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)

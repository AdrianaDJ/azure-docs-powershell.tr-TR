---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: 96ba4a6a80e7826b1cf95086f1410305322cf266
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759925"
---
# <span data-ttu-id="6ff1b-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6ff1b-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="6ff1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ff1b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff1b-103">Sanal bir hub 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="6ff1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ff1b-104">SYNTAX</span></span>

### <span data-ttu-id="6ff1b-105">ByVirtualHubName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ff1b-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ff1b-106">Byvirtualhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="6ff1b-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ff1b-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="6ff1b-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ff1b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ff1b-108">DESCRIPTION</span></span>
<span data-ttu-id="6ff1b-109">**Update-AzVirtualHub** cmdlet 'i sanal bir hub 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="6ff1b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ff1b-110">EXAMPLES</span></span>

### <span data-ttu-id="6ff1b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ff1b-111">Example 1</span></span>

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
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="6ff1b-112">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="6ff1b-113">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="6ff1b-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6ff1b-114">Example 2</span></span>

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
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="6ff1b-115">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="6ff1b-116">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="6ff1b-117">Bu örnek, örnek 1 ' e benzer, ancak aynı zamanda bir yol tablosunu sanal hub 'a ekler.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="6ff1b-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ff1b-118">PARAMETERS</span></span>

### <span data-ttu-id="6ff1b-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6ff1b-119">-AddressPrefix</span></span>
<span data-ttu-id="6ff1b-120">Bu sanal hub için adres alanı dizesi.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-120">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff1b-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="6ff1b-121">-AsJob</span></span>
<span data-ttu-id="6ff1b-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6ff1b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ff1b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff1b-123">-DefaultProfile</span></span>
<span data-ttu-id="6ff1b-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ff1b-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6ff1b-125">-HubVnetConnection</span></span>
<span data-ttu-id="6ff1b-126">Bu sanal hub ile ilişkilendirilmiş hub sanal ağ bağlantıları.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="6ff1b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ff1b-127">-InputObject</span></span>
<span data-ttu-id="6ff1b-128">Değiştirilecek sanal hub nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff1b-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ff1b-129">-Name</span></span>
<span data-ttu-id="6ff1b-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff1b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff1b-131">-ResourceGroupName</span></span>
<span data-ttu-id="6ff1b-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-132">The resource group name.</span></span>

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

### <span data-ttu-id="6ff1b-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6ff1b-133">-ResourceId</span></span>
<span data-ttu-id="6ff1b-134">Değiştirilecek sanal hub 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff1b-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="6ff1b-135">-RouteTable</span></span>
<span data-ttu-id="6ff1b-136">Bu sanal hub ile ilişkili yol tablosu.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="6ff1b-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6ff1b-137">-Tag</span></span>
<span data-ttu-id="6ff1b-138">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6ff1b-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ff1b-139">-Confirm</span></span>
<span data-ttu-id="6ff1b-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ff1b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff1b-141">-WhatIf</span></span>
<span data-ttu-id="6ff1b-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ff1b-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ff1b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff1b-144">CommonParameters</span></span>
<span data-ttu-id="6ff1b-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ff1b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff1b-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff1b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff1b-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ff1b-147">INPUTS</span></span>

### <span data-ttu-id="6ff1b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="6ff1b-148">System.String</span></span>

### <span data-ttu-id="6ff1b-149">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6ff1b-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="6ff1b-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ff1b-150">OUTPUTS</span></span>

### <span data-ttu-id="6ff1b-151">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6ff1b-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="6ff1b-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ff1b-152">NOTES</span></span>

## <span data-ttu-id="6ff1b-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ff1b-153">RELATED LINKS</span></span>

[<span data-ttu-id="6ff1b-154">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6ff1b-154">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="6ff1b-155">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6ff1b-155">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="6ff1b-156">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6ff1b-156">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

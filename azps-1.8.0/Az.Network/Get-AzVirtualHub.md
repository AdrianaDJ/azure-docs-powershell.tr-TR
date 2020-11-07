---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: d4945c93fdfb402e56e1822229a1bb9592951d20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760490"
---
# <span data-ttu-id="3414b-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3414b-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="3414b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3414b-102">SYNOPSIS</span></span>
<span data-ttu-id="3414b-103">Bir Azure VirtualHub 'ı Name ve ResourceGroupName ile alır veya tüm sanal hubları ResourceGroupName/Subscription ile listeler.</span><span class="sxs-lookup"><span data-stu-id="3414b-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="3414b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3414b-104">SYNTAX</span></span>

### <span data-ttu-id="3414b-105">Listbysubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3414b-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3414b-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3414b-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3414b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3414b-107">DESCRIPTION</span></span>
<span data-ttu-id="3414b-108">Bir Azure VirtualHub 'ı Name ve ResourceGroupName ile alır veya tüm sanal hubları ResourceGroupName/Subscription ile listeler.</span><span class="sxs-lookup"><span data-stu-id="3414b-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="3414b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3414b-109">EXAMPLES</span></span>

### <span data-ttu-id="3414b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3414b-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"

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

<span data-ttu-id="3414b-111">Yukarıdaki "testRG" kaynak grubu, Azure 'daki bu kaynak grubunda bir sanal WAN ve Batı ABD 'deki sanal bir hub oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3414b-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="3414b-112">Sanal hub "10.0.1.0/24" adres alanına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3414b-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="3414b-113">Ardından, sanal hub 'ı, ResourceGroupName ve ResourceName kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="3414b-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="3414b-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3414b-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualHub -Name westushub*

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub1
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub1
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub2
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub2
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="3414b-115">Bu cmdlet filtre kullanarak sanal hub 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="3414b-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="3414b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3414b-116">PARAMETERS</span></span>

### <span data-ttu-id="3414b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3414b-117">-DefaultProfile</span></span>
<span data-ttu-id="3414b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3414b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3414b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3414b-119">-Name</span></span>
<span data-ttu-id="3414b-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="3414b-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="3414b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3414b-121">-ResourceGroupName</span></span>
<span data-ttu-id="3414b-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3414b-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="3414b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3414b-123">CommonParameters</span></span>
<span data-ttu-id="3414b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3414b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3414b-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3414b-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3414b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3414b-126">INPUTS</span></span>

### <span data-ttu-id="3414b-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3414b-127">None</span></span>

## <span data-ttu-id="3414b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3414b-128">OUTPUTS</span></span>

### <span data-ttu-id="3414b-129">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3414b-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="3414b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3414b-130">NOTES</span></span>

## <span data-ttu-id="3414b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3414b-131">RELATED LINKS</span></span>

[<span data-ttu-id="3414b-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3414b-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="3414b-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3414b-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="3414b-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3414b-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
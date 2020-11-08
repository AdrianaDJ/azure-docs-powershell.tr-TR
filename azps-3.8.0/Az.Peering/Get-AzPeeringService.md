---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104488"
---
# <span data-ttu-id="7e24d-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="7e24d-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="7e24d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e24d-102">SYNOPSIS</span></span>
<span data-ttu-id="7e24d-103">Tek bir nesnedeki eşleme hizmeti nesnelerinin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="7e24d-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="7e24d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e24d-104">SYNTAX</span></span>

### <span data-ttu-id="7e24d-105">ByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7e24d-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e24d-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="7e24d-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e24d-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="7e24d-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e24d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e24d-108">DESCRIPTION</span></span>
<span data-ttu-id="7e24d-109">Abonelik için eşleme hizmetlerini alır</span><span class="sxs-lookup"><span data-stu-id="7e24d-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="7e24d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e24d-110">EXAMPLES</span></span>

### <span data-ttu-id="7e24d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e24d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="7e24d-112">Kaynak grubu için bir eşleme hizmeti alır</span><span class="sxs-lookup"><span data-stu-id="7e24d-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="7e24d-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7e24d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="7e24d-114">Kaynak grubu ve ad için eşleme hizmeti alır</span><span class="sxs-lookup"><span data-stu-id="7e24d-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="7e24d-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="7e24d-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="7e24d-116">Kaynak kimliğiyle bir eşleme hizmeti alır</span><span class="sxs-lookup"><span data-stu-id="7e24d-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="7e24d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e24d-117">PARAMETERS</span></span>

### <span data-ttu-id="7e24d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e24d-118">-DefaultProfile</span></span>
<span data-ttu-id="7e24d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e24d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e24d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e24d-120">-Name</span></span>
<span data-ttu-id="7e24d-121">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="7e24d-121">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e24d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e24d-122">-ResourceGroupName</span></span>
<span data-ttu-id="7e24d-123">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="7e24d-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e24d-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7e24d-124">-ResourceId</span></span>
<span data-ttu-id="7e24d-125">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="7e24d-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e24d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e24d-126">CommonParameters</span></span>
<span data-ttu-id="7e24d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e24d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e24d-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7e24d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e24d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e24d-129">INPUTS</span></span>

### <span data-ttu-id="7e24d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7e24d-130">System.String</span></span>

## <span data-ttu-id="7e24d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e24d-131">OUTPUTS</span></span>

### <span data-ttu-id="7e24d-132">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e24d-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="7e24d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e24d-133">NOTES</span></span>

## <span data-ttu-id="7e24d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e24d-134">RELATED LINKS</span></span>

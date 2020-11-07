---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: b2ebc3e91f08c2aa33853c8a90c929b31877a014
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932860"
---
# <span data-ttu-id="c8a74-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="c8a74-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="c8a74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8a74-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a74-103">Tek bir nesnedeki eşleme hizmeti nesnelerinin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="c8a74-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="c8a74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8a74-104">SYNTAX</span></span>

### <span data-ttu-id="c8a74-105">ByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c8a74-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8a74-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="c8a74-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8a74-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="c8a74-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8a74-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8a74-108">DESCRIPTION</span></span>
<span data-ttu-id="c8a74-109">Abonelik için eşleme hizmetlerini alır</span><span class="sxs-lookup"><span data-stu-id="c8a74-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="c8a74-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8a74-110">EXAMPLES</span></span>

### <span data-ttu-id="c8a74-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c8a74-111">Example 1</span></span>
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

<span data-ttu-id="c8a74-112">Kaynak grubu için bir eşleme hizmeti alır</span><span class="sxs-lookup"><span data-stu-id="c8a74-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="c8a74-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c8a74-113">Example 2</span></span>
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

<span data-ttu-id="c8a74-114">Kaynak grubu ve ad için eşleme hizmeti alır</span><span class="sxs-lookup"><span data-stu-id="c8a74-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="c8a74-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c8a74-115">Example 3</span></span>
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

<span data-ttu-id="c8a74-116">Kaynak kimliğiyle bir eşleme hizmeti alır</span><span class="sxs-lookup"><span data-stu-id="c8a74-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="c8a74-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8a74-117">PARAMETERS</span></span>

### <span data-ttu-id="c8a74-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a74-118">-DefaultProfile</span></span>
<span data-ttu-id="c8a74-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8a74-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a74-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c8a74-120">-Name</span></span>
<span data-ttu-id="c8a74-121">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="c8a74-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="c8a74-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a74-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8a74-123">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="c8a74-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="c8a74-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c8a74-124">-ResourceId</span></span>
<span data-ttu-id="c8a74-125">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="c8a74-125">The resource id string name.</span></span>

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

### <span data-ttu-id="c8a74-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a74-126">CommonParameters</span></span>
<span data-ttu-id="c8a74-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8a74-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a74-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c8a74-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a74-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8a74-129">INPUTS</span></span>

### <span data-ttu-id="c8a74-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c8a74-130">System.String</span></span>

## <span data-ttu-id="c8a74-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8a74-131">OUTPUTS</span></span>

### <span data-ttu-id="c8a74-132">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8a74-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="c8a74-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8a74-133">NOTES</span></span>

## <span data-ttu-id="c8a74-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8a74-134">RELATED LINKS</span></span>

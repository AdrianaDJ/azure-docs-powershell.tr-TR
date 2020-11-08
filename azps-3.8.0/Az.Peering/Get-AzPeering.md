---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: 58ba131ab0bebc65d8fd5259d24b2846da229721
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104490"
---
# <span data-ttu-id="0beaa-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="0beaa-101">Get-AzPeering</span></span>

## <span data-ttu-id="0beaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0beaa-102">SYNOPSIS</span></span>
<span data-ttu-id="0beaa-103">Aboneliğin eşleme kaynaklarını alır</span><span class="sxs-lookup"><span data-stu-id="0beaa-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="0beaa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0beaa-104">SYNTAX</span></span>

### <span data-ttu-id="0beaa-105">BySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0beaa-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0beaa-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="0beaa-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0beaa-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0beaa-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0beaa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0beaa-108">DESCRIPTION</span></span>
<span data-ttu-id="0beaa-109">Bir abonelikten, kaynak grubundan veya ada göre eş larınızı alır.</span><span class="sxs-lookup"><span data-stu-id="0beaa-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="0beaa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0beaa-110">EXAMPLES</span></span>

### <span data-ttu-id="0beaa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0beaa-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeering

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}

Name                 : ContosoSeattlePeering
Sku                  : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringSku
Kind                 : Direct
Connections          : {99999}
UseForPeeringService : False
PeerAsn              : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSSubResource
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions/resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="0beaa-112">Aboneliğin tüm kaynaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="0beaa-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="0beaa-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0beaa-113">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceGroupName test -Name myExchangePeering1

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="0beaa-114">Adlı Exchange eşliğini alır `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="0beaa-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="0beaa-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0beaa-115">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceId $resourceId

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="0beaa-116">Kaynak kimliği temel alınarak adlandırılan Exchange eşliğini alır `myExchangePeering1` .</span><span class="sxs-lookup"><span data-stu-id="0beaa-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="0beaa-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0beaa-117">PARAMETERS</span></span>

### <span data-ttu-id="0beaa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0beaa-118">-DefaultProfile</span></span>
<span data-ttu-id="0beaa-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0beaa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0beaa-120">-Tür</span><span class="sxs-lookup"><span data-stu-id="0beaa-120">-Kind</span></span>
<span data-ttu-id="0beaa-121">Tüm eşleme kaynağını türe göre gösterir.</span><span class="sxs-lookup"><span data-stu-id="0beaa-121">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0beaa-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="0beaa-122">-Name</span></span>
<span data-ttu-id="0beaa-123">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="0beaa-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0beaa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0beaa-124">-ResourceGroupName</span></span>
<span data-ttu-id="0beaa-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0beaa-125">The resource group name.</span></span>

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

### <span data-ttu-id="0beaa-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0beaa-126">-ResourceId</span></span>
<span data-ttu-id="0beaa-127">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="0beaa-127">The resource id string name.</span></span>

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

### <span data-ttu-id="0beaa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0beaa-128">CommonParameters</span></span>
<span data-ttu-id="0beaa-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0beaa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0beaa-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0beaa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0beaa-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0beaa-131">INPUTS</span></span>

### <span data-ttu-id="0beaa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0beaa-132">System.String</span></span>

## <span data-ttu-id="0beaa-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0beaa-133">OUTPUTS</span></span>

### <span data-ttu-id="0beaa-134">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0beaa-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="0beaa-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0beaa-135">NOTES</span></span>

## <span data-ttu-id="0beaa-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0beaa-136">RELATED LINKS</span></span>

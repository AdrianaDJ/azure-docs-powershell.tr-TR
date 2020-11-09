---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324370"
---
# <span data-ttu-id="12abd-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="12abd-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="12abd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12abd-102">SYNOPSIS</span></span>
<span data-ttu-id="12abd-103">Taşıma koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="12abd-103">Gets the move collection.</span></span>

## <span data-ttu-id="12abd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12abd-104">SYNTAX</span></span>

### <span data-ttu-id="12abd-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="12abd-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="12abd-106">Al</span><span class="sxs-lookup"><span data-stu-id="12abd-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12abd-107">List1</span><span class="sxs-lookup"><span data-stu-id="12abd-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="12abd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="12abd-108">DESCRIPTION</span></span>
<span data-ttu-id="12abd-109">Taşıma koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="12abd-109">Gets the move collection.</span></span>

## <span data-ttu-id="12abd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12abd-110">EXAMPLES</span></span>

### <span data-ttu-id="12abd-111">Örnek 1: abonelikteki tüm taşıma koleksiyonlarının ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="12abd-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="12abd-112">Abonelikteki tüm taşıma koleksiyonlarının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="12abd-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="12abd-113">Örnek 2: abonelikteki bir taşıma koleksiyonu adıyla birlikte taşıma koleksiyonunun ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="12abd-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="12abd-114">Abonelikte belirtilen taşıma koleksiyonu adıyla birlikte taşıma koleksiyonunun ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="12abd-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="12abd-115">Örnek 3: abonelikteki belirtilen kaynak grubu adıyla birlikte taşıma koleksiyonunun ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="12abd-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="12abd-116">Aboneliğin belirtilen kaynak grubu adıyla birlikte taşıma koleksiyonunun ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="12abd-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="12abd-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12abd-117">PARAMETERS</span></span>

### <span data-ttu-id="12abd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12abd-118">-DefaultProfile</span></span>
<span data-ttu-id="12abd-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12abd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12abd-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="12abd-120">-Name</span></span>
<span data-ttu-id="12abd-121">Koleksiyon adını taşıma.</span><span class="sxs-lookup"><span data-stu-id="12abd-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12abd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12abd-122">-ResourceGroupName</span></span>
<span data-ttu-id="12abd-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="12abd-123">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12abd-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="12abd-124">-SubscriptionId</span></span>
<span data-ttu-id="12abd-125">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="12abd-125">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12abd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12abd-126">CommonParameters</span></span>
<span data-ttu-id="12abd-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12abd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12abd-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="12abd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12abd-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12abd-129">INPUTS</span></span>

## <span data-ttu-id="12abd-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12abd-130">OUTPUTS</span></span>

### <span data-ttu-id="12abd-131">Microsoft. Azure. PowerShell. cmdlet. Kaynaktaşıyıcısı. modeller. Api20191001Preview. ımovecollection</span><span class="sxs-lookup"><span data-stu-id="12abd-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="12abd-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12abd-132">NOTES</span></span>

<span data-ttu-id="12abd-133">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="12abd-133">ALIASES</span></span>

## <span data-ttu-id="12abd-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12abd-134">RELATED LINKS</span></span>


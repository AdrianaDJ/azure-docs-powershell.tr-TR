---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268825"
---
# <span data-ttu-id="d84e6-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="d84e6-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="d84e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d84e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d84e6-103">Taşıma koleksiyonundaki Taşıveresoallerin bağımlılıklarını hesaplar, çözümler ve doğrular.</span><span class="sxs-lookup"><span data-stu-id="d84e6-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="d84e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d84e6-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d84e6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d84e6-105">DESCRIPTION</span></span>
<span data-ttu-id="d84e6-106">Taşıma koleksiyonundaki Taşıveresoallerin bağımlılıklarını hesaplar, çözümler ve doğrular.</span><span class="sxs-lookup"><span data-stu-id="d84e6-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="d84e6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d84e6-107">EXAMPLES</span></span>

### <span data-ttu-id="d84e6-108">Örnek 1: taşıma koleksiyonundaki taşıveresoaldaları hesaplar, çözümler ve doğrular.</span><span class="sxs-lookup"><span data-stu-id="d84e6-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 8/16/2020 2:28:18 PM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveCollections/PS-ce
                 ntralus-westcentralus-demoRM/operations/bce85a10-1ff3-4815-a677-7b188f7b441a
Message        : The resolve dependencies operation of one ore more resources has failed. Check the move status of the resource for more details. 
Possible Causes: The resolve dependencies operation of one ore more resources has failed.
Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : bce85a10-1ff3-4815-a677-7b188f7b441a
Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/16/2020 2:28:16 PM
Status         : Succeeded
```

<span data-ttu-id="d84e6-109">Taşıma koleksiyonundaki taşıveresoallerin bağımlılıklarını hesaplar, çözümler ve doğrular.</span><span class="sxs-lookup"><span data-stu-id="d84e6-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="d84e6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d84e6-110">PARAMETERS</span></span>

### <span data-ttu-id="d84e6-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="d84e6-111">-AsJob</span></span>
<span data-ttu-id="d84e6-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="d84e6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d84e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84e6-113">-DefaultProfile</span></span>
<span data-ttu-id="d84e6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d84e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d84e6-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="d84e6-115">-MoveCollectionName</span></span>
<span data-ttu-id="d84e6-116">Koleksiyon adını taşıma.</span><span class="sxs-lookup"><span data-stu-id="d84e6-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="d84e6-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d84e6-117">-NoWait</span></span>
<span data-ttu-id="d84e6-118">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="d84e6-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d84e6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d84e6-119">-ResourceGroupName</span></span>
<span data-ttu-id="d84e6-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d84e6-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="d84e6-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d84e6-121">-SubscriptionId</span></span>
<span data-ttu-id="d84e6-122">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d84e6-122">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84e6-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="d84e6-123">-Confirm</span></span>
<span data-ttu-id="d84e6-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d84e6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d84e6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d84e6-125">-WhatIf</span></span>
<span data-ttu-id="d84e6-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d84e6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d84e6-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d84e6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d84e6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84e6-128">CommonParameters</span></span>
<span data-ttu-id="d84e6-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d84e6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84e6-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d84e6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84e6-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d84e6-131">INPUTS</span></span>

## <span data-ttu-id="d84e6-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d84e6-132">OUTPUTS</span></span>

### <span data-ttu-id="d84e6-133">Microsoft. Azure. PowerShell. cmdlet. Kaynaktaşıyıcısı. modeller. Api20191001Preview. ıoperationstatus</span><span class="sxs-lookup"><span data-stu-id="d84e6-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="d84e6-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d84e6-134">NOTES</span></span>

<span data-ttu-id="d84e6-135">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d84e6-135">ALIASES</span></span>

## <span data-ttu-id="d84e6-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d84e6-136">RELATED LINKS</span></span>


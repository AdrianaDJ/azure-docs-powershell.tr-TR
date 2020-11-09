---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324316"
---
# <span data-ttu-id="498ba-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="498ba-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="498ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="498ba-102">SYNOPSIS</span></span>
<span data-ttu-id="498ba-103">Taşıma koleksiyonunu siler.</span><span class="sxs-lookup"><span data-stu-id="498ba-103">Deletes a move collection.</span></span>

## <span data-ttu-id="498ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="498ba-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="498ba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="498ba-105">DESCRIPTION</span></span>
<span data-ttu-id="498ba-106">Taşıma koleksiyonunu siler.</span><span class="sxs-lookup"><span data-stu-id="498ba-106">Deletes a move collection.</span></span>

## <span data-ttu-id="498ba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="498ba-107">EXAMPLES</span></span>

### <span data-ttu-id="498ba-108">Örnek 1: belirtilen abonelikten taşıma koleksiyonunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="498ba-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/12/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                    ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866d6
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/12/2020 3:27:27 PM
    Status         : Succeeded
```

<span data-ttu-id="498ba-109">Belirtilen abonelikten taşıma koleksiyonunu kaldırın.</span><span class="sxs-lookup"><span data-stu-id="498ba-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="498ba-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="498ba-110">PARAMETERS</span></span>

### <span data-ttu-id="498ba-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="498ba-111">-AsJob</span></span>
<span data-ttu-id="498ba-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="498ba-112">Run the command as a job</span></span>

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

### <span data-ttu-id="498ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498ba-113">-DefaultProfile</span></span>
<span data-ttu-id="498ba-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="498ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="498ba-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="498ba-115">-Name</span></span>
<span data-ttu-id="498ba-116">Koleksiyon adını taşıma.</span><span class="sxs-lookup"><span data-stu-id="498ba-116">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498ba-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="498ba-117">-NoWait</span></span>
<span data-ttu-id="498ba-118">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="498ba-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="498ba-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="498ba-119">-PassThru</span></span>
<span data-ttu-id="498ba-120">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="498ba-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="498ba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="498ba-121">-ResourceGroupName</span></span>
<span data-ttu-id="498ba-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="498ba-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="498ba-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="498ba-123">-SubscriptionId</span></span>
<span data-ttu-id="498ba-124">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="498ba-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="498ba-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="498ba-125">-Confirm</span></span>
<span data-ttu-id="498ba-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="498ba-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="498ba-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="498ba-127">-WhatIf</span></span>
<span data-ttu-id="498ba-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="498ba-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="498ba-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="498ba-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="498ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498ba-130">CommonParameters</span></span>
<span data-ttu-id="498ba-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="498ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498ba-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="498ba-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498ba-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="498ba-133">INPUTS</span></span>

## <span data-ttu-id="498ba-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="498ba-134">OUTPUTS</span></span>

### <span data-ttu-id="498ba-135">Microsoft. Azure. PowerShell. cmdlet. Kaynaktaşıyıcısı. modeller. Api20191001Preview. ıoperationstatus</span><span class="sxs-lookup"><span data-stu-id="498ba-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="498ba-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="498ba-136">NOTES</span></span>

<span data-ttu-id="498ba-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="498ba-137">ALIASES</span></span>

## <span data-ttu-id="498ba-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="498ba-138">RELATED LINKS</span></span>


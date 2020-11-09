---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324313"
---
# <span data-ttu-id="1f2a7-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="1f2a7-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="1f2a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f2a7-102">SYNOPSIS</span></span>
<span data-ttu-id="1f2a7-103">Taşıma koleksiyonundan taşıma kaynağı siler.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="1f2a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f2a7-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1f2a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f2a7-105">DESCRIPTION</span></span>
<span data-ttu-id="1f2a7-106">Taşıma koleksiyonundan taşıma kaynağı siler.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="1f2a7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f2a7-107">EXAMPLES</span></span>

### <span data-ttu-id="1f2a7-108">Örnek 1: kaynağı taşı koleksiyonundan kaldırma</span><span class="sxs-lookup"><span data-stu-id="1f2a7-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="1f2a7-109">Kaynağı belirtilen aboneliğin taşıma koleksiyonundan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="1f2a7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f2a7-110">PARAMETERS</span></span>

### <span data-ttu-id="1f2a7-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="1f2a7-111">-AsJob</span></span>
<span data-ttu-id="1f2a7-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="1f2a7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1f2a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f2a7-113">-DefaultProfile</span></span>
<span data-ttu-id="1f2a7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f2a7-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="1f2a7-115">-MoveCollectionName</span></span>
<span data-ttu-id="1f2a7-116">Koleksiyon adını taşıma.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="1f2a7-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f2a7-117">-Name</span></span>
<span data-ttu-id="1f2a7-118">Kaynak adını taşı.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f2a7-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1f2a7-119">-NoWait</span></span>
<span data-ttu-id="1f2a7-120">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="1f2a7-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1f2a7-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1f2a7-121">-PassThru</span></span>
<span data-ttu-id="1f2a7-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="1f2a7-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1f2a7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f2a7-123">-ResourceGroupName</span></span>
<span data-ttu-id="1f2a7-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="1f2a7-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1f2a7-125">-SubscriptionId</span></span>
<span data-ttu-id="1f2a7-126">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="1f2a7-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="1f2a7-127">-Confirm</span></span>
<span data-ttu-id="1f2a7-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f2a7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f2a7-129">-WhatIf</span></span>
<span data-ttu-id="1f2a7-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f2a7-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f2a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f2a7-132">CommonParameters</span></span>
<span data-ttu-id="1f2a7-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f2a7-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1f2a7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f2a7-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f2a7-135">INPUTS</span></span>

## <span data-ttu-id="1f2a7-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f2a7-136">OUTPUTS</span></span>

### <span data-ttu-id="1f2a7-137">Microsoft. Azure. PowerShell. cmdlet. Kaynaktaşıyıcısı. modeller. Api20191001Preview. ıoperationstatus</span><span class="sxs-lookup"><span data-stu-id="1f2a7-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="1f2a7-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f2a7-138">NOTES</span></span>

<span data-ttu-id="1f2a7-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1f2a7-139">ALIASES</span></span>

## <span data-ttu-id="1f2a7-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f2a7-140">RELATED LINKS</span></span>


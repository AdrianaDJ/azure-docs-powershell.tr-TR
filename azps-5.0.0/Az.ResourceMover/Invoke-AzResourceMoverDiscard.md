---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324328"
---
# <span data-ttu-id="b2051-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="b2051-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="b2051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2051-102">SYNOPSIS</span></span>
<span data-ttu-id="b2051-103">İstek gövdesine dahil edilen kaynak kümesini atar.</span><span class="sxs-lookup"><span data-stu-id="b2051-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="b2051-104">At işlemi, moveState ' CommitPending ' veya ' DiscardFailed ' içindeki moveResource 'da tetiklenir, moveResource moveState 'in başarılı bir şekilde tamamlanmasında MovePending 'a geçiş yapılır.</span><span class="sxs-lookup"><span data-stu-id="b2051-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="b2051-105">Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.</span><span class="sxs-lookup"><span data-stu-id="b2051-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b2051-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2051-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b2051-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2051-107">DESCRIPTION</span></span>
<span data-ttu-id="b2051-108">İstek gövdesine dahil edilen kaynak kümesini atar.</span><span class="sxs-lookup"><span data-stu-id="b2051-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="b2051-109">At işlemi, moveState ' CommitPending ' veya ' DiscardFailed ' içindeki moveResource 'da tetiklenir, moveResource moveState 'in başarılı bir şekilde tamamlanmasında MovePending 'a geçiş yapılır.</span><span class="sxs-lookup"><span data-stu-id="b2051-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="b2051-110">Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.</span><span class="sxs-lookup"><span data-stu-id="b2051-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b2051-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2051-111">EXAMPLES</span></span>

### <span data-ttu-id="b2051-112">Örnek 1: kaynakları atmadan önce bağımlıları doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="b2051-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') -ValidateOnly

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 9:44:54 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/62861ceb-28c9-4e0c-811b-84692a203181
Message        :
Name           : 62861ceb-28c9-4e0c-811b-84692a203181
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 9:44:54 AM
Status         : Succeeded

```

<span data-ttu-id="b2051-113">Kaynakları atmadan önce bağımlıları doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="b2051-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="b2051-114">Örnek 2: giriş olarak "MoveResource" kullanarak kaynakların taşınmasını atar</span><span class="sxs-lookup"><span data-stu-id="b2051-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:26:51 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/21f99cd3-89a4-4fcb-8b96-40d0572a6377
Message        :
Name           : 21f99cd3-89a4-4fcb-8b96-40d0572a6377
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:26:39 AM
Status         : Succeeded

```

<span data-ttu-id="b2051-115">Giriş olarak "MoveResource adı" kullanarak kaynakların taşınmasını atar.</span><span class="sxs-lookup"><span data-stu-id="b2051-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="b2051-116">Örnek 3: giriş olarak "SourceARMID" kullanarak kaynakların taşınmasını atar</span><span class="sxs-lookup"><span data-stu-id="b2051-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:33:37 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/b842efcd-e5fd-42b0-a277-01ee8225deed
Message        :
Name           : b842efcd-e5fd-42b0-a277-01ee8225deed
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:33:23 AM
Status         : Succeeded


```

<span data-ttu-id="b2051-117">Kaynak olarak "SourceARMID" kullanarak kaynakların taşınmasını atar.</span><span class="sxs-lookup"><span data-stu-id="b2051-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="b2051-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2051-118">PARAMETERS</span></span>

### <span data-ttu-id="b2051-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="b2051-119">-AsJob</span></span>
<span data-ttu-id="b2051-120">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="b2051-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b2051-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2051-121">-DefaultProfile</span></span>
<span data-ttu-id="b2051-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2051-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2051-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="b2051-123">-MoveResource</span></span>
<span data-ttu-id="b2051-124">Kaynak kimliği 'nin listesini alır veya ayarlar, varsayılan olarak, giriş türü Moveresourceınputtype özelliği aracılığıyla değiştirilmedikçe kaynak kimliğini taşımayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="b2051-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2051-125">-Moveresourceınputtype</span><span class="sxs-lookup"><span data-stu-id="b2051-125">-MoveResourceInputType</span></span>
<span data-ttu-id="b2051-126">Kaynak taşıma giriş türünü tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b2051-126">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2051-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2051-127">-Name</span></span>
<span data-ttu-id="b2051-128">Koleksiyon adını taşıma.</span><span class="sxs-lookup"><span data-stu-id="b2051-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="b2051-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b2051-129">-NoWait</span></span>
<span data-ttu-id="b2051-130">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="b2051-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b2051-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2051-131">-ResourceGroupName</span></span>
<span data-ttu-id="b2051-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b2051-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="b2051-133">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b2051-133">-SubscriptionId</span></span>
<span data-ttu-id="b2051-134">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b2051-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="b2051-135">-Yalnızca Validate</span><span class="sxs-lookup"><span data-stu-id="b2051-135">-ValidateOnly</span></span>
<span data-ttu-id="b2051-136">İşlemin yalnızca önkoşul çalıştırması gerekip gerekmediğini belirten değeri alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b2051-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="b2051-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="b2051-137">-Confirm</span></span>
<span data-ttu-id="b2051-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b2051-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2051-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2051-139">-WhatIf</span></span>
<span data-ttu-id="b2051-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b2051-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2051-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b2051-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2051-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2051-142">CommonParameters</span></span>
<span data-ttu-id="b2051-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2051-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2051-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b2051-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2051-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2051-145">INPUTS</span></span>

## <span data-ttu-id="b2051-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2051-146">OUTPUTS</span></span>

### <span data-ttu-id="b2051-147">Microsoft. Azure. PowerShell. cmdlet. Kaynaktaşıyıcısı. modeller. Api20191001Preview. ıoperationstatus</span><span class="sxs-lookup"><span data-stu-id="b2051-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="b2051-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2051-148">NOTES</span></span>

<span data-ttu-id="b2051-149">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b2051-149">ALIASES</span></span>

## <span data-ttu-id="b2051-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2051-150">RELATED LINKS</span></span>


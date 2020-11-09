---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324325"
---
# <span data-ttu-id="eb32b-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="eb32b-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="eb32b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb32b-102">SYNOPSIS</span></span>
<span data-ttu-id="eb32b-103">İstek gövdesine dahil edilen kaynak kümesini taşıma.</span><span class="sxs-lookup"><span data-stu-id="eb32b-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="eb32b-104">Taşıma işlemi, moveResource 'ın Slaytbekliyor ' veya ' MoveFailed 'tekilerilerilerilerilerileriyle tetiklenir, bu da moveResource.</span><span class="sxs-lookup"><span data-stu-id="eb32b-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="eb32b-105">Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.</span><span class="sxs-lookup"><span data-stu-id="eb32b-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="eb32b-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb32b-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eb32b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb32b-107">DESCRIPTION</span></span>
<span data-ttu-id="eb32b-108">İstek gövdesine dahil edilen kaynak kümesini taşıma.</span><span class="sxs-lookup"><span data-stu-id="eb32b-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="eb32b-109">Taşıma işlemi, moveResource 'ın Slaytbekliyor ' veya ' MoveFailed 'tekilerilerilerilerilerileriyle tetiklenir, bu da moveResource.</span><span class="sxs-lookup"><span data-stu-id="eb32b-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="eb32b-110">Kullanıcıya yardımcı olmak için, yalnızca validateOnly özelliği true olarak ayarlanmış olan işlem çağrı yapabilir.</span><span class="sxs-lookup"><span data-stu-id="eb32b-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="eb32b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb32b-111">EXAMPLES</span></span>

### <span data-ttu-id="eb32b-112">Örnek 1: kaynaklar için taşımayı başlatmadan önce bağımlıları doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="eb32b-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg')  -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:07:36 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Message        :
Name           : 8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:07:35 AM
Status         : Succeeded

```

<span data-ttu-id="eb32b-113">Kaynaklar için taşımayı başlatmadan önce bağımlıları doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="eb32b-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="eb32b-114">Örnek 2: giriş olarak "MoveResource" kullanarak taşıma koleksiyonundaki kaynak kümesi için taşıma Işlemini başlatma</span><span class="sxs-lookup"><span data-stu-id="eb32b-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') 

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:24:21 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/bc30d933-c2b6-47c9-b583-240d375b5864
Message        :
Name           : bc30d933-c2b6-47c9-b583-240d375b5864
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:24:21 AM
Status         : Succeeded

```

<span data-ttu-id="eb32b-115">Giriş olarak "MoveResource adı" kullanarak taşıma koleksiyonundaki kaynak kümesini taşıma işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="eb32b-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="eb32b-116">Örnek 3: giriş olarak "SourceARMID" kullanarak taşıma koleksiyonundaki kaynak kümesini taşıma Işlemini başlatma</span><span class="sxs-lookup"><span data-stu-id="eb32b-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:38:33 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/cbc0f921-de9b-45d5-91da-60e36b841b10
Message        :
Name           : cbc0f921-de9b-45d5-91da-60e36b841b10
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:37:23 AM
Status         : Succeeded

```

<span data-ttu-id="eb32b-117">Giriş olarak "SourceARMID" kullanarak taşıma koleksiyonundaki kaynak kümesini taşıma işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="eb32b-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="eb32b-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb32b-118">PARAMETERS</span></span>

### <span data-ttu-id="eb32b-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="eb32b-119">-AsJob</span></span>
<span data-ttu-id="eb32b-120">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="eb32b-120">Run the command as a job</span></span>

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

### <span data-ttu-id="eb32b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb32b-121">-DefaultProfile</span></span>
<span data-ttu-id="eb32b-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eb32b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb32b-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="eb32b-123">-MoveCollectionName</span></span>
<span data-ttu-id="eb32b-124">Koleksiyon adını taşıma.</span><span class="sxs-lookup"><span data-stu-id="eb32b-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="eb32b-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="eb32b-125">-MoveResource</span></span>
<span data-ttu-id="eb32b-126">Kaynak kimliği 'nin listesini alır veya ayarlar, varsayılan olarak, giriş türü Moveresourceınputtype özelliği aracılığıyla değiştirilmedikçe kaynak kimliğini taşımayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="eb32b-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="eb32b-127">-Moveresourceınputtype</span><span class="sxs-lookup"><span data-stu-id="eb32b-127">-MoveResourceInputType</span></span>
<span data-ttu-id="eb32b-128">Kaynak taşıma giriş türünü tanımlar.</span><span class="sxs-lookup"><span data-stu-id="eb32b-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="eb32b-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eb32b-129">-NoWait</span></span>
<span data-ttu-id="eb32b-130">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="eb32b-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eb32b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb32b-131">-ResourceGroupName</span></span>
<span data-ttu-id="eb32b-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="eb32b-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="eb32b-133">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="eb32b-133">-SubscriptionId</span></span>
<span data-ttu-id="eb32b-134">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="eb32b-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="eb32b-135">-Yalnızca Validate</span><span class="sxs-lookup"><span data-stu-id="eb32b-135">-ValidateOnly</span></span>
<span data-ttu-id="eb32b-136">İşlemin yalnızca önkoşul çalıştırması gerekip gerekmediğini belirten değeri alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="eb32b-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="eb32b-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb32b-137">-Confirm</span></span>
<span data-ttu-id="eb32b-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb32b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb32b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb32b-139">-WhatIf</span></span>
<span data-ttu-id="eb32b-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb32b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb32b-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb32b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb32b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb32b-142">CommonParameters</span></span>
<span data-ttu-id="eb32b-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb32b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb32b-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eb32b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb32b-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb32b-145">INPUTS</span></span>

## <span data-ttu-id="eb32b-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb32b-146">OUTPUTS</span></span>

### <span data-ttu-id="eb32b-147">Microsoft. Azure. PowerShell. cmdlet. Kaynaktaşıyıcısı. modeller. Api20191001Preview. ıoperationstatus</span><span class="sxs-lookup"><span data-stu-id="eb32b-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="eb32b-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb32b-148">NOTES</span></span>

<span data-ttu-id="eb32b-149">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="eb32b-149">ALIASES</span></span>

## <span data-ttu-id="eb32b-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb32b-150">RELATED LINKS</span></span>


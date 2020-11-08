---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278220"
---
# <span data-ttu-id="d366b-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="d366b-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="d366b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d366b-102">SYNOPSIS</span></span>
<span data-ttu-id="d366b-103">Taşıma koleksiyonundaki bir taşıma kaynağı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d366b-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="d366b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d366b-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d366b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d366b-105">DESCRIPTION</span></span>
<span data-ttu-id="d366b-106">Taşıma koleksiyonundaki bir taşıma kaynağı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d366b-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="d366b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d366b-107">EXAMPLES</span></span>

### <span data-ttu-id="d366b-108">Örnek 1: taşıma koleksiyonuna kaynak ekleme.</span><span class="sxs-lookup"><span data-stu-id="d366b-108">Example 1: Adding a resource to the move collection.</span></span>
```powershell
PS C:\> Add-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM" -SourceId "/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM" -Name PSDemoVM -ResourceSettingResourceType "Microsoft.Compute/virtualMachines" -ResourceSettingTargetResourceName PSDemoVM

Output:

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migr
                                          ate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          : DependencyComputationPending
MoveStatusDetail                        : {}
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       : The dependency computation is not completed for resource - /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resou
                                          rceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM.
                                              Possible Causes: Dependency computation is pending for resource.
                                              Recommended Action: Validate dependencies to compute the dependencies.

MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachi
                                          nes/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type          

```

<span data-ttu-id="d366b-109">Belirtilen abonelikteki taşıma koleksiyonuna kaynak ekleme.</span><span class="sxs-lookup"><span data-stu-id="d366b-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="d366b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d366b-110">PARAMETERS</span></span>

### <span data-ttu-id="d366b-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="d366b-111">-AsJob</span></span>
<span data-ttu-id="d366b-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="d366b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d366b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d366b-113">-DefaultProfile</span></span>
<span data-ttu-id="d366b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d366b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d366b-115">-Bağımlılar</span><span class="sxs-lookup"><span data-stu-id="d366b-115">-DependsOnOverride</span></span>
<span data-ttu-id="d366b-116">Kaynak bağımlılıklarını taşıma geçersiz kılmalarını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d366b-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="d366b-117">Oluşturmak için, BAĞıMLıDEĞER GEÇERSIZ kılma özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d366b-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResourceDependencyOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d366b-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="d366b-118">-ExistingTargetId</span></span>
<span data-ttu-id="d366b-119">Kaynağın varolan hedef ARM kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d366b-119">Gets or sets the existing target ARM Id of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d366b-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="d366b-120">-MoveCollectionName</span></span>
<span data-ttu-id="d366b-121">Koleksiyon adını taşıma.</span><span class="sxs-lookup"><span data-stu-id="d366b-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="d366b-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d366b-122">-Name</span></span>
<span data-ttu-id="d366b-123">Kaynak adını taşı.</span><span class="sxs-lookup"><span data-stu-id="d366b-123">The Move Resource Name.</span></span>

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

### <span data-ttu-id="d366b-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d366b-124">-NoWait</span></span>
<span data-ttu-id="d366b-125">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="d366b-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d366b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d366b-126">-ResourceGroupName</span></span>
<span data-ttu-id="d366b-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d366b-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="d366b-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="d366b-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="d366b-129">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="d366b-129">The resource type.</span></span>
<span data-ttu-id="d366b-130">Örneğin, değer Microsoft. COMPUTE/virtualMachines olabilir.</span><span class="sxs-lookup"><span data-stu-id="d366b-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d366b-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="d366b-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="d366b-132">Hedef kaynak adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d366b-132">Gets or sets the target Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d366b-133">-SourceID</span><span class="sxs-lookup"><span data-stu-id="d366b-133">-SourceId</span></span>
<span data-ttu-id="d366b-134">Kaynağın kaynak ARM kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d366b-134">Gets or sets the Source ARM Id of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d366b-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="d366b-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="d366b-136">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="d366b-136">The resource type.</span></span>
<span data-ttu-id="d366b-137">Örneğin, değer Microsoft. COMPUTE/virtualMachines olabilir.</span><span class="sxs-lookup"><span data-stu-id="d366b-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d366b-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="d366b-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="d366b-139">Hedef kaynak adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d366b-139">Gets or sets the target Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d366b-140">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d366b-140">-SubscriptionId</span></span>
<span data-ttu-id="d366b-141">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d366b-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="d366b-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="d366b-142">-Confirm</span></span>
<span data-ttu-id="d366b-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d366b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d366b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d366b-144">-WhatIf</span></span>
<span data-ttu-id="d366b-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d366b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d366b-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d366b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d366b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d366b-147">CommonParameters</span></span>
<span data-ttu-id="d366b-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d366b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d366b-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d366b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d366b-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d366b-150">INPUTS</span></span>

## <span data-ttu-id="d366b-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d366b-151">OUTPUTS</span></span>

### <span data-ttu-id="d366b-152">Microsoft. Azure. PowerShell. cmdlet. Kaynaktaşıyıcısı. modeller. Api20191001Preview. ımoveresource</span><span class="sxs-lookup"><span data-stu-id="d366b-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="d366b-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d366b-153">NOTES</span></span>

<span data-ttu-id="d366b-154">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d366b-154">ALIASES</span></span>

<span data-ttu-id="d366b-155">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="d366b-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d366b-156">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d366b-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d366b-157">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d366b-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d366b-158">BAĞıMLıNO geçersiz KıLMA <IMoveResourceDependencyOverride [] >: kaynak taşımayı taşıma geçersiz kılmalarını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d366b-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="d366b-159">`[Id <String>]`: Bağımlı kaynağın ARM KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d366b-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="d366b-160">`[TargetId <String>]`: MoveResource veya bağımlı kaynağın kaynak ARM KIMLIĞI 'nin kaynak kolu kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d366b-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="d366b-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d366b-161">RELATED LINKS</span></span>


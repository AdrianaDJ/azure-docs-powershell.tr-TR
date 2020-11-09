---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
ms.openlocfilehash: e0ce7e46e8105048d58ee8a4334eaf098b40399c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324337"
---
# <span data-ttu-id="28543-101">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="28543-101">Get-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="28543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28543-102">SYNOPSIS</span></span>
<span data-ttu-id="28543-103">Kaynağı taşı.</span><span class="sxs-lookup"><span data-stu-id="28543-103">Gets the Move Resource.</span></span>

## <span data-ttu-id="28543-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28543-104">SYNTAX</span></span>

### <span data-ttu-id="28543-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="28543-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="28543-106">Al</span><span class="sxs-lookup"><span data-stu-id="28543-106">Get</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="28543-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="28543-107">DESCRIPTION</span></span>
<span data-ttu-id="28543-108">Kaynağı taşı.</span><span class="sxs-lookup"><span data-stu-id="28543-108">Gets the Move Resource.</span></span>

## <span data-ttu-id="28543-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28543-109">EXAMPLES</span></span>

### <span data-ttu-id="28543-110">Örnek 1: taşıma koleksiyonundaki tüm kaynakların ayrıntılarını alma.</span><span class="sxs-lookup"><span data-stu-id="28543-110">Example 1: Get details of all the resources in the Move collection.</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM          

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.networ
                                          k/publicipaddresses/psdemovm-ip, /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psd
                                          emorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet, /subscriptions/e80eb9fa-c996-4435-aa32
                                          -5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemovm62
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : MovePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemovm62
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Network/networkInterfaces
ResourceSettingTargetResourceName       : psdemovm62
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network
                                          /networkInterfaces/psdemovm62
SourceResourceSettingResourceType       : Microsoft.Network/networkInterfaces
SourceResourceSettingTargetResourceName : psdemovm62
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemorm
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : CommitPending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemorm
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : resourceGroups
ResourceSettingTargetResourceName       : psdemorm2
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm
SourceResourceSettingResourceType       : resourceGroups
SourceResourceSettingTargetResourceName : psdemorm
Target                                  :
TargetId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psdemorm2
Type                                    :

```

<span data-ttu-id="28543-111">Taşıma koleksiyonundaki tüm kaynakların ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="28543-111">Get details of all the resources in the move collection.</span></span>

### <span data-ttu-id="28543-112">Örnek 2: kaynak adını taşı kullanarak taşıma koleksiyonundaki belirli bir kaynağın ayrıntılarını alma.</span><span class="sxs-lookup"><span data-stu-id="28543-112">Example 2: Get details of a specific resources in a Move collection using move resource name .</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Name PSDemoVM   
                                                     
Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="28543-113">Kaynak adını taşı kullanarak taşıma koleksiyonundaki belirli bir kaynağın ayrıntılarını alma.</span><span class="sxs-lookup"><span data-stu-id="28543-113">Get details of a specific resources in a Move collection using move resource name .</span></span>

### <span data-ttu-id="28543-114">Örnek 3: SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState gibi filtreler kullanarak, taşıma koleksiyonundaki belirli bir kaynağın ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="28543-114">Example 3:Get details of a specific resources in a Move collection using filters such as : SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Filter "Properties/SourceResourceName eq 'PSDemoVM'"

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="28543-115">Armid, moveStatusMoveState gibi filtre kullanarak, taşıma koleksiyonundaki belirli bir kaynağın ayrıntılarını alın.</span><span class="sxs-lookup"><span data-stu-id="28543-115">Get details of a specific resources in a Move collection using filter such as armid ,moveStatusMoveState(verify) etc.</span></span>

## <span data-ttu-id="28543-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28543-116">PARAMETERS</span></span>

### <span data-ttu-id="28543-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28543-117">-DefaultProfile</span></span>
<span data-ttu-id="28543-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28543-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28543-119">-Filtre</span><span class="sxs-lookup"><span data-stu-id="28543-119">-Filter</span></span>
<span data-ttu-id="28543-120">İşlemde uygulanacak filtre.</span><span class="sxs-lookup"><span data-stu-id="28543-120">The filter to apply on the operation.</span></span>
<span data-ttu-id="28543-121">Örneğin, $filter = Özellikler/ProvisioningState EQ ' tamamlandı ' kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="28543-121">For example, you can use $filter=Properties/ProvisioningState eq 'Succeeded'.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28543-122">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="28543-122">-MoveCollectionName</span></span>
<span data-ttu-id="28543-123">Koleksiyon adını taşıma.</span><span class="sxs-lookup"><span data-stu-id="28543-123">The Move Collection Name.</span></span>

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

### <span data-ttu-id="28543-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="28543-124">-Name</span></span>
<span data-ttu-id="28543-125">Kaynak adını taşı.</span><span class="sxs-lookup"><span data-stu-id="28543-125">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28543-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28543-126">-ResourceGroupName</span></span>
<span data-ttu-id="28543-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="28543-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="28543-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="28543-128">-SubscriptionId</span></span>
<span data-ttu-id="28543-129">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="28543-129">The Subscription ID.</span></span>

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

### <span data-ttu-id="28543-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28543-130">CommonParameters</span></span>
<span data-ttu-id="28543-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28543-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28543-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="28543-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28543-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28543-133">INPUTS</span></span>

## <span data-ttu-id="28543-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28543-134">OUTPUTS</span></span>

### <span data-ttu-id="28543-135">Microsoft. Azure. PowerShell. cmdlet. Kaynaktaşıyıcısı. modeller. Api20191001Preview. ımoveresource</span><span class="sxs-lookup"><span data-stu-id="28543-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="28543-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28543-136">NOTES</span></span>

<span data-ttu-id="28543-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="28543-137">ALIASES</span></span>

## <span data-ttu-id="28543-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28543-138">RELATED LINKS</span></span>


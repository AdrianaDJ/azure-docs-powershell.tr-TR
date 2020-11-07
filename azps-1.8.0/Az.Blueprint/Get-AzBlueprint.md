---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: e559e3804c5a89648df526ab3f4fc23f8cc70b77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761436"
---
# <span data-ttu-id="09147-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="09147-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="09147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09147-102">SYNOPSIS</span></span>
<span data-ttu-id="09147-103">Bir veya daha fazla grafik tanımı alın.</span><span class="sxs-lookup"><span data-stu-id="09147-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="09147-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09147-104">SYNTAX</span></span>

### <span data-ttu-id="09147-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="09147-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09147-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="09147-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09147-107">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="09147-107">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09147-108">Bysubscriptionnameandlatestyayımlandı</span><span class="sxs-lookup"><span data-stu-id="09147-108">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09147-109">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="09147-109">ManagementGroupScope</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09147-110">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="09147-110">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09147-111">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="09147-111">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09147-112">Bymanagementgroupnameandlatestyayınlanmış</span><span class="sxs-lookup"><span data-stu-id="09147-112">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09147-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="09147-113">DESCRIPTION</span></span>
<span data-ttu-id="09147-114">Bir veya daha fazla grafik tanımı alın.</span><span class="sxs-lookup"><span data-stu-id="09147-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="09147-115">Blueprint tanımları Yönetim grubunda veya abonelik kapsamında mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="09147-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="09147-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09147-116">EXAMPLES</span></span>

### <span data-ttu-id="09147-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="09147-117">Example 1</span></span>
```powershell
PS> Get-AzBlueprint

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
DefinitionLocationId : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="09147-118">Geçerli aboneliğin ve aboneliğin yönetim grubu hiyerarşisindeki şeması tanımlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="09147-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="09147-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="09147-119">Example 2</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId"

Name                 : PS-MG-BlueprintDefinition
Id                   : /providers/Microsoft.Management/managementGroups/myManagementGroupId/providers/Microsoft.Blueprint/blueprints/PS-MG-BlueprintDefinition
DefinitionLocationId : myManagementGroupId
Versions             : {1.0, 2.0, 3.0, 4.0}
TimeCreated          : 2019-03-04
TargetScope          : Subscription
Parameters           : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue, [Usergrouporapplicationname]:Contributor_RoleAssignmentName,
                       [Usergrouporapplicationname]:Owner_RoleAssignmentName}
ResourceGroups       : {ResourceGroup, ResourceGroup2}
```

<span data-ttu-id="09147-120">Belirtilen yönetim grubundaki şeması tanımlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="09147-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="09147-121">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="09147-121">Example 3</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
DefinitionLocationId : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="09147-122">Belirtilen aboneliğin ve aboneliğin yönetim grubu hiyerarşisindeki şeması tanımlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="09147-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="09147-123">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="09147-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="09147-124">Belirtilen abonelikteki belirtilen adda şeması tanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="09147-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="09147-125">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="09147-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="09147-126">Belirtilen yönetim grubundaki belirtilen ad ve sürümle şeması tanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="09147-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="09147-127">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="09147-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="09147-128">Belirtilen yönetim grubunda verilen adda en son yayınlanan şeması tanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="09147-128">Get the lastest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="09147-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09147-129">PARAMETERS</span></span>

### <span data-ttu-id="09147-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09147-130">-DefaultProfile</span></span>
<span data-ttu-id="09147-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09147-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09147-132">-Latestyayınlanmış</span><span class="sxs-lookup"><span data-stu-id="09147-132">-LatestPublished</span></span>
<span data-ttu-id="09147-133">En son yayınlanan mavi yazdırma tanımı bayrağı.</span><span class="sxs-lookup"><span data-stu-id="09147-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="09147-134">Ayarlandığında, yürütme, şeması tanımının en son yayınlanan sürümünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="09147-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="09147-135">Varsayılan olarak false olur.</span><span class="sxs-lookup"><span data-stu-id="09147-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySubscriptionNameAndLatestPublished, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09147-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="09147-136">-ManagementGroupId</span></span>
<span data-ttu-id="09147-137">Şeması tanımının kaydedildiği yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="09147-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09147-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="09147-138">-Name</span></span>
<span data-ttu-id="09147-139">Blueprint tanım adı.</span><span class="sxs-lookup"><span data-stu-id="09147-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09147-140">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="09147-140">-SubscriptionId</span></span>
<span data-ttu-id="09147-141">Şeması tanımının kaydedildiği abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="09147-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09147-142">-Version</span><span class="sxs-lookup"><span data-stu-id="09147-142">-Version</span></span>
<span data-ttu-id="09147-143">Şeması tanım sürümü yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="09147-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionNameAndVersion, ByManagementGroupNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09147-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09147-144">CommonParameters</span></span>
<span data-ttu-id="09147-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09147-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09147-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09147-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09147-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09147-147">INPUTS</span></span>

### <span data-ttu-id="09147-148">System. String</span><span class="sxs-lookup"><span data-stu-id="09147-148">System.String</span></span>

## <span data-ttu-id="09147-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09147-149">OUTPUTS</span></span>

### <span data-ttu-id="09147-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="09147-150">System.Object</span></span>
## <span data-ttu-id="09147-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09147-151">NOTES</span></span>

## <span data-ttu-id="09147-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09147-152">RELATED LINKS</span></span>

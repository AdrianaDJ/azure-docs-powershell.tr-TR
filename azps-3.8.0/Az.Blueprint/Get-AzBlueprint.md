---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: 512efeff7d89c8c9a95a3db8bbfe755564f8dadc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097854"
---
# <span data-ttu-id="53afb-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="53afb-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="53afb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53afb-102">SYNOPSIS</span></span>
<span data-ttu-id="53afb-103">Bir veya daha fazla grafik tanımı alın.</span><span class="sxs-lookup"><span data-stu-id="53afb-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="53afb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="53afb-104">SYNTAX</span></span>

### <span data-ttu-id="53afb-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="53afb-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53afb-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="53afb-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53afb-107">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="53afb-107">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53afb-108">Bysubscriptionnameandlatestyayımlandı</span><span class="sxs-lookup"><span data-stu-id="53afb-108">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53afb-109">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="53afb-109">ManagementGroupScope</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53afb-110">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="53afb-110">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53afb-111">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="53afb-111">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53afb-112">Bymanagementgroupnameandlatestyayınlanmış</span><span class="sxs-lookup"><span data-stu-id="53afb-112">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53afb-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="53afb-113">DESCRIPTION</span></span>
<span data-ttu-id="53afb-114">Bir veya daha fazla grafik tanımı alın.</span><span class="sxs-lookup"><span data-stu-id="53afb-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="53afb-115">Blueprint tanımları Yönetim grubunda veya abonelik kapsamında mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="53afb-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="53afb-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="53afb-116">EXAMPLES</span></span>

### <span data-ttu-id="53afb-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="53afb-117">Example 1</span></span>
```powershell
PS> Get-AzBlueprint

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="53afb-118">Geçerli aboneliğin ve aboneliğin yönetim grubu hiyerarşisindeki şeması tanımlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="53afb-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="53afb-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="53afb-119">Example 2</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId"

Name                 : PS-MG-BlueprintDefinition
Id                   : /providers/Microsoft.Management/managementGroups/myManagementGroupId/providers/Microsoft.Blueprint/blueprints/PS-MG-BlueprintDefinition
ManagementGroupId    : myManagementGroupId
Versions             : {1.0, 2.0, 3.0, 4.0}
TimeCreated          : 2019-03-04
TargetScope          : Subscription
Parameters           : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue, [Usergrouporapplicationname]:Contributor_RoleAssignmentName,
                       [Usergrouporapplicationname]:Owner_RoleAssignmentName}
ResourceGroups       : {ResourceGroup, ResourceGroup2}
```

<span data-ttu-id="53afb-120">Belirtilen yönetim grubundaki şeması tanımlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="53afb-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="53afb-121">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="53afb-121">Example 3</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="53afb-122">Belirtilen aboneliğin ve aboneliğin yönetim grubu hiyerarşisindeki şeması tanımlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="53afb-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="53afb-123">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="53afb-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="53afb-124">Belirtilen abonelikteki belirtilen adda şeması tanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="53afb-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="53afb-125">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="53afb-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="53afb-126">Belirtilen yönetim grubundaki belirtilen ad ve sürümle şeması tanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="53afb-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="53afb-127">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="53afb-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="53afb-128">Belirtilen yönetim grubunda verilen adla en son yayınlanan şeması tanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="53afb-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="53afb-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="53afb-129">PARAMETERS</span></span>

### <span data-ttu-id="53afb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53afb-130">-DefaultProfile</span></span>
<span data-ttu-id="53afb-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="53afb-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53afb-132">-Latestyayınlanmış</span><span class="sxs-lookup"><span data-stu-id="53afb-132">-LatestPublished</span></span>
<span data-ttu-id="53afb-133">En son yayınlanan mavi yazdırma tanımı bayrağı.</span><span class="sxs-lookup"><span data-stu-id="53afb-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="53afb-134">Ayarlandığında, yürütme, şeması tanımının en son yayınlanan sürümünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="53afb-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="53afb-135">Varsayılan olarak false olur.</span><span class="sxs-lookup"><span data-stu-id="53afb-135">Defaults to false.</span></span>

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

### <span data-ttu-id="53afb-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="53afb-136">-ManagementGroupId</span></span>
<span data-ttu-id="53afb-137">Şeması tanımının kaydedildiği yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="53afb-137">Management Group Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="53afb-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="53afb-138">-Name</span></span>
<span data-ttu-id="53afb-139">Blueprint tanım adı.</span><span class="sxs-lookup"><span data-stu-id="53afb-139">Blueprint definition name.</span></span>

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

### <span data-ttu-id="53afb-140">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="53afb-140">-SubscriptionId</span></span>
<span data-ttu-id="53afb-141">Şeması tanımının kaydedildiği abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="53afb-141">Subscription Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="53afb-142">-Version</span><span class="sxs-lookup"><span data-stu-id="53afb-142">-Version</span></span>
<span data-ttu-id="53afb-143">Şeması tanım sürümü yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="53afb-143">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="53afb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53afb-144">CommonParameters</span></span>
<span data-ttu-id="53afb-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="53afb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53afb-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53afb-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53afb-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="53afb-147">INPUTS</span></span>

### <span data-ttu-id="53afb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="53afb-148">System.String</span></span>

## <span data-ttu-id="53afb-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="53afb-149">OUTPUTS</span></span>

### <span data-ttu-id="53afb-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="53afb-150">System.Object</span></span>
## <span data-ttu-id="53afb-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="53afb-151">NOTES</span></span>

## <span data-ttu-id="53afb-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="53afb-152">RELATED LINKS</span></span>

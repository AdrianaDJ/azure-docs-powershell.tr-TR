---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: ab383b1fb46759c2369d94d4bb57284ba59cf671
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108480"
---
# <span data-ttu-id="428ba-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="428ba-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="428ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="428ba-102">SYNOPSIS</span></span>
<span data-ttu-id="428ba-103">Bir veya daha fazla grafik tanımı alın.</span><span class="sxs-lookup"><span data-stu-id="428ba-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="428ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="428ba-104">SYNTAX</span></span>

### <span data-ttu-id="428ba-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="428ba-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="428ba-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="428ba-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="428ba-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="428ba-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="428ba-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="428ba-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="428ba-109">Bymanagementgroupnameandlatestyayınlanmış</span><span class="sxs-lookup"><span data-stu-id="428ba-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="428ba-110">Bysubscriptionnameandlatestyayımlandı</span><span class="sxs-lookup"><span data-stu-id="428ba-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="428ba-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="428ba-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="428ba-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="428ba-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="428ba-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="428ba-113">DESCRIPTION</span></span>
<span data-ttu-id="428ba-114">Bir veya daha fazla grafik tanımı alın.</span><span class="sxs-lookup"><span data-stu-id="428ba-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="428ba-115">Blueprint tanımları Yönetim grubunda veya abonelik kapsamında mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="428ba-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="428ba-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="428ba-116">EXAMPLES</span></span>

### <span data-ttu-id="428ba-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="428ba-117">Example 1</span></span>
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

<span data-ttu-id="428ba-118">Geçerli aboneliğin ve aboneliğin yönetim grubu hiyerarşisindeki şeması tanımlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="428ba-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="428ba-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="428ba-119">Example 2</span></span>
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

<span data-ttu-id="428ba-120">Belirtilen yönetim grubundaki şeması tanımlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="428ba-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="428ba-121">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="428ba-121">Example 3</span></span>
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

<span data-ttu-id="428ba-122">Belirtilen aboneliğin ve aboneliğin yönetim grubu hiyerarşisindeki şeması tanımlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="428ba-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="428ba-123">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="428ba-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="428ba-124">Belirtilen abonelikteki belirtilen adda şeması tanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="428ba-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="428ba-125">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="428ba-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="428ba-126">Belirtilen yönetim grubundaki belirtilen ad ve sürümle şeması tanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="428ba-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="428ba-127">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="428ba-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="428ba-128">Belirtilen yönetim grubunda verilen adla en son yayınlanan şeması tanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="428ba-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="428ba-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="428ba-129">PARAMETERS</span></span>

### <span data-ttu-id="428ba-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428ba-130">-DefaultProfile</span></span>
<span data-ttu-id="428ba-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="428ba-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="428ba-132">-Latestyayınlanmış</span><span class="sxs-lookup"><span data-stu-id="428ba-132">-LatestPublished</span></span>
<span data-ttu-id="428ba-133">En son yayınlanan mavi yazdırma tanımı bayrağı.</span><span class="sxs-lookup"><span data-stu-id="428ba-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="428ba-134">Ayarlandığında, yürütme, şeması tanımının en son yayınlanan sürümünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="428ba-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="428ba-135">Varsayılan olarak false olur.</span><span class="sxs-lookup"><span data-stu-id="428ba-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428ba-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="428ba-136">-ManagementGroupId</span></span>
<span data-ttu-id="428ba-137">Şeması tanımının kaydedildiği yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="428ba-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428ba-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="428ba-138">-Name</span></span>
<span data-ttu-id="428ba-139">Blueprint tanım adı.</span><span class="sxs-lookup"><span data-stu-id="428ba-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428ba-140">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="428ba-140">-SubscriptionId</span></span>
<span data-ttu-id="428ba-141">Şeması tanımının kaydedildiği abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="428ba-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428ba-142">-Version</span><span class="sxs-lookup"><span data-stu-id="428ba-142">-Version</span></span>
<span data-ttu-id="428ba-143">Şeması tanım sürümü yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="428ba-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428ba-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428ba-144">CommonParameters</span></span>
<span data-ttu-id="428ba-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="428ba-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428ba-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="428ba-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428ba-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="428ba-147">INPUTS</span></span>

### <span data-ttu-id="428ba-148">System. String</span><span class="sxs-lookup"><span data-stu-id="428ba-148">System.String</span></span>

## <span data-ttu-id="428ba-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="428ba-149">OUTPUTS</span></span>

### <span data-ttu-id="428ba-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="428ba-150">System.Object</span></span>
## <span data-ttu-id="428ba-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="428ba-151">NOTES</span></span>

## <span data-ttu-id="428ba-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="428ba-152">RELATED LINKS</span></span>

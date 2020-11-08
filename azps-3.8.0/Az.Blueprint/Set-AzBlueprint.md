---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 155bf1a7851f6cc8e3283c66297df811738edd2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096466"
---
# <span data-ttu-id="4f191-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="4f191-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="4f191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f191-102">SYNOPSIS</span></span>
<span data-ttu-id="4f191-103">Şeması tanımını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="4f191-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="4f191-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f191-104">SYNTAX</span></span>

### <span data-ttu-id="4f191-105">UpdateBlueprintBySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f191-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f191-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4f191-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f191-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f191-107">DESCRIPTION</span></span>
<span data-ttu-id="4f191-108">Şeması tanımını güncelleyin ve belirtilen abonelik veya yönetim grubunun içine kaydet.</span><span class="sxs-lookup"><span data-stu-id="4f191-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="4f191-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f191-109">EXAMPLES</span></span>

### <span data-ttu-id="4f191-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4f191-110">Example 1</span></span>
```powershell
PS C:\> Set-AzBlueprint -Name MyBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="4f191-111">Yeni parametrelerle bir şeması tanımını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="4f191-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="4f191-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f191-112">PARAMETERS</span></span>

### <span data-ttu-id="4f191-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="4f191-113">-BlueprintFile</span></span>
<span data-ttu-id="4f191-114">Disk üzerindeki bir Blueprint JSON dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="4f191-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f191-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f191-115">-DefaultProfile</span></span>
<span data-ttu-id="4f191-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f191-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f191-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="4f191-117">-ManagementGroupId</span></span>
<span data-ttu-id="4f191-118">Şeması tanımının olduğu veya kaydedileceği yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="4f191-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup, ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f191-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f191-119">-Name</span></span>
<span data-ttu-id="4f191-120">Blueprint tanım adı.</span><span class="sxs-lookup"><span data-stu-id="4f191-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup, ImportBlueprint
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f191-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4f191-121">-SubscriptionId</span></span>
<span data-ttu-id="4f191-122">Şeması tanımının bulunduğu abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="4f191-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, ImportBlueprint, SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f191-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f191-123">-Confirm</span></span>
<span data-ttu-id="4f191-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f191-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f191-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f191-125">-WhatIf</span></span>
<span data-ttu-id="4f191-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f191-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f191-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f191-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f191-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f191-128">CommonParameters</span></span>
<span data-ttu-id="4f191-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f191-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4f191-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f191-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f191-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f191-131">INPUTS</span></span>

### <span data-ttu-id="4f191-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4f191-132">System.String</span></span>

## <span data-ttu-id="4f191-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f191-133">OUTPUTS</span></span>

### <span data-ttu-id="4f191-134">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="4f191-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="4f191-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f191-135">NOTES</span></span>

## <span data-ttu-id="4f191-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f191-136">RELATED LINKS</span></span>

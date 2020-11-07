---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 3213d5dbb981d9cc7d7871ce97f9fd78f375a59a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753113"
---
# <span data-ttu-id="eaf6b-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="eaf6b-101">New-AzBlueprint</span></span>

## <span data-ttu-id="eaf6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaf6b-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf6b-103">Yeni bir şeması tanımı oluşturun ve belirtilen aboneliğe veya yönetim grubuna kaydedin.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="eaf6b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eaf6b-104">SYNTAX</span></span>

### <span data-ttu-id="eaf6b-105">CreateBlueprintBySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eaf6b-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf6b-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="eaf6b-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaf6b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eaf6b-107">DESCRIPTION</span></span>
<span data-ttu-id="eaf6b-108">Yeni bir şeması tanımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="eaf6b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eaf6b-109">EXAMPLES</span></span>

### <span data-ttu-id="eaf6b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eaf6b-110">Example 1</span></span>
```powershell
PS C:\> New-AzBlueprint -Name MyNewBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

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

<span data-ttu-id="eaf6b-111">Belirtilen abonelik içinde yeni bir şeması tanımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="eaf6b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eaf6b-112">PARAMETERS</span></span>

### <span data-ttu-id="eaf6b-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="eaf6b-113">-BlueprintFile</span></span>
<span data-ttu-id="eaf6b-114">Disk üzerindeki bir Blueprint JSON dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf6b-115">-DefaultProfile</span></span>
<span data-ttu-id="eaf6b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaf6b-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="eaf6b-117">-ManagementGroupId</span></span>
<span data-ttu-id="eaf6b-118">Şeması tanımının olduğu veya kaydedileceği yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf6b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="eaf6b-119">-Name</span></span>
<span data-ttu-id="eaf6b-120">Blueprint tanım adı.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf6b-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="eaf6b-121">-SubscriptionId</span></span>
<span data-ttu-id="eaf6b-122">Şeması tanımının bulunduğu abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf6b-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="eaf6b-123">-Confirm</span></span>
<span data-ttu-id="eaf6b-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf6b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf6b-125">-WhatIf</span></span>
<span data-ttu-id="eaf6b-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaf6b-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf6b-128">CommonParameters</span></span>
<span data-ttu-id="eaf6b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="eaf6b-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaf6b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf6b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eaf6b-131">INPUTS</span></span>

### <span data-ttu-id="eaf6b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="eaf6b-132">System.String</span></span>

## <span data-ttu-id="eaf6b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eaf6b-133">OUTPUTS</span></span>

### <span data-ttu-id="eaf6b-134">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="eaf6b-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="eaf6b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eaf6b-135">NOTES</span></span>

## <span data-ttu-id="eaf6b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eaf6b-136">RELATED LINKS</span></span>
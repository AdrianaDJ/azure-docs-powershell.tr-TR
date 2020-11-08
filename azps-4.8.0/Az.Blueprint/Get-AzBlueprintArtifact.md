---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 725dca861c28f0194f800c80bd94d7e17efe15a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108479"
---
# <span data-ttu-id="5f925-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="5f925-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="5f925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f925-102">SYNOPSIS</span></span>
<span data-ttu-id="5f925-103">Bir şeması tanımından yapıları alın.</span><span class="sxs-lookup"><span data-stu-id="5f925-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="5f925-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f925-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f925-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f925-105">DESCRIPTION</span></span>
<span data-ttu-id="5f925-106">Bir şeması tanımından yapıları alın.</span><span class="sxs-lookup"><span data-stu-id="5f925-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="5f925-107">Şeması tanım sürümü belirtilmemişse taslak sürümü alınır.</span><span class="sxs-lookup"><span data-stu-id="5f925-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="5f925-108">Taslak sürümü olmadığı durumlarda, yayımlanan en son şeması tanımı döndürülür.</span><span class="sxs-lookup"><span data-stu-id="5f925-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="5f925-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f925-109">EXAMPLES</span></span>

### <span data-ttu-id="5f925-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5f925-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192
```

<span data-ttu-id="5f925-111">Bir şeması tanımından yapıları alın..</span><span class="sxs-lookup"><span data-stu-id="5f925-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="5f925-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f925-112">PARAMETERS</span></span>

### <span data-ttu-id="5f925-113">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="5f925-113">-Blueprint</span></span>
<span data-ttu-id="5f925-114">Blueprint nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5f925-114">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f925-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="5f925-115">-BlueprintVersion</span></span>
<span data-ttu-id="5f925-116">Tüm yapıları almak için şeması sürümü.</span><span class="sxs-lookup"><span data-stu-id="5f925-116">Version of the blueprint to get the artifacts from.</span></span>

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

### <span data-ttu-id="5f925-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f925-117">-DefaultProfile</span></span>
<span data-ttu-id="5f925-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f925-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f925-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f925-119">-Name</span></span>
<span data-ttu-id="5f925-120">Yapının adı</span><span class="sxs-lookup"><span data-stu-id="5f925-120">Name of the artifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f925-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f925-121">CommonParameters</span></span>
<span data-ttu-id="5f925-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f925-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f925-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f925-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f925-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f925-124">INPUTS</span></span>

### <span data-ttu-id="5f925-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5f925-125">System.String</span></span>

### <span data-ttu-id="5f925-126">Microsoft. Azure. Commands. Blueprint. modeller. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="5f925-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="5f925-127">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="5f925-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="5f925-128">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5f925-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="5f925-129">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5f925-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5f925-130">System. String []</span><span class="sxs-lookup"><span data-stu-id="5f925-130">System.String[]</span></span>

## <span data-ttu-id="5f925-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f925-131">OUTPUTS</span></span>

### <span data-ttu-id="5f925-132">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="5f925-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="5f925-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f925-133">NOTES</span></span>

## <span data-ttu-id="5f925-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f925-134">RELATED LINKS</span></span>

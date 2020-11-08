---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 7a1778ce107e9753f78876aff3a2dfba19e138e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103686"
---
# <span data-ttu-id="46474-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="46474-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="46474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46474-102">SYNOPSIS</span></span>
<span data-ttu-id="46474-103">Bir şeması dosyasını JSON biçiminde bir şeması nesnesine aktarın ve belirtilen abonelik veya yönetim grubunun içine kaydedin.</span><span class="sxs-lookup"><span data-stu-id="46474-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="46474-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46474-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46474-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46474-105">DESCRIPTION</span></span>
<span data-ttu-id="46474-106">Bir şeması tanımını dışlayıcılarla içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="46474-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="46474-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46474-107">EXAMPLES</span></span>

### <span data-ttu-id="46474-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="46474-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="46474-109">Bir şeması tanımını dışlayıcılarla içeri aktarın ve bir abonelik içinde saklayın.</span><span class="sxs-lookup"><span data-stu-id="46474-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="46474-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46474-110">PARAMETERS</span></span>

### <span data-ttu-id="46474-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46474-111">-DefaultProfile</span></span>
<span data-ttu-id="46474-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46474-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46474-113">-Force</span><span class="sxs-lookup"><span data-stu-id="46474-113">-Force</span></span>
<span data-ttu-id="46474-114">True olarak ayarlandığında, yürütme onay sormaz.</span><span class="sxs-lookup"><span data-stu-id="46474-114">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46474-115">-Includealt klasörler</span><span class="sxs-lookup"><span data-stu-id="46474-115">-IncludeSubFolders</span></span>
<span data-ttu-id="46474-116">True olarak ayarlandığında, alt klasörlerdeki yapıt dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="46474-116">When set to true, artifact in the subfolders will be included.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46474-117">-Inputpath</span><span class="sxs-lookup"><span data-stu-id="46474-117">-InputPath</span></span>
<span data-ttu-id="46474-118">Disk üzerindeki bir Blueprint JSON dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="46474-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="46474-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="46474-119">-ManagementGroupId</span></span>
<span data-ttu-id="46474-120">Şeması tanımının olduğu veya kaydedileceği yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="46474-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46474-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="46474-121">-Name</span></span>
<span data-ttu-id="46474-122">Blueprint tanım adı.</span><span class="sxs-lookup"><span data-stu-id="46474-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="46474-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="46474-123">-SubscriptionId</span></span>
<span data-ttu-id="46474-124">Şeması tanımının bulunduğu abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="46474-124">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46474-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46474-125">CommonParameters</span></span>
<span data-ttu-id="46474-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46474-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="46474-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46474-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46474-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46474-128">INPUTS</span></span>

### <span data-ttu-id="46474-129">System. String</span><span class="sxs-lookup"><span data-stu-id="46474-129">System.String</span></span>

## <span data-ttu-id="46474-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46474-130">OUTPUTS</span></span>

### <span data-ttu-id="46474-131">System. String</span><span class="sxs-lookup"><span data-stu-id="46474-131">System.String</span></span>

## <span data-ttu-id="46474-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46474-132">NOTES</span></span>

## <span data-ttu-id="46474-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46474-133">RELATED LINKS</span></span>

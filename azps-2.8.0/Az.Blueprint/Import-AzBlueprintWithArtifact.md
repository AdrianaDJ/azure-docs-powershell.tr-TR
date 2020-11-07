---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 3853cc1785ca0e9f087b1e30870d17d304666df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753118"
---
# <span data-ttu-id="7795d-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="7795d-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="7795d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7795d-102">SYNOPSIS</span></span>
<span data-ttu-id="7795d-103">Bir şeması dosyasını JSON biçiminde bir şeması nesnesine aktarın ve belirtilen abonelik veya yönetim grubunun içine kaydedin.</span><span class="sxs-lookup"><span data-stu-id="7795d-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="7795d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7795d-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7795d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7795d-105">DESCRIPTION</span></span>
<span data-ttu-id="7795d-106">Bir şeması tanımını dışlayıcılarla içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="7795d-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="7795d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7795d-107">EXAMPLES</span></span>

### <span data-ttu-id="7795d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7795d-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="7795d-109">Bir şeması tanımını dışlayıcılarla içeri aktarın ve bir abonelik içinde saklayın.</span><span class="sxs-lookup"><span data-stu-id="7795d-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="7795d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7795d-110">PARAMETERS</span></span>

### <span data-ttu-id="7795d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7795d-111">-DefaultProfile</span></span>
<span data-ttu-id="7795d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7795d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7795d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7795d-113">-Force</span></span>
<span data-ttu-id="7795d-114">True olarak ayarlandığında, yürütme onay sormaz.</span><span class="sxs-lookup"><span data-stu-id="7795d-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="7795d-115">-Inputpath</span><span class="sxs-lookup"><span data-stu-id="7795d-115">-InputPath</span></span>
<span data-ttu-id="7795d-116">Disk üzerindeki bir Blueprint JSON dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="7795d-116">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="7795d-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7795d-117">-ManagementGroupId</span></span>
<span data-ttu-id="7795d-118">Şeması tanımının olduğu veya kaydedileceği yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="7795d-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="7795d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7795d-119">-Name</span></span>
<span data-ttu-id="7795d-120">Blueprint tanım adı.</span><span class="sxs-lookup"><span data-stu-id="7795d-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="7795d-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7795d-121">-SubscriptionId</span></span>
<span data-ttu-id="7795d-122">Şeması tanımının bulunduğu abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="7795d-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="7795d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7795d-123">CommonParameters</span></span>
<span data-ttu-id="7795d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7795d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7795d-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7795d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7795d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7795d-126">INPUTS</span></span>

### <span data-ttu-id="7795d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7795d-127">System.String</span></span>

## <span data-ttu-id="7795d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7795d-128">OUTPUTS</span></span>

### <span data-ttu-id="7795d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7795d-129">System.String</span></span>

## <span data-ttu-id="7795d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7795d-130">NOTES</span></span>

## <span data-ttu-id="7795d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7795d-131">RELATED LINKS</span></span>

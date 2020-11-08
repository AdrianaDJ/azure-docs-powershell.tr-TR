---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2136a224a5d187951b77c6f48e0b610b48b021b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097856"
---
# <span data-ttu-id="18c16-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="18c16-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="18c16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18c16-102">SYNOPSIS</span></span>
<span data-ttu-id="18c16-103">Belirtilen şeması tanımını belirtilen çıktı konumuna JSON dosyası olarak dışarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="18c16-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="18c16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18c16-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18c16-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18c16-105">DESCRIPTION</span></span>
<span data-ttu-id="18c16-106">Bir şeması tanımını dışlayıcılarla dışarı aktarın ve diske kaydedin.</span><span class="sxs-lookup"><span data-stu-id="18c16-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="18c16-107">Bu cmdlet, Blueprint 'in en son sürümünü (taslak veya yayınlanan) dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="18c16-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="18c16-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18c16-108">EXAMPLES</span></span>

### <span data-ttu-id="18c16-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="18c16-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="18c16-110">Bir şeması tanımını dışlayıcılarla dışarı aktarın ve diske kaydedin.</span><span class="sxs-lookup"><span data-stu-id="18c16-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="18c16-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18c16-111">PARAMETERS</span></span>

### <span data-ttu-id="18c16-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="18c16-112">-Blueprint</span></span>
<span data-ttu-id="18c16-113">Dışarı aktarılacak şeması tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="18c16-113">The blueprint definition object to export.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18c16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c16-114">-DefaultProfile</span></span>
<span data-ttu-id="18c16-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18c16-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18c16-116">-Force</span><span class="sxs-lookup"><span data-stu-id="18c16-116">-Force</span></span>
<span data-ttu-id="18c16-117">True olarak ayarlandığında, yürütme onay sormaz.</span><span class="sxs-lookup"><span data-stu-id="18c16-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="18c16-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="18c16-118">-OutputPath</span></span>
<span data-ttu-id="18c16-119">Mavi yazdırma tanımını JSON biçiminde dışarı aktarmak için diskteki dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="18c16-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="18c16-120">-Version</span><span class="sxs-lookup"><span data-stu-id="18c16-120">-Version</span></span>
<span data-ttu-id="18c16-121">Şeması tanım sürümü yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="18c16-121">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="18c16-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c16-122">CommonParameters</span></span>
<span data-ttu-id="18c16-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18c16-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="18c16-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18c16-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c16-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18c16-125">INPUTS</span></span>

### <span data-ttu-id="18c16-126">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="18c16-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="18c16-127">System. String</span><span class="sxs-lookup"><span data-stu-id="18c16-127">System.String</span></span>

## <span data-ttu-id="18c16-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18c16-128">OUTPUTS</span></span>

### <span data-ttu-id="18c16-129">System. String</span><span class="sxs-lookup"><span data-stu-id="18c16-129">System.String</span></span>

## <span data-ttu-id="18c16-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18c16-130">NOTES</span></span>

## <span data-ttu-id="18c16-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18c16-131">RELATED LINKS</span></span>

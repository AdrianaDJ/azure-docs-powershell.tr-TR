---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2c349d99e8a3529d4f1423a43bd31ab2500664c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753130"
---
# <span data-ttu-id="b1009-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="b1009-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="b1009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1009-102">SYNOPSIS</span></span>
<span data-ttu-id="b1009-103">Belirtilen şeması tanımını belirtilen çıktı konumuna JSON dosyası olarak dışarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="b1009-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="b1009-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1009-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1009-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1009-105">DESCRIPTION</span></span>
<span data-ttu-id="b1009-106">Bir şeması tanımını dışlayıcılarla dışarı aktarın ve diske kaydedin.</span><span class="sxs-lookup"><span data-stu-id="b1009-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="b1009-107">Bu cmdlet, Blueprint 'in en son sürümünü (taslak veya yayınlanan) dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="b1009-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="b1009-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1009-108">EXAMPLES</span></span>

### <span data-ttu-id="b1009-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b1009-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="b1009-110">Bir şeması tanımını dışlayıcılarla dışarı aktarın ve diske kaydedin.</span><span class="sxs-lookup"><span data-stu-id="b1009-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="b1009-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1009-111">PARAMETERS</span></span>

### <span data-ttu-id="b1009-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="b1009-112">-Blueprint</span></span>
<span data-ttu-id="b1009-113">Dışarı aktarılacak şeması tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b1009-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="b1009-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1009-114">-DefaultProfile</span></span>
<span data-ttu-id="b1009-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1009-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1009-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b1009-116">-Force</span></span>
<span data-ttu-id="b1009-117">True olarak ayarlandığında, yürütme onay sormaz.</span><span class="sxs-lookup"><span data-stu-id="b1009-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="b1009-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b1009-118">-OutputPath</span></span>
<span data-ttu-id="b1009-119">Mavi yazdırma tanımını JSON biçiminde dışarı aktarmak için diskteki dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="b1009-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="b1009-120">-Version</span><span class="sxs-lookup"><span data-stu-id="b1009-120">-Version</span></span>
<span data-ttu-id="b1009-121">Şeması tanım sürümü yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="b1009-121">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="b1009-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1009-122">CommonParameters</span></span>
<span data-ttu-id="b1009-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1009-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b1009-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1009-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1009-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1009-125">INPUTS</span></span>

### <span data-ttu-id="b1009-126">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="b1009-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="b1009-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b1009-127">System.String</span></span>

## <span data-ttu-id="b1009-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1009-128">OUTPUTS</span></span>

### <span data-ttu-id="b1009-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b1009-129">System.String</span></span>

## <span data-ttu-id="b1009-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1009-130">NOTES</span></span>

## <span data-ttu-id="b1009-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1009-131">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276909"
---
# <span data-ttu-id="7f9be-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="7f9be-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="7f9be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f9be-102">SYNOPSIS</span></span>
<span data-ttu-id="7f9be-103">Belirtilen şeması tanımını belirtilen çıktı konumuna JSON dosyası olarak dışarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="7f9be-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="7f9be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f9be-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f9be-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f9be-105">DESCRIPTION</span></span>
<span data-ttu-id="7f9be-106">Bir şeması tanımını dışlayıcılarla dışarı aktarın ve diske kaydedin.</span><span class="sxs-lookup"><span data-stu-id="7f9be-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="7f9be-107">Bu cmdlet, Blueprint 'in en son sürümünü (taslak veya yayınlanan) dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="7f9be-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="7f9be-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f9be-108">EXAMPLES</span></span>

### <span data-ttu-id="7f9be-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f9be-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="7f9be-110">Bir şeması tanımını dışlayıcılarla dışarı aktarın ve diske kaydedin.</span><span class="sxs-lookup"><span data-stu-id="7f9be-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="7f9be-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f9be-111">PARAMETERS</span></span>

### <span data-ttu-id="7f9be-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="7f9be-112">-Blueprint</span></span>
<span data-ttu-id="7f9be-113">Dışarı aktarılacak şeması tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7f9be-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="7f9be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f9be-114">-DefaultProfile</span></span>
<span data-ttu-id="7f9be-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f9be-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f9be-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7f9be-116">-Force</span></span>
<span data-ttu-id="7f9be-117">True olarak ayarlandığında, yürütme onay sormaz.</span><span class="sxs-lookup"><span data-stu-id="7f9be-117">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9be-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="7f9be-118">-OutputPath</span></span>
<span data-ttu-id="7f9be-119">Mavi yazdırma tanımını JSON biçiminde dışarı aktarmak için diskteki dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="7f9be-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9be-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7f9be-120">-PassThru</span></span>
<span data-ttu-id="7f9be-121">Ayarlandığında cmdlet, dışarı aktarılan şeması tanımını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7f9be-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="7f9be-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7f9be-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9be-123">-Version</span><span class="sxs-lookup"><span data-stu-id="7f9be-123">-Version</span></span>
<span data-ttu-id="7f9be-124">Şeması tanım sürümü yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="7f9be-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="7f9be-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f9be-125">-Confirm</span></span>
<span data-ttu-id="7f9be-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f9be-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9be-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f9be-127">-WhatIf</span></span>
<span data-ttu-id="7f9be-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f9be-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f9be-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f9be-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9be-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f9be-130">CommonParameters</span></span>
<span data-ttu-id="7f9be-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f9be-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f9be-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7f9be-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f9be-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f9be-133">INPUTS</span></span>

### <span data-ttu-id="7f9be-134">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="7f9be-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="7f9be-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7f9be-135">System.String</span></span>

## <span data-ttu-id="7f9be-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f9be-136">OUTPUTS</span></span>

### <span data-ttu-id="7f9be-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7f9be-137">System.String</span></span>

## <span data-ttu-id="7f9be-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f9be-138">NOTES</span></span>

## <span data-ttu-id="7f9be-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f9be-139">RELATED LINKS</span></span>

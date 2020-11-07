---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 8d1a4dfcaaa101a87fc687e78b8086823be7caab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752477"
---
# <span data-ttu-id="8b546-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8b546-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="8b546-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b546-102">SYNOPSIS</span></span>
<span data-ttu-id="8b546-103">Veri Fabrikası 'nden bir veri kümesi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b546-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="8b546-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b546-104">SYNTAX</span></span>

### <span data-ttu-id="8b546-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8b546-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b546-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b546-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b546-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="8b546-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b546-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b546-108">DESCRIPTION</span></span>
<span data-ttu-id="8b546-109">Remove-AzDataFactoryV2Dataset cmdlet 'i Azure Veri Fabrikası 'ndan veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b546-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="8b546-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b546-110">EXAMPLES</span></span>

### <span data-ttu-id="8b546-111">Örnek 1: veri kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="8b546-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="8b546-112">Bu komut, wikiadf adlı veri fabrikası 'ndan dawikiaggreg</span><span class="sxs-lookup"><span data-stu-id="8b546-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="8b546-113">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b546-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="8b546-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b546-114">PARAMETERS</span></span>

### <span data-ttu-id="8b546-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8b546-115">-DataFactoryName</span></span>
<span data-ttu-id="8b546-116">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b546-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8b546-117">Bu cmdlet, bu parametrenin belirttiği veri fabrikası veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b546-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b546-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b546-118">-DefaultProfile</span></span>
<span data-ttu-id="8b546-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b546-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b546-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8b546-120">-Force</span></span>
<span data-ttu-id="8b546-121">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="8b546-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8b546-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b546-122">-InputObject</span></span>
<span data-ttu-id="8b546-123">Kaldırılacak veri kümesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b546-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b546-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b546-124">-Name</span></span>
<span data-ttu-id="8b546-125">Kaldırılacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b546-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b546-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b546-126">-ResourceGroupName</span></span>
<span data-ttu-id="8b546-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b546-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8b546-128">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b546-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b546-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8b546-129">-ResourceId</span></span>
<span data-ttu-id="8b546-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="8b546-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b546-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b546-131">-Confirm</span></span>
<span data-ttu-id="8b546-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b546-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b546-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b546-133">-WhatIf</span></span>
<span data-ttu-id="8b546-134">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="8b546-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8b546-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b546-135">CommonParameters</span></span>
<span data-ttu-id="8b546-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b546-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b546-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b546-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b546-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b546-138">INPUTS</span></span>

### <span data-ttu-id="8b546-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="8b546-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="8b546-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8b546-140">System.String</span></span>

## <span data-ttu-id="8b546-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b546-141">OUTPUTS</span></span>

### <span data-ttu-id="8b546-142">System. void</span><span class="sxs-lookup"><span data-stu-id="8b546-142">System.Void</span></span>

## <span data-ttu-id="8b546-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b546-143">NOTES</span></span>
<span data-ttu-id="8b546-144">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="8b546-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8b546-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b546-145">RELATED LINKS</span></span>

[<span data-ttu-id="8b546-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8b546-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="8b546-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8b546-147">Set-AzDataFactoryV2Dataset</span></span>]()

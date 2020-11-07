---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: faf5d80b231b93124279f3c9bb6a347f89d988d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762021"
---
# <span data-ttu-id="7fcb0-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7fcb0-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="7fcb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcb0-103">Veri Fabrikası 'nden bir veri kümesi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fcb0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7fcb0-104">SYNTAX</span></span>

### <span data-ttu-id="7fcb0-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7fcb0-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fcb0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7fcb0-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fcb0-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="7fcb0-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fcb0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7fcb0-108">DESCRIPTION</span></span>
<span data-ttu-id="7fcb0-109">Remove-AzureRmDataFactoryV2Dataset cmdlet 'i Azure Veri Fabrikası 'ndan veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="7fcb0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7fcb0-110">EXAMPLES</span></span>

### <span data-ttu-id="7fcb0-111">Örnek 1: veri kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="7fcb0-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="7fcb0-112">Bu komut, wikiadf adlı veri fabrikası 'ndan dawikiaggreg</span><span class="sxs-lookup"><span data-stu-id="7fcb0-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="7fcb0-113">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="7fcb0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7fcb0-114">PARAMETERS</span></span>

### <span data-ttu-id="7fcb0-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7fcb0-115">-DataFactoryName</span></span>
<span data-ttu-id="7fcb0-116">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7fcb0-117">Bu cmdlet, bu parametrenin belirttiği veri fabrikası veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fcb0-118">-DefaultProfile</span></span>
<span data-ttu-id="7fcb0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7fcb0-120">-Force</span></span>
<span data-ttu-id="7fcb0-121">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7fcb0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fcb0-122">-InputObject</span></span>
<span data-ttu-id="7fcb0-123">Kaldırılacak veri kümesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb0-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="7fcb0-124">-Name</span></span>
<span data-ttu-id="7fcb0-125">Kaldırılacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fcb0-126">-ResourceGroupName</span></span>
<span data-ttu-id="7fcb0-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7fcb0-128">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb0-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7fcb0-129">-ResourceId</span></span>
<span data-ttu-id="7fcb0-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-130">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb0-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="7fcb0-131">-Confirm</span></span>
<span data-ttu-id="7fcb0-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fcb0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fcb0-133">-WhatIf</span></span>
<span data-ttu-id="7fcb0-134">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7fcb0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcb0-135">CommonParameters</span></span>
<span data-ttu-id="7fcb0-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcb0-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fcb0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcb0-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7fcb0-138">INPUTS</span></span>

### <span data-ttu-id="7fcb0-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="7fcb0-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="7fcb0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7fcb0-140">System.String</span></span>

## <span data-ttu-id="7fcb0-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7fcb0-141">OUTPUTS</span></span>

### <span data-ttu-id="7fcb0-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="7fcb0-142">System.Object</span></span>

## <span data-ttu-id="7fcb0-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7fcb0-143">NOTES</span></span>
<span data-ttu-id="7fcb0-144">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="7fcb0-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7fcb0-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7fcb0-145">RELATED LINKS</span></span>

[<span data-ttu-id="7fcb0-146">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7fcb0-146">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="7fcb0-147">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7fcb0-147">Set-AzureRmDataFactoryV2Dataset</span></span>]()

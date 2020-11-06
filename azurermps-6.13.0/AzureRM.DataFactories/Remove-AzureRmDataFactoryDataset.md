---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: d4bb50dcc9e3f04d69131afbb7ac8b4f85e5070c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593687"
---
# <span data-ttu-id="ac99f-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ac99f-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="ac99f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac99f-102">SYNOPSIS</span></span>
<span data-ttu-id="ac99f-103">Veri kümesini Azure Veri Fabrikası 'ndan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ac99f-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac99f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac99f-104">SYNTAX</span></span>

### <span data-ttu-id="ac99f-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ac99f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac99f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ac99f-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac99f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac99f-107">DESCRIPTION</span></span>
<span data-ttu-id="ac99f-108">**Remove-AzureRmDataFactoryDataset** cmdlet 'ı Azure Veri Fabrikası 'ndan bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ac99f-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="ac99f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac99f-109">EXAMPLES</span></span>

### <span data-ttu-id="ac99f-110">Örnek 1: veri kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ac99f-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="ac99f-111">Bu komut, wikiadf adlı veri fabrikası 'ndan dawikiaggreg</span><span class="sxs-lookup"><span data-stu-id="ac99f-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="ac99f-112">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ac99f-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="ac99f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac99f-113">PARAMETERS</span></span>

### <span data-ttu-id="ac99f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ac99f-114">-DataFactory</span></span>
<span data-ttu-id="ac99f-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac99f-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ac99f-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikası veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ac99f-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac99f-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ac99f-117">-DataFactoryName</span></span>
<span data-ttu-id="ac99f-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac99f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ac99f-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ac99f-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac99f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac99f-120">-DefaultProfile</span></span>
<span data-ttu-id="ac99f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ac99f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac99f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ac99f-122">-Force</span></span>
<span data-ttu-id="ac99f-123">Bu cmdlet 'in bir veri kümesini onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac99f-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ac99f-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="ac99f-124">-Name</span></span>
<span data-ttu-id="ac99f-125">Kaldırılacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac99f-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac99f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac99f-126">-ResourceGroupName</span></span>
<span data-ttu-id="ac99f-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac99f-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ac99f-128">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ac99f-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac99f-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="ac99f-129">-Confirm</span></span>
<span data-ttu-id="ac99f-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ac99f-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac99f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac99f-131">-WhatIf</span></span>
<span data-ttu-id="ac99f-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac99f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac99f-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ac99f-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac99f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac99f-134">CommonParameters</span></span>
<span data-ttu-id="ac99f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac99f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac99f-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac99f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac99f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac99f-137">INPUTS</span></span>

### <span data-ttu-id="ac99f-138">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="ac99f-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ac99f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ac99f-139">System.String</span></span>

## <span data-ttu-id="ac99f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac99f-140">OUTPUTS</span></span>

### <span data-ttu-id="ac99f-141">System. void</span><span class="sxs-lookup"><span data-stu-id="ac99f-141">System.Void</span></span>

## <span data-ttu-id="ac99f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac99f-142">NOTES</span></span>
* <span data-ttu-id="ac99f-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="ac99f-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ac99f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac99f-144">RELATED LINKS</span></span>

[<span data-ttu-id="ac99f-145">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ac99f-145">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="ac99f-146">Yeni-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ac99f-146">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)



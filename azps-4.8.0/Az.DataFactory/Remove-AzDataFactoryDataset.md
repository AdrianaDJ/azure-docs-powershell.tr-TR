---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 925362c3f576a9c243b42efc9af421a30c74d0ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268005"
---
# <span data-ttu-id="bc674-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="bc674-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="bc674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc674-102">SYNOPSIS</span></span>
<span data-ttu-id="bc674-103">Veri kümesini Azure Veri Fabrikası 'ndan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc674-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="bc674-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc674-104">SYNTAX</span></span>

### <span data-ttu-id="bc674-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bc674-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc674-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bc674-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc674-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc674-107">DESCRIPTION</span></span>
<span data-ttu-id="bc674-108">**Remove-AzDataFactoryDataset** cmdlet 'ı Azure Veri Fabrikası 'ndan bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc674-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="bc674-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc674-109">EXAMPLES</span></span>

### <span data-ttu-id="bc674-110">Örnek 1: veri kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="bc674-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="bc674-111">Bu komut, wikiadf adlı veri fabrikası 'ndan dawikiaggreg</span><span class="sxs-lookup"><span data-stu-id="bc674-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="bc674-112">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="bc674-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="bc674-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc674-113">PARAMETERS</span></span>

### <span data-ttu-id="bc674-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bc674-114">-DataFactory</span></span>
<span data-ttu-id="bc674-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc674-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="bc674-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikası veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc674-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bc674-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bc674-117">-DataFactoryName</span></span>
<span data-ttu-id="bc674-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc674-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bc674-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc674-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bc674-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc674-120">-DefaultProfile</span></span>
<span data-ttu-id="bc674-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bc674-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc674-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bc674-122">-Force</span></span>
<span data-ttu-id="bc674-123">Bu cmdlet 'in bir veri kümesini onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc674-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="bc674-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc674-124">-Name</span></span>
<span data-ttu-id="bc674-125">Kaldırılacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc674-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="bc674-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc674-126">-ResourceGroupName</span></span>
<span data-ttu-id="bc674-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc674-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bc674-128">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc674-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bc674-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc674-129">-Confirm</span></span>
<span data-ttu-id="bc674-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc674-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc674-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc674-131">-WhatIf</span></span>
<span data-ttu-id="bc674-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc674-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc674-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc674-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc674-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc674-134">CommonParameters</span></span>
<span data-ttu-id="bc674-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc674-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc674-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc674-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc674-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc674-137">INPUTS</span></span>

### <span data-ttu-id="bc674-138">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="bc674-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="bc674-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bc674-139">System.String</span></span>

## <span data-ttu-id="bc674-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc674-140">OUTPUTS</span></span>

### <span data-ttu-id="bc674-141">System. void</span><span class="sxs-lookup"><span data-stu-id="bc674-141">System.Void</span></span>

## <span data-ttu-id="bc674-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc674-142">NOTES</span></span>
* <span data-ttu-id="bc674-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="bc674-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bc674-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc674-144">RELATED LINKS</span></span>

[<span data-ttu-id="bc674-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="bc674-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="bc674-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="bc674-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)



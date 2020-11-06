---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 85e9e96db366adcb30494ac22e7d1b73bbff9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587977"
---
# <span data-ttu-id="6b775-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="6b775-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="6b775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b775-102">SYNOPSIS</span></span>
<span data-ttu-id="6b775-103">Veri kümesini Azure Veri Fabrikası 'ndan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b775-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b775-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b775-104">SYNTAX</span></span>

### <span data-ttu-id="6b775-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b775-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b775-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6b775-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b775-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b775-107">DESCRIPTION</span></span>
<span data-ttu-id="6b775-108">**Remove-AzureRmDataFactoryDataset** cmdlet 'ı Azure Veri Fabrikası 'ndan bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b775-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="6b775-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b775-109">EXAMPLES</span></span>

### <span data-ttu-id="6b775-110">Örnek 1: veri kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6b775-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="6b775-111">Bu komut, wikiadf adlı veri fabrikası 'ndan dawikiaggreg</span><span class="sxs-lookup"><span data-stu-id="6b775-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="6b775-112">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="6b775-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="6b775-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b775-113">PARAMETERS</span></span>

### <span data-ttu-id="6b775-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6b775-114">-DataFactory</span></span>
<span data-ttu-id="6b775-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b775-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6b775-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikası veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b775-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b775-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6b775-117">-DataFactoryName</span></span>
<span data-ttu-id="6b775-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b775-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6b775-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b775-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b775-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6b775-120">-Force</span></span>
<span data-ttu-id="6b775-121">Bu cmdlet 'in bir veri kümesini onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b775-121">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="6b775-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b775-122">-Name</span></span>
<span data-ttu-id="6b775-123">Kaldırılacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b775-123">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="6b775-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b775-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b775-125">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b775-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6b775-126">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b775-126">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b775-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b775-127">-Confirm</span></span>
<span data-ttu-id="6b775-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b775-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b775-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b775-129">-WhatIf</span></span>
<span data-ttu-id="6b775-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b775-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b775-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b775-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b775-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b775-132">-DefaultProfile</span></span>
<span data-ttu-id="6b775-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b775-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b775-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b775-134">CommonParameters</span></span>
<span data-ttu-id="6b775-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b775-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b775-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b775-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b775-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b775-137">INPUTS</span></span>

## <span data-ttu-id="6b775-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b775-138">OUTPUTS</span></span>

### <span data-ttu-id="6b775-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b775-139">System.Boolean</span></span>

## <span data-ttu-id="6b775-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b775-140">NOTES</span></span>
* <span data-ttu-id="6b775-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="6b775-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6b775-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b775-142">RELATED LINKS</span></span>

[<span data-ttu-id="6b775-143">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="6b775-143">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="6b775-144">Yeni-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="6b775-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)



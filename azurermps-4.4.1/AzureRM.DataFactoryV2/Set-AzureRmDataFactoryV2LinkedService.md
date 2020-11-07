---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: f977344f2beabe8352a7417130063c3e9d4d3e1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765188"
---
# <span data-ttu-id="f7508-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f7508-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="f7508-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7508-102">SYNOPSIS</span></span>
<span data-ttu-id="f7508-103">Veri deposuna veya bulut hizmetine veri fabrikasına bağlar.</span><span class="sxs-lookup"><span data-stu-id="f7508-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7508-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7508-104">SYNTAX</span></span>

### <span data-ttu-id="f7508-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7508-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f7508-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f7508-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="f7508-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7508-107">DESCRIPTION</span></span>
<span data-ttu-id="f7508-108">Set-AzureRmDataFactoryV2LinkedService cmdlet 'i, Azure Veri Fabrikası 'ne bir veri deposu veya bulut hizmeti bağlar.</span><span class="sxs-lookup"><span data-stu-id="f7508-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="f7508-109">Zaten var olan bağlantılı bir hizmet için bir ad belirtirseniz, bu cmdlet bağlantılı hizmeti değiştirmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7508-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="f7508-110">Force parametresini belirtirseniz cmdlet, mevcut bağlı hizmetin yerini alınmadan değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f7508-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="f7508-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="f7508-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="f7508-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7508-112">EXAMPLES</span></span>

### <span data-ttu-id="f7508-113">Örnek 1: bağlantılı hizmet oluşturma</span><span class="sxs-lookup"><span data-stu-id="f7508-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

```

<span data-ttu-id="f7508-114">Bu komut WikiADF adındaki LinkedServiceCuratedWikiData adlı bir bağlantılı hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f7508-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="f7508-115">Bu bağlantılı hizmet, dosyada belirtilen bir Azure blob deposunu WikiADF adlı Data Factory öğesine bağlar.</span><span class="sxs-lookup"><span data-stu-id="f7508-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="f7508-116">Komut sonucu, ardışık düzen işlecini kullanarak Format-List cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="f7508-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f7508-117">Bu Windows PowerShell cmdlet 'i sonuçları biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="f7508-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="f7508-118">Daha fazla bilgi için Get-Help biçim-liste yazın.</span><span class="sxs-lookup"><span data-stu-id="f7508-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="f7508-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7508-119">PARAMETERS</span></span>

### <span data-ttu-id="f7508-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="f7508-120">-Confirm</span></span>
<span data-ttu-id="f7508-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7508-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7508-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f7508-122">-DataFactoryName</span></span>
<span data-ttu-id="f7508-123">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7508-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f7508-124">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bağlantılı bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f7508-124">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7508-125">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="f7508-125">-DefinitionFile</span></span>
<span data-ttu-id="f7508-126">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="f7508-126">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7508-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f7508-127">-Force</span></span>
<span data-ttu-id="f7508-128">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="f7508-128">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f7508-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="f7508-129">-Name</span></span>
<span data-ttu-id="f7508-130">Oluşturulacak bağlı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7508-130">Specifies the name of the linked service to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7508-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7508-131">-ResourceGroupName</span></span>
<span data-ttu-id="f7508-132">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7508-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f7508-133">Bu cmdlet, bu parametrenin belirttiği grup için bağlantılı bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f7508-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7508-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f7508-134">-ResourceId</span></span>
<span data-ttu-id="f7508-135">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="f7508-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f7508-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7508-136">-WhatIf</span></span>
<span data-ttu-id="f7508-137">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="f7508-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="f7508-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7508-138">INPUTS</span></span>

### <span data-ttu-id="f7508-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f7508-139">System.String</span></span>


## <span data-ttu-id="f7508-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7508-140">OUTPUTS</span></span>

### <span data-ttu-id="f7508-141">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="f7508-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>


## <span data-ttu-id="f7508-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7508-142">NOTES</span></span>
<span data-ttu-id="f7508-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="f7508-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f7508-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7508-144">RELATED LINKS</span></span>
[<span data-ttu-id="f7508-145">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f7508-145">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="f7508-146">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f7508-146">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()

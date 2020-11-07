---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 2f7cfba7db5d675a73d21d6cd1814c13a1998ab1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762381"
---
# <span data-ttu-id="0060c-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0060c-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="0060c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0060c-102">SYNOPSIS</span></span>
<span data-ttu-id="0060c-103">Veri deposuna veya bulut hizmetine veri fabrikasına bağlar.</span><span class="sxs-lookup"><span data-stu-id="0060c-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0060c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0060c-104">SYNTAX</span></span>

### <span data-ttu-id="0060c-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0060c-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0060c-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0060c-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0060c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0060c-107">DESCRIPTION</span></span>
<span data-ttu-id="0060c-108">Set-AzureRmDataFactoryV2LinkedService cmdlet 'i, Azure Veri Fabrikası 'ne bir veri deposu veya bulut hizmeti bağlar.</span><span class="sxs-lookup"><span data-stu-id="0060c-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="0060c-109">Zaten var olan bağlantılı bir hizmet için bir ad belirtirseniz, bu cmdlet bağlantılı hizmeti değiştirmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0060c-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="0060c-110">Force parametresini belirtirseniz cmdlet, mevcut bağlı hizmetin yerini alınmadan değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0060c-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="0060c-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="0060c-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="0060c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0060c-112">EXAMPLES</span></span>

### <span data-ttu-id="0060c-113">Örnek 1: bağlantılı hizmet oluşturma</span><span class="sxs-lookup"><span data-stu-id="0060c-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="0060c-114">Bu komut WikiADF adındaki LinkedServiceCuratedWikiData adlı bir bağlantılı hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0060c-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="0060c-115">Bu bağlantılı hizmet, dosyada belirtilen bir Azure blob deposunu WikiADF adlı Data Factory öğesine bağlar.</span><span class="sxs-lookup"><span data-stu-id="0060c-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="0060c-116">Komut sonucu, ardışık düzen işlecini kullanarak Format-List cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="0060c-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0060c-117">Bu Windows PowerShell cmdlet 'i sonuçları biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="0060c-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="0060c-118">Daha fazla bilgi için Get-Help biçim-liste yazın.</span><span class="sxs-lookup"><span data-stu-id="0060c-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="0060c-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0060c-119">PARAMETERS</span></span>

### <span data-ttu-id="0060c-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0060c-120">-DataFactoryName</span></span>
<span data-ttu-id="0060c-121">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0060c-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0060c-122">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bağlantılı bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0060c-122">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0060c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0060c-123">-DefaultProfile</span></span>
<span data-ttu-id="0060c-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0060c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0060c-125">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="0060c-125">-DefinitionFile</span></span>
<span data-ttu-id="0060c-126">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="0060c-126">The JSON file path.</span></span>

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

### <span data-ttu-id="0060c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="0060c-127">-Force</span></span>
<span data-ttu-id="0060c-128">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="0060c-128">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0060c-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="0060c-129">-Name</span></span>
<span data-ttu-id="0060c-130">Oluşturulacak bağlı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0060c-130">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="0060c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0060c-131">-ResourceGroupName</span></span>
<span data-ttu-id="0060c-132">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0060c-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0060c-133">Bu cmdlet, bu parametrenin belirttiği grup için bağlantılı bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0060c-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0060c-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0060c-134">-ResourceId</span></span>
<span data-ttu-id="0060c-135">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0060c-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0060c-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="0060c-136">-Confirm</span></span>
<span data-ttu-id="0060c-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0060c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0060c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0060c-138">-WhatIf</span></span>
<span data-ttu-id="0060c-139">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="0060c-139">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0060c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0060c-140">CommonParameters</span></span>
<span data-ttu-id="0060c-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0060c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0060c-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0060c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0060c-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0060c-143">INPUTS</span></span>

### <span data-ttu-id="0060c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0060c-144">System.String</span></span>

## <span data-ttu-id="0060c-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0060c-145">OUTPUTS</span></span>

### <span data-ttu-id="0060c-146">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="0060c-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="0060c-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0060c-147">NOTES</span></span>
<span data-ttu-id="0060c-148">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="0060c-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0060c-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0060c-149">RELATED LINKS</span></span>

[<span data-ttu-id="0060c-150">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0060c-150">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="0060c-151">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0060c-151">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()

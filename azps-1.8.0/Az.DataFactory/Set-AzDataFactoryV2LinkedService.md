---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 2ff8e4a92c01c38b81ad5f1fded5661501b1c46c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761113"
---
# <span data-ttu-id="a5e27-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a5e27-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="a5e27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5e27-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e27-103">Veri deposuna veya bulut hizmetine veri fabrikasına bağlar.</span><span class="sxs-lookup"><span data-stu-id="a5e27-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="a5e27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5e27-104">SYNTAX</span></span>

### <span data-ttu-id="a5e27-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5e27-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5e27-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="a5e27-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5e27-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5e27-107">DESCRIPTION</span></span>
<span data-ttu-id="a5e27-108">Set-AzDataFactoryV2LinkedService cmdlet 'i, Azure Veri Fabrikası 'ne bir veri deposu veya bulut hizmeti bağlar.</span><span class="sxs-lookup"><span data-stu-id="a5e27-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="a5e27-109">Zaten var olan bağlantılı bir hizmet için bir ad belirtirseniz, bu cmdlet bağlantılı hizmeti değiştirmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5e27-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="a5e27-110">Force parametresini belirtirseniz cmdlet, mevcut bağlı hizmetin yerini alınmadan değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a5e27-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="a5e27-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:--Veri Fabrikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a5e27-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="a5e27-112">--Bağlantılı hizmetler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a5e27-112">-- Create linked services.</span></span>
<span data-ttu-id="a5e27-113">--Veri kümeleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a5e27-113">-- Create datasets.</span></span>
<span data-ttu-id="a5e27-114">--Ardışık düzen oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a5e27-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="a5e27-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5e27-115">EXAMPLES</span></span>

### <span data-ttu-id="a5e27-116">Örnek 1: bağlantılı hizmet oluşturma</span><span class="sxs-lookup"><span data-stu-id="a5e27-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="a5e27-117">Bu komut WikiADF adındaki LinkedServiceCuratedWikiData adlı bir bağlantılı hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5e27-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="a5e27-118">Bu bağlantılı hizmet, dosyada belirtilen bir Azure blob deposunu WikiADF adlı Data Factory öğesine bağlar.</span><span class="sxs-lookup"><span data-stu-id="a5e27-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="a5e27-119">Komut sonucu, ardışık düzen işlecini kullanarak Format-List cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="a5e27-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a5e27-120">Bu Windows PowerShell cmdlet 'i sonuçları biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="a5e27-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="a5e27-121">Daha fazla bilgi için Get-Help biçim-liste yazın.</span><span class="sxs-lookup"><span data-stu-id="a5e27-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="a5e27-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5e27-122">PARAMETERS</span></span>

### <span data-ttu-id="a5e27-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a5e27-123">-DataFactoryName</span></span>
<span data-ttu-id="a5e27-124">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5e27-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a5e27-125">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bağlantılı bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5e27-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a5e27-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e27-126">-DefaultProfile</span></span>
<span data-ttu-id="a5e27-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5e27-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5e27-128">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="a5e27-128">-DefinitionFile</span></span>
<span data-ttu-id="a5e27-129">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="a5e27-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e27-130">-Force</span><span class="sxs-lookup"><span data-stu-id="a5e27-130">-Force</span></span>
<span data-ttu-id="a5e27-131">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="a5e27-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a5e27-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5e27-132">-Name</span></span>
<span data-ttu-id="a5e27-133">Oluşturulacak bağlı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5e27-133">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5e27-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e27-134">-ResourceGroupName</span></span>
<span data-ttu-id="a5e27-135">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5e27-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a5e27-136">Bu cmdlet, bu parametrenin belirttiği grup için bağlantılı bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5e27-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a5e27-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a5e27-137">-ResourceId</span></span>
<span data-ttu-id="a5e27-138">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="a5e27-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a5e27-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5e27-139">-Confirm</span></span>
<span data-ttu-id="a5e27-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5e27-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e27-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e27-141">-WhatIf</span></span>
<span data-ttu-id="a5e27-142">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="a5e27-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a5e27-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e27-143">CommonParameters</span></span>
<span data-ttu-id="a5e27-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5e27-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e27-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e27-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e27-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5e27-146">INPUTS</span></span>

### <span data-ttu-id="a5e27-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e27-147">System.String</span></span>

## <span data-ttu-id="a5e27-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5e27-148">OUTPUTS</span></span>

### <span data-ttu-id="a5e27-149">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="a5e27-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="a5e27-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5e27-150">NOTES</span></span>
<span data-ttu-id="a5e27-151">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="a5e27-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a5e27-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5e27-152">RELATED LINKS</span></span>

[<span data-ttu-id="a5e27-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a5e27-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="a5e27-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a5e27-154">Remove-AzDataFactoryV2LinkedService</span></span>]()

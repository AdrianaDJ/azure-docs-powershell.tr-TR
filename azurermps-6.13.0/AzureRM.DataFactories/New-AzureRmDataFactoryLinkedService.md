---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: cd67307c13e5704da67659ba67f6f609eeff4df8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593690"
---
# <span data-ttu-id="f8725-101">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="f8725-101">New-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="f8725-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8725-102">SYNOPSIS</span></span>
<span data-ttu-id="f8725-103">Bir veri deposunu veya bulut hizmetini bir Azure veri fabrikasına bağlar.</span><span class="sxs-lookup"><span data-stu-id="f8725-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8725-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8725-104">SYNTAX</span></span>

### <span data-ttu-id="f8725-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f8725-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8725-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f8725-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8725-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8725-107">DESCRIPTION</span></span>
<span data-ttu-id="f8725-108">**New-AzureRmDataFactoryLinkedService** cmdlet 'i, veri deposunu veya bulut hizmetini Azure Veri Fabrikası 'ne bağlar.</span><span class="sxs-lookup"><span data-stu-id="f8725-108">The **New-AzureRmDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="f8725-109">Zaten var olan bağlantılı bir hizmet için bir ad belirtirseniz, bu cmdlet bağlantılı hizmeti değiştirmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8725-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="f8725-110">*Force* parametresini belirtirseniz cmdlet, mevcut bağlı hizmetin yerini alınmadan değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f8725-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="f8725-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="f8725-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="f8725-112">Veri Fabrikası oluşturma.</span><span class="sxs-lookup"><span data-stu-id="f8725-112">Create a data factory.</span></span> 
- <span data-ttu-id="f8725-113">Bağlantılı hizmetler oluşturma.</span><span class="sxs-lookup"><span data-stu-id="f8725-113">Create linked services.</span></span> 
- <span data-ttu-id="f8725-114">Veri kümeleri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="f8725-114">Create datasets.</span></span> 
- <span data-ttu-id="f8725-115">Ardışık düzen oluşturma.</span><span class="sxs-lookup"><span data-stu-id="f8725-115">Create a pipeline.</span></span>

## <span data-ttu-id="f8725-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8725-116">EXAMPLES</span></span>

### <span data-ttu-id="f8725-117">Örnek 1: bağlantılı hizmet oluşturma</span><span class="sxs-lookup"><span data-stu-id="f8725-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="f8725-118">Bu komut WikiADF adındaki LinkedServiceCuratedWikiData adlı bir bağlantılı hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8725-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="f8725-119">Bu bağlantılı hizmet, dosyada belirtilen bir Azure blob deposunu WikiADF adlı Data Factory öğesine bağlar.</span><span class="sxs-lookup"><span data-stu-id="f8725-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="f8725-120">Komut sonucu, ardışık düzen işlecini kullanarak Format-List cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="f8725-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f8725-121">Bu Windows PowerShell cmdlet 'i sonuçları biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="f8725-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="f8725-122">Daha fazla bilgi için yazın `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="f8725-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="f8725-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8725-123">PARAMETERS</span></span>

### <span data-ttu-id="f8725-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8725-124">-DataFactory</span></span>
<span data-ttu-id="f8725-125">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8725-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f8725-126">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bağlantılı bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8725-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8725-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f8725-127">-DataFactoryName</span></span>
<span data-ttu-id="f8725-128">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8725-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f8725-129">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bağlantılı bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8725-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8725-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8725-130">-DefaultProfile</span></span>
<span data-ttu-id="f8725-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f8725-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8725-132">-Dosya</span><span class="sxs-lookup"><span data-stu-id="f8725-132">-File</span></span>
<span data-ttu-id="f8725-133">Bağlı hizmetin açıklamasını içeren JavaScript nesne Gösterim (JSON) dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8725-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8725-134">-Force</span><span class="sxs-lookup"><span data-stu-id="f8725-134">-Force</span></span>
<span data-ttu-id="f8725-135">Bu cmdlet 'in mevcut bir bağlı hizmetin yerini onaylamanızı istemeden değiştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8725-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f8725-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8725-136">-Name</span></span>
<span data-ttu-id="f8725-137">Oluşturulacak bağlı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8725-137">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8725-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8725-138">-ResourceGroupName</span></span>
<span data-ttu-id="f8725-139">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8725-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f8725-140">Bu cmdlet, bu parametrenin belirttiği grup için bağlantılı bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8725-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8725-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="f8725-141">-Confirm</span></span>
<span data-ttu-id="f8725-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8725-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8725-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8725-143">-WhatIf</span></span>
<span data-ttu-id="f8725-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8725-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8725-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f8725-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8725-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8725-146">CommonParameters</span></span>
<span data-ttu-id="f8725-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8725-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8725-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8725-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8725-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8725-149">INPUTS</span></span>

### <span data-ttu-id="f8725-150">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="f8725-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f8725-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f8725-151">System.String</span></span>

## <span data-ttu-id="f8725-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8725-152">OUTPUTS</span></span>

### <span data-ttu-id="f8725-153">Microsoft. Azure. Commands. DataFactory. modeller. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="f8725-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="f8725-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8725-154">NOTES</span></span>
* <span data-ttu-id="f8725-155">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="f8725-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f8725-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8725-156">RELATED LINKS</span></span>

[<span data-ttu-id="f8725-157">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="f8725-157">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="f8725-158">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="f8725-158">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)



---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: 7466ad5617fb78d48deb92ac2d623fc05ad90634
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594747"
---
# <span data-ttu-id="0991a-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0991a-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="0991a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0991a-102">SYNOPSIS</span></span>
<span data-ttu-id="0991a-103">Veri Fabrikası içinde bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0991a-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0991a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0991a-104">SYNTAX</span></span>

### <span data-ttu-id="0991a-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0991a-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="0991a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0991a-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
```
## <span data-ttu-id="0991a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0991a-107">DESCRIPTION</span></span>
<span data-ttu-id="0991a-108">Get-AzureRmDataFactoryV2LinkedService cmdlet 'i Azure Veri Fabrikası 'ndaki bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0991a-108">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="0991a-109">Bağlantılı hizmetin adını belirtirseniz, bu cmdlet bu bağlantılı hizmet hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0991a-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="0991a-110">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0991a-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="0991a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0991a-111">EXAMPLES</span></span>

### <span data-ttu-id="0991a-112">Örnek 1: bağlantılı hizmetler hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="0991a-112">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="0991a-113">Bu komut WikiADF adlı veri fabrikası ile bağlantılı hizmetler hakkında bilgi alır ve ardından bağlantılı hizmetleri Format-List cmdlet 'ine, ardışık düzen işlecini kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="0991a-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0991a-114">Bu Windows PowerShell cmdlet 'i sonuçları biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="0991a-114">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="0991a-115">Daha fazla bilgi için Get-Help biçim-liste yazın.</span><span class="sxs-lookup"><span data-stu-id="0991a-115">For more information, type Get-Help Format-List.</span></span>

<span data-ttu-id="0991a-116">Aşağıdaki yollardan birini kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="0991a-116">You can use either one of the following ways:</span></span>

### <span data-ttu-id="0991a-117">Örnek 2: belirli bir bağlantılı hizmetle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="0991a-117">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="0991a-118">Bu komut, WikiADF adındaki LinkedServiceCuratedWikiData adındaki bağlantılı hizmetle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="0991a-118">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="0991a-119">Örnek 3: DataFactory parametresini belirterek belirli bir bağlantılı hizmetle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="0991a-119">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="0991a-120">İlk komut, ContosoFactory adındaki veri fabrikasını almak için Get-AzureRmDataFactoryV2 cmdlet 'ini kullanır ve $DataFactory değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0991a-120">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="0991a-121">İkinci komut $DataFactory depolanan veri fabrikası için bağlantılı hizmetle ilgili bilgileri alır ve bu bilgileri ardışık düzen işlecini kullanarak Format-Table cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="0991a-121">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0991a-122">Format-Table cmdlet, çıktıyı veri kümesi sütunu olarak belirtilen özelliklere sahip veri kümesi olarak biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="0991a-122">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="0991a-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0991a-123">PARAMETERS</span></span>

### <span data-ttu-id="0991a-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0991a-124">-DataFactory</span></span>
<span data-ttu-id="0991a-125">PSDataFactory nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0991a-125">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="0991a-126">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait bağlantılı hizmetleri alır.</span><span class="sxs-lookup"><span data-stu-id="0991a-126">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0991a-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0991a-127">-DataFactoryName</span></span>
<span data-ttu-id="0991a-128">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0991a-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0991a-129">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait bağlantılı hizmetleri alır.</span><span class="sxs-lookup"><span data-stu-id="0991a-129">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0991a-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="0991a-130">-Name</span></span>
<span data-ttu-id="0991a-131">Bilgi alınacak bağlantılı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0991a-131">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0991a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0991a-132">-ResourceGroupName</span></span>
<span data-ttu-id="0991a-133">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0991a-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0991a-134">Bu cmdlet, bu parametrenin belirttiği gruba ait olan bağlantılı hizmetleri alır.</span><span class="sxs-lookup"><span data-stu-id="0991a-134">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="0991a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0991a-135">INPUTS</span></span>

### <span data-ttu-id="0991a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0991a-136">System.String</span></span>
<span data-ttu-id="0991a-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="0991a-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="0991a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0991a-138">OUTPUTS</span></span>

### <span data-ttu-id="0991a-139">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. modeller. PSLinkedService, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0991a-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0991a-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="0991a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>


## <span data-ttu-id="0991a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0991a-141">NOTES</span></span>
<span data-ttu-id="0991a-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="0991a-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0991a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0991a-143">RELATED LINKS</span></span>
[<span data-ttu-id="0991a-144">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0991a-144">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="0991a-145">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0991a-145">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()

---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 7503d775b7241bbb1be6196db153e41587c0e736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764883"
---
# <span data-ttu-id="8b8db-101">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8b8db-101">Get-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="8b8db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b8db-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8db-103">Azure Veri Fabrikası 'ndaki bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8b8db-103">Gets information about linked services in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b8db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b8db-104">SYNTAX</span></span>

### <span data-ttu-id="8b8db-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8b8db-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b8db-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8b8db-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b8db-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b8db-107">DESCRIPTION</span></span>
<span data-ttu-id="8b8db-108">**Get-AzureRmDataFactoryLinkedService** cmdlet 'ı Azure Veri Fabrikası 'ndaki bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8b8db-108">The **Get-AzureRmDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="8b8db-109">Bağlantılı hizmetin adını belirtirseniz, bu cmdlet bu bağlantılı hizmet hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8b8db-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="8b8db-110">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8b8db-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="8b8db-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b8db-111">EXAMPLES</span></span>

### <span data-ttu-id="8b8db-112">Örnek 1: bağlantılı hizmetler hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="8b8db-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="8b8db-113">Bu komut WikiADF adlı veri fabrikası ile bağlantılı hizmetler hakkında bilgi alır ve ardından bağlantılı hizmetleri Format-List cmdlet 'ine, ardışık düzen işlecini kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="8b8db-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8b8db-114">Bu cmdlet sonuçları biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="8b8db-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="8b8db-115">Daha fazla bilgi için yazın `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="8b8db-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="8b8db-116">Örnek 2: belirli bir bağlantılı hizmetle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="8b8db-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="8b8db-117">Bu komut, WikiADF adlı veri fabrikası içinde HDILinkedService adındaki bağlantılı hizmetle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="8b8db-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="8b8db-118">Örnek 3: DataFactory parametresini belirterek belirli bir bağlantılı hizmetle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="8b8db-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzureRmDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="8b8db-119">İlk komut, ContosoFactory adındaki veri fabrikasını almak için Get-AzureRmDataFactory cmdlet 'ini kullanır ve $DataFactory değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8b8db-119">The first command uses the Get-AzureRmDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="8b8db-120">İkinci komut $DataFactory depolanan veri fabrikası için bağlantılı hizmetle ilgili bilgileri alır ve bu bilgileri ardışık düzen işlecini kullanarak Format-Table cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="8b8db-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8b8db-121">**Biçim tablosu** çıktıyı, veri kümesi sütunu olarak belirtilen özelliklere sahip veri kümesi olarak biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="8b8db-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="8b8db-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b8db-122">PARAMETERS</span></span>

### <span data-ttu-id="8b8db-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b8db-123">-DataFactory</span></span>
<span data-ttu-id="8b8db-124">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b8db-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8b8db-125">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait bağlantılı hizmetleri alır.</span><span class="sxs-lookup"><span data-stu-id="8b8db-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b8db-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8b8db-126">-DataFactoryName</span></span>
<span data-ttu-id="8b8db-127">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b8db-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8b8db-128">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait bağlantılı hizmetleri alır.</span><span class="sxs-lookup"><span data-stu-id="8b8db-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b8db-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b8db-129">-Name</span></span>
<span data-ttu-id="8b8db-130">Bilgi alınacak bağlantılı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b8db-130">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="8b8db-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b8db-131">-ResourceGroupName</span></span>
<span data-ttu-id="8b8db-132">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b8db-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8b8db-133">Bu cmdlet, bu parametrenin belirttiği gruba ait olan bağlantılı hizmetleri alır.</span><span class="sxs-lookup"><span data-stu-id="8b8db-133">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b8db-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b8db-134">-DefaultProfile</span></span>
<span data-ttu-id="8b8db-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b8db-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b8db-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8db-136">CommonParameters</span></span>
<span data-ttu-id="8b8db-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b8db-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8db-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b8db-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8db-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b8db-139">INPUTS</span></span>

## <span data-ttu-id="8b8db-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b8db-140">OUTPUTS</span></span>

### <span data-ttu-id="8b8db-141">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Windowsazme. Commands. Utilities. PSLinkedService, Microsoft. Windowsazme. Commands. Utilities. PSLinkedService, Microsoft. Windowsazme</span><span class="sxs-lookup"><span data-stu-id="8b8db-141">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="8b8db-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b8db-142">NOTES</span></span>
* <span data-ttu-id="8b8db-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="8b8db-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8b8db-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b8db-144">RELATED LINKS</span></span>

[<span data-ttu-id="8b8db-145">Yeni-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8b8db-145">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="8b8db-146">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8b8db-146">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


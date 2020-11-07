---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: ac3a45f9e150d65829a222e75e7072c6a2bdcd1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938359"
---
# <span data-ttu-id="27eec-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="27eec-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="27eec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27eec-102">SYNOPSIS</span></span>
<span data-ttu-id="27eec-103">Veri Fabrikası içinde bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="27eec-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="27eec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27eec-104">SYNTAX</span></span>

### <span data-ttu-id="27eec-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27eec-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27eec-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="27eec-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27eec-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="27eec-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27eec-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="27eec-108">DESCRIPTION</span></span>
<span data-ttu-id="27eec-109">Get-AzDataFactoryV2LinkedService cmdlet 'i Azure Veri Fabrikası 'ndaki bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="27eec-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="27eec-110">Bağlantılı hizmetin adını belirtirseniz, bu cmdlet bu bağlantılı hizmet hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="27eec-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="27eec-111">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm bağlantılı hizmetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="27eec-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="27eec-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27eec-112">EXAMPLES</span></span>

### <span data-ttu-id="27eec-113">Örnek 1: bağlantılı hizmetler hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="27eec-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

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

<span data-ttu-id="27eec-114">Bu komut WikiADF adlı veri fabrikası ile bağlantılı hizmetler hakkında bilgi alır ve ardından bağlantılı hizmetleri Format-List cmdlet 'ine, ardışık düzen işlecini kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="27eec-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="27eec-115">Bu Windows PowerShell cmdlet 'i sonuçları biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="27eec-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="27eec-116">Daha fazla bilgi için Get-Help biçim-liste yazın.</span><span class="sxs-lookup"><span data-stu-id="27eec-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="27eec-117">Aşağıdaki yollardan birini kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="27eec-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="27eec-118">Örnek 2: belirli bir bağlantılı hizmetle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="27eec-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="27eec-119">Bu komut, WikiADF adındaki LinkedServiceCuratedWikiData adındaki bağlantılı hizmetle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="27eec-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="27eec-120">Örnek 3: DataFactory parametresini belirterek belirli bir bağlantılı hizmetle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="27eec-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="27eec-121">İlk komut, ContosoFactory adındaki veri fabrikasını almak için Get-AzDataFactoryV2 cmdlet 'ini kullanır ve $DataFactory değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="27eec-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="27eec-122">İkinci komut $DataFactory depolanan veri fabrikası için bağlantılı hizmetle ilgili bilgileri alır ve bu bilgileri ardışık düzen işlecini kullanarak Format-Table cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="27eec-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="27eec-123">Format-Table cmdlet, çıktıyı veri kümesi sütunu olarak belirtilen özelliklere sahip veri kümesi olarak biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="27eec-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="27eec-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27eec-124">PARAMETERS</span></span>

### <span data-ttu-id="27eec-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="27eec-125">-DataFactory</span></span>
<span data-ttu-id="27eec-126">PSDataFactory nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27eec-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="27eec-127">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait bağlantılı hizmetleri alır.</span><span class="sxs-lookup"><span data-stu-id="27eec-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27eec-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="27eec-128">-DataFactoryName</span></span>
<span data-ttu-id="27eec-129">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27eec-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="27eec-130">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait bağlantılı hizmetleri alır.</span><span class="sxs-lookup"><span data-stu-id="27eec-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="27eec-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27eec-131">-DefaultProfile</span></span>
<span data-ttu-id="27eec-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27eec-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27eec-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="27eec-133">-Name</span></span>
<span data-ttu-id="27eec-134">Bilgi alınacak bağlantılı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27eec-134">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27eec-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27eec-135">-ResourceGroupName</span></span>
<span data-ttu-id="27eec-136">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27eec-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="27eec-137">Bu cmdlet, bu parametrenin belirttiği gruba ait olan bağlantılı hizmetleri alır.</span><span class="sxs-lookup"><span data-stu-id="27eec-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="27eec-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="27eec-138">-ResourceId</span></span>
<span data-ttu-id="27eec-139">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="27eec-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="27eec-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27eec-140">CommonParameters</span></span>
<span data-ttu-id="27eec-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27eec-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27eec-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27eec-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27eec-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27eec-143">INPUTS</span></span>

### <span data-ttu-id="27eec-144">System. String</span><span class="sxs-lookup"><span data-stu-id="27eec-144">System.String</span></span>

### <span data-ttu-id="27eec-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="27eec-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="27eec-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27eec-146">OUTPUTS</span></span>

### <span data-ttu-id="27eec-147">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="27eec-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="27eec-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27eec-148">NOTES</span></span>
<span data-ttu-id="27eec-149">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="27eec-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="27eec-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27eec-150">RELATED LINKS</span></span>

[<span data-ttu-id="27eec-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="27eec-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="27eec-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="27eec-152">Remove-AzDataFactoryV2LinkedService</span></span>]()

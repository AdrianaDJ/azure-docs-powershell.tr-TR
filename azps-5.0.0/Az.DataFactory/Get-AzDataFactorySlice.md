---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321042"
---
# <span data-ttu-id="57756-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="57756-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="57756-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57756-102">SYNOPSIS</span></span>
<span data-ttu-id="57756-103">Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="57756-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="57756-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57756-104">SYNTAX</span></span>

### <span data-ttu-id="57756-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57756-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57756-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="57756-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57756-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="57756-107">DESCRIPTION</span></span>
<span data-ttu-id="57756-108">**Get-AzDataFactorySlice** cmdlet 'ı Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="57756-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="57756-109">Görüntülenecek bir veri dilimleri aralığı tanımlamak için başlangıç saati ve bitiş saati belirtin.</span><span class="sxs-lookup"><span data-stu-id="57756-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="57756-110">Veri diliminin durumu aşağıdaki değerlerden biridir:</span><span class="sxs-lookup"><span data-stu-id="57756-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="57756-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="57756-111">PendingExecution.</span></span>
<span data-ttu-id="57756-112">Veri işleme başlamadı.</span><span class="sxs-lookup"><span data-stu-id="57756-112">Data processing has not started.</span></span> 
- <span data-ttu-id="57756-113">Progress.</span><span class="sxs-lookup"><span data-stu-id="57756-113">InProgress.</span></span>
<span data-ttu-id="57756-114">Veri işleme sürüyor.</span><span class="sxs-lookup"><span data-stu-id="57756-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="57756-115">Çalıştırılmaya.</span><span class="sxs-lookup"><span data-stu-id="57756-115">Ready.</span></span>
<span data-ttu-id="57756-116">Veri işleme tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="57756-116">Data processing is completed.</span></span>
<span data-ttu-id="57756-117">Veri dilimi, bağımlı dilimlerin kullanması için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="57756-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="57756-118">Erişilemedi.</span><span class="sxs-lookup"><span data-stu-id="57756-118">Failed.</span></span>
<span data-ttu-id="57756-119">Dilimi üreten çalışma başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="57756-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="57756-120">Git.</span><span class="sxs-lookup"><span data-stu-id="57756-120">Skip.</span></span>
<span data-ttu-id="57756-121">Veri Fabrikası dilimin işlenmesini atlar.</span><span class="sxs-lookup"><span data-stu-id="57756-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="57756-122">Yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="57756-122">Retry.</span></span>
<span data-ttu-id="57756-123">Veri Fabrikası dilimi üreten çalıştırmayı yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="57756-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="57756-124">Zaman aşımına uğradı. Veri işleme zaman aşımına uğradı.</span><span class="sxs-lookup"><span data-stu-id="57756-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="57756-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="57756-125">PendingValidation.</span></span>
<span data-ttu-id="57756-126">Veri dilimi işlenmeden önce doğrulamayı bekliyor.</span><span class="sxs-lookup"><span data-stu-id="57756-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="57756-127">Doğrulamayı yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="57756-127">Retry Validation.</span></span>
<span data-ttu-id="57756-128">Veri Fabrikası dilimin doğrulamasını yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="57756-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="57756-129">Doğrulanamadı.</span><span class="sxs-lookup"><span data-stu-id="57756-129">Failed Validation.</span></span>
<span data-ttu-id="57756-130">Dilim doğrulanamadı.</span><span class="sxs-lookup"><span data-stu-id="57756-130">Validation of the slice failed.</span></span>
<span data-ttu-id="57756-131">Dilimlerin her biri için Get-AzDataFactoryRun cmdlet 'ini kullanarak dilimi üreten çalışma hakkında daha fazla bilgi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57756-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="57756-132">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57756-132">EXAMPLES</span></span>

### <span data-ttu-id="57756-133">Örnek 1: veri kümesi veri dilimlerini alma</span><span class="sxs-lookup"><span data-stu-id="57756-133">Example 1: Get data slices for a dataset</span></span>
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

<span data-ttu-id="57756-134">Bu komut, wikiadf adlı veri fabrikası 'ndaki wikiaggreg</span><span class="sxs-lookup"><span data-stu-id="57756-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="57756-135">Komut, StartDateTime parametresi belirttiğinde üretilen dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="57756-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="57756-136">Aşağıdaki örnek kod, bu DataSet 'in kullanılabilirliğini JavaScript nesne gösterimi (JSON) dosyasının her saati olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="57756-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="57756-137">kullanılabilirlik: {dönem: "saat", periodMultiplier: 1} bazı sonuçlar hazır ve diğerleri de PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="57756-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="57756-138">Hazır dilimler zaten çalıştırıldı.</span><span class="sxs-lookup"><span data-stu-id="57756-138">Ready slices have already run.</span></span>
<span data-ttu-id="57756-139">Bekleyen dilimler, Set-AzDataFactoryPipelineActivePeriod cmdlet 'inin belirttiği aralıktaki her saatin sonunda çalıştırılmasını beklemektedir.</span><span class="sxs-lookup"><span data-stu-id="57756-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="57756-140">Bu örnekte, ardışık düzen ve dilimin başlangıç ve bitiş dönemleri bir gün değeri (24 saat) olur.</span><span class="sxs-lookup"><span data-stu-id="57756-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="57756-141">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="57756-141">Example 2</span></span>

<span data-ttu-id="57756-142">Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="57756-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="57756-143">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="57756-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="57756-144">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57756-144">PARAMETERS</span></span>

### <span data-ttu-id="57756-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="57756-145">-DataFactory</span></span>
<span data-ttu-id="57756-146">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57756-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="57756-147">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="57756-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="57756-148">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="57756-148">-DataFactoryName</span></span>
<span data-ttu-id="57756-149">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57756-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="57756-150">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="57756-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="57756-151">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="57756-151">-DatasetName</span></span>
<span data-ttu-id="57756-152">Bu cmdlet 'in dilimleri aldığı veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57756-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57756-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57756-153">-DefaultProfile</span></span>
<span data-ttu-id="57756-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="57756-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57756-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="57756-155">-EndDateTime</span></span>
<span data-ttu-id="57756-156">Bir dönemin sonunu **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="57756-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="57756-157">Bu cmdlet, bu parametrenin belirttiği zamandan önce üretilmiş olan dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="57756-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="57756-158">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="57756-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="57756-159">*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00</span><span class="sxs-lookup"><span data-stu-id="57756-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57756-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57756-160">-ResourceGroupName</span></span>
<span data-ttu-id="57756-161">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57756-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="57756-162">Bu cmdlet, bu parametrenin belirttiği gruba ait dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="57756-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="57756-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="57756-163">-StartDateTime</span></span>
<span data-ttu-id="57756-164">Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="57756-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="57756-165">Bu cmdlet, bu parametrenin belirttiği zamandan sonra üretilen dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="57756-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57756-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57756-166">CommonParameters</span></span>
<span data-ttu-id="57756-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57756-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57756-168">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57756-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57756-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57756-169">INPUTS</span></span>

### <span data-ttu-id="57756-170">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="57756-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="57756-171">System. String</span><span class="sxs-lookup"><span data-stu-id="57756-171">System.String</span></span>

## <span data-ttu-id="57756-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57756-172">OUTPUTS</span></span>

### <span data-ttu-id="57756-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="57756-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="57756-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57756-174">NOTES</span></span>
* <span data-ttu-id="57756-175">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="57756-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="57756-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57756-176">RELATED LINKS</span></span>

[<span data-ttu-id="57756-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="57756-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="57756-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="57756-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="57756-179">Set-Azdatafactorypipelineactivedönem</span><span class="sxs-lookup"><span data-stu-id="57756-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)



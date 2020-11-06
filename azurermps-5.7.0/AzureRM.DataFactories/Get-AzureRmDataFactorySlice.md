---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 77b12c17f46c9a04d1166b3066fa5ea9c2df1d74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586744"
---
# <span data-ttu-id="5a048-101">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="5a048-101">Get-AzureRmDataFactorySlice</span></span>

## <span data-ttu-id="5a048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a048-102">SYNOPSIS</span></span>
<span data-ttu-id="5a048-103">Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5a048-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a048-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a048-104">SYNTAX</span></span>

### <span data-ttu-id="5a048-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5a048-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a048-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5a048-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a048-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a048-107">DESCRIPTION</span></span>
<span data-ttu-id="5a048-108">**Get-AzureRmDataFactorySlice** cmdlet 'ı Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5a048-108">The **Get-AzureRmDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="5a048-109">Görüntülenecek bir veri dilimleri aralığı tanımlamak için başlangıç saati ve bitiş saati belirtin.</span><span class="sxs-lookup"><span data-stu-id="5a048-109">Specify a start time and an end time to define a range of data slices to view.</span></span>

<span data-ttu-id="5a048-110">Veri diliminin durumu aşağıdaki değerlerden biridir:</span><span class="sxs-lookup"><span data-stu-id="5a048-110">The status of a data slice is one of the following values:</span></span> 

- <span data-ttu-id="5a048-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="5a048-111">PendingExecution.</span></span>
<span data-ttu-id="5a048-112">Veri işleme başlamadı.</span><span class="sxs-lookup"><span data-stu-id="5a048-112">Data processing has not started.</span></span> 
- <span data-ttu-id="5a048-113">Progress.</span><span class="sxs-lookup"><span data-stu-id="5a048-113">InProgress.</span></span>
<span data-ttu-id="5a048-114">Veri işleme sürüyor.</span><span class="sxs-lookup"><span data-stu-id="5a048-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="5a048-115">Çalıştırılmaya.</span><span class="sxs-lookup"><span data-stu-id="5a048-115">Ready.</span></span>
<span data-ttu-id="5a048-116">Veri işleme tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="5a048-116">Data processing is completed.</span></span>
<span data-ttu-id="5a048-117">Veri dilimi, bağımlı dilimlerin kullanması için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="5a048-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="5a048-118">Erişilemedi.</span><span class="sxs-lookup"><span data-stu-id="5a048-118">Failed.</span></span>
<span data-ttu-id="5a048-119">Dilimi üreten çalışma başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="5a048-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="5a048-120">Git.</span><span class="sxs-lookup"><span data-stu-id="5a048-120">Skip.</span></span>
<span data-ttu-id="5a048-121">Veri Fabrikası dilimin işlenmesini atlar.</span><span class="sxs-lookup"><span data-stu-id="5a048-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="5a048-122">Yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="5a048-122">Retry.</span></span>
<span data-ttu-id="5a048-123">Veri Fabrikası dilimi üreten çalıştırmayı yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="5a048-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="5a048-124">Zaman aşımına uğradı. Veri işleme zaman aşımına uğradı.</span><span class="sxs-lookup"><span data-stu-id="5a048-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="5a048-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="5a048-125">PendingValidation.</span></span>
<span data-ttu-id="5a048-126">Veri dilimi işlenmeden önce doğrulamayı bekliyor.</span><span class="sxs-lookup"><span data-stu-id="5a048-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="5a048-127">Doğrulamayı yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="5a048-127">Retry Validation.</span></span>
<span data-ttu-id="5a048-128">Veri Fabrikası dilimin doğrulamasını yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="5a048-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="5a048-129">Doğrulanamadı.</span><span class="sxs-lookup"><span data-stu-id="5a048-129">Failed Validation.</span></span>
<span data-ttu-id="5a048-130">Dilim doğrulanamadı.</span><span class="sxs-lookup"><span data-stu-id="5a048-130">Validation of the slice failed.</span></span>

<span data-ttu-id="5a048-131">Dilimlerin her biri için Get-AzureRmDataFactoryRun cmdlet 'ini kullanarak dilimi üreten çalışma hakkında daha fazla bilgi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a048-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzureRmDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="5a048-132">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a048-132">EXAMPLES</span></span>

### <span data-ttu-id="5a048-133">Örnek 1: veri kümesi veri dilimlerini alma</span><span class="sxs-lookup"><span data-stu-id="5a048-133">Example 1: Get data slices for a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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

<span data-ttu-id="5a048-134">Bu komut, wikiadf adlı veri fabrikası 'ndaki wikiaggreg</span><span class="sxs-lookup"><span data-stu-id="5a048-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="5a048-135">Komut, StartDateTime parametresi belirttiğinde üretilen dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="5a048-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="5a048-136">Aşağıdaki örnek kod, bu DataSet 'in kullanılabilirliğini JavaScript nesne gösterimi (JSON) dosyasının her saati olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5a048-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>

                        availability: 
                        {
                        period: "Hour",
                        periodMultiplier: 1
                        }

                    Some of the results are Ready and others are PendingExecution.
<span data-ttu-id="5a048-137">Hazır dilimler zaten çalıştırıldı.</span><span class="sxs-lookup"><span data-stu-id="5a048-137">Ready slices have already run.</span></span>
<span data-ttu-id="5a048-138">Bekleyen dilimler, Set-AzureRmDataFactoryPipelineActivePeriod cmdlet 'inin belirttiği aralıktaki her saatin sonunda çalıştırılmasını beklemektedir.</span><span class="sxs-lookup"><span data-stu-id="5a048-138">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzureRmDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="5a048-139">Bu örnekte, ardışık düzen ve dilimin başlangıç ve bitiş dönemleri bir gün değeri (24 saat) olur.</span><span class="sxs-lookup"><span data-stu-id="5a048-139">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="5a048-140">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a048-140">PARAMETERS</span></span>

### <span data-ttu-id="5a048-141">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5a048-141">-DataFactory</span></span>
<span data-ttu-id="5a048-142">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a048-142">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5a048-143">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="5a048-143">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a048-144">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5a048-144">-DataFactoryName</span></span>
<span data-ttu-id="5a048-145">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a048-145">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5a048-146">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="5a048-146">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a048-147">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="5a048-147">-DatasetName</span></span>
<span data-ttu-id="5a048-148">Bu cmdlet 'in dilimleri aldığı veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a048-148">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a048-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a048-149">-DefaultProfile</span></span>
<span data-ttu-id="5a048-150">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5a048-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a048-151">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="5a048-151">-EndDateTime</span></span>
<span data-ttu-id="5a048-152">Bir dönemin sonunu **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a048-152">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="5a048-153">Bu cmdlet, bu parametrenin belirttiği zamandan önce üretilmiş olan dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="5a048-153">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="5a048-154">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="5a048-154">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="5a048-155">*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir:</span><span class="sxs-lookup"><span data-stu-id="5a048-155">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="5a048-156">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pasifik standart saati)</span><span class="sxs-lookup"><span data-stu-id="5a048-156">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="5a048-157">Varsayılan saat dilimi göstergesi UTC.</span><span class="sxs-lookup"><span data-stu-id="5a048-157">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a048-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a048-158">-ResourceGroupName</span></span>
<span data-ttu-id="5a048-159">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a048-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5a048-160">Bu cmdlet, bu parametrenin belirttiği gruba ait dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="5a048-160">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a048-161">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="5a048-161">-StartDateTime</span></span>
<span data-ttu-id="5a048-162">Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a048-162">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="5a048-163">Bu cmdlet, bu parametrenin belirttiği zamandan sonra üretilen dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="5a048-163">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a048-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a048-164">CommonParameters</span></span>
<span data-ttu-id="5a048-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a048-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a048-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a048-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a048-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a048-167">INPUTS</span></span>

### <span data-ttu-id="5a048-168">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5a048-168">None</span></span>
<span data-ttu-id="5a048-169">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5a048-169">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a048-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a048-170">OUTPUTS</span></span>

### <span data-ttu-id="5a048-171">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft. Windowsazve. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5a048-171">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="5a048-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a048-172">NOTES</span></span>
* <span data-ttu-id="5a048-173">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="5a048-173">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5a048-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a048-174">RELATED LINKS</span></span>

[<span data-ttu-id="5a048-175">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="5a048-175">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

[<span data-ttu-id="5a048-176">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="5a048-176">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="5a048-177">Set-Azurermdatafactoryptam</span><span class="sxs-lookup"><span data-stu-id="5a048-177">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)



---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 038f611edbbec0f5f6bb1be433a1c1cee8fa2990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587987"
---
# <span data-ttu-id="b2e29-101">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="b2e29-101">Get-AzureRmDataFactorySlice</span></span>

## <span data-ttu-id="b2e29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e29-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e29-103">Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="b2e29-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2e29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2e29-104">SYNTAX</span></span>

### <span data-ttu-id="b2e29-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b2e29-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2e29-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b2e29-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2e29-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2e29-107">DESCRIPTION</span></span>
<span data-ttu-id="b2e29-108">**Get-AzureRmDataFactorySlice** cmdlet 'ı Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="b2e29-108">The **Get-AzureRmDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="b2e29-109">Görüntülenecek bir veri dilimleri aralığı tanımlamak için başlangıç saati ve bitiş saati belirtin.</span><span class="sxs-lookup"><span data-stu-id="b2e29-109">Specify a start time and an end time to define a range of data slices to view.</span></span>

<span data-ttu-id="b2e29-110">Veri diliminin durumu aşağıdaki değerlerden biridir:</span><span class="sxs-lookup"><span data-stu-id="b2e29-110">The status of a data slice is one of the following values:</span></span> 

- <span data-ttu-id="b2e29-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="b2e29-111">PendingExecution.</span></span>
<span data-ttu-id="b2e29-112">Veri işleme başlamadı.</span><span class="sxs-lookup"><span data-stu-id="b2e29-112">Data processing has not started.</span></span> 
- <span data-ttu-id="b2e29-113">Progress.</span><span class="sxs-lookup"><span data-stu-id="b2e29-113">InProgress.</span></span>
<span data-ttu-id="b2e29-114">Veri işleme sürüyor.</span><span class="sxs-lookup"><span data-stu-id="b2e29-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="b2e29-115">Çalıştırılmaya.</span><span class="sxs-lookup"><span data-stu-id="b2e29-115">Ready.</span></span>
<span data-ttu-id="b2e29-116">Veri işleme tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="b2e29-116">Data processing is completed.</span></span>
<span data-ttu-id="b2e29-117">Veri dilimi, bağımlı dilimlerin kullanması için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="b2e29-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="b2e29-118">Erişilemedi.</span><span class="sxs-lookup"><span data-stu-id="b2e29-118">Failed.</span></span>
<span data-ttu-id="b2e29-119">Dilimi üreten çalışma başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="b2e29-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="b2e29-120">Git.</span><span class="sxs-lookup"><span data-stu-id="b2e29-120">Skip.</span></span>
<span data-ttu-id="b2e29-121">Veri Fabrikası dilimin işlenmesini atlar.</span><span class="sxs-lookup"><span data-stu-id="b2e29-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="b2e29-122">Yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="b2e29-122">Retry.</span></span>
<span data-ttu-id="b2e29-123">Veri Fabrikası dilimi üreten çalıştırmayı yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="b2e29-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="b2e29-124">Zaman aşımına uğradı. Veri işleme zaman aşımına uğradı.</span><span class="sxs-lookup"><span data-stu-id="b2e29-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="b2e29-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="b2e29-125">PendingValidation.</span></span>
<span data-ttu-id="b2e29-126">Veri dilimi işlenmeden önce doğrulamayı bekliyor.</span><span class="sxs-lookup"><span data-stu-id="b2e29-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="b2e29-127">Doğrulamayı yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="b2e29-127">Retry Validation.</span></span>
<span data-ttu-id="b2e29-128">Veri Fabrikası dilimin doğrulamasını yeniden dener.</span><span class="sxs-lookup"><span data-stu-id="b2e29-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="b2e29-129">Doğrulanamadı.</span><span class="sxs-lookup"><span data-stu-id="b2e29-129">Failed Validation.</span></span>
<span data-ttu-id="b2e29-130">Dilim doğrulanamadı.</span><span class="sxs-lookup"><span data-stu-id="b2e29-130">Validation of the slice failed.</span></span>

<span data-ttu-id="b2e29-131">Dilimlerin her biri için Get-AzureRmDataFactoryRun cmdlet 'ini kullanarak dilimi üreten çalışma hakkında daha fazla bilgi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2e29-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzureRmDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="b2e29-132">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2e29-132">EXAMPLES</span></span>

### <span data-ttu-id="b2e29-133">Örnek 1: veri kümesi veri dilimlerini alma</span><span class="sxs-lookup"><span data-stu-id="b2e29-133">Example 1: Get data slices for a dataset</span></span>
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

<span data-ttu-id="b2e29-134">Bu komut, wikiadf adlı veri fabrikası 'ndaki wikiaggreg</span><span class="sxs-lookup"><span data-stu-id="b2e29-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="b2e29-135">Komut, StartDateTime parametresi belirttiğinde üretilen dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="b2e29-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="b2e29-136">Aşağıdaki örnek kod, bu DataSet 'in kullanılabilirliğini JavaScript nesne gösterimi (JSON) dosyasının her saati olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b2e29-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>

                        availability: 
                        {
                        period: "Hour",
                        periodMultiplier: 1
                        }

                    Some of the results are Ready and others are PendingExecution.
<span data-ttu-id="b2e29-137">Hazır dilimler zaten çalıştırıldı.</span><span class="sxs-lookup"><span data-stu-id="b2e29-137">Ready slices have already run.</span></span>
<span data-ttu-id="b2e29-138">Bekleyen dilimler, Set-AzureRmDataFactoryPipelineActivePeriod cmdlet 'inin belirttiği aralıktaki her saatin sonunda çalıştırılmasını beklemektedir.</span><span class="sxs-lookup"><span data-stu-id="b2e29-138">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzureRmDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="b2e29-139">Bu örnekte, ardışık düzen ve dilimin başlangıç ve bitiş dönemleri bir gün değeri (24 saat) olur.</span><span class="sxs-lookup"><span data-stu-id="b2e29-139">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="b2e29-140">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2e29-140">PARAMETERS</span></span>

### <span data-ttu-id="b2e29-141">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b2e29-141">-DataFactory</span></span>
<span data-ttu-id="b2e29-142">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2e29-142">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b2e29-143">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="b2e29-143">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2e29-144">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b2e29-144">-DataFactoryName</span></span>
<span data-ttu-id="b2e29-145">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2e29-145">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b2e29-146">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="b2e29-146">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2e29-147">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="b2e29-147">-DatasetName</span></span>
<span data-ttu-id="b2e29-148">Bu cmdlet 'in dilimleri aldığı veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2e29-148">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="b2e29-149">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="b2e29-149">-EndDateTime</span></span>
<span data-ttu-id="b2e29-150">Bir dönemin sonunu **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2e29-150">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="b2e29-151">Bu cmdlet, bu parametrenin belirttiği zamandan önce üretilmiş olan dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="b2e29-151">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="b2e29-152">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b2e29-152">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="b2e29-153">*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir:</span><span class="sxs-lookup"><span data-stu-id="b2e29-153">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="b2e29-154">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pasifik standart saati)</span><span class="sxs-lookup"><span data-stu-id="b2e29-154">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="b2e29-155">Varsayılan saat dilimi göstergesi UTC.</span><span class="sxs-lookup"><span data-stu-id="b2e29-155">The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="b2e29-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e29-156">-ResourceGroupName</span></span>
<span data-ttu-id="b2e29-157">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2e29-157">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b2e29-158">Bu cmdlet, bu parametrenin belirttiği gruba ait dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="b2e29-158">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2e29-159">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="b2e29-159">-StartDateTime</span></span>
<span data-ttu-id="b2e29-160">Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2e29-160">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="b2e29-161">Bu cmdlet, bu parametrenin belirttiği zamandan sonra üretilen dilimleri alır.</span><span class="sxs-lookup"><span data-stu-id="b2e29-161">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2e29-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e29-162">-DefaultProfile</span></span>
<span data-ttu-id="b2e29-163">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2e29-163">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2e29-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e29-164">CommonParameters</span></span>
<span data-ttu-id="b2e29-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2e29-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e29-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e29-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e29-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2e29-167">INPUTS</span></span>

## <span data-ttu-id="b2e29-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2e29-168">OUTPUTS</span></span>

### <span data-ttu-id="b2e29-169">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft. Windowsazve. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b2e29-169">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b2e29-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2e29-170">NOTES</span></span>
* <span data-ttu-id="b2e29-171">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="b2e29-171">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b2e29-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2e29-172">RELATED LINKS</span></span>

[<span data-ttu-id="b2e29-173">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="b2e29-173">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

[<span data-ttu-id="b2e29-174">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="b2e29-174">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="b2e29-175">Set-Azurermdatafactoryptam</span><span class="sxs-lookup"><span data-stu-id="b2e29-175">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)



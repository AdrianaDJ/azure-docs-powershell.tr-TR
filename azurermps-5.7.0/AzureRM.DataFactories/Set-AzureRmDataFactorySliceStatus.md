---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 8e1d189173c9825876018351ef36a2b73f285a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587577"
---
# <span data-ttu-id="572d2-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="572d2-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="572d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="572d2-102">SYNOPSIS</span></span>
<span data-ttu-id="572d2-103">Azure Veri Fabrikası 'nde bir veri kümesi için dilimlerin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="572d2-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="572d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="572d2-104">SYNTAX</span></span>

### <span data-ttu-id="572d2-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="572d2-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572d2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="572d2-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="572d2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="572d2-107">DESCRIPTION</span></span>
<span data-ttu-id="572d2-108">**Set-AzureRmDataFactorySliceStatus** cmdlet 'ı Azure Veri Fabrikası 'nde bir veri kümesi için dilimlerin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="572d2-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="572d2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="572d2-109">EXAMPLES</span></span>

### <span data-ttu-id="572d2-110">Örnek 1: tüm dilimlerin durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="572d2-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="572d2-111">Bu komut, Dawikiaggregduduara adlı veri kümesindeki tüm dilimlerin, WikiADF adlı veri fabrikası beklemeyi beklemek için durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="572d2-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="572d2-112">*UpdateType* parametresinde UpstreamInPipeline değeri vardır ve bu nedenle komut veri kümesindeki her bir dilimin ve tüm bağımlı veri kümelerinin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="572d2-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="572d2-113">Dependent veri kümeleri, potansiyel satış için giriş veri kümeleri olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="572d2-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="572d2-114">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="572d2-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="572d2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="572d2-115">PARAMETERS</span></span>

### <span data-ttu-id="572d2-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="572d2-116">-DataFactory</span></span>
<span data-ttu-id="572d2-117">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="572d2-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="572d2-118">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimlerin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="572d2-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="572d2-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="572d2-119">-DataFactoryName</span></span>
<span data-ttu-id="572d2-120">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="572d2-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="572d2-121">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimlerin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="572d2-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="572d2-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="572d2-122">-DatasetName</span></span>
<span data-ttu-id="572d2-123">Bu cmdlet 'in dilimleri değiştirdiği veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="572d2-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="572d2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572d2-124">-DefaultProfile</span></span>
<span data-ttu-id="572d2-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="572d2-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="572d2-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="572d2-126">-EndDateTime</span></span>
<span data-ttu-id="572d2-127">Bir dönemin sonunu **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="572d2-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="572d2-128">Bu saat, veri diliminin sonu.</span><span class="sxs-lookup"><span data-stu-id="572d2-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="572d2-129">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="572d2-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="572d2-130">*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir:</span><span class="sxs-lookup"><span data-stu-id="572d2-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="572d2-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pasifik standart saati)</span><span class="sxs-lookup"><span data-stu-id="572d2-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="572d2-132">Varsayılan saat dilimi göstergesi UTC.</span><span class="sxs-lookup"><span data-stu-id="572d2-132">The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="572d2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572d2-133">-ResourceGroupName</span></span>
<span data-ttu-id="572d2-134">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="572d2-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="572d2-135">Bu cmdlet, bu parametrenin belirttiği gruba ait olan dilimlerin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="572d2-135">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="572d2-136">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="572d2-136">-StartDateTime</span></span>
<span data-ttu-id="572d2-137">Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="572d2-137">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="572d2-138">Bu saat, veri diliminin başlangıcıdır.</span><span class="sxs-lookup"><span data-stu-id="572d2-138">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="572d2-139">-Durum</span><span class="sxs-lookup"><span data-stu-id="572d2-139">-Status</span></span>
<span data-ttu-id="572d2-140">Veri dilimine atanacak bir durum belirtir.</span><span class="sxs-lookup"><span data-stu-id="572d2-140">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="572d2-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="572d2-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="572d2-142">Bekliyor.</span><span class="sxs-lookup"><span data-stu-id="572d2-142">Waiting.</span></span>
<span data-ttu-id="572d2-143">Veri dilimi işlenmeden önce geçerlilik ilkelerine yönelik doğrulamayı beklemektedir.</span><span class="sxs-lookup"><span data-stu-id="572d2-143">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="572d2-144">Çalıştırılmaya.</span><span class="sxs-lookup"><span data-stu-id="572d2-144">Ready.</span></span>
<span data-ttu-id="572d2-145">Veri işleme tamamlandı ve veri dilimi hazır.</span><span class="sxs-lookup"><span data-stu-id="572d2-145">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="572d2-146">Progress.</span><span class="sxs-lookup"><span data-stu-id="572d2-146">InProgress.</span></span>
<span data-ttu-id="572d2-147">Veri işleme sürüyor.</span><span class="sxs-lookup"><span data-stu-id="572d2-147">Data processing is in-progress.</span></span> 
- <span data-ttu-id="572d2-148">Erişilemedi.</span><span class="sxs-lookup"><span data-stu-id="572d2-148">Failed.</span></span>
<span data-ttu-id="572d2-149">Veri işleme başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="572d2-149">Data processing failed.</span></span>
- <span data-ttu-id="572d2-150">Atlanan.</span><span class="sxs-lookup"><span data-stu-id="572d2-150">Skipped.</span></span>
<span data-ttu-id="572d2-151">Veri diliminin işlenmesi atlandı.</span><span class="sxs-lookup"><span data-stu-id="572d2-151">Skipped processing the data slice.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572d2-152">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="572d2-152">-UpdateType</span></span>
<span data-ttu-id="572d2-153">Dilimin güncelleştirme türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="572d2-153">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="572d2-154">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="572d2-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="572d2-155">Tek tek.</span><span class="sxs-lookup"><span data-stu-id="572d2-155">Individual.</span></span>
<span data-ttu-id="572d2-156">Belirtilen zaman aralığındaki veri kümesindeki her bir dilimin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="572d2-156">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="572d2-157">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="572d2-157">UpstreamInPipeline.</span></span>
<span data-ttu-id="572d2-158">Veri kümesindeki her bir dilimin ve potansiyel satışın etkinlik veri kümeleri olarak kullanılan tüm bağımlı veri kümelerinin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="572d2-158">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572d2-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572d2-159">CommonParameters</span></span>
<span data-ttu-id="572d2-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="572d2-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572d2-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="572d2-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572d2-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="572d2-162">INPUTS</span></span>

### <span data-ttu-id="572d2-163">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="572d2-163">None</span></span>
<span data-ttu-id="572d2-164">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="572d2-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="572d2-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="572d2-165">OUTPUTS</span></span>

### <span data-ttu-id="572d2-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="572d2-166">System.Boolean</span></span>

## <span data-ttu-id="572d2-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="572d2-167">NOTES</span></span>
* <span data-ttu-id="572d2-168">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="572d2-168">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="572d2-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="572d2-169">RELATED LINKS</span></span>

[<span data-ttu-id="572d2-170">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="572d2-170">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)



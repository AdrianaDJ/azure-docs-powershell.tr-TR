---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: a7418dd1e0570d4e92310371e658dd130b36bc44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761119"
---
# <span data-ttu-id="68097-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="68097-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="68097-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68097-102">SYNOPSIS</span></span>
<span data-ttu-id="68097-103">Azure Veri Fabrikası 'nde bir veri kümesi için dilimlerin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="68097-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="68097-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68097-104">SYNTAX</span></span>

### <span data-ttu-id="68097-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68097-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68097-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="68097-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68097-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="68097-107">DESCRIPTION</span></span>
<span data-ttu-id="68097-108">**Set-AzDataFactorySliceStatus** cmdlet 'ı Azure Veri Fabrikası 'nde bir veri kümesindeki dilimlerin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="68097-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="68097-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68097-109">EXAMPLES</span></span>

### <span data-ttu-id="68097-110">Örnek 1: tüm dilimlerin durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="68097-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="68097-111">Bu komut, Dawikiaggregduduara adlı veri kümesindeki tüm dilimlerin, WikiADF adlı veri fabrikası beklemeyi beklemek için durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="68097-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="68097-112">*UpdateType* parametresinde UpstreamInPipeline değeri vardır ve bu nedenle komut veri kümesindeki her bir dilimin ve tüm bağımlı veri kümelerinin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="68097-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="68097-113">Dependent veri kümeleri, potansiyel satış için giriş veri kümeleri olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="68097-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="68097-114">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="68097-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="68097-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68097-115">PARAMETERS</span></span>

### <span data-ttu-id="68097-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="68097-116">-DataFactory</span></span>
<span data-ttu-id="68097-117">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="68097-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="68097-118">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimlerin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="68097-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="68097-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="68097-119">-DataFactoryName</span></span>
<span data-ttu-id="68097-120">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68097-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="68097-121">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimlerin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="68097-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="68097-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="68097-122">-DatasetName</span></span>
<span data-ttu-id="68097-123">Bu cmdlet 'in dilimleri değiştirdiği veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68097-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="68097-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68097-124">-DefaultProfile</span></span>
<span data-ttu-id="68097-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="68097-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68097-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="68097-126">-EndDateTime</span></span>
<span data-ttu-id="68097-127">Bir dönemin sonunu **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="68097-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="68097-128">Bu saat, veri diliminin sonu.</span><span class="sxs-lookup"><span data-stu-id="68097-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="68097-129">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="68097-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="68097-130">*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00</span><span class="sxs-lookup"><span data-stu-id="68097-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="68097-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68097-131">-ResourceGroupName</span></span>
<span data-ttu-id="68097-132">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68097-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="68097-133">Bu cmdlet, bu parametrenin belirttiği gruba ait olan dilimlerin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="68097-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="68097-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="68097-134">-StartDateTime</span></span>
<span data-ttu-id="68097-135">Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="68097-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="68097-136">Bu saat, veri diliminin başlangıcıdır.</span><span class="sxs-lookup"><span data-stu-id="68097-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="68097-137">-Durum</span><span class="sxs-lookup"><span data-stu-id="68097-137">-Status</span></span>
<span data-ttu-id="68097-138">Veri dilimine atanacak bir durum belirtir.</span><span class="sxs-lookup"><span data-stu-id="68097-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="68097-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="68097-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68097-140">Bekliyor.</span><span class="sxs-lookup"><span data-stu-id="68097-140">Waiting.</span></span>
<span data-ttu-id="68097-141">Veri dilimi işlenmeden önce geçerlilik ilkelerine yönelik doğrulamayı beklemektedir.</span><span class="sxs-lookup"><span data-stu-id="68097-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="68097-142">Çalıştırılmaya.</span><span class="sxs-lookup"><span data-stu-id="68097-142">Ready.</span></span>
<span data-ttu-id="68097-143">Veri işleme tamamlandı ve veri dilimi hazır.</span><span class="sxs-lookup"><span data-stu-id="68097-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="68097-144">Progress.</span><span class="sxs-lookup"><span data-stu-id="68097-144">InProgress.</span></span>
<span data-ttu-id="68097-145">Veri işleme sürüyor.</span><span class="sxs-lookup"><span data-stu-id="68097-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="68097-146">Erişilemedi.</span><span class="sxs-lookup"><span data-stu-id="68097-146">Failed.</span></span>
<span data-ttu-id="68097-147">Veri işleme başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="68097-147">Data processing failed.</span></span>
- <span data-ttu-id="68097-148">Atlanan.</span><span class="sxs-lookup"><span data-stu-id="68097-148">Skipped.</span></span>
<span data-ttu-id="68097-149">Veri diliminin işlenmesi atlandı.</span><span class="sxs-lookup"><span data-stu-id="68097-149">Skipped processing the data slice.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68097-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="68097-150">-UpdateType</span></span>
<span data-ttu-id="68097-151">Dilimin güncelleştirme türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="68097-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="68097-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="68097-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68097-153">Tek tek.</span><span class="sxs-lookup"><span data-stu-id="68097-153">Individual.</span></span>
<span data-ttu-id="68097-154">Belirtilen zaman aralığındaki veri kümesindeki her bir dilimin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="68097-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="68097-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="68097-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="68097-156">Veri kümesindeki her bir dilimin ve potansiyel satışın etkinlik veri kümeleri olarak kullanılan tüm bağımlı veri kümelerinin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="68097-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68097-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68097-157">CommonParameters</span></span>
<span data-ttu-id="68097-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68097-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68097-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68097-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68097-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68097-160">INPUTS</span></span>

### <span data-ttu-id="68097-161">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="68097-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="68097-162">System. String</span><span class="sxs-lookup"><span data-stu-id="68097-162">System.String</span></span>

## <span data-ttu-id="68097-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68097-163">OUTPUTS</span></span>

### <span data-ttu-id="68097-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68097-164">System.Boolean</span></span>

## <span data-ttu-id="68097-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68097-165">NOTES</span></span>
* <span data-ttu-id="68097-166">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="68097-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="68097-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68097-167">RELATED LINKS</span></span>

[<span data-ttu-id="68097-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="68097-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


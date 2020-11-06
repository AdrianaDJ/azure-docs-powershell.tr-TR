---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 30e6a3ec6d3cd9cba978ed51d6545b3f68375779
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586904"
---
# <span data-ttu-id="26a17-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="26a17-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="26a17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26a17-102">SYNOPSIS</span></span>
<span data-ttu-id="26a17-103">Azure Veri Fabrikası 'nde bir veri kümesi için dilimlerin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="26a17-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26a17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26a17-104">SYNTAX</span></span>

### <span data-ttu-id="26a17-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26a17-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26a17-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="26a17-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26a17-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="26a17-107">DESCRIPTION</span></span>
<span data-ttu-id="26a17-108">**Set-AzureRmDataFactorySliceStatus** cmdlet 'ı Azure Veri Fabrikası 'nde bir veri kümesi için dilimlerin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="26a17-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="26a17-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26a17-109">EXAMPLES</span></span>

### <span data-ttu-id="26a17-110">Örnek 1: tüm dilimlerin durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="26a17-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="26a17-111">Bu komut, Dawikiaggregduduara adlı veri kümesindeki tüm dilimlerin, WikiADF adlı veri fabrikası beklemeyi beklemek için durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="26a17-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="26a17-112">*UpdateType* parametresinde UpstreamInPipeline değeri vardır ve bu nedenle komut veri kümesindeki her bir dilimin ve tüm bağımlı veri kümelerinin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="26a17-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="26a17-113">Dependent veri kümeleri, potansiyel satış için giriş veri kümeleri olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="26a17-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="26a17-114">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="26a17-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="26a17-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26a17-115">PARAMETERS</span></span>

### <span data-ttu-id="26a17-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="26a17-116">-DataFactory</span></span>
<span data-ttu-id="26a17-117">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="26a17-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="26a17-118">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimlerin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="26a17-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="26a17-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="26a17-119">-DataFactoryName</span></span>
<span data-ttu-id="26a17-120">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26a17-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="26a17-121">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimlerin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="26a17-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="26a17-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="26a17-122">-DatasetName</span></span>
<span data-ttu-id="26a17-123">Bu cmdlet 'in dilimleri değiştirdiği veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26a17-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="26a17-124">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="26a17-124">-EndDateTime</span></span>
<span data-ttu-id="26a17-125">Bir dönemin sonunu **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="26a17-125">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="26a17-126">Bu saat, veri diliminin sonu.</span><span class="sxs-lookup"><span data-stu-id="26a17-126">This time is the end of a data slice.</span></span>
<span data-ttu-id="26a17-127">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="26a17-127">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="26a17-128">*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir:</span><span class="sxs-lookup"><span data-stu-id="26a17-128">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="26a17-129">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pasifik standart saati)</span><span class="sxs-lookup"><span data-stu-id="26a17-129">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="26a17-130">Varsayılan saat dilimi göstergesi UTC.</span><span class="sxs-lookup"><span data-stu-id="26a17-130">The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="26a17-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26a17-131">-ResourceGroupName</span></span>
<span data-ttu-id="26a17-132">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26a17-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="26a17-133">Bu cmdlet, bu parametrenin belirttiği gruba ait olan dilimlerin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="26a17-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="26a17-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="26a17-134">-StartDateTime</span></span>
<span data-ttu-id="26a17-135">Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="26a17-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="26a17-136">Bu saat, veri diliminin başlangıcıdır.</span><span class="sxs-lookup"><span data-stu-id="26a17-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="26a17-137">-Durum</span><span class="sxs-lookup"><span data-stu-id="26a17-137">-Status</span></span>
<span data-ttu-id="26a17-138">Veri dilimine atanacak bir durum belirtir.</span><span class="sxs-lookup"><span data-stu-id="26a17-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="26a17-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="26a17-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26a17-140">Bekliyor.</span><span class="sxs-lookup"><span data-stu-id="26a17-140">Waiting.</span></span>
<span data-ttu-id="26a17-141">Veri dilimi işlenmeden önce geçerlilik ilkelerine yönelik doğrulamayı beklemektedir.</span><span class="sxs-lookup"><span data-stu-id="26a17-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="26a17-142">Çalıştırılmaya.</span><span class="sxs-lookup"><span data-stu-id="26a17-142">Ready.</span></span>
<span data-ttu-id="26a17-143">Veri işleme tamamlandı ve veri dilimi hazır.</span><span class="sxs-lookup"><span data-stu-id="26a17-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="26a17-144">Progress.</span><span class="sxs-lookup"><span data-stu-id="26a17-144">InProgress.</span></span>
<span data-ttu-id="26a17-145">Veri işleme sürüyor.</span><span class="sxs-lookup"><span data-stu-id="26a17-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="26a17-146">Erişilemedi.</span><span class="sxs-lookup"><span data-stu-id="26a17-146">Failed.</span></span>
<span data-ttu-id="26a17-147">Veri işleme başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="26a17-147">Data processing failed.</span></span>
- <span data-ttu-id="26a17-148">Atlanan.</span><span class="sxs-lookup"><span data-stu-id="26a17-148">Skipped.</span></span>
<span data-ttu-id="26a17-149">Veri diliminin işlenmesi atlandı.</span><span class="sxs-lookup"><span data-stu-id="26a17-149">Skipped processing the data slice.</span></span>

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

### <span data-ttu-id="26a17-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="26a17-150">-UpdateType</span></span>
<span data-ttu-id="26a17-151">Dilimin güncelleştirme türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="26a17-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="26a17-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="26a17-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26a17-153">Tek tek.</span><span class="sxs-lookup"><span data-stu-id="26a17-153">Individual.</span></span>
<span data-ttu-id="26a17-154">Belirtilen zaman aralığındaki veri kümesindeki her bir dilimin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="26a17-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="26a17-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="26a17-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="26a17-156">Veri kümesindeki her bir dilimin ve potansiyel satışın etkinlik veri kümeleri olarak kullanılan tüm bağımlı veri kümelerinin durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="26a17-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

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

### <span data-ttu-id="26a17-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a17-157">-DefaultProfile</span></span>
<span data-ttu-id="26a17-158">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26a17-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26a17-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a17-159">CommonParameters</span></span>
<span data-ttu-id="26a17-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26a17-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a17-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26a17-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a17-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26a17-162">INPUTS</span></span>

## <span data-ttu-id="26a17-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26a17-163">OUTPUTS</span></span>

### <span data-ttu-id="26a17-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26a17-164">System.Boolean</span></span>

## <span data-ttu-id="26a17-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26a17-165">NOTES</span></span>
* <span data-ttu-id="26a17-166">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="26a17-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="26a17-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26a17-167">RELATED LINKS</span></span>

[<span data-ttu-id="26a17-168">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="26a17-168">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)



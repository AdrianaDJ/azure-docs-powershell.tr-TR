---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 95d0ce0ffe48f845c15f7f00de59a70bfc466fe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762230"
---
# <span data-ttu-id="c6788-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="c6788-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="c6788-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6788-102">SYNOPSIS</span></span>
<span data-ttu-id="c6788-103">Veri Fabrikası ile ilişkilendirilmiş etkinlik pencereleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6788-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6788-104">SYNTAX</span></span>

### <span data-ttu-id="c6788-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c6788-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6788-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c6788-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6788-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6788-107">DESCRIPTION</span></span>
<span data-ttu-id="c6788-108">**Get-AzureRmDataFactoryActivityWindow** cmdlet 'i, veri fabrikası ile ilişkilendirilmiş etkinlik pencereleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="c6788-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6788-109">EXAMPLES</span></span>

### <span data-ttu-id="c6788-110">Örnek 1: Veri Fabrikası ile ilişkilendirilmiş etkinlik pencerelerini alma</span><span class="sxs-lookup"><span data-stu-id="c6788-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

<span data-ttu-id="c6788-111">Bu komut, WikiADF adlı veri fabrikası ile ilişkili tüm etkinlik penceresi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="c6788-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6788-112">PARAMETERS</span></span>

### <span data-ttu-id="c6788-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="c6788-113">-ActivityName</span></span>
<span data-ttu-id="c6788-114">Etkinliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="c6788-115">Bu cmdlet, bu parametrenin belirttiği etkinlik için etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c6788-116">-DataFactory</span></span>
<span data-ttu-id="c6788-117">Cmdlet tarafından döndürülen **Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="c6788-118">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6788-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c6788-119">-DataFactoryName</span></span>
<span data-ttu-id="c6788-120">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="c6788-121">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6788-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="c6788-122">-DatasetName</span></span>
<span data-ttu-id="c6788-123">Veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="c6788-124">Bu cmdlet, bu parametrenin belirttiği veri kümesine ait etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6788-125">-Filtre</span><span class="sxs-lookup"><span data-stu-id="c6788-125">-Filter</span></span>
<span data-ttu-id="c6788-126">Azure Arama filtresi dil bilgisi kullanılarak ifade edilen etkinlik penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-126">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="c6788-127">Dil bilgisi hakkında bilgi için, Azure Search için OData Expression sözdiziminde https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) MSDN 'de) bakın.</span><span class="sxs-lookup"><span data-stu-id="c6788-127">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="c6788-128">Etkinlik Windows listesi, bu parametrenin belirttiği arama dizesine göre filtrelenmiş.</span><span class="sxs-lookup"><span data-stu-id="c6788-128">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-129">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="c6788-129">-OrderBy</span></span>
<span data-ttu-id="c6788-130">Yanıtın etkinlik penceresi liste parametrelerinden biriyle sıralı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-130">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="c6788-131">Virgülle ayrılmış özelliklerin listesi.</span><span class="sxs-lookup"><span data-stu-id="c6788-131">This is a list of comma separated properties.</span></span>
<span data-ttu-id="c6788-132">Örneğin: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="c6788-132">For example: WindowStart, PercentComplete.</span></span>

<span data-ttu-id="c6788-133">Varsayılan olarak, düzen artan sıradır (ASC).</span><span class="sxs-lookup"><span data-stu-id="c6788-133">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="c6788-134">Listeyi azalan düzende sıralamak istiyorsanız açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="c6788-134">Specify DESC if you want to order the list in descending order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-135">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="c6788-135">-PipelineName</span></span>
<span data-ttu-id="c6788-136">Ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="c6788-137">Bu cmdlet, bu parametrenin belirttiği ardışık düzene ait etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-137">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6788-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6788-138">-ResourceGroupName</span></span>
<span data-ttu-id="c6788-139">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-139">Specifies the name of the resource group.</span></span>
<span data-ttu-id="c6788-140">Bu cmdlet, bu parametrenin belirttiği kaynak grubuna ait etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-140">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6788-141">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="c6788-141">-RunEnd</span></span>
<span data-ttu-id="c6788-142">Etkinlik penceresinin bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-142">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="c6788-143">Bu cmdlet, çalışma zamanları *Runstart* ve *runend* zamanları arasında kalan etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-143">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-144">-RunStart</span><span class="sxs-lookup"><span data-stu-id="c6788-144">-RunStart</span></span>
<span data-ttu-id="c6788-145">Etkinlik penceresinin başlangıç saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-145">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="c6788-146">Bu cmdlet, çalışma zamanları *Runstart* ve *runend* zamanları arasında kalan etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-146">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-147">-Üst</span><span class="sxs-lookup"><span data-stu-id="c6788-147">-Top</span></span>
<span data-ttu-id="c6788-148">Bu cmdlet 'in döndürdüğü etkinlik pencerelerinin maksimum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-148">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-149">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="c6788-149">-WindowEnd</span></span>
<span data-ttu-id="c6788-150">Etkinlik bitiş saati penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-150">Specifies the end time of activity window.</span></span>
<span data-ttu-id="c6788-151">Bu cmdlet, süresi *Windowstart* ve *windowend* Times ile biten etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-151">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-152">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="c6788-152">-WindowStart</span></span>
<span data-ttu-id="c6788-153">Etkinlik başlangıç saati penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-153">Specifies the start time of activity window.</span></span>
<span data-ttu-id="c6788-154">Bu cmdlet, süresi *Windowstart* ve *windowend* Times ile biten etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-154">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-155">-WindowState</span><span class="sxs-lookup"><span data-stu-id="c6788-155">-WindowState</span></span>
<span data-ttu-id="c6788-156">Etkinlik penceresinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-156">Specifies the state of the activity window.</span></span>
<span data-ttu-id="c6788-157">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c6788-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6788-158">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c6788-158">None</span></span>
- <span data-ttu-id="c6788-159">Bekliyor</span><span class="sxs-lookup"><span data-stu-id="c6788-159">Waiting</span></span>
- <span data-ttu-id="c6788-160">Progress</span><span class="sxs-lookup"><span data-stu-id="c6788-160">InProgress</span></span>
- <span data-ttu-id="c6788-161">Çalıştırılmaya</span><span class="sxs-lookup"><span data-stu-id="c6788-161">Ready</span></span>
- <span data-ttu-id="c6788-162">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="c6788-162">Failed</span></span>
- <span data-ttu-id="c6788-163">Atlanan</span><span class="sxs-lookup"><span data-stu-id="c6788-163">Skipped</span></span>

<span data-ttu-id="c6788-164">Bu cmdlet, bu parametrenin belirttiği durumda etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-164">This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-165">-Windowsub State</span><span class="sxs-lookup"><span data-stu-id="c6788-165">-WindowSubstate</span></span>
<span data-ttu-id="c6788-166">Etkinlik penceresinin alt durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6788-166">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="c6788-167">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c6788-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6788-168">Edildi</span><span class="sxs-lookup"><span data-stu-id="c6788-168">Canceled</span></span>
- <span data-ttu-id="c6788-169">Zaman aşımına uğradı</span><span class="sxs-lookup"><span data-stu-id="c6788-169">timedOut</span></span>
- <span data-ttu-id="c6788-170">Doğrulama</span><span class="sxs-lookup"><span data-stu-id="c6788-170">Validating</span></span>

<span data-ttu-id="c6788-171">Bu cmdlet, bu parametrenin belirttiği alt durumundaki etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c6788-171">This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6788-172">-DefaultProfile</span></span>
<span data-ttu-id="c6788-173">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6788-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6788-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6788-174">CommonParameters</span></span>
<span data-ttu-id="c6788-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6788-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6788-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6788-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6788-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6788-177">INPUTS</span></span>

## <span data-ttu-id="c6788-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6788-178">OUTPUTS</span></span>

### <span data-ttu-id="c6788-179">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Windowsazve. Commands. Utilities. PSActivyWindow, Microsoft. Windowsazme. Commands. Utilities.</span><span class="sxs-lookup"><span data-stu-id="c6788-179">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSActivyWindow, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="c6788-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6788-180">NOTES</span></span>

## <span data-ttu-id="c6788-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6788-181">RELATED LINKS</span></span>

[<span data-ttu-id="c6788-182">Azure Veri Fabrikası cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c6788-182">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)



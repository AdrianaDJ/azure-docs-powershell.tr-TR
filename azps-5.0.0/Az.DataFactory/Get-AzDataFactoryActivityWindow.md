---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 5b18af8890d255dbd5514cccc0279acafe6bd611
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321078"
---
# <span data-ttu-id="42891-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="42891-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="42891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42891-102">SYNOPSIS</span></span>
<span data-ttu-id="42891-103">Veri Fabrikası ile ilişkilendirilmiş etkinlik pencereleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="42891-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="42891-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42891-104">SYNTAX</span></span>

### <span data-ttu-id="42891-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42891-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42891-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="42891-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42891-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="42891-107">DESCRIPTION</span></span>
<span data-ttu-id="42891-108">**Get-AzDataFactoryActivityWindow** cmdlet 'i, veri fabrikası ile ilişkilendirilmiş etkinlik pencereleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="42891-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="42891-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42891-109">EXAMPLES</span></span>

### <span data-ttu-id="42891-110">Örnek 1: Veri Fabrikası ile ilişkilendirilmiş etkinlik pencerelerini alma</span><span class="sxs-lookup"><span data-stu-id="42891-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
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

<span data-ttu-id="42891-111">Bu komut, WikiADF adlı veri fabrikası ile ilişkili tüm etkinlik penceresi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="42891-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="42891-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42891-112">PARAMETERS</span></span>

### <span data-ttu-id="42891-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="42891-113">-ActivityName</span></span>
<span data-ttu-id="42891-114">Etkinliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="42891-115">Bu cmdlet, bu parametrenin belirttiği etkinlik için etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="42891-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="42891-116">-DataFactory</span></span>
<span data-ttu-id="42891-117">Cmdlet tarafından döndürülen **Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="42891-118">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="42891-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="42891-119">-DataFactoryName</span></span>
<span data-ttu-id="42891-120">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="42891-121">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="42891-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="42891-122">-DatasetName</span></span>
<span data-ttu-id="42891-123">Veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="42891-124">Bu cmdlet, bu parametrenin belirttiği veri kümesine ait etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="42891-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42891-125">-DefaultProfile</span></span>
<span data-ttu-id="42891-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="42891-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42891-127">-Filtre</span><span class="sxs-lookup"><span data-stu-id="42891-127">-Filter</span></span>
<span data-ttu-id="42891-128">Azure Arama filtresi dil bilgisi kullanılarak ifade edilen etkinlik penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="42891-129">Dil bilgisi hakkında bilgi için, Azure Search için OData Expression sözdiziminde https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) MSDN 'de) bakın.</span><span class="sxs-lookup"><span data-stu-id="42891-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="42891-130">Etkinlik Windows listesi, bu parametrenin belirttiği arama dizesine göre filtrelenmiş.</span><span class="sxs-lookup"><span data-stu-id="42891-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="42891-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="42891-131">-OrderBy</span></span>
<span data-ttu-id="42891-132">Yanıtın etkinlik penceresi liste parametrelerinden biriyle sıralı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="42891-133">Virgülle ayrılmış özelliklerin listesi.</span><span class="sxs-lookup"><span data-stu-id="42891-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="42891-134">Örneğin: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="42891-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="42891-135">Varsayılan olarak, düzen artan sıradır (ASC).</span><span class="sxs-lookup"><span data-stu-id="42891-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="42891-136">Listeyi azalan düzende sıralamak istiyorsanız açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="42891-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="42891-137">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="42891-137">-PipelineName</span></span>
<span data-ttu-id="42891-138">Ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="42891-139">Bu cmdlet, bu parametrenin belirttiği ardışık düzene ait etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="42891-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42891-140">-ResourceGroupName</span></span>
<span data-ttu-id="42891-141">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="42891-142">Bu cmdlet, bu parametrenin belirttiği kaynak grubuna ait etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="42891-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="42891-143">-RunEnd</span></span>
<span data-ttu-id="42891-144">Etkinlik penceresinin bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="42891-145">Bu cmdlet, çalışma zamanları *Runstart* ve *runend* zamanları arasında kalan etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="42891-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="42891-146">-RunStart</span></span>
<span data-ttu-id="42891-147">Etkinlik penceresinin başlangıç saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="42891-148">Bu cmdlet, çalışma zamanları *Runstart* ve *runend* zamanları arasında kalan etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="42891-149">-Üst</span><span class="sxs-lookup"><span data-stu-id="42891-149">-Top</span></span>
<span data-ttu-id="42891-150">Bu cmdlet 'in döndürdüğü etkinlik pencerelerinin maksimum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="42891-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="42891-151">-WindowEnd</span></span>
<span data-ttu-id="42891-152">Etkinlik bitiş saati penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="42891-153">Bu cmdlet, süresi *Windowstart* ve *windowend* Times ile biten etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="42891-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="42891-154">-WindowStart</span></span>
<span data-ttu-id="42891-155">Etkinlik başlangıç saati penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="42891-156">Bu cmdlet, süresi *Windowstart* ve *windowend* Times ile biten etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="42891-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="42891-157">-WindowState</span></span>
<span data-ttu-id="42891-158">Etkinlik penceresinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="42891-159">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="42891-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42891-160">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="42891-160">None</span></span>
- <span data-ttu-id="42891-161">Bekliyor</span><span class="sxs-lookup"><span data-stu-id="42891-161">Waiting</span></span>
- <span data-ttu-id="42891-162">Progress</span><span class="sxs-lookup"><span data-stu-id="42891-162">InProgress</span></span>
- <span data-ttu-id="42891-163">Çalıştırılmaya</span><span class="sxs-lookup"><span data-stu-id="42891-163">Ready</span></span>
- <span data-ttu-id="42891-164">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="42891-164">Failed</span></span>
- <span data-ttu-id="42891-165">Atlandı bu cmdlet, bu parametrenin belirttiği durumda etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="42891-166">-Windowsub State</span><span class="sxs-lookup"><span data-stu-id="42891-166">-WindowSubstate</span></span>
<span data-ttu-id="42891-167">Etkinlik penceresinin alt durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="42891-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="42891-168">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="42891-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42891-169">Edildi</span><span class="sxs-lookup"><span data-stu-id="42891-169">Canceled</span></span>
- <span data-ttu-id="42891-170">Zaman aşımına uğradı</span><span class="sxs-lookup"><span data-stu-id="42891-170">timedOut</span></span>
- <span data-ttu-id="42891-171">Bu cmdlet 'in doğrulanması, bu parametrenin belirttiği alt durumdaki etkinlik pencerelerini alır.</span><span class="sxs-lookup"><span data-stu-id="42891-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="42891-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42891-172">CommonParameters</span></span>
<span data-ttu-id="42891-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42891-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42891-174">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42891-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42891-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42891-175">INPUTS</span></span>

### <span data-ttu-id="42891-176">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="42891-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="42891-177">System. String</span><span class="sxs-lookup"><span data-stu-id="42891-177">System.String</span></span>

### <span data-ttu-id="42891-178">System. Nullable ' 1 [[System. DATETIME, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="42891-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="42891-179">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="42891-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="42891-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42891-180">OUTPUTS</span></span>

### <span data-ttu-id="42891-181">Microsoft. Azure. Commands. DataFactory. modeller. PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="42891-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="42891-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42891-182">NOTES</span></span>

## <span data-ttu-id="42891-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42891-183">RELATED LINKS</span></span>

[<span data-ttu-id="42891-184">Azure Veri Fabrikası cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="42891-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)



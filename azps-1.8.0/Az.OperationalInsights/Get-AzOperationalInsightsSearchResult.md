---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
ms.openlocfilehash: 47a8edf304ebc5481073151c180c01a65259149c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759859"
---
# <span data-ttu-id="f5469-101">Get-AzOperationalInsightsSearchResult</span><span class="sxs-lookup"><span data-stu-id="f5469-101">Get-AzOperationalInsightsSearchResult</span></span>

## <span data-ttu-id="f5469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5469-102">SYNOPSIS</span></span>
<span data-ttu-id="f5469-103">Belirtilen parametrelere dayalı olarak arama sonuçlarını getirir.</span><span class="sxs-lookup"><span data-stu-id="f5469-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="f5469-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5469-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String> [[-Top] <Int64>]
 [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>] [[-Start] <DateTime>]
 [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5469-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5469-105">DESCRIPTION</span></span>
<span data-ttu-id="f5469-106">**Get-Azoperationalınsightssearchresult** cmdlet 'i, arama sonuçlarını belirtilen parametrelere göre döndürür.</span><span class="sxs-lookup"><span data-stu-id="f5469-106">The **Get-AzOperationalInsightsSearchResult** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="f5469-107">Döndürülen nesnenin meta veri özelliğindeki aramanın durumuna erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f5469-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="f5469-108">Durum beklemede olduğunda, arama tamamlanmaz ve sonuçlar arşivden olacaktır.</span><span class="sxs-lookup"><span data-stu-id="f5469-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="f5469-109">Döndürülen nesnenin değer özelliğinden aramanın sonuçlarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f5469-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="f5469-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5469-110">EXAMPLES</span></span>

### <span data-ttu-id="f5469-111">Örnek 1: sorgu kullanarak arama sonuçları alma</span><span class="sxs-lookup"><span data-stu-id="f5469-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="f5469-112">Bu komut, sorgu kullanarak tüm arama sonuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f5469-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="f5469-113">Örnek 2: bir KIMLIK kullanarak arama sonuçları alma</span><span class="sxs-lookup"><span data-stu-id="f5469-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="f5469-114">Bu komut arama sonuçlarını bir KIMLIK kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="f5469-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="f5469-115">Örnek 3: sonuçları görüntülemeden önce aramanın tamamlanmasını bekleyin</span><span class="sxs-lookup"><span data-stu-id="f5469-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="f5469-116">Bu komut dosyası aramayı başlatır ve sonuçları görüntülemeden önce tamamlanıncaya kadar bekler.</span><span class="sxs-lookup"><span data-stu-id="f5469-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="f5469-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5469-117">PARAMETERS</span></span>

### <span data-ttu-id="f5469-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5469-118">-DefaultProfile</span></span>
<span data-ttu-id="f5469-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f5469-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5469-120">Uç</span><span class="sxs-lookup"><span data-stu-id="f5469-120">-End</span></span>
<span data-ttu-id="f5469-121">Sorgulanan zaman aralığının sonu.</span><span class="sxs-lookup"><span data-stu-id="f5469-121">End of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5469-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f5469-122">-Id</span></span>
<span data-ttu-id="f5469-123">Kimlik verilirse, bu kimliğin arama sonuçları özgün sorgu parametreleri kullanılarak alınır.</span><span class="sxs-lookup"><span data-stu-id="f5469-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5469-124">-PostHighlight</span><span class="sxs-lookup"><span data-stu-id="f5469-124">-PostHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5469-125">-PreHighlight</span><span class="sxs-lookup"><span data-stu-id="f5469-125">-PreHighlight</span></span>
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

### <span data-ttu-id="f5469-126">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="f5469-126">-Query</span></span>
<span data-ttu-id="f5469-127">Yürütülecek arama sorgusu.</span><span class="sxs-lookup"><span data-stu-id="f5469-127">The search query that will be executed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5469-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5469-128">-ResourceGroupName</span></span>
<span data-ttu-id="f5469-129">Çalışma alanını içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f5469-129">The name of the resource group that contains the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5469-130">-Başlangıç</span><span class="sxs-lookup"><span data-stu-id="f5469-130">-Start</span></span>
<span data-ttu-id="f5469-131">Sorgulanan zaman aralığının başlangıcı.</span><span class="sxs-lookup"><span data-stu-id="f5469-131">Start of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5469-132">-Üst</span><span class="sxs-lookup"><span data-stu-id="f5469-132">-Top</span></span>
<span data-ttu-id="f5469-133">En fazla döndürülecek sonuç sayısı, 5000 ile sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="f5469-133">The maximum number of results to be returned, limited to 5000.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 10
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5469-134">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="f5469-134">-WorkspaceName</span></span>
<span data-ttu-id="f5469-135">Bir çalışma alanı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5469-135">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5469-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5469-136">CommonParameters</span></span>
<span data-ttu-id="f5469-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5469-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5469-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5469-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5469-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5469-139">INPUTS</span></span>

### <span data-ttu-id="f5469-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f5469-140">System.String</span></span>

### <span data-ttu-id="f5469-141">System. Int64</span><span class="sxs-lookup"><span data-stu-id="f5469-141">System.Int64</span></span>

### <span data-ttu-id="f5469-142">System. Nullable ' 1 [[System. DATETIME, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="f5469-142">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f5469-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5469-143">OUTPUTS</span></span>

### <span data-ttu-id="f5469-144">Microsoft. Azure. Commands. Operationalınsights. model. Pssearchsearchsearchresultsresponse</span><span class="sxs-lookup"><span data-stu-id="f5469-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="f5469-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5469-145">NOTES</span></span>

## <span data-ttu-id="f5469-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5469-146">RELATED LINKS</span></span>

[<span data-ttu-id="f5469-147">Get-Azoperationalınsightssavedsearchresult</span><span class="sxs-lookup"><span data-stu-id="f5469-147">Get-AzOperationalInsightsSavedSearchResult</span></span>](./Get-AzOperationalInsightsSavedSearchResult.md)



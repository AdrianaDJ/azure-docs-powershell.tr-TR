---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
ms.openlocfilehash: f4f0ee7a7ab98835e438ffd3d993d0d2bfd7833c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588845"
---
# <span data-ttu-id="26998-101">Get-AzureRmOperationalInsightsSearchResults</span><span class="sxs-lookup"><span data-stu-id="26998-101">Get-AzureRmOperationalInsightsSearchResults</span></span>

## <span data-ttu-id="26998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26998-102">SYNOPSIS</span></span>
<span data-ttu-id="26998-103">Belirtilen parametrelere dayalı olarak arama sonuçlarını getirir.</span><span class="sxs-lookup"><span data-stu-id="26998-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26998-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26998-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Top] <Int64>] [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>]
 [[-Start] <DateTime>] [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26998-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="26998-105">DESCRIPTION</span></span>
<span data-ttu-id="26998-106">**Get-Azurermoperationalınsightssearchresults** cmdlet 'i, arama sonuçlarını belirtilen parametrelere göre döndürür.</span><span class="sxs-lookup"><span data-stu-id="26998-106">The **Get-AzureRmOperationalInsightsSearchResults** cmdlet returns the search results based on the specified parameters.</span></span>

<span data-ttu-id="26998-107">Döndürülen nesnenin meta veri özelliğindeki aramanın durumuna erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26998-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="26998-108">Durum beklemede olduğunda, arama tamamlanmaz ve sonuçlar arşivden olacaktır.</span><span class="sxs-lookup"><span data-stu-id="26998-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>

<span data-ttu-id="26998-109">Döndürülen nesnenin değer özelliğinden aramanın sonuçlarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26998-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="26998-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26998-110">EXAMPLES</span></span>

### <span data-ttu-id="26998-111">Örnek 1: sorgu kullanarak arama sonuçları alma</span><span class="sxs-lookup"><span data-stu-id="26998-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="26998-112">Bu komut, sorgu kullanarak tüm arama sonuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="26998-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="26998-113">Örnek 2: bir KIMLIK kullanarak arama sonuçları alma</span><span class="sxs-lookup"><span data-stu-id="26998-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="26998-114">Bu komut arama sonuçlarını bir KIMLIK kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="26998-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="26998-115">Örnek 3: sonuçları görüntülemeden önce aramanın tamamlanmasını bekleyin</span><span class="sxs-lookup"><span data-stu-id="26998-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="26998-116">Bu komut dosyası aramayı başlatır ve sonuçları görüntülemeden önce tamamlanıncaya kadar bekler.</span><span class="sxs-lookup"><span data-stu-id="26998-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="26998-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26998-117">PARAMETERS</span></span>

### <span data-ttu-id="26998-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26998-118">-DefaultProfile</span></span>
<span data-ttu-id="26998-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="26998-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26998-120">Uç</span><span class="sxs-lookup"><span data-stu-id="26998-120">-End</span></span>
<span data-ttu-id="26998-121">Sorgulanan zaman aralığının sonu.</span><span class="sxs-lookup"><span data-stu-id="26998-121">End of the queried time range.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26998-122">-ID</span><span class="sxs-lookup"><span data-stu-id="26998-122">-Id</span></span>
<span data-ttu-id="26998-123">Kimlik verilirse, bu kimliğin arama sonuçları özgün sorgu parametreleri kullanılarak alınır.</span><span class="sxs-lookup"><span data-stu-id="26998-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26998-124">-PostHighlight</span><span class="sxs-lookup"><span data-stu-id="26998-124">-PostHighlight</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26998-125">-PreHighlight</span><span class="sxs-lookup"><span data-stu-id="26998-125">-PreHighlight</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26998-126">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="26998-126">-Query</span></span>
<span data-ttu-id="26998-127">Yürütülecek arama sorgusu.</span><span class="sxs-lookup"><span data-stu-id="26998-127">The search query that will be executed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26998-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26998-128">-ResourceGroupName</span></span>
<span data-ttu-id="26998-129">Çalışma alanını içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="26998-129">The name of the resource group that contains the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26998-130">-Başlangıç</span><span class="sxs-lookup"><span data-stu-id="26998-130">-Start</span></span>
<span data-ttu-id="26998-131">Sorgulanan zaman aralığının başlangıcı.</span><span class="sxs-lookup"><span data-stu-id="26998-131">Start of the queried time range.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26998-132">-Üst</span><span class="sxs-lookup"><span data-stu-id="26998-132">-Top</span></span>
<span data-ttu-id="26998-133">En fazla döndürülecek sonuç sayısı, 5000 ile sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="26998-133">The maximum number of results to be returned, limited to 5000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26998-134">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="26998-134">-WorkspaceName</span></span>
<span data-ttu-id="26998-135">Bir çalışma alanı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="26998-135">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26998-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26998-136">CommonParameters</span></span>
<span data-ttu-id="26998-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26998-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26998-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26998-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26998-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26998-139">INPUTS</span></span>

### <span data-ttu-id="26998-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="26998-140">None</span></span>
<span data-ttu-id="26998-141">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="26998-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26998-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26998-142">OUTPUTS</span></span>

### <span data-ttu-id="26998-143">PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="26998-143">PSSearchGetSearchResultsResponse</span></span>
<span data-ttu-id="26998-144">**Pssearchgetsearchresultsresponse** NESNESI, JSON biçiminde aramadan döndürülen kayıtların ve aramanın sonuçları hakkında bilgi içeren bir meta veri nesnesinin döndürdüğü bir değer özelliği içerir.</span><span class="sxs-lookup"><span data-stu-id="26998-144">The **PSSearchGetSearchResultsResponse** object includes a Value property that includes the records returned from the search in JSON format and a metadata object that includes information about the results of the search.</span></span>

## <span data-ttu-id="26998-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26998-145">NOTES</span></span>

## <span data-ttu-id="26998-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26998-146">RELATED LINKS</span></span>

[<span data-ttu-id="26998-147">Get-Azurermoperationalınsightssavedsearchresults</span><span class="sxs-lookup"><span data-stu-id="26998-147">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>](./Get-AzureRmOperationalInsightsSavedSearchResults.md)



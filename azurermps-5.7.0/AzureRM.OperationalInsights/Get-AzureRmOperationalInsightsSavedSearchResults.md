---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 9b885193a3e00b9bfe062de4b47feedae36e545f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762363"
---
# <span data-ttu-id="bec72-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="bec72-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="bec72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bec72-102">SYNOPSIS</span></span>
<span data-ttu-id="bec72-103">Sorgudaki sonuçları getirir.</span><span class="sxs-lookup"><span data-stu-id="bec72-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bec72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bec72-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bec72-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bec72-105">DESCRIPTION</span></span>
<span data-ttu-id="bec72-106">**Get-Azurermoperationalınsightssavedsearchresults** cmdlet 'i, arama kimliği tarafından belirtilen sorgudan sonuçları döndürür.</span><span class="sxs-lookup"><span data-stu-id="bec72-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="bec72-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bec72-107">EXAMPLES</span></span>

### <span data-ttu-id="bec72-108">Örnek 1: kayıtlı bir aramanın tüm arama sonuçlarını alma</span><span class="sxs-lookup"><span data-stu-id="bec72-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="bec72-109">Bu komut, kaydedilmiş bir aramanın tüm arama sonuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bec72-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="bec72-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bec72-110">PARAMETERS</span></span>

### <span data-ttu-id="bec72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec72-111">-DefaultProfile</span></span>
<span data-ttu-id="bec72-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bec72-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bec72-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec72-113">-ResourceGroupName</span></span>
<span data-ttu-id="bec72-114">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bec72-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="bec72-115">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="bec72-115">-SavedSearchId</span></span>
<span data-ttu-id="bec72-116">Kayıtlı bir arama KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bec72-116">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="bec72-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="bec72-117">-WorkspaceName</span></span>
<span data-ttu-id="bec72-118">Bir çalışma alanı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="bec72-118">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="bec72-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec72-119">CommonParameters</span></span>
<span data-ttu-id="bec72-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bec72-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec72-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec72-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec72-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bec72-122">INPUTS</span></span>

### <span data-ttu-id="bec72-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bec72-123">None</span></span>
<span data-ttu-id="bec72-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="bec72-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bec72-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bec72-125">OUTPUTS</span></span>

### <span data-ttu-id="bec72-126">Microsoft. Azure. Commands. Operationalınsights. model. Pssearchsearchsearchresultsresponse</span><span class="sxs-lookup"><span data-stu-id="bec72-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="bec72-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bec72-127">NOTES</span></span>

## <span data-ttu-id="bec72-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bec72-128">RELATED LINKS</span></span>

[<span data-ttu-id="bec72-129">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="bec72-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



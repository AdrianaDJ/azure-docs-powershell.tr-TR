---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
ms.openlocfilehash: 0d813f6d0834a40708cc828d5b508cc6452dffc1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938609"
---
# <span data-ttu-id="6cf33-101">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="6cf33-101">Get-AzOperationalInsightsSavedSearchResult</span></span>

## <span data-ttu-id="6cf33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cf33-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf33-103">Sorgudaki sonuçları getirir.</span><span class="sxs-lookup"><span data-stu-id="6cf33-103">Returns the results from a query.</span></span>

## <span data-ttu-id="6cf33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6cf33-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cf33-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6cf33-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf33-106">**Get-Azoperationalınsightssavedsearchresult** cmdlet 'i, arama kimliğiyle belirtilen sorgudan sonuçları döndürür.</span><span class="sxs-lookup"><span data-stu-id="6cf33-106">The **Get-AzOperationalInsightsSavedSearchResult** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="6cf33-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6cf33-107">EXAMPLES</span></span>

### <span data-ttu-id="6cf33-108">Örnek 1: kayıtlı bir aramanın tüm arama sonuçlarını alma</span><span class="sxs-lookup"><span data-stu-id="6cf33-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzOperationalInsightSavedSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="6cf33-109">Bu komut, kaydedilmiş bir aramanın tüm arama sonuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6cf33-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="6cf33-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6cf33-110">PARAMETERS</span></span>

### <span data-ttu-id="6cf33-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf33-111">-DefaultProfile</span></span>
<span data-ttu-id="6cf33-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6cf33-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cf33-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf33-113">-ResourceGroupName</span></span>
<span data-ttu-id="6cf33-114">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cf33-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="6cf33-115">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="6cf33-115">-SavedSearchId</span></span>
<span data-ttu-id="6cf33-116">Kayıtlı bir arama KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cf33-116">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="6cf33-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="6cf33-117">-WorkspaceName</span></span>
<span data-ttu-id="6cf33-118">Bir çalışma alanı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cf33-118">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="6cf33-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf33-119">CommonParameters</span></span>
<span data-ttu-id="6cf33-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6cf33-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf33-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cf33-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf33-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6cf33-122">INPUTS</span></span>

### <span data-ttu-id="6cf33-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6cf33-123">System.String</span></span>

## <span data-ttu-id="6cf33-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6cf33-124">OUTPUTS</span></span>

### <span data-ttu-id="6cf33-125">Microsoft. Azure. Commands. Operationalınsights. model. Pssearchsearchsearchresultsresponse</span><span class="sxs-lookup"><span data-stu-id="6cf33-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="6cf33-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6cf33-126">NOTES</span></span>

## <span data-ttu-id="6cf33-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6cf33-127">RELATED LINKS</span></span>

[<span data-ttu-id="6cf33-128">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="6cf33-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)



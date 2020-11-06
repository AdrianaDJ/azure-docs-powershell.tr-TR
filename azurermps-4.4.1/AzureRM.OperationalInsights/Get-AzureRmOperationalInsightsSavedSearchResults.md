---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 88adac87543c0a51542cc0f79f2f1eb10ca8184b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593047"
---
# <span data-ttu-id="aea0d-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="aea0d-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="aea0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea0d-102">SYNOPSIS</span></span>
<span data-ttu-id="aea0d-103">Sorgudaki sonuçları getirir.</span><span class="sxs-lookup"><span data-stu-id="aea0d-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aea0d-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aea0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aea0d-105">DESCRIPTION</span></span>
<span data-ttu-id="aea0d-106">**Get-Azurermoperationalınsightssavedsearchresults** cmdlet 'i, arama kimliği tarafından belirtilen sorgudan sonuçları döndürür.</span><span class="sxs-lookup"><span data-stu-id="aea0d-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="aea0d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aea0d-107">EXAMPLES</span></span>

### <span data-ttu-id="aea0d-108">Örnek 1: kayıtlı bir aramanın tüm arama sonuçlarını alma</span><span class="sxs-lookup"><span data-stu-id="aea0d-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="aea0d-109">Bu komut, kaydedilmiş bir aramanın tüm arama sonuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="aea0d-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="aea0d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aea0d-110">PARAMETERS</span></span>

### <span data-ttu-id="aea0d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea0d-111">-ResourceGroupName</span></span>
<span data-ttu-id="aea0d-112">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aea0d-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="aea0d-113">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="aea0d-113">-SavedSearchId</span></span>
<span data-ttu-id="aea0d-114">Kayıtlı bir arama KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="aea0d-114">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="aea0d-115">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="aea0d-115">-WorkspaceName</span></span>
<span data-ttu-id="aea0d-116">Bir çalışma alanı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="aea0d-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="aea0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea0d-117">-DefaultProfile</span></span>
<span data-ttu-id="aea0d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aea0d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aea0d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea0d-119">CommonParameters</span></span>
<span data-ttu-id="aea0d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aea0d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea0d-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea0d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea0d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aea0d-122">INPUTS</span></span>

## <span data-ttu-id="aea0d-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aea0d-123">OUTPUTS</span></span>

### <span data-ttu-id="aea0d-124">Microsoft. Azure. Commands. Operationalınsights. model. Pssearchsearchsearchresultsresponse</span><span class="sxs-lookup"><span data-stu-id="aea0d-124">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="aea0d-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aea0d-125">NOTES</span></span>

## <span data-ttu-id="aea0d-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aea0d-126">RELATED LINKS</span></span>

[<span data-ttu-id="aea0d-127">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="aea0d-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



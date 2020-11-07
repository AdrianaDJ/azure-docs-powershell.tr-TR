---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 6a330541d72dd2672eea829fdc5bdcc160f10606
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761939"
---
# <span data-ttu-id="c4be6-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="c4be6-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="c4be6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4be6-102">SYNOPSIS</span></span>
<span data-ttu-id="c4be6-103">Belirtilen çalışma alanı için tüm kaydedilen aramaları döndürür.</span><span class="sxs-lookup"><span data-stu-id="c4be6-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="c4be6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4be6-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4be6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4be6-105">DESCRIPTION</span></span>
<span data-ttu-id="c4be6-106">**Get-Azoperationalınsightssavedsearch** cmdlet 'i, kayıtlı BIR arama kimliği belirtmezseniz belirtilen kaynak grubundaki belirli bir çalışma alanı için kaydedilen aramaların tümünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="c4be6-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="c4be6-107">Kayıtlı bir arama KIMLIĞI belirtirseniz, bu KIMLIĞE karşılık gelen kayıtlı arama döndürülür.</span><span class="sxs-lookup"><span data-stu-id="c4be6-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="c4be6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4be6-108">EXAMPLES</span></span>

### <span data-ttu-id="c4be6-109">Örnek 1: çalışma alanı için tüm kaydedilen aramaları alma</span><span class="sxs-lookup"><span data-stu-id="c4be6-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="c4be6-110">Bu komut, çalışma alanıyla ilişkilendirilmiş kaydedilmiş kaynakların tümünü alır.</span><span class="sxs-lookup"><span data-stu-id="c4be6-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="c4be6-111">Örnek 2: KIMLIĞE göre kaydedilmiş belirli bir aramayı alma</span><span class="sxs-lookup"><span data-stu-id="c4be6-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="c4be6-112">Bu komut, belirli bir kaydedilmiş aramayı KIMLIĞIYLE alır.</span><span class="sxs-lookup"><span data-stu-id="c4be6-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="c4be6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4be6-113">PARAMETERS</span></span>

### <span data-ttu-id="c4be6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4be6-114">-DefaultProfile</span></span>
<span data-ttu-id="c4be6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c4be6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4be6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4be6-116">-ResourceGroupName</span></span>
<span data-ttu-id="c4be6-117">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4be6-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c4be6-118">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="c4be6-118">-SavedSearchId</span></span>
<span data-ttu-id="c4be6-119">Kayıtlı bir arama KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4be6-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="c4be6-120">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="c4be6-120">-WorkspaceName</span></span>
<span data-ttu-id="c4be6-121">Bir çalışma alanı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4be6-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="c4be6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4be6-122">CommonParameters</span></span>
<span data-ttu-id="c4be6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4be6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4be6-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4be6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4be6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4be6-125">INPUTS</span></span>

### <span data-ttu-id="c4be6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c4be6-126">System.String</span></span>

## <span data-ttu-id="c4be6-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4be6-127">OUTPUTS</span></span>

### <span data-ttu-id="c4be6-128">Microsoft. Azure. Commands. Operationalınsights. model. Pssearchsearchlistlistresponse</span><span class="sxs-lookup"><span data-stu-id="c4be6-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="c4be6-129">Microsoft. Azure. Commands. Operationalınsights. modeller</span><span class="sxs-lookup"><span data-stu-id="c4be6-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="c4be6-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4be6-130">NOTES</span></span>

## <span data-ttu-id="c4be6-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4be6-131">RELATED LINKS</span></span>

[<span data-ttu-id="c4be6-132">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c4be6-132">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)



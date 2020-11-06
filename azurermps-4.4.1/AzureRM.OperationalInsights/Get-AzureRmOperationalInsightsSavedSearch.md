---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 4daf2a86515522c3843d5d0225c133f0ff3686ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592596"
---
# <span data-ttu-id="2f42f-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="2f42f-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="2f42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f42f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f42f-103">Belirtilen çalışma alanı için tüm kaydedilen aramaları döndürür.</span><span class="sxs-lookup"><span data-stu-id="2f42f-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f42f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f42f-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f42f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f42f-105">DESCRIPTION</span></span>
<span data-ttu-id="2f42f-106">**Get-Azurermoperationalınsightssavedsearch** cmdlet 'i, kayıtlı BIR arama kimliği belirtmezseniz belirtilen kaynak grubundaki belirli bir çalışma alanı için kaydedilen aramaların tümünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="2f42f-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="2f42f-107">Kayıtlı bir arama KIMLIĞI belirtirseniz, bu KIMLIĞE karşılık gelen kayıtlı arama döndürülür.</span><span class="sxs-lookup"><span data-stu-id="2f42f-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="2f42f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f42f-108">EXAMPLES</span></span>

### <span data-ttu-id="2f42f-109">Örnek 1: çalışma alanı için tüm kaydedilen aramaları alma</span><span class="sxs-lookup"><span data-stu-id="2f42f-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="2f42f-110">Bu komut, çalışma alanıyla ilişkilendirilmiş kaydedilmiş kaynakların tümünü alır.</span><span class="sxs-lookup"><span data-stu-id="2f42f-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="2f42f-111">Örnek 2: KIMLIĞE göre kaydedilmiş belirli bir aramayı alma</span><span class="sxs-lookup"><span data-stu-id="2f42f-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="2f42f-112">Bu komut, belirli bir kaydedilmiş aramayı KIMLIĞIYLE alır.</span><span class="sxs-lookup"><span data-stu-id="2f42f-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="2f42f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f42f-113">PARAMETERS</span></span>

### <span data-ttu-id="2f42f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f42f-114">-ResourceGroupName</span></span>
<span data-ttu-id="2f42f-115">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f42f-115">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="2f42f-116">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="2f42f-116">-SavedSearchId</span></span>
<span data-ttu-id="2f42f-117">Kayıtlı bir arama KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f42f-117">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="2f42f-118">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="2f42f-118">-WorkspaceName</span></span>
<span data-ttu-id="2f42f-119">Bir çalışma alanı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f42f-119">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="2f42f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f42f-120">-DefaultProfile</span></span>
<span data-ttu-id="2f42f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f42f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f42f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f42f-122">CommonParameters</span></span>
<span data-ttu-id="2f42f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f42f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f42f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f42f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f42f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f42f-125">INPUTS</span></span>

## <span data-ttu-id="2f42f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f42f-126">OUTPUTS</span></span>

### <span data-ttu-id="2f42f-127">Microsoft. Azure. Commands. Operationalınsights. model. Pssearchsearchlistlistresponse</span><span class="sxs-lookup"><span data-stu-id="2f42f-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="2f42f-128">Microsoft. Azure. Commands. Operationalınsights. modeller</span><span class="sxs-lookup"><span data-stu-id="2f42f-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="2f42f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f42f-129">NOTES</span></span>

## <span data-ttu-id="2f42f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f42f-130">RELATED LINKS</span></span>

[<span data-ttu-id="2f42f-131">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="2f42f-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



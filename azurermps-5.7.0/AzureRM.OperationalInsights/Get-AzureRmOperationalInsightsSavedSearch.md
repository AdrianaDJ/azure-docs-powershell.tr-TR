---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7022c7b2fcc9fb0f11ded4034a0c78c4faa65237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588850"
---
# <span data-ttu-id="21f8a-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="21f8a-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="21f8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="21f8a-103">Belirtilen çalışma alanı için tüm kaydedilen aramaları döndürür.</span><span class="sxs-lookup"><span data-stu-id="21f8a-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21f8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21f8a-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21f8a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21f8a-105">DESCRIPTION</span></span>
<span data-ttu-id="21f8a-106">**Get-Azurermoperationalınsightssavedsearch** cmdlet 'i, kayıtlı BIR arama kimliği belirtmezseniz belirtilen kaynak grubundaki belirli bir çalışma alanı için kaydedilen aramaların tümünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="21f8a-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="21f8a-107">Kayıtlı bir arama KIMLIĞI belirtirseniz, bu KIMLIĞE karşılık gelen kayıtlı arama döndürülür.</span><span class="sxs-lookup"><span data-stu-id="21f8a-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="21f8a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21f8a-108">EXAMPLES</span></span>

### <span data-ttu-id="21f8a-109">Örnek 1: çalışma alanı için tüm kaydedilen aramaları alma</span><span class="sxs-lookup"><span data-stu-id="21f8a-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="21f8a-110">Bu komut, çalışma alanıyla ilişkilendirilmiş kaydedilmiş kaynakların tümünü alır.</span><span class="sxs-lookup"><span data-stu-id="21f8a-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="21f8a-111">Örnek 2: KIMLIĞE göre kaydedilmiş belirli bir aramayı alma</span><span class="sxs-lookup"><span data-stu-id="21f8a-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="21f8a-112">Bu komut, belirli bir kaydedilmiş aramayı KIMLIĞIYLE alır.</span><span class="sxs-lookup"><span data-stu-id="21f8a-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="21f8a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21f8a-113">PARAMETERS</span></span>

### <span data-ttu-id="21f8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f8a-114">-DefaultProfile</span></span>
<span data-ttu-id="21f8a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="21f8a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21f8a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f8a-116">-ResourceGroupName</span></span>
<span data-ttu-id="21f8a-117">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f8a-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="21f8a-118">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="21f8a-118">-SavedSearchId</span></span>
<span data-ttu-id="21f8a-119">Kayıtlı bir arama KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f8a-119">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f8a-120">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="21f8a-120">-WorkspaceName</span></span>
<span data-ttu-id="21f8a-121">Bir çalışma alanı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f8a-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="21f8a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f8a-122">CommonParameters</span></span>
<span data-ttu-id="21f8a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21f8a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f8a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21f8a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f8a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21f8a-125">INPUTS</span></span>

### <span data-ttu-id="21f8a-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="21f8a-126">None</span></span>
<span data-ttu-id="21f8a-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="21f8a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21f8a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21f8a-128">OUTPUTS</span></span>

### <span data-ttu-id="21f8a-129">Microsoft. Azure. Commands. Operationalınsights. model. Pssearchsearchlistlistresponse</span><span class="sxs-lookup"><span data-stu-id="21f8a-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="21f8a-130">Microsoft. Azure. Commands. Operationalınsights. modeller</span><span class="sxs-lookup"><span data-stu-id="21f8a-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="21f8a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21f8a-131">NOTES</span></span>

## <span data-ttu-id="21f8a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21f8a-132">RELATED LINKS</span></span>

[<span data-ttu-id="21f8a-133">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="21f8a-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



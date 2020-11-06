---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: fdfe52151346bbf173226213c9450484d49fe040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588132"
---
# <span data-ttu-id="4d449-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="4d449-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="4d449-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d449-102">SYNOPSIS</span></span>
<span data-ttu-id="4d449-103">Zaten mevcut olan kaydedilmiş bir aramayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4d449-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d449-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d449-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d449-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d449-105">DESCRIPTION</span></span>
<span data-ttu-id="4d449-106">**Set-Azurermoperationalınsightssavedsearch** cmdlet 'i zaten var olan kaydedilmiş bir aramayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4d449-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="4d449-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d449-107">EXAMPLES</span></span>

### <span data-ttu-id="4d449-108">Örnek 1: kaydedilmiş bir aramayı güncelleştirilmiş özelliklerle ayarlar</span><span class="sxs-lookup"><span data-stu-id="4d449-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="4d449-109">Bu komut, kaydedilmiş bir aramayı güncelleştirilmiş özelliklerle ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4d449-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="4d449-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d449-110">PARAMETERS</span></span>

### <span data-ttu-id="4d449-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="4d449-111">-Category</span></span>
<span data-ttu-id="4d449-112">Kategori adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d449-112">Specifies the category name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d449-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d449-113">-DefaultProfile</span></span>
<span data-ttu-id="4d449-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4d449-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d449-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4d449-115">-DisplayName</span></span>
<span data-ttu-id="4d449-116">Görünen adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d449-116">Specifies the display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d449-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="4d449-117">-ETag</span></span>
<span data-ttu-id="4d449-118">ETag adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d449-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="4d449-119">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="4d449-119">-Query</span></span>
<span data-ttu-id="4d449-120">Sorgu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d449-120">Specifies the query name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d449-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d449-121">-ResourceGroupName</span></span>
<span data-ttu-id="4d449-122">Kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d449-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="4d449-123">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="4d449-123">-SavedSearchId</span></span>
<span data-ttu-id="4d449-124">Kayıtlı arama KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d449-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="4d449-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4d449-125">-Tag</span></span>
<span data-ttu-id="4d449-126">Kaydedilmiş arama etiketleri.</span><span class="sxs-lookup"><span data-stu-id="4d449-126">The saved search tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d449-127">-Version</span><span class="sxs-lookup"><span data-stu-id="4d449-127">-Version</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d449-128">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="4d449-128">-WorkspaceName</span></span>
<span data-ttu-id="4d449-129">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d449-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="4d449-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d449-130">CommonParameters</span></span>
<span data-ttu-id="4d449-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d449-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d449-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d449-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d449-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d449-133">INPUTS</span></span>

### <span data-ttu-id="4d449-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4d449-134">None</span></span>
<span data-ttu-id="4d449-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4d449-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d449-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d449-136">OUTPUTS</span></span>

## <span data-ttu-id="4d449-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d449-137">NOTES</span></span>

## <span data-ttu-id="4d449-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d449-138">RELATED LINKS</span></span>

[<span data-ttu-id="4d449-139">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="4d449-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



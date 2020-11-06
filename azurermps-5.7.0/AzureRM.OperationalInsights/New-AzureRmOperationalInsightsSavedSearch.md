---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: c8ad9196cd0f89670de38f6c99550e397016661e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594903"
---
# <span data-ttu-id="241bd-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="241bd-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="241bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="241bd-102">SYNOPSIS</span></span>
<span data-ttu-id="241bd-103">Belirtilen parametrelerle birlikte yeni bir kaydedilmiş arama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="241bd-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="241bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="241bd-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="241bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="241bd-105">DESCRIPTION</span></span>
<span data-ttu-id="241bd-106">**Yeni-Azurermoperationalınsightssavedsearch** cmdlet 'i, çalışma alanı için belirtilen parametrelerle birlikte yeni bir kaydedilmiş arama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="241bd-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="241bd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="241bd-107">EXAMPLES</span></span>

### <span data-ttu-id="241bd-108">Örnek 1: yeni bir kaydedilen arama oluşturma</span><span class="sxs-lookup"><span data-stu-id="241bd-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="241bd-109">Bu komut yeni bir kaydedilmiş arama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="241bd-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="241bd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="241bd-110">PARAMETERS</span></span>

### <span data-ttu-id="241bd-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="241bd-111">-Category</span></span>
<span data-ttu-id="241bd-112">Kategori adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="241bd-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="241bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241bd-113">-DefaultProfile</span></span>
<span data-ttu-id="241bd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="241bd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="241bd-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="241bd-115">-DisplayName</span></span>
<span data-ttu-id="241bd-116">Kayıtlı arama görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="241bd-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="241bd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="241bd-117">-Force</span></span>
<span data-ttu-id="241bd-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="241bd-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241bd-119">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="241bd-119">-Query</span></span>
<span data-ttu-id="241bd-120">Sorgu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="241bd-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="241bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="241bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="241bd-122">Kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="241bd-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="241bd-123">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="241bd-123">-SavedSearchId</span></span>
<span data-ttu-id="241bd-124">Kayıtlı arama KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="241bd-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="241bd-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="241bd-125">-Tag</span></span>
<span data-ttu-id="241bd-126">Kaydedilmiş arama etiketleri.</span><span class="sxs-lookup"><span data-stu-id="241bd-126">The saved search tags.</span></span>

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

### <span data-ttu-id="241bd-127">-Version</span><span class="sxs-lookup"><span data-stu-id="241bd-127">-Version</span></span>
<span data-ttu-id="241bd-128">Sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="241bd-128">Specifies the version.</span></span>

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

### <span data-ttu-id="241bd-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="241bd-129">-WorkspaceName</span></span>
<span data-ttu-id="241bd-130">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="241bd-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="241bd-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="241bd-131">-Confirm</span></span>
<span data-ttu-id="241bd-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="241bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="241bd-133">-WhatIf</span></span>
<span data-ttu-id="241bd-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="241bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="241bd-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="241bd-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241bd-136">CommonParameters</span></span>
<span data-ttu-id="241bd-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="241bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241bd-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="241bd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241bd-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="241bd-139">INPUTS</span></span>

### <span data-ttu-id="241bd-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="241bd-140">None</span></span>
<span data-ttu-id="241bd-141">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="241bd-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="241bd-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="241bd-142">OUTPUTS</span></span>

## <span data-ttu-id="241bd-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="241bd-143">NOTES</span></span>

## <span data-ttu-id="241bd-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="241bd-144">RELATED LINKS</span></span>

[<span data-ttu-id="241bd-145">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="241bd-145">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



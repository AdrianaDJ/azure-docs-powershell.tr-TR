---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7e93042ab376ff0020067a29f9b0642e0ab04de9
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938574"
---
# <span data-ttu-id="bc8d9-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="bc8d9-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="bc8d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc8d9-102">SYNOPSIS</span></span>
<span data-ttu-id="bc8d9-103">Belirtilen parametrelerle birlikte yeni bir kaydedilmiş arama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="bc8d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc8d9-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc8d9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc8d9-105">DESCRIPTION</span></span>
<span data-ttu-id="bc8d9-106">**New-Azoperationalınsightssavedsearch** cmdlet 'i, çalışma alanı için belirtilen parametrelerle birlikte yeni bir kaydedilmiş arama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="bc8d9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc8d9-107">EXAMPLES</span></span>

### <span data-ttu-id="bc8d9-108">Örnek 1: yeni bir kaydedilen arama oluşturma</span><span class="sxs-lookup"><span data-stu-id="bc8d9-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="bc8d9-109">Bu komut yeni bir kaydedilmiş arama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="bc8d9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc8d9-110">PARAMETERS</span></span>

### <span data-ttu-id="bc8d9-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="bc8d9-111">-Category</span></span>
<span data-ttu-id="bc8d9-112">Kategori adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc8d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc8d9-113">-DefaultProfile</span></span>
<span data-ttu-id="bc8d9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bc8d9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc8d9-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bc8d9-115">-DisplayName</span></span>
<span data-ttu-id="bc8d9-116">Kayıtlı arama görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-116">Specifies the saved search display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc8d9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bc8d9-117">-Force</span></span>
<span data-ttu-id="bc8d9-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc8d9-119">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="bc8d9-119">-Query</span></span>
<span data-ttu-id="bc8d9-120">Kaydedilen Arama için sorgu ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-120">Specifies the query expression for the saved search.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc8d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc8d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="bc8d9-122">Kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="bc8d9-123">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="bc8d9-123">-SavedSearchId</span></span>
<span data-ttu-id="bc8d9-124">Kayıtlı arama KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="bc8d9-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bc8d9-125">-Tag</span></span>
<span data-ttu-id="bc8d9-126">Kaydedilmiş arama etiketleri.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-126">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc8d9-127">-Version</span><span class="sxs-lookup"><span data-stu-id="bc8d9-127">-Version</span></span>
<span data-ttu-id="bc8d9-128">Sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-128">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc8d9-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="bc8d9-129">-WorkspaceName</span></span>
<span data-ttu-id="bc8d9-130">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="bc8d9-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc8d9-131">-Confirm</span></span>
<span data-ttu-id="bc8d9-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc8d9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc8d9-133">-WhatIf</span></span>
<span data-ttu-id="bc8d9-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc8d9-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc8d9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc8d9-136">CommonParameters</span></span>
<span data-ttu-id="bc8d9-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc8d9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc8d9-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc8d9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc8d9-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc8d9-139">INPUTS</span></span>

### <span data-ttu-id="bc8d9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bc8d9-140">System.String</span></span>

### <span data-ttu-id="bc8d9-141">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc8d9-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bc8d9-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="bc8d9-142">System.Int64</span></span>

## <span data-ttu-id="bc8d9-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc8d9-143">OUTPUTS</span></span>

### <span data-ttu-id="bc8d9-144">Sistem .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="bc8d9-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="bc8d9-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc8d9-145">NOTES</span></span>

## <span data-ttu-id="bc8d9-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc8d9-146">RELATED LINKS</span></span>

[<span data-ttu-id="bc8d9-147">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="bc8d9-147">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)



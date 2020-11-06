---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: a233e41ed91a40e8fb16ccda7ed640f8ad5239ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589186"
---
# <span data-ttu-id="e3f5d-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="e3f5d-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="e3f5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f5d-103">Belirtilen parametrelerle birlikte yeni bir kaydedilmiş arama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3f5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3f5d-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tags] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3f5d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3f5d-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f5d-106">**Yeni-Azurermoperationalınsightssavedsearch** cmdlet 'i, çalışma alanı için belirtilen parametrelerle birlikte yeni bir kaydedilmiş arama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="e3f5d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3f5d-107">EXAMPLES</span></span>

### <span data-ttu-id="e3f5d-108">Örnek 1: yeni bir kaydedilen arama oluşturma</span><span class="sxs-lookup"><span data-stu-id="e3f5d-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="e3f5d-109">Bu komut yeni bir kaydedilmiş arama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="e3f5d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3f5d-110">PARAMETERS</span></span>

### <span data-ttu-id="e3f5d-111">-Kategori</span><span class="sxs-lookup"><span data-stu-id="e3f5d-111">-Category</span></span>
<span data-ttu-id="e3f5d-112">Kategori adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="e3f5d-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e3f5d-113">-DisplayName</span></span>
<span data-ttu-id="e3f5d-114">Kayıtlı arama görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-114">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="e3f5d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e3f5d-115">-Force</span></span>
<span data-ttu-id="e3f5d-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3f5d-117">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="e3f5d-117">-Query</span></span>
<span data-ttu-id="e3f5d-118">Sorgu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-118">Specifies the query name.</span></span>

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

### <span data-ttu-id="e3f5d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f5d-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3f5d-120">Kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-120">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="e3f5d-121">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="e3f5d-121">-SavedSearchId</span></span>
<span data-ttu-id="e3f5d-122">Kayıtlı arama KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-122">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="e3f5d-123">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="e3f5d-123">-Tags</span></span>
<span data-ttu-id="e3f5d-124">Kaydedilen Arama için kaynak etiketlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-124">Specifies the resource tags for the saved search.</span></span>

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

### <span data-ttu-id="e3f5d-125">-Version</span><span class="sxs-lookup"><span data-stu-id="e3f5d-125">-Version</span></span>
<span data-ttu-id="e3f5d-126">Sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-126">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f5d-127">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="e3f5d-127">-WorkspaceName</span></span>
<span data-ttu-id="e3f5d-128">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-128">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="e3f5d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3f5d-129">-Confirm</span></span>
<span data-ttu-id="e3f5d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3f5d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3f5d-131">-WhatIf</span></span>
<span data-ttu-id="e3f5d-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3f5d-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3f5d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f5d-134">-DefaultProfile</span></span>
<span data-ttu-id="e3f5d-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3f5d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f5d-136">CommonParameters</span></span>
<span data-ttu-id="e3f5d-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3f5d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f5d-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f5d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f5d-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3f5d-139">INPUTS</span></span>

## <span data-ttu-id="e3f5d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3f5d-140">OUTPUTS</span></span>

## <span data-ttu-id="e3f5d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3f5d-141">NOTES</span></span>

## <span data-ttu-id="e3f5d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3f5d-142">RELATED LINKS</span></span>

[<span data-ttu-id="e3f5d-143">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="e3f5d-143">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


